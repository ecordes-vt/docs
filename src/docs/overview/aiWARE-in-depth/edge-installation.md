<!-- markdownlint-disable no-inline-html -->

# Installing aiWARE Edge

This page outlines the procedure to install, configure, and validate an instance of Veritone aiWARE Edge for use in a fully network-isolated, on-premise deployment.

## Prerequisites

This procedure requires a Linux host (either physical, or VM) running on a supported chipset (ARM64 or AMD64).

> The current version of Edge is not _natively_ compatible with Windows nor MacOS. However, you can use Ubuntu Linux running on VirtualBox VM to achieve successful installation on a Mac.

### Step 1: Choose the Run Mode

You can run aiWARE Edge (Coreless) in a &quot;Single Node&quot; or a &quot;Two Nodes&quot; mode, depending on your needs. In a Single Node mode, all the necessary components will be installed on a single virtual or physical machine. This is useful for UAT, non-production environments, or other smaller-scale installations.
The Two Nodes setup is recommended for running the Admin UI.

### Step 2: Allocate Machines

The installation and configuration steps defined below assume that one or two (depending on the run mode) physical or virtual machines are available, accessible, and meet the following criteria.

The operating system for both nodes should be:

#### Processing Node

- 2 x CPU, 8-Cores each (Intel Xeon or similar)
- 32GB RAM DDR4
- At least 400GB of disk space per box on SSD
- Ubuntu Linux 18.04

#### Admin Node (_not_ required in a Single-Node mode)

- 2 x CPU, 8-Cores each (Intel Xeon or similar)
- 8GB RAM DDR4
- At least 400GB of disk space per box on SSD
- Ubuntu Linux 18.04

#### Special Instructions for AWS Hosting

The steps below tell how to stand up your own instance in AWS. 

1\. Log in to AWS - https://us-west-1.console.aws.amazon.com/

> Ensure you’re in the correct region.

2\. Launch Instance

* Select Ubuntu Server 18.04 LTS (HVM), SSD Volume Type - ami-0dd005d3eb03f66e8

* Choose m4.2xlarge as your Instance Type (CPU - 8, Memory - 32 GB)

* Skip “Configure Instance”, Select “Add Storage”

* Increase size from 8 GB → 150 GB (minimum)

* Configure Security Group

* Launch + Review

Create a new key pair and follow instructions on where to store it in on your local machine.

### Step 3: Machine Configuration

Ensure that the following steps are completed on each physical/virtual machine before proceeding with the aiWARE Edge installation.

#### Local SSH Configuration

If you are running aiWARE locally, you can skip these steps. This creates a shortcut for your SSH config.

1.  On your local machine, open Command Line (Terminal) Interface

2.  Enter `nano ~/.ssh/config`. (You may need to create the directory with `mkdir ~/.ssh` before editing the file.) There are 3 items needed for a remote node:

    1.  Hostname - Public DNS (IPv4): found in AWS within Instance details

    2.  IdentityFile: file path to where key pair is located

    3.  User: `ubuntu`

3.  Format your file like this:

    ```pre
    Host coreless 
    Hostname xxx.yourdns.amazon.com 
    IdentityFile /Users/Path/to/keypair.pem User ubuntu
    ```

4.  Once SSH has been configured, enter `ssh coreless` or Connect via AWS "Connect."

    1.  Example: `ssh -i "keypair.pem" ubuntu@ec2-public-dns.us-west-1.compute.amazonaws.com`

5.  Type "Yes" to connect to IP.

#### Required Prerequisites

