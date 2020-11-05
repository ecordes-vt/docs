<!-- markdownlint-disable -->

<style>
aside  {
  border-style: solid;
  border-radius: 9px;
  border-width: 2.2px;
  border-color:#ccc;
  padding: 5px;
  background: #e6e8ef;
}

aside.small {
  display:inline;
  font-size:9pt;
  position:relative; top:-4px;
}

.topruled {
  border-top-width: 1.2px;
  border-top-style: solid;
  border-top-color: rgb(76, 76, 100);
  line-height:45%;
}
.bottomruled {
  border-bottom-width: 1.2px;
  border-bottom-style: solid;
  border-bottom-color: rgb(76, 76, 100);
  line-height:45%;
}
</style>

<h2 style="display: inline;">Step 5: Test your engine in aiWARE &nbsp;</h2>&nbsp;&nbsp;<aside class="small">
<b>ESTIMATED TIME:</b> 20 minutes </aside> &nbsp;

<div style="width: 35%"><iframe src="https://player.vimeo.com/video/375527833?color=ff9933&title=0&byline=0&portrait=0" style="border:0;top:0;left:0;width:75%;height:75%;" allow="autoplay; fullscreen" allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

Now that you've onboarded an engine (and set its status to DEPLOYED), you can test the engine in a live Job, in aiWARE.

