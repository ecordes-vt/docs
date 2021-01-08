# Configuration

aiWARE includes a configuration system for the main components of edge.  The config item consists of:
* Section - E.g., `admin`, `controller`, `db`, `registry`, `nfs`, `ceph` and `application`
* Key - E.g., db_max_open
* Type - Boolean, Integer, String
* Environment Variable - If this is set, the config item can be set via Environment Variable

To see the config items see [Config](../config/readme.md)

These configs can be set at the following levels:
* System - Admin, Controller, DB, Engine, NFS, Registry

To set a config item, you can set it via the UI or via CLI.

This sets the db_max_idle to 10.
```bash
aiware config set controller db_max_idle 10
```

## Listing configuration

```bash
aiware config ls
```

# Engine and Service configs

The `application` section is special.  When a key is set at in section `application` it is set system-wide. It can be overridden at the engine or application or organization level.

NOTE:
* Engine or Service will have to dynamically get that request for every organization as it will not be passed in as organization specific.  For example, the engine will have to retrieve the config setting via the controller API on every new Work Request

aiWARE supports credentials for common services.  Please see [Credentials](../config/config.md)

When an engine or service requests a config, controller will check the following:
* engine or service
* system-wide

Some of the services aiWARE supports are:
* AWS
* Azure
* Heroku
* Salesforce
* Twilio

You can see a list of the predefined keys for services and applications at [Credentials](../config/config.md)

## Environment Variables
aiWARE will set these as environment variables as `CFG_<KEY>`.  Any non alphanumeric characters will be replaced with an underscore.

For example, aws.secret_key will be set as CRED_AWS_SECRET_KEY for applications and environments when they are launched.

## Engine configuration
Engines register the keys they are require in the manifest under the json field `config`.  An example would be:
```json
{
  "config": ["aws.key", "aws.secret"]
}
```

The engine can also register additional keys via API.  An example to add a config to an engine would be:
```bash
aiware config --engine=<ENGINE_ID> add application aws.secret
aiware config --engine=<ENGINE_ID> set application aws.secret 1234567890
aiware config --engine=<ENGINE_ID> ls application
```

These will be passed to the engine instance on launch as environment variables: CFG_<KEY>=Value.  For example, resolution=high would be passed as CFG_RESOLUTION=high. Any non-alphanumeric characters will be replaced with an underscore (_)

### Default engine settings

The registry agent loads the default engine keys from the engine image as it is checked out and sets them if not set.  It gets them from `/var/aiware/manifest.json`.

An example config would be:
```.env
domain_name=veritone.com
email_template=simple
```

## Service configuration
These configs will be passed to the engine instance on launch as environment variables: ENG_<KEY>=Value.  For example, resolution=high would be passed as ENG_RESOLUTION=high.


The application can also register additional keys via API.  An example to add a config to an engine would be:
```bash
aiware config --service=<SERVICE_ID> add application aws.secret
aiware config --service=<SERVICE_ID> set application aws.secret 1234567890
aiware config --service=<SERVICE_ID> ls application
```

### Default service settings

The registry agent loads the default service keys from the service image as it is checked out and sets them if not set.  It gets them from `/var/aiware/manifest.json`.

An example config would be:
```.env
domain_name=veritone.com
email_template=simple
```

## Resolution

aiWARE will use the values for a specific service key in the following order:
* Engine or Application
* System (section is services)

If calling the API instead of using environment variables, the API will use WorkRequestID as section.  This will be a new endpoint.

# TODO
1. Supply organization-level configs -- These should come with GetWork call
