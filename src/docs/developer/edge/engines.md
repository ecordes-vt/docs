<!-- markdownlint-disable -->

# Engines in Veritone aiWARE Edge

## Engine Types

Veritone engine types include `chunk`, `stream`, and `batch`.  The runtime of the engines can be packaged via Docker for traditional cognitive engines, or [Node-RED](https://nodered.org/) for engines built in Automate Studio.

See the following table for the difference between the different engine types.

Chunk | Stream | Batch
 -- | -- | --
Processes a chunk at a time, producing vtn-standard outputs which are then aggregated by Output Writer to produce engine results for the task.<br/><br/>The chunks are normally the outputs of a parent task (e.g. Stream Ingestor splitting a stream into chunks of wav files), and can be processed in any order and by multiple engine instances to produce a quicker result. | Receives stream input from either an external source or a parent task, may produce vtn-standard outputs as the stream is processed, or other stream data (e.g. Stream Ingestor).<br/><br/>The engine needs the data in a single context to avoid losing accuracy or incurring complexity. For example, tracking objects across frames would be easier in a single stream than collating them across multiple chunks. | May not consume any input data from a parent task of the job.  However, it typically uses the payload for the task to perform the business logic, and outputs often produced directly into the container TDO.<br/><br/>Batch engines are typically associated with V1F (Iron-based) engines.


## Engine Toolkit

Engine Toolkit (ET) abstracts the input/output layer between the Engine and Veritone platform, freeing engine developers of having to deal with the nuances of getting input data (e.g. from queues) and producing the engine outputs (e.g. back to queue).

## New Engine Toolkit

1.  Backward compatible -- For chunk engines and other current functionality as described in Veritone docs.

2.  Unified protocol -- The new version of Engine Toolkit strives to provide support to all engine types - keeping the interface consistent so that the choice of implementing chunk, stream, or batch shouldn't be depending on how engines should get their data.

## V3F Framework

The figure below shows at a high level the V3 Framework (V3F), which is where Engine Toolkit makes requests to Controller for work. The requests are made on behalf of the engines that the Engine Toolkit represents, including native engines such as Webstream Adaptor (WSA), Stream Ingestor (SI), and Output Writer.

![](V3F-engine-framework.png)

The Controller queries the database for tasks that are assigned to the engines, formulates the task I/O information, and assigns work requests, batches of work items, back to Engine Toolkit.

For each work item in the work request, Engine Toolkit:

1.  Retrieves the input data from the filesystem (FS) for the tasks.

2.  Invokes the core engine's `/process` webhook.

3.  Stores the result back to the filesystem for the next task.

Engine Toolkit also has a heartbeat loop to report back to Controller the work item progress: number of processed chunks, errors, etc.

There is a RunTimeTTL set by Controller as directive to Engine Toolkit to terminate when the time is up. In addition, Controller may issue a `terminate` action as a response to the `getWork` request.

Note that besides the databases, the File System contains the state of jobs/tasks as work is being done: processed chunks, in-processing chunks, or error chunks.  The input/output relationship between tasks is specified in the Edge database and represented in the file system accordingly. For engines to emit input/output chunks or streams, the interaction with the File System should be done by Engine Toolkit to ensure correctness. To learn more about the File System, see [File System](overview/aiWARE-in-depth/file-system).

## Native Engines in Engine Toolkit

Engine Toolkit for V3F includes a number of native engines such as Webstream Adapter, TV & Radio Adapter, Stream Ingestors (various flavors), and Output Writer. This provides the flexibility to turn engine instances into "super-workers," helping to push data through the initial ingestion pipeline as well as to finalize the engine outputs.

To activate the adapters or stream ingestors, it is recommended that the Docker image containing the Engine Toolkit binary should have `ffmpeg` and `streamlink` modules included. <!-- INTERNAL Internal engines built by Veritone engineers should include these applications and add them to the system path if not installed properly (e.g. via apt-get or apk add). -->

**Engine IDs:**

1.  Web stream adaptor (engineId:9e611ad7-2d3b-48f6-a51b-0a1ba40feab4)

2.  TV & Radio adaptor (engineId: 74dfd76b-472a-48f0-8395-c7e01dd7fd24)

3.  Stream Ingestor v2 for playback (engineId:352556c7-de07-4d55-b33f-74b1cf237f25 )

4.  Stream Ingestor v2 for asset creation (engineId: 75fc943b-b5b0-4fe1-bcb6-9a7e1884257a)

5.  Stream Ingestor v2 for FFMPEG (engineId: 8bdb0e3b-ff28-4f6e-a3ba-887bd06e6440)

6.  OutputWriter (engineId: 8eccf9cc-6b6d-4d7d-8cb3-7ebf4950c5f3)

For more details, see the [Stream Ingestor v2](overview/aiWARE-in-depth/stream-ingestor) page.

## Engine Interaction with Engine Toolkit in V3F

Chunk engines continue to provide the `/process` webhook endpoint as documented earlier ([see V2F Toolkit page](https://docs.veritone.com/#/developer/engines/toolkit/)).
The input chunk is provided in the `cacheUri` parameter.  The chunk result can be returned in the response for the `/process` call, or it can be sent asynchronously at a later time. (In the latter case, chunk engines act like stream engines for one chunk.)

Stream engines should also expose the `/process` webhook endpoint. Its input data will also be from `cacheURI`, and produces either [VTN Standard](developer/engines/standards/engine-output/) or other format(s) as task outputs back to ET using the heartbeat/callback endpoint.  Naturally, stream engines will respond almost immediately in handling the `/process` webhook, providing some ACK on the response or other informative response to ET.

Batch engines are similarly invoked and are required to provide heartbeats back to ET for status update with a completion status (per discussion further below). Batch engines can be used to perform their own business logic, and produce the results in a freeform fashion, e.g., producing assets directly to the TDO associated with the job that the task is in. However, they can also produce task outputs for downstream tasks in the job by following the pattern of chunk or stream engines -- producing output results by posting back to ET's `/callback` endpoint. Naturally, this should be set up as part of the job DAG with output of the engine defined in the task routes and I/Os.

## Converting V2F Engines to V3F

In V3F, Kafka has been deprecated. Converting an engine from V2F to V3F requires taking this into account.

For chunk Engines that already use the Engine Toolkit (and thus do not have any direct interaction with Kafka), conversion to V3F is an easy process. Just pick up the latest distribution of the Engine Toolkit. (Follow the best practices described below when you create your Dockerfile.)

Stream Engines need to be updated to move away from consuming directly from Kafka. Think of a stream engine as a chunk engine processing just a single chunk. The payload would come from the `payload` field in the post request to the `/process` webhook (vs. PAYLOAD_JSON env variable in V2F). Pay heed to the Heartbeat Webhook and Result Webhook discussions further below. If your engine takes more than one second to process a unit of work, plan on sending one heartbeat per second to the `heartbeatWebhook`.

From V2F | Converting to V3F
-- | --
Upon start up, read PAYLOAD_JSON for job info | Need to expose 2 webhooks :  `/readyz` and `/process` - set environment variables accordingly ([See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=webhook-environment-variables)). Job information is in the `payload` field of the `/process` request.
Read input stream from Kafka | Read input stream from the `cacheURI` which is set in the POST request to /process webhook
Output results to Kafka | Post the result to the resultWebhook of Engine Toolkit.  See [Result Webhook (from Engine Toolkit)](overview/aiWARE-in-depth/engines?id=result-webhook-from-engine-toolkit)
Heartbeat to Kafka | Post heartbeat message to the heartbeatWebhook of Engine Toolkit.  See [Heartbeat Webhook (from EngineToolkit)](overview/aiWARE-in-depth/engines?id=heartbeat-webhook-from-enginetoolkit)

Batch Engines should provide the `/process` webhook, similarly to stream engines. The payload to the engine is available in the request to the webhook.  The batch engine SHOULD NOT update task status or output directly. Heartbeats should be provided by posting back to the `/callback` endpoint from ET

From V2F | Converting to V3F
-- | --
Upon start up, read PAYLOAD_JSON for job info | Need to provide 2 webhooks :  `/readyz` and `/process` - set environment variables accordingly ([See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=webhook-environment-variables)).  Job information is in the `payload` field of the /process request
Update Task Status to `running` or `complete` | Do not update task status back to core.  Instead submit heartbeat message to the `heartbeatWebhook` of Engine Toolkit.  See [Heartbeat Webhook (from EngineToolkit)](overview/aiWARE-in-depth/engines?id=heartbeat-webhook-from-enginetoolkit)

## Engine Toolkit Docker image

Engine Toolkit is available as a Docker image.
To include the Engine Toolkit in your engine Docker, use a [multi-stage build](https://docs.docker.com/develop/develop-images/multistage-build/) process, and copy the toolkit binary to a specific location in your image. Below is a sample Dockerfile snippet showing how the multistage build process is designed to work (notice the multiple FROM statements):

```pre

FROM veritone/aiware-engine-toolkit as vt-engine-toolkit

FROM YOUROWN_DOCKER_IMAGE

COPY --from=vt-engine-toolkit /opt/aiware/engine /opt/aiware/engine

ENTRYPOINT ["/opt/aiware/engine", "YOUR_ENGINE_BINARY"]

```

NOTES:

1. Refreshing the Engine Toolkit:  Make sure the docker image is refreshed by doing a `docker pull veritone/aiware-engine-toolkit` prior to your `docker build`. For a local aiWARE environment, it is best to pull before building.
  
2. Using Engine Toolkit in an Alpine-based image:  To use Engine Toolkit with an alpine image, make sure to include this in the Dockerfile:

`RUN apk add --no-cache libc6-compat`

3. It is important to specify `/opt/aiware/engine` as the toolkit-binary location. Doing so will ensure that the most up-to-date binary is automatically used.

## Environment Variables

Engine Toolkit will pass on all environment variables defined when the
engine instance is started to the engine’s process with the exception of
`AIWARE_` -prefixed environment variables.

For internally developed engines, a white list of environment variables
can be supplied. When that is set for the engine via an environment
variable, AIWARE\_ENV\_WHITE\_LIST,  defined in the Dockerfile, Engine
Toolkit will allow those variables to be accessible to the engine.

For example, the following Dockerfile snippet sets AIWARE\_ENV\_WHITE\_LIST  so
that the environment variables, AIWARE\_BUILD\_ID,AIWARE\_xyz, can be
passed on to the engine process:

```
ENV AIWARE\_ENV\_WHITE\_LIST AIWARE\_BUILD\_ID,AIWARE\_xyz
```

> NOTE: AIWARE\_CONTROLLER is automatically added to the white list.

## Controller / Engine Toolkit / Node-Red engine relationship

For Node-RED engines in V3F, the runtime logic is provided by a single Docker image (node-red-runner) -- which needs the `ENGINE_ID` + runtime definition associated with a build when the container is started.  The difference between Node-RED Engines and other engines is:

1. A column exists in the `edge.build` table to hold the build runtime -- which is where the runtime definition is stored.  Controller will retrieve the runtime JSON of a build (via GraphQL) and store that in this column.

2. When Controller asks an agent to start an engine, the runtime JSON needs to be given as well.
 
3. Agent on the engine node will start the container with the given `dockerImage` (in this case it should be the `node-red-runner`) with the additional behavior:

    a. Store the `buildRuntime` to a file (e.g. `/cache/engines/{engineId}/{buildId}/runtime.json`). This file will be mounted to the engine Docker container in the same location (e.g. `-v /cache/engines/{engineId}/{buildId}/runtime.json:/cache/engines/{engineId}/{buildId}/runtime.json`).
    
    b.  Set the following environment variables when starting the engine Docker container:
    
 ```pre
    AIWARE_BUILD_RUNTIME t= to the file location as set in a)
    
    ENGINE_ID = the engine id (from the HostActionLaunch)
    
    BUILD_ID = the build id (from the HostActionLaunch)
```

   c. Agent will also set the `ENGINE_ID` and `BUILD_ID` for the engine.
    
4. Engine Toolkit will be agnostic about this `AIWARE_BUILD_RUNTIME` -- the Node-RED process, however, will look for this variable -- which points to a file from which it can load the build runtime definition.

5. With this approach, the Engine Toolkit does not have to do anything special for Node-RED engines.  The same framework will work for all kinds of engines.

**Node-RED plugins cache:**
* Need a folder to cache node-red plugins. 
* The folder is shared by all engines in an organization.
* The folder name is given in AIWARE_AUTOMATE_SHARE_FOLDER environment variable.

## Node-RED (Automate) Engine Runner in Engine Toolkit

In V3F, engines actively get their work items from Controller given
their ENGINE\_IDs (environment variable or /var/manifest.json).  The
work items can be for any builds with the assumption that the engine
instance runs with the most recently deployed  build.

For Node Red engines in V3F, the engine logic will be provided by a
single Docker image (node-red-runner) -- which  will need  ENGINE\_ID +
runtime definition associated with a build when the container is
started.  The difference between NR Engines and other engines require
the following enhancements to the current V3 Edge components:

1.   Need a column in the edge.build table to hold the build runtime --
    which is where the runtime definition being stored.  Controller will
    retrieve the runtime JSON of a build (via GraphQL) and store that in
    this column
2.  When Controller asks an agent to start an engine, the runtime JSON
    should be given as well → A new field \`buildRuntime\` ofJSON should
    be added to the HostActionLaunch struct.
3.  Agent on the engine node will start the container with the given
    \`dockerImage\` ( in this case it should be the
    node-red-runner) with the additional behavior:

a.  Store the buildRuntime to a file (e.g.
    /cache/engines/{engineId}/{buildId}/runtime.json).  This file will
    be mounted to the engine Docker container in the same location (e.g.
    -v
    /cache/engines/{engineId}/{buildId}/runtime.json:/cache/engines/{engineId}/{buildId}/runtime.json)
b.  Set the following environment variables when starting the engine
    Docker container:

```
AIWARE\_BUILD\_RUNTIME t= to the file location as set in a)

ENGINE\_ID = the engine id (from the HostActionLaunch)

BUILD\_ID = the build id (from the HostActionLaunch)
```

c.  Agent should also set the ENGINE\_ID and BUILD\_ID for the engine.

4.  Engine toolkit will be agnostic about this AIWARE\_BUILD\_RUNTIME --
    the Node-RED process however will look for this variable -- again
    this points to a file where it can load the build runtime
    definition.
5.  With this approach, engine toolkit does not have to do anything
    special for Node-RED engines.

The Node-RED (Automate) engine runner is a Docker image that has Engine Toolkit & Node-RED installed, and it acts as a proxy agent. The ENTRYPOINT for the Docker image should be `/app/engine node main.js`, where main.js is the Node-RED engine runner.

Node-RED engines are denoted with `"runtime":"nodeRed"` in their `manifest.json`.  They may have their own package requirements or custom execution environment that may take some time to install. Some optimizations could be done by having the engines execution runtime setup in a designated location in the File System, e.g., /cache/nodered/engines/{engineId}-{buildId} directory to contain scripts, JSON etc. to set up engine runtime environments.

The work item will be passed on to the Node-RED engine runner `/process` endpoint which then call into the engine's runtime execution code accordingly.

<!--
TODO: The getWork API to Controller would need to be enhanced to allow retrieving Node Red work items (e.g. need runtime parameter). 
-->

## Deep Dive: Engine Interaction with Engine Toolkit

This section gives more details about the interaction between Engine Toolkit and aiWARE infrastructure.

Discovery of Webhooks
---------------------

Engine Toolkit will use the following [environment variables](https://docs.veritone.com/#/developer/engines/toolkit/?id=webhook-environment-variables) to discover the webhooks as provided by the core engine:

```pre
ENV VERITONE_WEBHOOK_READY="http://0.0.0.0:8888/readyz"
ENV VERITONE_WEBHOOK_PROCESS="http://0.0.0.0:8888/process"
```

Process Webhook (from Engine)
-----------------------------

**Request**

Engine Toolkit invokes the webhook with the following input data in its POST payload:

name | data type | notes
-- | -- | --
chunk | File | [See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook) - will not be available for stream engine
chunkMimeType | string | [See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook)
startOffsetMS | int | [See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook)
endOffsetMS | int | [See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook)
width | int | [See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook)
height | int | [See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook)
libraryId | string | [See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook)
libraryEngineModelId | string | [See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook)
cacheURI | string | [See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook) - stream engine should use this to retrieve the input stream
veritoneApiBaseUrl | string | [See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook)
token | string | [See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook)
payload | JSON string | [See documentation](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook)
chunkContext |  string | **NEW** This gives some context for the result
heartbeatWebhook | string | **NEW** This is the heartbeat webhook provided by Engine Toolkit.  Engines with async processing for the `/process` webhook, such as stream or batch engines, should submit heartbeats with progress information.  This is the equivalent of stream engines emitting into the engine_status Kafka queue for heartbeats
resultWebhook | String  | **NEW** This is the result webhook provided by Engine Toolkit. The engine should submit results of the processing as soon as it could.  This is the equivalent of stream engines emitting into the chunk_all Kafka queue when it finished processing some data off the input stream.
externalCallbackWebhook | string | **NEW** Engines may pass this callback URI to an external entity performing the real processing
maxTTL | int | NEW the maximum  time that engine toolkit can wait for results from the engine.
internalJobId            | string                   | **NEW** The internal job id
internalTaskId           | string                   | **NEW** The internal task id
taskTmpDir               | string                   | **NEW** temporary directory that serves as a scratchpad for the engine to store temporary data related to the task.  This directory will be purged after a certain time (3 days default).  For any permanent data, use other means.  This directory should already exist when the engine receives its chunk input.
engineDir                | string                   | **NEW** directory that the engine can use to store shared assets across different instances
libraryModelDirectory    | string                   | **NEW** directory that the engine can use to store library engine models -- either after a training job is done -- or when in matching mode and the engine would like to cache the model for quick access in subsequent tasks.
chunk-metadata-xxxx      | string                   | **NEW** -- The input chunk may have metadata as intended by the parent task -- which is typically sent by the caller to the parent task. Engine Toolkit will make these available to the engine task with the prefix `chunk-metadata-` and stringified value.
redisETUrl               | string                   | **NEW** Only available if REDIS is available for the cluster in which the engine processes its tasks. Engines will not be given direct access to the Redis server, instead engines will GET/POST to Engine Toolkit, which will then call Redis via API for the getting or setting of the keys.
controllerToken          | string                   | **NEW** For any requests to Controller, engine MUST use this token

**Response**

**Synchronous**

Chunk engines that produce JSON response conforming to VTN Standard will continue to do so as [documented here](https://docs.veritone.com/#/developer/engines/toolkit/?id=process-webhook).

**Asynchronous**

For stream or batch engines with async or stand-alone processing mode, it is required that the following be returned in the JSON response.  Suggested value for `v` is `maxTTL` - or more if maxTTL is insufficient.  For example, if the engine is to call out to external entity for processing and thus may require more than hours to process.

name | data type | notes
-- | -- | --
estimatedProcessingTimeInSeconds | int | Amount of seconds that the engine  estimates to produce some results. 

Heartbeat Webhook (from Engine Toolkit)
--------------------------------------

Engines performing the processing asynchronously such as stream or batch engines should submit heartbeats to Engine Toolkit on a regular interval (suggested: once every second).  The webhook URI can be discovered in the `heartbeatWebhook` field of the original `/process` request.

**Request**

The request to the `heartbeatWebhook` should have the following data.

name | data type | notes
-- | -- | --
status | string (enum) | Required. Possible values: running, complete, failed
bytesRead | int64 | Optional
bytesWritten | int64 | Optional
messagesWritten | int64 | Optional  Number of results submitted thus far
infoMs | string | Optional: informational message about the running status of the engine
failureReason | String (enum) | Required when status is set to failed.  Possible values:<br/>internal_error<br/>external_error<br/>unknown<br/>url_not_found<br/>url_not_allowed<br/>url_timeout<br/>url_connection_refused<br/>url_error<br/>invalid_data<br/>rate_limited<br/>api_not_allowed<br/>api_authentication_error<br/>api_not_found<br/>api_error<br/>file_write_error<br/>stream_read_error<br/>system_dependency_missing<br/>system_error<br/>heartbeat_timeout<br/>other
failureMsg | string | Optional: supplemental info for `failureReason`

**Response**

`204 - No content`

Result Webhook (from Engine Toolkit)
------------------------------------

Whenever the engine has a complete unit of processed work for the task, it should submit the result back to Engine Toolkit for persistence.  The webhook is given to the engine in the `resultWebhook` field of the /process request.  See [resultWebhook](https://docs.google.com/document/d/1VC06SkIlMi-3FoqrqU3N_WGIwV7j2EmphRRSOXzbAi0/edit#bookmark=id.31uhqi2c55f5).

**Request**

The request to the `resultWebhook` should have the following data.

name | data type | notes
-- | -- | --
chunkContext | string | Optional. This is the value of the `chunkContext` as passed into the request of the `/process` .  It should be present if the engine is chunk engine
startOffsetMs | int64 | Optional - offset of the start of the chunk from the beginning of the input stream for which this result was produced | |
endOffsetMs | int64 | Optional - offset of the end of the chunk from the beginning of the input stream for which this result was produced
output | JSON | Required VTN-Standard of the result.  See [documentation](https://docs.veritone.com/#/developer/engines/standards/engine-output/) for engine vtn-standard output format.


For example:

```pre
POST <http://localhost:1234/result/task1234>

{ 
  "index" : 1,
  "startOffsetMs": 0,
  "endOffsetMs": 1200,
  "output" : {"series": [
    {
      "startTimeMs": 0,
      "stopTimeMs": 300,
      "words": [
        {
          "word": "this"
        }
      ]
    },
    {
      "startTimeMs": 300,
      "stopTimeMs": 500,
      "words": [
        {
          "word": "is"
        }
      ]
    },
    {
      "startTimeMs": 500,
      "stopTimeMs": 800,
      "words": [
        {
          "word": "a"
        }
      ]
    },
    {
      "startTimeMs": 800,
      "stopTimeMs": 1200,
      "words": [
        {
          "word": "sentence"
        }
      ]
    }
  ]}
}
```

**Response**

`204 - No content`

## 'sendOutputToUris' option

When an engine finishes processing a chunk successfully, if its task
was created with the `sendOutputToUris` option, Engine Toolkit will post the result to that URI following this pattern:

```
POST
{uri}/internalJobID={internalJobID}&internalTaskID={internalTaskID}&jobID={jobID}&taskID={taskID}&chunkID={chunkID}&timestamp={timestamp
when chunk is produced}
```

In addition, if there are metadata that were produced by a parent task
that started with `x-aiware-`,  those metadata will be sent on as
custom headers for the POST request.

For example, a job has the following tasks, with Engine Task 1 having a
notification URI associated with its task:

![Example DAG](ex-1.png)

A caller can `push` a chunk to the `push adapter` to make the chunk
available to Engine Task 1 almost immediately. The push adapter will
store the request Headers as part of the chunk metadata.  This chunk
metadata can then be passed to the engine `/process` webhook and the
notification servers as configured by the caller.

A use case for this pattern is to measure the roundtrip from the time
the chunk was sent to push adapter task, to the time that EngineTask 1
finishes processing the chunk. In this situation:

1.  A Notification server is established
2.  The caller creates a job, using the controller CreateJob API,
    passing on the uri of the notification server to the task
3.  When the caller pushes a chunkt to the Push Adapter via HTTP, it
    should also send a Header, `x-aiware-chunk-timestamp` =  the epoch
    time of the current time.
4.  Assuming, that the engine is aware of this header, for example to
    calculate the elapsed time between the caller sending the chunk and
    the time that the engine receives the data, in the engine’s  handler
    for the `/process` webhook, it can retrieve the
    `chunk-metadata-x-aiware-chunk-timestamp` from the request
    parameters and perform the calculation
5.  When the engine posted the engine output back to Engine Toolkit,
    either synchronously as returned from `/process` or asynchronously
    to the `resultWebhook`, Engine Toolkit will send the same output
    to the notification server, with the same header,
    `x-aiware-chunk-timestamp`, and the same value as posted initially
    by the caller.
6.  The notification server retrieves the `x-aiware-chunk-timestamp`
    header and performs the calculation for the total round trip -- from
    start to finish.

## Chunk Metadata

As mentioned above, input chunk metadata can be made available to the
engine as part of the fields for the `/process` webhook.  The names
for the metadata fields are prefixed with `chunk-metadata-` to
minimize name collision with other data.

The values will be strings. Therefore the engine should perform type
conversion as needed.

## Engines and Training Libraries

Engines may need training data to produce _library engine models_, which can then
be passed on to a job for the engine to use in processing.

> See [Library-Enabled Engines](developer/libraries/engines?id=test-libraries) for more information about library engine models. Also see [Training](developer/libraries/training) for information on how to persist training data.


### Training libraries
------------------

An engine can be started in a job with `mode=library-train` in the
task payload. Follows is a sample of mutation to create such job:

```graphql
mutation createTrainingJob{
  createJob(input:{
    clusterId :"____YOUR_CLUSTER_ID____________"
    tasks:[
      {
        engineId:"__ENGINE_ID__",
        payload:{
          mode:"library-train"
          libraryId:"33e7c3fd-dc76-45ca-915e-49a18fe14546"
          libraryEngineModelId:"e0fafd01-03db-4d6b-b651-526b4320b2b5"
        }
      }
    ]
  }) {
    id
    tasks{
      records{
        engineId
        payload
      }
    }
  }
}
```

Details of training are private to the engine. It is up to the engine
to know how to capture the state information that it considers "training,"
and store that captured state info in a library engine model using the Veritone
GraphQL API. (Veritone provides the state-persistence API, but puts no restrictions on
how an engine accomplishes, or formats, its "training." Your library engine model can contain whatever private data
the engine might need when it is called upon, in the future, to recall its "training." The format of the data
is up to you.)

In V3F, an engine -- be it chunk, stream, or batch, training mode or not
-- will be invoked in the same way, e.g via the `/process` webhook, with
data pertaining to its task. The engine should examine the payload
field of the request for the `mode`.  Training libraries can take a while to run,
and thus, in training mode, the engine behaves as a batch engine, which means it
should respond to `/process` as soon as possible, and post back to the
`/heartbeat` webhook periodically (once per second) so the Engine Toolkit can monitor progress.
When training is finished and the library engine model is updated, the
engine can then post to `/heartbeat` webhook with a `"complete"` status.

Besides uploading the final trained engine model to S3 or wherever
persistence storage is, the engine may store the model in the directory
created by Engine Toolkit and given to the engine as the value of the
field `libraryModelDirectory`. This is to optimize the loading of the
library model and is not a replacement for cloud storage; the library engine model
should be persisted back to Veritone core using the GraphQL API.
See the [Training](developer/libraries/training) discussion for information on how to persist training data programmatically.

### Consuming Training Libraries

In normal processing, the engine will be given a library model's
libraryId and libraryEngineModelId in the payload field.  Also,
`mode=library-run` will be present in the `payload` field.

Since loading a library engine model can be time-consuming, the engine
should cache library engine models using the `libraryModelDirectory`
parameter that the Engine Toolkit has created and made available to the
engine in the request POSTed to the engine’s `/process` webhook.  This
location can store `libraryEngineModels` for use across chunk processing
of a task or even across different tasks.

When using this pattern, the library engine model data goes into directories
using the following naming scheme:

`/cache/{shard}/libraries/{libraryId}/{libraryEngineModelId}`

This is the recommended patter:

1.  Engine gets the `libraryEngineModelId` from the `payload` field.
2.  Check the cache directory indicated by the `libraryModelDirectory` for
    the library model engine (see above). If it is not there, the library
    engine model is not yet downloaded. Thus the engine could download
    the library engine model to that directory.
3.  Once the library engine model is downloaded to the local file, it is
    then available to that engine instance as well as other future
    engine instances that were passed the same `libraryId` and library
    engine model id.

> As it is possible that multiple engine instances may be using the same
model at the same time, the engine developer should be prepared to
devise a scheme to avoid corrupting the model.

## Engines and Redis

An engine may want to share states as chunks being processed for a task
or job. Engine Toolkit provides limited access to Redis for this. _Note that if
the cluster does not have a Redis server set up and made accessible from
within the Docker container running the engine, this feature will not be
available._

Engine Toolkit looks for the presence of AIWARE\_REDIS\_HOST,
AIWARE\_REDIS\_PORT before it starts the local redisET server. It will
pass the url to this local server to the engine `/process` webhook via the
form field `redisETUrl`,

e.g

`redisETUrl = http://localhost:xxx`

The engine can only GET or POST within the context that was given to the
`/process` endpoint.

For job -- the `internalJobId` should only be the same `internalJobId` as
passed to the `/process` webhook.

```
GET /keys/j{internalJobId}/{key}

POST /keys/j{internalJobId}/{key}
```

Similarly, for tasks, the `internalTaskId` should only be the same
`internalTaskId` as passed to the `/process` webhook.

```
GET /keys/t{internalTaskId}/{key}

POST /keys/t{internalTaskId}/{key}
```

> A key value will have a TTL in Redis cache. The default value is 24
hours. If the engine wants to have a different TTL for the key, it can
pass on to the POST request with the query string ttlInSeconds.

For example:

```
POST /keys/t{internalTaskId}/{key}?ttlInSeconds=3600

Potential HTTP response code:

200 - for GET requests - the contents of the key as POSTed previously
and key is not yet expired

200 - for POST request - empty body (should it be 204?)

404 - for GET requests with invalid keys or expired ttl, or GET/POST
request outside of the allowed internalTaskId, internalJobId

400 - for bad requests such as missing body

500 - for other internal server error - e.g. Redis issue
```
