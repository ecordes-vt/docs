# Agent

aiWARE is built on top of the agent which is a single static go binary.  The agent is responsible for setting up the individual host and communicating with Controller.  Depending on the mode, the agent will act appropriately.  The agent also installs itself as a command line interface (CLI) for the cluster.

# Modes

In aiWARE, every server can be one or more modes.

| Mode      |  Required | Description                                       |
| :-------- | :------- | :--------------------------------------- |
| db | Yes | This is a database server
| controller | Yes | This is the controller that provides the business logic for edge.  This also serves the Edge UI |
| nfs | Yes | This provides storage for the cluster |
| engine | Yes | This runs engines which processes content |
| registry| No | This runs a docker registry.  The controller
| prometheus | No | This provides metrics.  This is required for autoscale, edge UI and alerting |
| nsq | No | This provides an NSQ server for use in the cluster |
| redis | No | This provides a Redis server for use in the cluster |
| automate | No | this provides an automate server that runs automate studio |

This is set before installation of `aiware-agent` by the environment variable `AIWARE_MODE`.  For example, to set the mode to be controller, you would set:
```bash
export AIWARE_MODE=controller
```

## Multiple Modes

Servers can be multiple modes by separating the modes with a comma.  For example,
```bash
export AIWARE_MODE=db,controller,nfs,engine,prometheus
```

When `aiware-agent` launches, it will setup:
* DB
* Controller (connected to DB)
* NFS
* Engine
* Prometheus

## Single Mode

This is a special mode that expands to:
* DB
* Controller
* Registry
* Engine

# aiWARE Agent Service Directory
When aiWARE agent is installed, it installs into `/etc/systemd/system/` directory.

To change the run time environment variables,
1. edit `/etc/systemd/system/aiware-agent.service.env`
2. `systemctl daemon-reload`
3. `service aiware-agent restart`
