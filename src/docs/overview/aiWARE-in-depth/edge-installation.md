<!-- markdownlint-disable no-inline-html -->

# Installing Edge

This page outlines the procedure to install, configure, and validate an instance of Veritone aiWARE Edge (Coreless) for use in a fully network-isolated, on-premise deployment.

## Prerequisites

This procedure requires a Linux host (either physical, or VM) running on a supported chipset (ARM64 or AMD64).

> The current version of Edge is not _natively_ compatible with Windows nor MacOS. However, you can use Ubuntu Linux running on VirtualBox VM to achieve successful installation on a Mac.

### Step 1: Choose the Run Mode

You can run aiWARE Edge (Coreless) in a &quot;Single Node&quot; or a &quot;Two Nodes&quot; mode, depending on your needs. In a Single Node mode, all the necessary components will be installed on a single virtual or physical machine. This is useful for UAT, non-production environments, or other smaller-scale installations.
The Two Nodes setup is recommended for running the Admin UI.

### Step 2: Allocate Machines

The installation and configuration steps defined below assume that one or two (depending on the run mode) physical or virtual machines are available, accessible, and meet the following criteria.

The operating system for both nodes should be:

#### Engine Node

- 2 x CPU, 8-Cores each (Intel Xeon or similar)
- 32GB RAM DDR4
- At least 400GB of disk space per box on SSD
- Ubuntu Linux 18.04

#### Admin Node (_not_ required in a Single-Node mode)

- 2 x CPU, 8-Cores each (Intel Xeon or similar)
- 8GB RAM DDR4
- At least 400GB of disk space per box on SSD
- Ubuntu Linux 18.04

### Step 3: Machine Configuration

Ensure that the following steps are completed on each physical/virtual machine before proceeding with the aiWARE Edge installation.

| **#** | **Action** | **Commands** |
| --- | --- | --- |
| 1) | Install docker.io, nfs-common, awscli, &amp; uuid packages | `apt-get update -y` <br/>`apt-get upgrade -y`<br/>`apt-get install -y docker.io nfs-common`<br/>`apt-get install -y awscli uuid` |
| 2) | Create aiWARE directory and mount disk | `mkdir -p /opt/aiware`<br/>`# Replace sdXX with a data disk. If all on the root disk, skip the below`<br/>`mkfs.ext4 /dev/sdXX`<br/>`mount /dev/sdXX /opt/aiware` |
| 3) | Create local directories | `mkdir -p /opt/aiware/cache /opt/aiware/postgres`<br/>`/opt/aiware/cache /opt/aiware/nfs` |
| 4) | Map /cache | `# Only on the single node and admin node`<br/>`ln -s /opt/aiware/nfs /cache` |
| 5) | Install Logging Components (optional) | `apt-get install -y prometheus-node-exporter`<br/>`docker run --volume=/:/rootfs:ro`<br/>`--volume=/var/run:/var/run:ro`<br/>`--volume=/sys:/sys:ro`<br/>`--volume=/var/lib/docker/:/var/lib/docker:ro`<br/>`--volume=/dev/disk/:/dev/disk:ro`<br/>`--publish=30095:8080 --detach=true --name=cadvisor`<br/>`gcr.io/google-containers/cadvisor:latest` |
| 6) | Firewall | Either disable the firewall (ufw disable), or enable the following ports: `2049, 5432, 8000, 8001, 9000, 9001, 9090, 9093`
 |

## Installation

### Run Mode: Single Node

#### Step 1: Elevate Permissions to Root

`sudo bash`

This will ensure that all following steps are executed as root.

#### Step 2: Set Up Environment Variables &amp; Directories

`export AIWARE\_MODE=single`

`export AIWARE\_DB\_PORT=5432 # if PG is running locally`

`export AIWARE\_CACHE=/opt/aiware/cache`

`export AIWARE\_DB\_ROOT=/opt/aiware/postgres`

`export AIWARE\_REGISTRY\_ROOT=/opt/aiware/registry`

`export AIWARE\_REGION=us-east-1 # only relevant if running in AWS`

`export AIWARE\_HOST\_EXPIRE=false`

`export AIWARE\_INIT\_TOKEN=uuidgen # generate a random UUID for edge token`

`export AIWARE_CONTROLLER=http://ip_of_node:9000/edge/v1 # primary ip of the node`

#### Step 3: Run the Installation Command

`curl -sfL https://get.aiware.com | sh -`

This will run a shell sc ript that installs the `aiware-agent` as a service. You can check the status by running the `service aiware-agent status` command.

#### Step 4: Validate the Installation

1. Run: `docker ps -a`. This should show the `aiware-prom-alertmgr`, `aiware-prometheus`, `cadvisor`, `aiware-controller`, `aiware-postgres`, and `aiware-registry`.

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
git_author: al
build_url: https://jenkins.veritone.com/job/aiware/job/edge-controller/1281/
build_number: 1281
"
}
```

Get more info:

1. `ai job create --help`, to see how you can run a job.
2. `ai job get --help`, to see how you can get job info.

## Run Mode: Two Nodes

### Admin Node

#### Step 1: Elevate Permissions to Root

`sudo bash`

This will ensure that all following steps are executed as root.

#### Step 2: Setup Environment Variables and Directories

`export AIWARE_MODE=controller,db,registry,nfs,prometheus`

`export AIWARE_DB_PORT=5432 # if PG is running locally`

`export AIWARE_DB_ROOT=/opt/aiware/postgres`

`export AIWARE_REGISTRY_ROOT=/opt/aiware/registry`

`export AIWARE_REGION=us-east-1`

`export AIWARE_HOST_EXPIRE=false`

`export AIWARE_LICENSE=<LICENSE_KEY>`

`export AIWARE_INIT_TOKEN=uuidgen # generate a random UUID for edge token`

#### Step 3: Run Installation Command

`curl -sfL https://get.aiware.com | sh -`

#### Step 4: Validate the Installation

1. Run: `exportfs` to validate `/opt/aiware/nfs` is exported
2. Run: `docker ps` to validate `aiware-controller, aiware-postgres, aiware-registry` are running

Please note the IP address of the Admin box and use it for the other systems.

### Engine Node

#### Step 1: Elevate Permissions to Root

`sudo bash`

This will ensure that all following steps are executed as root.

#### Step 2: Setup Environment Variables and Directories

`export AIWARE_MODE=engine`

`export AIWARE_REGION=us-east-1`

`export AIWARE_CONTROLLER=http://IP\_OF\_ADMIN\_NODE:9000/edge/v1`

`export AIWARE_HOST_EXPIRE=false`

#### Step 3: Run Installation Command

`curl -sfL https://get.aiware.com | sh -`

## Environment Variables

| **Variable** | **Default Value** | **Description** |
| --- | --- | --- |
| AIWARE\_CONTROLLER | nil | URI to controller. Either config or AIWARE\_CONTROLLER is required |
| AIWARE\_LOG\_LEVEL | info | The API Token to use with controller |
| AIWARE\_LICENSE | nil | The license key for aiWARE |
| AIWARE\_CORE\_TOKEN | nil | Token for aiWARE CORE |
| AIWARE\_CLUSTERID | nil | Cluster Id for aiWARE CORE |
| AIWARE\_CORE\_URL | [https://api.veritone.com/v3/graphql](https://api.veritone.com/v3/graphql) | URL for Veritone API |
| AIWARE\_HOST\_IP | nil | Agent will use this IP instead of trying to figure out which IP to use if the host has multiple |
| AIWARE\_DB\_MIGRATE | Migrate the Database if it is on an older or non-existent schema version |
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