| **#** | **Action** | **Commands** |
| --- | --- | --- |
| 0) | Elevate permissions to root | `sudo bash` |
| 1) | Install docker.io, nfs-common, awscli, &amp; uuid packages | `apt-get update -y` <br/>`apt-get upgrade -y`<br/>`apt-get install -y docker.io nfs-common awscli uuid prometheus-node-exporter` |
| 2) | Create aiWARE directory  | `mkdir -p /opt/aiware` |
| OPTIONAL | Mount disc | `# Replace sdXX with a data disk.` <br/>`# If all on the root disk, skip the below`<br/>`mkfs.ext4 /dev/sdXX`<br/>`mount /dev/sdXX /opt/aiware` |
| 3) | Create local directories | `mkdir -p /opt/aiware/postgres /opt/aiware/nfs /opt/aiware/registry /cache/1`<br/>`touch /cache/1/1.json` |
| 4) | Install Logging Components (optional) | `apt-get install -y prometheus-node-exporter`<br/>`docker run --volume=/:/rootfs:ro`<br/>`--volume=/var/run:/var/run:ro`<br/>`--volume=/sys:/sys:ro`<br/>`--volume=/var/lib/docker/:/var/lib/docker:ro`<br/>`--volume=/dev/disk/:/dev/disk:ro`<br/>`--publish=30095:8080 --detach=true --name=cadvisor`<br/>`gcr.io/google-containers/cadvisor:latest` |
| 5) | Firewall disable | Either disable the firewall with `ufw disable`, or enable the following ports: `2049, 5432, 8000, 8001, 9000, 9001, 9090, 9093`
 |

## Installation

### Run Mode: Single Node

#### Step 1: Elevate Permissions to Root

`sudo bash`

This will ensure that all following steps are executed as root.

#### Step 2: Set Up Environment Variables &amp; Directories

```pre
export AIWARE_MODE=db,controller,engine,prometheus
export AIWARE_HOST_EXPIRE=false
export AIWARE_DB_PORT=5432 # IF: PG is running locally
export AIWARE_REGION=us-east-2 # IF: running in AWS

# use IP address to set URL
export AIWARE_CONTROLLER={$HOSTNAME}:9000/edge/v1

# generate a random UUID for edge token
export AIWARE_INIT_TOKEN=`uuidgen`
echo aiWARE Edge token is $AIWARE_INIT_TOKEN

#### OPTIONAL ####
export AIWARE_LICENSE=<LICENSE_TOKEN> # IF: you have one

export AIWARE_DB_ROOT=/opt/aiware/postgres
export AIWARE_REGISTRY_ROOT=/opt/aiware/registry
```

?> To debug engines, you may want to use `export AIWARE_AUTOREMOVE_ENGINES=false`. This will cause engine instances to persist after shutdown. **WARNING**: This will cause disk space to be used up very quickly on the partition that houses `/var/lib/docker` (most likely the root partition), so _it should only be used in a debug scenario, and then only for a short period._

#### Step 3: Run the Installation Command

`curl -sfL https://get.aiware.com | sh -`

This will run a shell script that installs the `aiware-agent` as a service. You can check its status by running `service aiware-agent status`.

#### Step 4: Validate the Installation

1. Run: `docker ps -a`. This should show the `aiware-prom-alertmgr`, `aiware-prometheus`, `aiware-pushgateway`, and `aiware-postgres`.

1. You can connect to the database at `localhost:5342`, or whichever port you have specified for `AIWARE_DB_PORT`, with **postgres/postgres** as the username/password.

1. Run: `docker logs -tf aiware-controller` to see the activity of `aiware-controller`.

