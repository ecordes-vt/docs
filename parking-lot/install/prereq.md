# Pre-requisites
aiWARE requires a Linux box or Linux VM running on a supported chipset (ARM64 or AMD64). It is not natively compatible with Windows or MacOS. You can use Ubuntu Linux running on VirtualBox VM to achieve successful installation on a Mac.

# Supported Operating Systems
* Ubuntu 18.04
* Ubuntu 20.04

# Supported Cloud Platforms
aiWARE can run on any environment that provides a linux VM.  aiWARE can be infrastructure or cloud-aware if run on a supported cloud platform.  Currently, aiWARE supports:
* AWS
* Azure (Coming Soon)

# Minimum Hardware
* 8GB RAM
* 100GB root partition

# Required packages

* docker.io - For running docker containers
* nfs-common - For connecting to NFS servers
* uuid - for generating UUIDs
* awscli - if using AWS

```bash
# system should be current
apt-get update -y
apt-get upgrade -y

# install paclages
apt-get install -y docker.io nfs-common awscli uuid
```

## NFS

```bash
apt-get install -y nfs-kernel-server
```

## Node statistics
aiWARE uses prometheus to collect host statistics.  To get these statistics, please include this in the startup of the server.

```bash
wget https://github.com/prometheus/node_exporter/releases/download/v1.0.1/node_exporter-1.0.1.linux-amd64.tar.gz
tar -xzf node_exporter-1.0.1.linux-amd64.tar.gz
service prometheus-node-exporter stop
cp node_exporter-1.0.1.linux-amd64/node_exporter /usr/bin/prometheus-node-exporter
curl https://get.aiware.com/files/nfs-prometheus-node-exporter -o prometheus-node-exporter
cp prometheus-node-exporter /etc/default
```

# Required directories

aiWARE by default installs into `/opt/aiware`.  This can be changed with `AIWARE_ROOT` environment variable.

# Known Issues
## 172.0.0.0/8 Are not supported

Currently `172.0.0.0.0/8` are not supported.  Please use `10.0.0.0/8` or `192.168.0.0/16` instead.