One of the easiest ways to do this is, of course, to use the [GraphQL Playground](https://api.veritone.com/v3/graphq) web IDE.

## Check the Engine's Availability

Before running a Job, check to see that the engine exists and is visible via the API.

1\. Log in to [Veritone](https://developer.veritone.com).

2\. Navigate to the [GraphQL Sandbox IDE](https://api.veritone.com/v3/graphql).

3\. In the GraphQL Sandbox, create &mdash; and then execute &mdash; a query like the following, using _your_ engine's ID:

```graphql
query myEngine{
  engine(id:"386e022f-edd1-46ec-b1cc-84d203a37250"){
    builds {
      records {
        id
        status
      }
    }
    name
    state
    ownerOrganizationId
    isPublic
    manifest
    mode
    outputFormats
    supportedInputFormats
    supportedSourceTypes
  }
}
```

This query will show you the status of each build of your engine. If one of your builds is shown as `"status": "deployed"`, that specific build is the one that will be invoked when you try to run a job using your engine.

The query should produce a familiar-looking set of fields and values. If not &mdash; if you get an error of some kind &mdash; don't try to run the engine until the error has been addressed. 

> If the error message is `"The requested object was not found"`, chances are your engine is not in a Deployed state. (Go into the engine Builds list for your engine (in the Veritone Developer web UI) and Deploy the engine, if need be, or Unpause it if it was paused. See [Step 4](developer/engines/tutorial/engine-tutorial-step-4) for a refresher on how to use the Builds UI.) 

## Run a Job and Inspect the Results

To test the engine, run a GraphQL mutation that looks like this (being sure to substitute your engine's ID in the appropriate place):

```graphql
mutation createVocabExtractionJob{
  createJob(input: {
    target: { startDateTime:1574311000, stopDateTime: 1574315000 }
    # targetId: 1121185051    # comment this line if using without a TDO
    clusterId :"rt-1cdc1d6d-a500-467a-bc46-d3c5bf3d6901"
    tasks: [
       {
        # webstream adapter (WSA)
        engineId: "9e611ad7-2d3b-48f6-a51b-0a1ba40fe255"
        payload: { url: "http://se.cs.depaul.edu/Java/Chapter04/Lincoln.txt" } 
        ioFolders: [
          { referenceId: "wsaOutputFolder", mode: stream, type: output }
        ],
        executionPreferences: { priority: -20000 }
      }
      {
        # data-chunking engine  
        engineId: "8bdb0e3b-ff28-4f6e-a3ba-887bd06e6440"  
        payload:{ ffmpegTemplate: "rawchunk" }
        ioFolders: [
          { referenceId: "chunkInputFolder", mode: stream, type: input },
          { referenceId: "chunkOutputFolder", mode: chunk, type: output }
        ],
        executionPreferences: { parentCompleteBeforeStarting: true, priority: -20000 }
      }
      {
        # The hello-world engine -- PUT YOUR ENGINE'S ID HERE:
        engineId: "05a138cd-cedc-435c-8593-9c47f885391f"
        ioFolders: [
          { referenceId: "engineInputFolder", mode: chunk, type: input },
          { referenceId: "engineOutputFolder", mode: chunk, type: output }
        ],
        executionPreferences: {	parentCompleteBeforeStarting: true, priority: -20000 }
      }
      {
        # output writer
        engineId: "8eccf9cc-6b6d-4d7d-8cb3-7ebf4950c5f3"  
        ioFolders: [
          { referenceId: "owInputFolder", mode: chunk, type: input }
        ],
        executionPreferences: {	parentCompleteBeforeStarting: true, priority: -20000 }
      }
    ]
    routes: [
      {  ## WSA --> chunk
        parentIoFolderReferenceId: "wsaOutputFolder"
        childIoFolderReferenceId: "chunkInputFolder"
        options: {}
      }
      {  ## chunk --> Engine
        parentIoFolderReferenceId: "chunkOutputFolder"
        childIoFolderReferenceId: "engineInputFolder"
        options: {}
      }
      {  ## Engine --> output writer
        parentIoFolderReferenceId: "engineOutputFolder"
        childIoFolderReferenceId: "owInputFolder"
        options: {}
      } 
    ]
  }) {
    targetId
    id
  }
}
```

The job has four tasks: an ingestion task involving the Veritone Webstream Adapter, a chunking task (in case the data is large enough to need chunking), our cognition engine, and Output Writer (a Veritone engine that aggregates JSON results).

> To learn more about how and why the `createJob` mutation is structured the way it is, please see [Working with Jobs](quickstart/jobs/?id=working-with-jobs). Also be sure to see the [Job Examples page](overview/aiWARE-in-depth/job-examples).

The mutation should produce a response similar to:

```json
{
  "data": {
    "createJob": {
      "id": "20114505_9aG5dkXpfh",
      "targetId": "710414094"
    }
  }
}
```

The `id` of `"20114505_9aG5dkXpfh"` is the Job ID. The `targetId` is the ID of the TDO (Temporal Data Object) associated with this job.

#### Poll the Job

To determine the job's status, poll the job with this query (substituting the appropriate `jobId`):

```graphql
query jobStatus {
  job(id: "20114505_9aG5dkXpfh") {
    status
    targetId
    tasks {
      records {   
        status    
        engine {
          id
          name        
        }
      }
    }
  }
}
```

Over the space of a few seconds or minutes, you should see the job status change from `pending` to `running`, and each task should go from `queued` to `running` to `complete` (or `failed`, if something went wrong).

#### Get the Results

When the job finishes (with a `status` of `complete`), run the following query to obtain the engine's results (but again, substitute the correct `jobId`):

```graphql
query getEngineOutput {
  engineResults(jobId:"19104215_i6Vz2XQtCR") {
    records {
      tdoId
      engineId
      startOffsetMs
      stopOffsetMs
      jsondata
      assetId
      userEdited
    }
  }
}
```

For our Hello World engine, results will typically look similar to this:

```json
{
   "taskId": "19104215_i6Vz2XQtCR9tzRz",
   "generatedDateUTC": "0001-01-01T00:00:00Z",
   "validationContracts": [
      "keyword"
   ],
   "object": [
      {
         "label": "the",
         "type": "keyword"
      },
      {
         "label": "Gettysburg",
         "type": "keyword"
      },
      {
         "label": "Address",
         "type": "keyword"
      },
      {
         "label": "Fourscore",
         "type": "keyword"
      },
      {
         "label": "and",
         "type": "keyword"
      },
      {
         "label": "seven",
         "type": "keyword"
      },
      {
         "label": "years",
         "type": "keyword"
      }, 
      {
         "label": "ago",
         "type": "keyword"
      }
   ]
}
```

(NOTE: The keyword-object array in this JSON fragment has been edited for length.)

## Further Reading

We hope you've enjoyed this tutorial. Be sure to check out some of these other greeat resources:

- Learn how to [customize engine output](developer/engines/tutorial/customizing-engine-output)
- See our API documentation: <https://docs.veritone.com/#/apis/>
- API examples that you can run in the live Sandbox: <https://docs.veritone.com/#/apis/examples>
- Veritone's Data Model: <https://docs.veritone.com/#/apis/data-model>
- See our schema: <https://api.veritone.com/v3/graphqldocs>
- Our VTN Standard helps ensure engine interoperability: <https://docs.veritone.com/#/developer/engines/engine-output>
- Other tutorials: <https://docs.veritone.com/#/apis/tutorials> 

### Review What We Did in This Tutorial:
* [Step 0 &mdash; Set up your project](developer/engines/tutorial/)
* [Step 1 &mdash; Register your project with Veritone](developer/engines/tutorial/engine-tutorial-step-1)
* [Step 2 &mdash; Use Docker to create a build](developer/engines/tutorial/engine-tutorial-step-2)
* [Step 3 &mdash; Test your build locally](developer/engines/tutorial/engine-tutorial-step-3) using the Engine Developer Toolkit's Test Console App
* [Step 4 &mdash; Push your engine build to Veritone](developer/engines/tutorial/engine-tutorial-step-4) 
* [Step 5 &mdash; Test your engine in aiWARE](developer/engines/tutorial/engine-tutorial-step-5) and, if necessary, debug/rebuild/re-deploy