1. Go to [http://&lt;HOST&gt;:9000/edge/v1/version](http://10.10.7.92:9000/edge/v1/version), or `curl localhost:9000/edge/v1/version`, for aiWARE Edge version information. This will return information such as :

```pre

{
"version": "---
build_date: Tue Feb 4 22:52:57 UTC 2020
git_repo: realtime
git_branch: HEAD
git_commit: f8a8130c88b8ed5b0e50a8f26bf45d5d9b1a22e1
git_author: joe
build_url: https://jenkins.veritone.com/job/aiware/job/edge-controller/1281/
build_number: 1281
"
}
```

**Get more info:**

1. `ai job create --help`, to see how you can run a job.
2. `ai job get --help`, to see how you can get job info.

## Run Mode: Two-Node Installation

### Admin Node

#### Required Prerequisites

See [Required Prerequisites](#required-prerequisites) above.

#### Step 1: Elevate Permissions to Root

`sudo bash`

This will ensure that all following steps are executed as root.

#### Step 2: Setup Environment Variables and Directories

```pre
export AIWARE_MODE=controller,db,registry,nfs,prometheus
export AIWARE_HOST_EXPIRE=false
export AIWARE_REGION=us-east-2 # IF: running in AWS

export AIWARE_DB_PORT=5432 # if PG is running locally
export AIWARE_DB_ROOT=/opt/aiware/postgres
export AIWARE_REGISTRY_ROOT=/opt/aiware/registry

# generate a random UUID for edge token
export AIWARE_INIT_TOKEN=`uuidgen`
echo aiWARE Edge token is $AIWARE_INIT_TOKEN

#### OPTIONAL ####
export AIWARE_LICENSE=<LICENSE_TOKEN> # IF: you have one
```

#### Step 3: Run Installation Command

`curl -sfL https://get.aiware.com | sh -`

#### Step 4: Validate the Installation

1. Run: `exportfs` to validate `/opt/aiware/nfs` is exported
2. Run: `docker ps` to validate `aiware-controller, aiware-postgres, aiware-registry` are running

> Note the IP address of the Admin box for use on the Processing Node.

### Processing Node

#### Required Prerequisites

See [Required Prerequisites](#required-prerequisites) above.

#### Step 1: Elevate Permissions to Root

`sudo bash`

This will ensure that all following steps are executed as root.

#### Step 2: Setup Environment Variables and Directories

```pre
export AIWARE_MODE=engine
export AIWARE_REGION=us-east-2
export AIWARE_HOST_EXPIRE=false

# This is the IP of the admin box, as noted above
export AIWARE_CONTROLLER=http://IP_OF_ADMIN_NODE:9000/edge/v1  
```

#### Step 3: Run Installation Command

`curl -sfL https://get.aiware.com | sh -`

## Environment Variables

These variables (created by aiWARE) will exist after installation:

| **Variable** | **Default Value** | **Description** |
| -- | --- | --- |
| AIWARE\_CONTROLLER | nil | URI to controller. Either config or AIWARE\_CONTROLLER is required |
| AIWARE\_LOG\_LEVEL | info | The API Token to use with controller |
| AIWARE\_LICENSE | nil | The license key for aiWARE |
| AIWARE\_CORE\_TOKEN | nil | Token for aiWARE CORE |
| AIWARE\_CLUSTERID | nil | Cluster Id for aiWARE CORE |
| AIWARE\_CORE\_URL | [https://api.veritone.com/v3/graphql](https://api.veritone.com/v3/graphql) | URL for Veritone API |
| AIWARE\_HOST\_IP | nil | Agent will use this IP instead of trying to figure out which IP to use if the host has multiple |
| AIWARE\_DB\_MIGRATE |  | Migrate the Database if it is on an older or non-existent schema version |
| AIWARE\_MODE | None | This is the mode for the host. This can be comma separated list. Valid values are: None (Default), All, Single, Engine, Database, Controller, NFS, Docker |
| AIWARE\_SERVER\_TYPE | Nil | This defaults to the host type from the cloud provider. |
| AIWARE\_NFS\_ROOT | /opt/aiware/nfs | This is the default directory for serving NFS /cache |
| AIWARE\_CACHE | /cache | This is the directory used for cache |
| AIWARE\_HOST\_EXPIRE | true | If yes or true, this host will expire. If any other value, then the host will not expire |
| AIWARE\_AUTOREMOVE\_ENGINES | true | This sets AutoRemove on the docker containers after they exit |
| AIWARE\_DB\_HOST | localhost | The port to use when launching PG |
| AIWARE\_DB\_PORT | 5432 | The port to use when launching PG |
| AIWARE\_DB\_USERNAME | postgres | The username to use when launching Postgres |
| AIWARE\_DB\_PASSWORD | postgres | The password to use when launching Postgres |
| AIWARE\_DB\_DBNAME | postgres | The database to use for postgres |
| AIWARE\_DB\_ROOT | /opt/aiware/postgres | The postgres root |
| AIWARE\_DB\_IMAGE | postgres:11 | The postgres image to launch |
| AIWARE\_DB\_MAX\_OPEN | 19 | Max open connections |
| AIWARE\_DB\_MAX\_IDLE | 2 | Max idle connections |
| AIWARE\_NFS\_ROOT | /opt/aiware/nfs | The nfs root |
| AIWARE\_NFS\_PERMITTED | empty | Set to 10.\* to permit 10.0.0.0/8 IPs otherwise unrestricted |
| AIWARE\_NFS\_MOUNT\_OPTS | nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport,lookupcache=positive | Options used for mount the NFS shares |
| AIWARE\_REGISTRY\_ROOT | /opt/aiware/registry | The registry root |
| AIWARE\_REGISTRY\_PORT | 9001 | The port to use when launching the docker registry |
| AIWARE\_REGISTRY\_IMAGE | registry:latest |
| AIWARE\_CONTROLLER\_PORT | 9000 | The port to use when launching controller |
| AIWARE\_CONTROLLER\_IMAGE | aiware-controller:latest | The image to use when launching controller |
| AIWARE\_CORE\_URL | NULL |
| AIWARE\_CONTROLLER\_AUTH\_DISABLED | NULL | Disable authentication |
| AIWARE\_PROMETHEUS\_IMAGE | prom/prometheus:v2.14.0 | The prometheus image to launch |
| AIWARE\_PROMETHEUS\_PORT | 9090 | The port to use for prometheus |
| AIWARE\_PROMETHEUS\_ROOT | /opt/aiware/prometheus | The directory that will be used for /etc/prometheus |
| AIWARE\_AWSLOGS\_ENABLED | false | Enable AWSLOGS/Cloudwatch for agents |
| AIWARE\_AWSLOGS\_REGION | us-east-1 | Region for the logs |
| AIWARE\_AWSLOGS\_GROUP | aiware | Log group for the logs |
| AIWARE\_AWSLOGS\_STREAM | v3f | Log stream to use |

## How to Update Edge Instance to Latest Build

The following steps will update the local aiWARE Edge instance with the latest build.

### Step 1: Elevate Permissions to Root

`sudo bash`

### Step 2: Stop/Remove Docker Containers

```pre
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```

### Step 3: Set Environment Variables

```pre
export $(cat /etc/systemd/system/aiware-agent.service.env | xargs)
export AIWARE_CONTROLLER=http://<ip of node>:9000/edge/v1
```

### Step 4: Run Installation Command

`curl -sfL https://get.aiware.com | sh -`

### Step 5: Locate and Take Note of API Token

`export` will allow you to see environment variables scoped to the current session

## Adding Edge to Relativity | Single Node or Admin Node

Once you have completed configuring your Edge with aiWARE, the steps below outline how to connect to your Relativity Instance.

### Step 1: Log in to Relativity 9 or 10 (Veritone aiWARE for Relativity  <- login info here)

### Step 2: Select Workspace

### Step 3: Change Processing Environment to Edge in Veritone Admin under Veritone AI Hub in Relativity

### Step 4: Add Public DNS to API Endpoint - this can be found in AWS within your instance or other External Server

For example: http://ec2-54-153-95-43.us-west-1.compute.amazonaws.com:9000

### Step 5: Add API Key from EDGE

Go to the Edge in command line

`export`

```pre
root@ip-172-31-12-79:~# export
declare -x AIWARE_CACHE="/opt/aiware/cache"
declare -x AIWARE_CONTROLLER="http://172.31.12.79:9000/edge/v1"
declare -x AIWARE_DB_PORT="5432"
declare -x AIWARE_DB_ROOT="/opt/aiware/postgres"
declare -x AIWARE_HOST_EXPIRE="false"
declare -x AIWARE_INIT_TOKEN="08bb6a59-58c7-4d46-b0dc-3fa8bf794fb5"
```

## Installing an Engine Locally

This example uses a translation engine (Pangeanic Spanish-to-English), but the procedure is the same for other cognitive engines.

<style>
.markdown-section pre>code.lang-sql {
  color:white;
  background-color:black;
  font-size: .75rem;
  line-height: 120%;
}
</style>

### Step 1: Create a File Named 'add-spanish.sql' with the Following Contents

```sql
INSERT INTO edge.engine_category (
    engine_category_id,
    engine_category_name,
    engine_category_type
  )
VALUES (
    '3b2b2ff8-44aa-4db4-9b71-ff96c3bf5923',
    'Translate',
    'Cognition'
  ) ON CONFLICT (engine_category_id) DO NOTHING;
INSERT INTO edge.engine (
    internal_organization_id,
    engine_id,
    engine_name,
    engine_state,
    engine_type,
    engine_output_type,
    engine_category_id,
    dependency,
    core_job_data,
    fields,
    validation,
    application_id,
    jwt_rights,
    parallel_processing,
    parent_complete_before_processing,
    edge_version,
    dontrun_complete,
    priority_adjustment,
    child_priority_adjustment_on_complete,
    replacement_engine_id,
    created_date_time,
    modified_date_time,
    cpu_shares,
    idle_timeout,
    update_status_interval
  )
VALUES (
    (
      SELECT internal_organization_id
      FROM edge.organization
      limit 1
    ), '95c910f6-4a26-4b66-96cb-488befa86466', 'Spanish-to-English', 'active', 'batch', 'chunk', '3b2b2ff8-44aa-4db4-9b71-ff96c3bf5923', '{}', '{}', '{}', '{}', '{}', '{}', false, false, 0, false, 0, 0, NULL,
    0,
    0,
    1024,
    0,
    10
  ) ON CONFLICT (engine_id) DO NOTHING;
INSERT INTO edge.build (
    build_id,
    engine_id,
    "version",
    build_state,
    docker_image,
    mf_engine_name,
    mf_engine_mode,
    mf_cluster_size,
    mf_custom_profile,
    mf_gpu_supported,
    mf_require_ec2,
    soft_vcpu_limit,
    soft_gpu_limit,
    soft_mem_bytes_limit,
    disk_free_bytes,
    license_expiration_timestamp,
    build_default_ttl,
    runtime
  )
VALUES (
    '66a6088b-d49e-4bc5-b9a7-4fa17af57b7e',
    '95c910f6-4a26-4b66-96cb-488befa86466',
    29,
    'deployed',
    '026972849384.dkr.ecr.us-east-1.amazonaws.com/prod-validated:95c910f6-4a26-4b66-96cb-488befa86466-66a6088b-d49e-4bc5-b9a7-4fa17af57b7e',
    'Spanish-to-English',
    'batch',
    'large',
    '',
    'none',
    false,
    1024,
    0,
    1073741824,
    1073741824,
    0,
    21600,
    '{"edge": {}}'
  ) ON CONFLICT (build_id) DO NOTHING;
  ```
  
### Step 2: Create a File Named 'add-ow.sql' with the Following Contents

This SQL script will add Output Writer to the system. (Output Writer is a necessary component for most aiWARE jobs.)
  
  ```sql
  INSERT INTO "edge"."build"(
      "build_id",
      "engine_id",
      "version",
      "build_state",
      "docker_image",
      "mf_engine_name",
      "mf_engine_mode",
      "mf_cluster_size",
      "mf_custom_profile",
      "mf_gpu_supported",
      "mf_require_ec2",
      "soft_vcpu_limit",
      "soft_gpu_limit",
      "soft_mem_bytes_limit",
      "disk_free_bytes",
      "license_expiration_timestamp",
      "build_default_ttl",
      "created_date_time",
      "modified_date_time",
      "runtime"
    )
  VALUES (
      '89599c9c-209f-4d8a-af02-0ab9e104f689',
      '8eccf9cc-6b6d-4d7d-8cb3-7ebf4950c5f3',
      16,
      'deployed',
      '026972849384.dkr.ecr.us-east-1.amazonaws.com/prod-validated:8eccf9cc-6b6d-4d7d-8cb3-7ebf4950c5f3-89599c9c-209f-4d8a-af02-0ab9e104f689',
      '',
      'chunk',
      'small',
      '',
      'none',
      FALSE,
      1024,
      0,
      1073741824,
      1073741824,
      0,
      21600,
      1583276111,
      1583276111,
      '{"edge": {}}'
    );
  ```

### Step 3: Turn Preload On
    
You need to do this each time you upload a new engine to your Edge installation.

Run this SQL:

```sql
update edge.engine SET preload = true;
```

### Step 4: Run 'cat' in Terminal to Insert the Relevant Records into the Edge Database

```bash
cat add-spanish.sql | docker container exec -i aiware-postgres /usr/bin/psql -U postgres -f -
cat add-ow-ec.sql | docker container exec -i aiware-postgres /usr/bin/psql -U postgres -f -
cat engines-preload.sql | docker container exec -i aiware-postgres /usr/bin/psql -U postgres -f -
```

### Step 5: Run 'docker pull' to Update Engines

```bash
docker pull registry.central.aiware.com/{ENGINEID}:{BUILDID}
```

## Create a Job Locally

You can use `curl` or Postman (or the equivalent) to run jobs locally with the REST API. This example uses the Pangeanic Spanish to English translation engine you installed above.

### Step 1: Run the Job

If you're using curl, this will create an engine job on the Edge instance. (Once you post the Curl command, wait a minute before pressing enter. This will give you the internal ID (save for later.) Don't forget to insert your API token in the header.

```curl
curl --request POST \
 --url http://localhost:9000/edge/v1/proc/job/create \
 --header 'authorization: Bearer <token here>' \
 --header 'content-type: application/json' \
 --data '{
 "jobs": [
   {
     "dueDateTime": "2020-03-09T20:49:18.331Z",
     "tasks": [
       {
         "correlationTaskId": "b44cd814-8646-41b9-ba40-86f854f8abe5",
         "dueDateTime": "2020-03-09T20:49:18.331Z",
         "engineId": "95c910f6-4a26-4b66-96cb-488befa86466",
         "ioFolders": [
           {
             "correlationID": "11744fac-1f17-4467-8c7d-9ff177117913",
             "mode": "chunk",
             "optionsJSON": "{}",
             "type": "output"
           }
         ],
         "maxEngines": 1,
         "maxRetries": 10,
         "payloadJSON": "{\"url\":\"https://vt-maxagg-test.s3.amazonaws.com/media/spanish.txt\"}",
         "taskPayloadJSON": "{\"url\":\"https://vt-maxagg-test.s3.amazonaws.com/media/spanish.txt\"}",
         "taskStatus": "pending",
					"priority": -10
       },
       {
         "correlationTaskId": "8b99ae25-eb0b-4b32-b708-4ab1658cbcbb",
         "dueDateTime": "2020-02-14T20:49:18.331Z",
         "engineId": "8eccf9cc-6b6d-4d7d-8cb3-7ebf4950c5f3",
         "ioFolders": [
           {
             "correlationID": "5c88a9da-a800-4b08-98ad-dadcaca5c53f",
             "mode": "chunk",
             "optionsJSON": "{}",
             "type": "input"
           }
         ],
         "maxEngines": 1,
         "maxRetries": 10,
         "payloadJSON": "{}",
         "taskPayloadJSON": "{}",
         "taskStatus": "pending"
       }
     ],
     "taskRoutes": [
       {
         "taskChildId": "b44cd814-8646-41b9-ba40-86f854f8abe5"
       },
       {
         "taskParentId": "b44cd814-8646-41b9-ba40-86f854f8abe5",
         "taskParentOutputId": "11744fac-1f17-4467-8c7d-9ff177117913",
         "taskChildId": "8b99ae25-eb0b-4b32-b708-4ab1658cbcbb",
         "taskChildInputId": "5c88a9da-a800-4b08-98ad-dadcaca5c53f"
       }
     ]
   }
 ]
}'
```

### Step 2: Validate the Cognition Engine Task

A few minutes after the above curl request is submitted, confirm that the engine task exists in the database.

```bash
docker container exec -it aiware-postgres /usr/bin/psql -U postgres -c 'SELECT task_status FROM edge.task'
```

### Step 3: Poll for job Status

Periodically issue this curl command (substituting your job's ID):

```curl
curl --request GET \
 --url http://localhost:9000/edge/v1/proc/job/<job id here>/outputs \
 --header 'authorization: Bearer <token here>'
 ```

When the job has completed, the file name of the output file will appear in the API response. This means that the file is ready to download. For example:

```json
{
 "outputs": {
   "internalJobID": "e1484460-7cb5-4cab-87ea-436c4768904f",
   "outputs": [
     {
       "created": 1581102672,
       "name": "vtn-standard-489cbc5b-b6b0-43d5-8b12-e790865986b5.json",
       "size": 4344
     }
   ]
 }
}
```

### Step 4: Download Job Results

Run this command, substituting your API token in the header (and your `internalJobID` and output file name in the URL):

```curl
curl --request GET \
 --url http://localhost:9000/edge/v1/proc/job/e1484460-7cb5-4cab-87ea-436c4768904f/output/vtn-standard-489cbc5b-b6b0-43d5-8b12-e790865986b5.json \
 --header 'authorization: Bearer <token here>'
 ```

?> If prompted for a password, just hit Enter. There is no password.

## Create a Job With Relativity

You can use the Relativity UI to push through jobs. You'll be able to track the files progress in both the UI and your command terminal. This example uses the Pangeanic Spanish to English translation engine you installed above.

### Step 1: Select a file in Relativity 

### Step 2: Choose the dropdown where it says “Edit” and select “Translate”

### Step 3: Choose Language you’d wish to Translate 

### Step 4: Confirm in the Translation Logs that the job is “In Progress” and has a Veritone Recording ID (will be the internal Job ID in Edge)

### Step 5: Confirm there's a Veritone Recording ID

Go to command line and onput `watch docker ps -a`. If the job is running properly, you’ll see a container that has the Engine ID + Build ID. To track your progress in Edge, copy the container id, hit `control + c` to exit out of `watch docker ps -a`. Insert `docker logs -tf “container id”`. Once the container is done, you’ll be back at the root. 

### Step 6: Confirm Output Writer container is running  

`watch docker ps -a`  in your command line interface 

### Step 7: Output Writer completes

Run `docker logs -tf aiware-controller 2>&1 | grep -i "internal job id"` in command line 

### Step 8: If job completed in Edge, the final call with be a Get to grab the vtn-standard json

### Step 9: You’ll be able to confirm the job completed in Relativity by going to the Translation Logs

## Licensing

### Overview

aiWARE Edge needs a license key that allows us to control what engine(s), how long the environment is available, and other concerns.

The licenses will be JWT tokens that can be validated by a service that knows the secret.

### Setup - Min.io


### Step 1: Create min.io access key and secret key with command below:

```pre
docker run --detach -p 10000:9000 \
  -e "MINIO_ACCESS_KEY=exampleEXAMPLE" \
  -e "MINIO_SECRET_KEY=exampleexampleexampleEXAMPLEKEY" \
  minio/minio server /opt/aiware/minio
  ```

### Step 2: Add port to AWS Instance (or Server) - Inbound only

### Step 3: Ensure that min.io is one of the containers on your Edge with command below:

`docker ps -a`

### Step 4: Create connection (via platform like Cyberduck) using ip address, access key, and secret key. Here’s what you’ll need: 

1. Public IP Address

2. Port 10000

3. MINIO_ACCESS_KEY

4. MINIO_SECRET_KEY

### Step 5: Once connected, create bucket that will be repository for CSV reports

### Step 6: Open up a second terminal, but don’t SSH in yet. Next we will create the license. With your aiware-license-keys folder on your local machine, you’ll need to update the license-template-example.json. Fields you will need to update: 

1. <allowedEngineIds>

2. <clusterID> - can be anything, but can also put rt-1cdc1d6d-a500-467a-bc46-d3c5bf3d6901

3. <reportStatisticsBucket> = bucket name for S3 for min.io

4. <requireReporting> = true

5. <customerId> - can create an org in core for tracking purposes

```json
{
    "allowedEngineIds": [
        "95c910f6-4a26-4b66-96cb-488befa86466",
        "c0e55cde-340b-44d7-bb42-2e0d65e98255"
    ],
    "excludedEngineIds": [
        "dd1f9266-21a6-4675-90f1-a4c3ed843e64"
    ],
    "enginesOwnedByCoreOrgIds": [
        "413a8cb5-c1f4-4548-89cc-a2fcdf1426dd",
        "5093d8c4-e057-4fee-9596-7216ac5bfd1a"
    ],
    "requireCore": false,
    "coreURI": "",
    "clusterID": "rt-239483920",
    "coreOrganizationId": "",
    "reportStatisticsBucket": "gfernandez-test",
    "allowedReportingFailures": 3,
    "requireReporting": true,
    "maxHosts": 11,
    "customerId": "12345",
    "allowedModes": [
        "Engine",
        "DB"
    ]
}
```
### Step 7:  Copy aiware-license-keys to Server 

`scp -r /Users/username/aiware-license-keys ubuntu@172.31.4.238:/home/ubuntu`

### Step 8: Execute command 

`aiware-agent license generate <path-to-private-key> <claims-file-json> <valid-period-in-days>`

Example below: 

`aiware-agent license generate /home/ubuntu/aiware-license-keys/app1.rsa /home/ubuntu/aiware-license-keys/license-template-example.json 2`

### Step 9: Copy license that’s produced 

### Step 10: Export AIWARE_LICENSE + AIWARE_MINIO_ENABLED=true, along with the other exports in the Configuration Guide 

`export AIWARE_MINIO_ENABLED=true`

`export AIWARE_LICENSE=<LICENSE_TOKEN>`

## Troubleshooting

#### Troubleshooting Jobs on Edge

These troubleshooting steps help to isolate the root cause of processing issues between Relativity and aiWARE Edge.

#### Step 1: Create a file on Edge named get-tasks.sql with the following contents

```sql
SELECT internal_job_id, internal_task_id, started_date_time, completed_date_time
FROM edge.task
WHERE task_status = 'complete'
 AND engine_id = '8eccf9cc-6b6d-4d7d-8cb3-7ebf4950c5f3'
ORDER BY completed_date_time DESC
LIMIT 20
```
#### Step 2: Execute the following command to run the query

`cat get-tasks.sql | docker container exec -i aiware-postgres /usr/bin/psql -U postgres -f -`

#### Step 3: Analyze the output. Make note of the <internal_job_id>  of any one of the completed tasks

#### Step 4: Search for the <internal_job_id> in the Veritone Recording ID field on the Translation Logs page.

Please validate that file is still in progress and not completed.  If it is completed, please pick a different job id from Step 3.

#### Step 5: Submit API request to validate outputs API

```curl
curl -sfl  --url http://localhost:9000/edge/v1/proc/<internal_job_id>/outputs \
--header 'authorization: Bearer <token here>'
```

Replace <token here> with the token from your Edge. Replace <internal_job_id> the job id from Step 4. Execute the command from the Edge server directly.

Note: that you should also test from the agent server where the job analyzer agent is installed. To execute the above in Powershell, run: 

This should return a JSON object with an output array and a name key that includes the name of a json file. 

If there is not an output, there is an issue with the /cache filesystem on the controller. If there is an output, proceed to Step 6.


#### Step 6: Submit API to validate output API

```curl
curl -sfl  --url 
http://localhost:9000/edge/v1/proc/<internal_job_id>/output/<output> \
 --header 'authorization: Bearer <token here>'
 ```

Replace <token here> with the token from your Edge. Replace <internal_job_id> the job id from Step 4. Replace <output> with the name of the json file (including the file extension) from Step 5.  Execute the command from the Edge server directly.

This should return the translated/transcribed result, indicating that the problem is not on the Edge.

#### View Engine Builds

Scenario - The engine + build you’re expecting to appear in Docker after you push a job through don’t appear. One reason could be multiple build IDs associated to an engine

#### Step 1: Create a file on Edge named engine-builds.sql with the following contents 

```sql
SELECT mf_engine_name, engine_id, build_id, build_state
FROM edge.build
WHERE build_state = 'deployed'
```
### Step 2: Execute the following command to run the query

`cat engine-builds.sql | docker container exec -i aiware-postgres /usr/bin/psql -U postgres -f -`

#### Step 3:  Analyze the output. Make note of the multiple build_id associated to one engine_id

### Check Job Status on Edge (File System or Relativity + Coreless)

Grep controller logs to view calls being made (can confirm Relativity’s connection to Edge or if job POST 

`docker logs -tf aiware-controller 2>&1 | grep -i "relativity"`
`docker logs -tf aiware-controller 2>&1 | grep -i "Internal Job ID"`

Grep syslog, ignoring prometheus (Good way to confirm if jobs have started, can view the engines being pulled down) 

`tail -f /var/log/syslog |grep -iv prometheus`

Get engine docker logs (Good for tracking progress of Transcription + Translation engine)

`docker logs -tf <container id>`

Confirming all containers placed on Edge 

`docker images`


