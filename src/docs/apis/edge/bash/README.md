# aiWARE Edge API Bash client

## Overview

This is a Bash client script for accessing aiWARE Edge API service.

The script uses cURL underneath for making all REST calls.

## Usage

```shell
# Make sure the script has executable rights
$ chmod u+x aiware

# Print the list of operations available on the service
$ ./aiware -h

# Print the service description
$ ./aiware --about

# Print detailed information about specific operation
$ ./aiware <operationId> -h

# Make GET request
./aiware --host http://<hostname>:<port> --accept xml <operationId> <queryParam1>=<value1> <header_key1>:<header_value2>

# Make GET request using arbitrary curl options (must be passed before <operationId>) to an SSL service using username:password
aiware -k -sS --tlsv1.2 --host https://<hostname> -u <user>:<password> --accept xml <operationId> <queryParam1>=<value1> <header_key1>:<header_value2>

# Make POST request
$ echo '<body_content>' | aiware --host <hostname> --content-type json <operationId> -

# Make POST request with simple JSON content, e.g.:
# {
#   "key1": "value1",
#   "key2": "value2",
#   "key3": 23
# }
$ echo '<body_content>' | aiware --host <hostname> --content-type json <operationId> key1==value1 key2=value2 key3:=23 -

# Preview the cURL command without actually executing it
$ aiware --host http://<hostname>:<port> --dry-run <operationid>

```

## Docker image

You can easily create a Docker image containing a preconfigured environment
for using the REST Bash client including working autocompletion and short
welcome message with basic instructions, using the generated Dockerfile:

```shell
docker build -t my-rest-client .
docker run -it my-rest-client
```

By default you will be logged into a Zsh environment which has much more
advanced auto completion, but you can switch to Bash, where basic autocompletion
is also available.

## Shell completion

### Bash

The generated bash-completion script can be either directly loaded to the current Bash session using:

```shell
source aiware.bash-completion
```

Alternatively, the script can be copied to the `/etc/bash-completion.d` (or on OSX with Homebrew to `/usr/local/etc/bash-completion.d`):

```shell
sudo cp aiware.bash-completion /etc/bash-completion.d/aiware
```

#### OS X

On OSX you might need to install bash-completion using Homebrew:

```shell
brew install bash-completion
```

and add the following to the `~/.bashrc`:

```shell
if [ -f $(brew --prefix)/etc/bash_completion ]; then
  . $(brew --prefix)/etc/bash_completion
fi
```

### Zsh

In Zsh, the generated `_aiware` Zsh completion file must be copied to one of the folders under `$FPATH` variable.

## Documentation for API Endpoints

All URIs are relative to */edge/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AdminApi* | [**addEngineToResource**](docs/AdminApi.md#addenginetoresource) | **POST** /admin/resource/{ResourceID}/engine | This API adds the engine to the resource
*AdminApi* | [**addServiceToResource**](docs/AdminApi.md#addservicetoresource) | **POST** /admin/resource/{ResourceID}/service | This API adds the service to the resource
*AdminApi* | [**addserversServerType**](docs/AdminApi.md#addserversservertype) | **POST** /admin/server_type/{ServerTypeID}/add | This API add servers to the specified server type
*AdminApi* | [**adminTerminateCluster**](docs/AdminApi.md#adminterminatecluster) | **POST** /admin/terminate | This terminates the cluster
*AdminApi* | [**applyLicense**](docs/AdminApi.md#applylicense) | **POST** /admin/licenses/apply | This applies a license to aiWARE
*AdminApi* | [**checkAuth**](docs/AdminApi.md#checkauth) | **POST** /admin/auth | This check auth for a token
*AdminApi* | [**clearBacklog**](docs/AdminApi.md#clearbacklog) | **POST** /admin/backlog/clear | This clears some or all of the currently queued tasks
*AdminApi* | [**createAdminApplication**](docs/AdminApi.md#createadminapplication) | **POST** /admin/applications/create | This creates a new application
*AdminApi* | [**createAdminCore**](docs/AdminApi.md#createadmincore) | **POST** /admin/cores/create | This creates a new core
*AdminApi* | [**createAdminOrganization**](docs/AdminApi.md#createadminorganization) | **POST** /admin/organizations/create | This updates the config for the cluster for a given key
*AdminApi* | [**createPermission**](docs/AdminApi.md#createpermission) | **POST** /admin/users/permission/create | This creates a new permission
*AdminApi* | [**createResource**](docs/AdminApi.md#createresource) | **POST** /admin/resource/create | This API creates a new resource definition such as a database, nsq or redis DB.
*AdminApi* | [**createRole**](docs/AdminApi.md#createrole) | **POST** /admin/users/role/create | This creates a new role
*AdminApi* | [**createServerType**](docs/AdminApi.md#createservertype) | **POST** /admin/server_types/create | This creates a new server type
*AdminApi* | [**createServerTypeEngineRunning**](docs/AdminApi.md#createservertypeenginerunning) | **POST** /admin/server_types/running_engine/create | This creates a new server_type_engine_running
*AdminApi* | [**createToken**](docs/AdminApi.md#createtoken) | **POST** /admin/tokens/create | This creates a new token
*AdminApi* | [**createUser**](docs/AdminApi.md#createuser) | **POST** /admin/users/create | This creates a new user
*AdminApi* | [**deleteApplication**](docs/AdminApi.md#deleteapplication) | **POST** /admin/applications/{ApplicationID}/delete | This deletes an application
*AdminApi* | [**deleteLicense**](docs/AdminApi.md#deletelicense) | **DELETE** /admin/licenses/{LicenseID}/delete | This deletes a license from aiWARE
*AdminApi* | [**deleteResource**](docs/AdminApi.md#deleteresource) | **POST** /admin/resource/{ResourceID}/delete | This deletes the specified resource
*AdminApi* | [**deleteRole**](docs/AdminApi.md#deleterole) | **POST** /admin/users/role/{RoleID}/delete | This deletes a role
*AdminApi* | [**deleteServerType**](docs/AdminApi.md#deleteservertype) | **DELETE** /admin/server_type/{ServerTypeID}/delete | This API deletes the specified server type
*AdminApi* | [**deleteServerTypePost**](docs/AdminApi.md#deleteservertypepost) | **POST** /admin/server_type/{ServerTypeID}/delete | This API deletes the specified server type
*AdminApi* | [**deleteServerTypeRunningEngine**](docs/AdminApi.md#deleteservertyperunningengine) | **DELETE** /admin/server_type/{ServerTypeID}/engine/{EngineID}/delete | This API deletes the running engine for a server type
*AdminApi* | [**deleteToken**](docs/AdminApi.md#deletetoken) | **POST** /admin/token/{TokenID}/delete | This deletes a token
*AdminApi* | [**deleteUser**](docs/AdminApi.md#deleteuser) | **POST** /admin/user/{UserID}/delete | This deletes a user
*AdminApi* | [**desiredserversServerType**](docs/AdminApi.md#desiredserversservertype) | **POST** /admin/server_type/{ServerTypeID}/desired | This API add servers to the specified server type
*AdminApi* | [**getAdminApplicationDetail**](docs/AdminApi.md#getadminapplicationdetail) | **GET** /admin/applications/{ApplicationID}/detail | This provides information on the given application.
*AdminApi* | [**getAdminCoreDetail**](docs/AdminApi.md#getadmincoredetail) | **GET** /admin/core/{CoreID}/detail | This provides information on the given core.
*AdminApi* | [**getAdminCores**](docs/AdminApi.md#getadmincores) | **GET** /admin/cores | This provides a list of core systems
*AdminApi* | [**getAdminEngineConfigSectionKey**](docs/AdminApi.md#getadminengineconfigsectionkey) | **GET** /admin/engine/{EngineID}/config/{ConfigSection}/{ConfigKey} | This provides a config section key for the engine
*AdminApi* | [**getAdminOrganizationDetail**](docs/AdminApi.md#getadminorganizationdetail) | **GET** /admin/organization/{OrganizationID}/detail | This gets organization detail by ID
*AdminApi* | [**getAdminOrganizationTokens**](docs/AdminApi.md#getadminorganizationtokens) | **GET** /admin/organization/{OrganizationID}/tokens | This provides information on the given organization tokens.
*AdminApi* | [**getAdminOrganizations**](docs/AdminApi.md#getadminorganizations) | **GET** /admin/organizations | This provides a list of organizations
*AdminApi* | [**getAdminPermissionDetail**](docs/AdminApi.md#getadminpermissiondetail) | **GET** /admin/users/permission/{PermissionID}/detail | This gets permission detail by ID
*AdminApi* | [**getAdminRoleDetail**](docs/AdminApi.md#getadminroledetail) | **GET** /admin/users/role/{RoleID}/detail | This gets role detail by ID
*AdminApi* | [**getAdminServiceConfig**](docs/AdminApi.md#getadminserviceconfig) | **GET** /admin/service/{ServiceID}/config | This provides all the config for the service
*AdminApi* | [**getAdminServiceConfigSection**](docs/AdminApi.md#getadminserviceconfigsection) | **GET** /admin/service/{ServiceID}/config/{ConfigSection} | This provides all the config for the service
*AdminApi* | [**getAdminServiceConfigSectionKey**](docs/AdminApi.md#getadminserviceconfigsectionkey) | **GET** /admin/service/{ServiceID}/config/{ConfigSection}/{ConfigKey} | This provides a config section key for the service
*AdminApi* | [**getAdminServiceInstances**](docs/AdminApi.md#getadminserviceinstances) | **GET** /admin/service/instances | This lists the service instances available for a system
*AdminApi* | [**getAdminStatus**](docs/AdminApi.md#getadminstatus) | **GET** /admin/status | This provides information on the status of the aiWARE edge
*AdminApi* | [**getAdminTokenDetail**](docs/AdminApi.md#getadmintokendetail) | **GET** /admin/token/{TokenID}/detail | Get the token info by ID
*AdminApi* | [**getAdminTokenPermissions**](docs/AdminApi.md#getadmintokenpermissions) | **GET** /admin/token/{TokenID}/permissions | This provides a list of all token permissions for a token by TokenID
*AdminApi* | [**getAdminTokens**](docs/AdminApi.md#getadmintokens) | **GET** /admin/tokens | This provides information about all tokens.
*AdminApi* | [**getAdminUserDetail**](docs/AdminApi.md#getadminuserdetail) | **GET** /admin/user/{UserID}/detail | This provides information on the given user.
*AdminApi* | [**getAdminUserPermissions**](docs/AdminApi.md#getadminuserpermissions) | **GET** /admin/user/{UserID}/permissions | This provides a list of all user permissions for an user by UserID
*AdminApi* | [**getAdminUserTokens**](docs/AdminApi.md#getadminusertokens) | **GET** /admin/user/{UserID}/tokens | This provides information on the given user.
*AdminApi* | [**getAdminUsers**](docs/AdminApi.md#getadminusers) | **GET** /admin/users | This provides a list of users in the system
*AdminApi* | [**getAdminUsersPermission**](docs/AdminApi.md#getadminuserspermission) | **GET** /admin/users/permissions | This provides a list of all user permissions in the system
*AdminApi* | [**getAdminUsersRoles**](docs/AdminApi.md#getadminusersroles) | **GET** /admin/users/roles | This provides a list of user role in the system
*AdminApi* | [**getApplications**](docs/AdminApi.md#getapplications) | **GET** /admin/applications | Get the list of applications deployed and available on aiWARE
*AdminApi* | [**getBacklogSummary**](docs/AdminApi.md#getbacklogsummary) | **GET** /admin/backlog/summary | This provides summary information on the current backlog
*AdminApi* | [**getConfig**](docs/AdminApi.md#getconfig) | **GET** /admin/config | This provides all the config for the cluster
*AdminApi* | [**getConfigSection**](docs/AdminApi.md#getconfigsection) | **GET** /admin/config/{ConfigSection} | This provides all the config for the cluster
*AdminApi* | [**getConfigSectionKey**](docs/AdminApi.md#getconfigsectionkey) | **GET** /admin/config/{ConfigSection}/{ConfigKey} | This provides a config section key for the cluster
*AdminApi* | [**getEnginesForResource**](docs/AdminApi.md#getenginesforresource) | **GET** /admin/resource/{ResourceID}/engines | Get list of engines for resource
*AdminApi* | [**getLicenseDetail**](docs/AdminApi.md#getlicensedetail) | **GET** /admin/licenses/{LicenseID}/detail | This gets detail on a license key
*AdminApi* | [**getLicenses**](docs/AdminApi.md#getlicenses) | **GET** /admin/licenses | This provides a licenses on the system
*AdminApi* | [**getResource**](docs/AdminApi.md#getresource) | **GET** /admin/resource/{ResourceID} | Get a resource definition
*AdminApi* | [**getResources**](docs/AdminApi.md#getresources) | **GET** /admin/resources | Get the list of resources
*AdminApi* | [**getResourcesForEngine**](docs/AdminApi.md#getresourcesforengine) | **GET** /admin/engine/{EngineID}/resources | Get list of resources for engine
*AdminApi* | [**getResourcesForHost**](docs/AdminApi.md#getresourcesforhost) | **GET** /admin/host/{HostID}/resources | Get list of resources for host
*AdminApi* | [**getResourcesForService**](docs/AdminApi.md#getresourcesforservice) | **GET** /admin/service/{ServiceID}/resources | Get list of resources for service
*AdminApi* | [**getServerType**](docs/AdminApi.md#getservertype) | **GET** /admin/server_type/{ServerTypeID}/detail | This provides detail on the server type
*AdminApi* | [**getServerTypeEngineRunning**](docs/AdminApi.md#getservertypeenginerunning) | **GET** /admin/server_types/running_engines | This lists the running engine with server types
*AdminApi* | [**getServerTypeEngineRunningDetail**](docs/AdminApi.md#getservertypeenginerunningdetail) | **GET** /admin/server_type/{ServerTypeID}/engine/{EngineID}/detail | This gets the detail of server type - running engine
*AdminApi* | [**getServerTypes**](docs/AdminApi.md#getservertypes) | **GET** /admin/server_types | This lists the server types available on the system
*AdminApi* | [**getServices**](docs/AdminApi.md#getservices) | **GET** /admin/services | This lists the services available on the system
*AdminApi* | [**loginUser**](docs/AdminApi.md#loginuser) | **POST** /admin/users/login | This logs a user in if successful
*AdminApi* | [**oauthLoginUser**](docs/AdminApi.md#oauthloginuser) | **POST** /admin/users/oauth2_login | This logs a user in if successful with OAuth2
*AdminApi* | [**registerUser**](docs/AdminApi.md#registeruser) | **POST** /admin/users/register | This registers a new user
*AdminApi* | [**removeEngineForResource**](docs/AdminApi.md#removeengineforresource) | **POST** /admin/resource/{ResourceID}/engine/{EngineID}/delete | This API removes the engine to the resource
*AdminApi* | [**removeserversServerType**](docs/AdminApi.md#removeserversservertype) | **POST** /admin/server_type/{ServerTypeID}/remove | This API removes servers from the specified server type
*AdminApi* | [**resetAllocTable**](docs/AdminApi.md#resetalloctable) | **POST** /admin/backlog/reset-alloc | This resets the alloc table
*AdminApi* | [**updateApplication**](docs/AdminApi.md#updateapplication) | **POST** /admin/applications/{ApplicationID}/update | This updates an application
*AdminApi* | [**updateConfigAll**](docs/AdminApi.md#updateconfigall) | **POST** /admin/config | This gets the config for the cluster
*AdminApi* | [**updateConfigSection**](docs/AdminApi.md#updateconfigsection) | **POST** /admin/config/{ConfigSection} | This gets the config for the cluster
*AdminApi* | [**updateConfigSectionKey**](docs/AdminApi.md#updateconfigsectionkey) | **POST** /admin/config/{ConfigSection}/{ConfigKey} | This updates the config for the cluster for a given key
*AdminApi* | [**updateEnginesForResource**](docs/AdminApi.md#updateenginesforresource) | **POST** /admin/resource/{ResourceID}/engine/update | This API updates the specified server type-running engine
*AdminApi* | [**updateOrganization**](docs/AdminApi.md#updateorganization) | **POST** /admin/organization/{OrganizationID}/update | This updates a organization
*AdminApi* | [**updatePermission**](docs/AdminApi.md#updatepermission) | **POST** /admin/users/permission/{PermissionID}/update | This updates a permission
*AdminApi* | [**updateResource**](docs/AdminApi.md#updateresource) | **POST** /admin/resource/{ResourceID}/update | This API updates the specified resource
*AdminApi* | [**updateResourceState**](docs/AdminApi.md#updateresourcestate) | **POST** /admin/resource/{ResourceID}/updatestate | This API updates the state of the specified resource
*AdminApi* | [**updateRole**](docs/AdminApi.md#updaterole) | **POST** /admin/users/role/{RoleID}/update | This updates a role
*AdminApi* | [**updateServerType**](docs/AdminApi.md#updateservertype) | **POST** /admin/server_type/{ServerTypeID}/update | This API updates the specified server type
*AdminApi* | [**updateServerTypeEngineRunning**](docs/AdminApi.md#updateservertypeenginerunning) | **POST** /admin/server_type/{ServerTypeID}/engine/{EngineID}/update | This API updates the specified server type-running engine
*AdminApi* | [**updateToken**](docs/AdminApi.md#updatetoken) | **POST** /admin/token/{TokenID}/update | This updates a token
*AdminApi* | [**updateUser**](docs/AdminApi.md#updateuser) | **POST** /admin/user/{UserID}/update | This updates a user
*AdminApi* | [**userPasswordForgot**](docs/AdminApi.md#userpasswordforgot) | **POST** /admin/users/password/forgot | This api will help users to reset their password when they forgot
*AdminApi* | [**userPasswordReset**](docs/AdminApi.md#userpasswordreset) | **POST** /admin/users/password/reset | Helps users to reset their password
*AdminApi* | [**userPasswordUpdate**](docs/AdminApi.md#userpasswordupdate) | **POST** /admin/users/password/update | This api will help users to update their password
*EngineApi* | [**createBuild**](docs/EngineApi.md#createbuild) | **POST** /admin/build/create | This API creates a new engine build
*EngineApi* | [**createEngine**](docs/EngineApi.md#createengine) | **POST** /admin/engine/create | This API creates a new engine
*EngineApi* | [**createEngineCategory**](docs/EngineApi.md#createenginecategory) | **POST** /admin/engine/category/create | This API creates a new engine category
*EngineApi* | [**deleteBuildPost**](docs/EngineApi.md#deletebuildpost) | **POST** /engine/{EngineID}/build/{BuildID}/delete | This API provides the engine detail result
*EngineApi* | [**deleteEnginePost**](docs/EngineApi.md#deleteenginepost) | **POST** /admin/engine/{EngineID}/delete | This API delets an engine
*EngineApi* | [**getEngineBuild**](docs/EngineApi.md#getenginebuild) | **GET** /admin/build/{BuildID}/detail | This gets a particular build
*EngineApi* | [**getEngineBuilds**](docs/EngineApi.md#getenginebuilds) | **GET** /admin/engine/{EngineID}/builds | Get the list of builds deployed and available on aiWARE for a particular engine
*EngineApi* | [**getEngineBuildsByState**](docs/EngineApi.md#getenginebuildsbystate) | **GET** /engine/builds | The api returns engine build records by build state
*EngineApi* | [**getEngineCategories**](docs/EngineApi.md#getenginecategories) | **GET** /admin/engine/categories | This provides a list of engine categories
*EngineApi* | [**getEngineCategoryDetail**](docs/EngineApi.md#getenginecategorydetail) | **GET** /admin/engine/category/{EngineCategoryID}/detail | This provides detail for an engine category
*EngineApi* | [**getEngineContainerCount**](docs/EngineApi.md#getenginecontainercount) | **GET** /engine/container_count | Get engine container count
*EngineApi* | [**getEngineDetail**](docs/EngineApi.md#getenginedetail) | **GET** /admin/engine/{EngineID}/detail | This API provides the engine detail result
*EngineApi* | [**getEngineInstanceDetail**](docs/EngineApi.md#getengineinstancedetail) | **GET** /engine/instance/{EngineInstanceID}/detail | Get information about an engine Instance
*EngineApi* | [**getEngineInstanceList**](docs/EngineApi.md#getengineinstancelist) | **GET** /engine/instances | Get engines instances with filtering
*EngineApi* | [**getEngineInstanceLogs**](docs/EngineApi.md#getengineinstancelogs) | **GET** /engine/instance/{EngineInstanceID}/logs | Get engine instance logs as a zip file
*EngineApi* | [**getEngineInstanceStatus**](docs/EngineApi.md#getengineinstancestatus) | **GET** /engine/instance/{EngineInstanceID}/status | Get the latest status of the engine instance
*EngineApi* | [**getEngineInstanceWork**](docs/EngineApi.md#getengineinstancework) | **POST** /engine/instance/{EngineInstanceID}/getwork | Get a work request
*EngineApi* | [**getEngineInstanceWorkDetail**](docs/EngineApi.md#getengineinstanceworkdetail) | **GET** /engine/instance/{EngineInstanceID}/workdetail | Get detail of the work being done by the engine instance
*EngineApi* | [**getEngineInstances**](docs/EngineApi.md#getengineinstances) | **GET** /engine/{EngineID}/instances | Get information about the instances of an engine
*EngineApi* | [**getEngineLaunchDetail**](docs/EngineApi.md#getenginelaunchdetail) | **GET** /engine/{EngineID}/launch/{LaunchID}/detail | This API returns the list of launches for this engine
*EngineApi* | [**getEngineLaunches**](docs/EngineApi.md#getenginelaunches) | **GET** /engine/{EngineID}/launches | This API returns the list of launches for this engine
*EngineApi* | [**getEngines**](docs/EngineApi.md#getengines) | **GET** /admin/engines | Get the list of engines deployed and available on aiWARE
*EngineApi* | [**getJobsBacklogCountByEngine**](docs/EngineApi.md#getjobsbacklogcountbyengine) | **POST** /proc/jobs/backlog_count_by_engine | Get backlog count by engine
*EngineApi* | [**getResourcesForEngineInstance**](docs/EngineApi.md#getresourcesforengineinstance) | **GET** /engine/instance/{EngineInstanceID}/resources | Get resources for engine instance
*EngineApi* | [**pauseBuild**](docs/EngineApi.md#pausebuild) | **POST** /admin/build/{BuildID}/pause | This API pauses a build so that tasks based on this engine build will not run.
*EngineApi* | [**pauseEngine**](docs/EngineApi.md#pauseengine) | **POST** /admin/engine/{EngineID}/pause | This API pauses an engine so that tasks based on this engine will not run.
*EngineApi* | [**registerEngineInstanceNoAuth**](docs/EngineApi.md#registerengineinstancenoauth) | **POST** /engine/instance/register | Register a new engine instance without authorization
*EngineApi* | [**replaceEngine**](docs/EngineApi.md#replaceengine) | **POST** /admin/engine/{EngineID}/replace | This API replaced an engine so that tasks based on this engine will not run.
*EngineApi* | [**resumeBuild**](docs/EngineApi.md#resumebuild) | **POST** /admin/build/{BuildID}/resume | This API resumes a build so that tasks based on this engine build will start running.
*EngineApi* | [**resumeEngine**](docs/EngineApi.md#resumeengine) | **POST** /admin/engine/{EngineID}/resume | This API resumes a build so that tasks based on this engine build will start running.
*EngineApi* | [**terminateEngineInstance**](docs/EngineApi.md#terminateengineinstance) | **POST** /engine/instance/{EngineInstanceID}/terminate | Delete the engine instance record
*EngineApi* | [**updateEngine**](docs/EngineApi.md#updateengine) | **POST** /admin/engine/{EngineID}/update | This API updates the specified engine
*EngineApi* | [**updateEngineBuild**](docs/EngineApi.md#updateenginebuild) | **POST** /admin/build/{BuildID}/update | This API updates the specified engine
*EngineApi* | [**updateEngineBuildState**](docs/EngineApi.md#updateenginebuildstate) | **POST** /engine/build/{BuildID}/state | Update the Engine Build State
*EngineApi* | [**updateEngineCategory**](docs/EngineApi.md#updateenginecategory) | **POST** /admin/engine/category/{EngineCategoryID}/update | This updates the specified engine category
*EngineApi* | [**updateEngineInstanceStatus**](docs/EngineApi.md#updateengineinstancestatus) | **POST** /engine/instance/{EngineInstanceID}/updatestatus | Update the Engine Instance Status.  Heartbeat to communicate back to controller both aggregated work and delta work from last heartbeat
*FlowApi* | [**cleanAutomateRequests**](docs/FlowApi.md#cleanautomaterequests) | **GET** /flowaction/requests/clean | Clean old automate requests.
*FlowApi* | [**createNodeRedContainerInfo**](docs/FlowApi.md#createnoderedcontainerinfo) | **POST** /flow/nrcontainer/create | Create node-red container infomation
*FlowApi* | [**deleteAutomateContainer**](docs/FlowApi.md#deleteautomatecontainer) | **POST** /flow/delete/{ContainerID} | Delete automate container.
*FlowApi* | [**updateAutomateRequestStatus**](docs/FlowApi.md#updateautomaterequeststatus) | **POST** /flow/request/update | Put this automate request into update status mode. This automate request will be updated to new status.
*FlowApi* | [**updateAutomateStatus**](docs/FlowApi.md#updateautomatestatus) | **POST** /flow/{HostID}/updatestatus | Get updated information to launch node-red container, terminate node-red container.
*HostApi* | [**drainHost**](docs/HostApi.md#drainhost) | **POST** /host/{HostID}/drain | Put this host into drain mode.  A host in drain mode will not have work assigned to engines on the host.
*HostApi* | [**getHostCpuUsage**](docs/HostApi.md#gethostcpuusage) | **GET** /hosts/cpu_usage | Get host cpu usage
*HostApi* | [**getHostDetail**](docs/HostApi.md#gethostdetail) | **GET** /host/{HostID}/detail | Get the latest info of the host
*HostApi* | [**getHostMemoryUsage**](docs/HostApi.md#gethostmemoryusage) | **GET** /engine/memory_usage | Get host memory usage
*HostApi* | [**getHostStatus**](docs/HostApi.md#gethoststatus) | **GET** /host/{HostID}/status | Get the latest status of the host
*HostApi* | [**getHosts**](docs/HostApi.md#gethosts) | **GET** /hosts | This provides a list of hosts in the system
*HostApi* | [**getHostsCounts**](docs/HostApi.md#gethostscounts) | **GET** /hosts/counts | Get the server counts in a time-range
*HostApi* | [**getHostsCountsByType**](docs/HostApi.md#gethostscountsbytype) | **GET** /hosts/counts_by_type | Get the server counts in a time-range
*HostApi* | [**getHostsLaunch**](docs/HostApi.md#gethostslaunch) | **GET** /host/{HostID}/launch | This provides a list of host launches in the system
*HostApi* | [**hostAlert**](docs/HostApi.md#hostalert) | **POST** /host/alert | Notifies the controller about a system alert.
*HostApi* | [**launchHost**](docs/HostApi.md#launchhost) | **POST** /host/launch | Launch a new host with a particular server type
*HostApi* | [**pauseHost**](docs/HostApi.md#pausehost) | **POST** /host/{HostID}/pause | Pause all engines on this host.
*HostApi* | [**registerEngineInstance**](docs/HostApi.md#registerengineinstance) | **POST** /host/{HostID}/engine/register | Register a new engine instance
*HostApi* | [**registerHost**](docs/HostApi.md#registerhost) | **POST** /host/register | Update the Host Status
*HostApi* | [**resumeHost**](docs/HostApi.md#resumehost) | **POST** /host/{HostID}/resume | Resume all engines on this host.
*HostApi* | [**terminateHost**](docs/HostApi.md#terminatehost) | **POST** /host/{HostID}/terminate | Delete the host/agent record.  Any work still running on this host will be restarted on other hosts.
*HostApi* | [**updateHostStatus**](docs/HostApi.md#updatehoststatus) | **POST** /host/{HostID}/updatestatus | Update the Host Status
*ProcessApi* | [**addTask**](docs/ProcessApi.md#addtask) | **POST** /proc/job/{JobID}/addtask | Adds a Task to a current job
*ProcessApi* | [**addTaskRoute**](docs/ProcessApi.md#addtaskroute) | **POST** /proc/job/{JobID}/addtaskroute | Adds a Task Route to a current job
*ProcessApi* | [**createJob**](docs/ProcessApi.md#createjob) | **POST** /proc/job/create | This creates a new Job
*ProcessApi* | [**deleteJob**](docs/ProcessApi.md#deletejob) | **POST** /proc/job/{JobID}/delete | This API deletes the specified job
*ProcessApi* | [**deleteTask**](docs/ProcessApi.md#deletetask) | **POST** /proc/task/{TaskID}/delete | This API deletes the specified task
*ProcessApi* | [**getEngineErrorTimeRanges**](docs/ProcessApi.md#getengineerrortimeranges) | **GET** /proc/tasks/error/engine_error_time_ranges | This gets engine error count by error tasks grouped by time ranges and sorted by a range start time
*ProcessApi* | [**getJobDetail**](docs/ProcessApi.md#getjobdetail) | **GET** /proc/job/{JobID}/detail | Gets Job Detail
*ProcessApi* | [**getJobDownload**](docs/ProcessApi.md#getjobdownload) | **GET** /proc/job/{JobID}/download/{JobOutputName} | Returns the contents of the job&#39;s output
*ProcessApi* | [**getJobOutput**](docs/ProcessApi.md#getjoboutput) | **GET** /proc/job/{JobID}/output/{JobOutputName} | Returns the contents of the job&#39;s output
*ProcessApi* | [**getJobOutputs**](docs/ProcessApi.md#getjoboutputs) | **GET** /proc/job/{JobID}/outputs | Returns a list of output information about this job
*ProcessApi* | [**getJobPerformance**](docs/ProcessApi.md#getjobperformance) | **GET** /proc/job/{JobID}/performance | This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time
*ProcessApi* | [**getJobStatus**](docs/ProcessApi.md#getjobstatus) | **GET** /proc/job/{JobID}/status | Gets Job Status
*ProcessApi* | [**getJobWorkRequests**](docs/ProcessApi.md#getjobworkrequests) | **GET** /proc/job/{JobID}/workrequests | This provides a list of workrequests of a job
*ProcessApi* | [**getJobs**](docs/ProcessApi.md#getjobs) | **GET** /proc/jobs | This gets a list of jobs
*ProcessApi* | [**getJobsOrganizationStats**](docs/ProcessApi.md#getjobsorganizationstats) | **GET** /proc/jobs/stats/organization | This gets processing stats of the jobs by organization
*ProcessApi* | [**getJobsPerformance**](docs/ProcessApi.md#getjobsperformance) | **GET** /proc/jobs/performance | This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time
*ProcessApi* | [**getJobsStats**](docs/ProcessApi.md#getjobsstats) | **GET** /proc/jobs/stats | This gets processing stats of the jobs
*ProcessApi* | [**getJobsTimeRangesStats**](docs/ProcessApi.md#getjobstimerangesstats) | **GET** /proc/jobs/stats/time_ranges | This gets processing stats of the jobs grouped by time ranges and sorted by a range start time
*ProcessApi* | [**getRatePendingScheduledJobs**](docs/ProcessApi.md#getratependingscheduledjobs) | **GET** /proc/scheduled_jobs/rate_pending_time_ranges | This gets the rate of pending scheduled jobs by time ranges
*ProcessApi* | [**getScheduledJobDetail**](docs/ProcessApi.md#getscheduledjobdetail) | **GET** /proc/scheduled_job/{ScheduledJobID}/detail | This gets scheduled job detail
*ProcessApi* | [**getScheduledJobs**](docs/ProcessApi.md#getscheduledjobs) | **GET** /proc/scheduled_jobs | This gets a list of scheduled jobs
*ProcessApi* | [**getServerErrorCounts**](docs/ProcessApi.md#getservererrorcounts) | **GET** /proc/tasks/error/server_error_counts | Get server error counts in a time-range
*ProcessApi* | [**getTaskDetail**](docs/ProcessApi.md#gettaskdetail) | **GET** /proc/task/{TaskID}/detail | Gets Task Detail
*ProcessApi* | [**getTaskDownload**](docs/ProcessApi.md#gettaskdownload) | **GET** /proc/task/{TaskID}/download/{TaskOutputName} | Returns the contents of the task&#39;s output
*ProcessApi* | [**getTaskLogs**](docs/ProcessApi.md#gettasklogs) | **GET** /proc/task/{TaskID}/logs | Gets logs associated with a task
*ProcessApi* | [**getTaskOutput**](docs/ProcessApi.md#gettaskoutput) | **GET** /proc/task/{TaskID}/output/{TaskOutputName} | Returns the contents of the task&#39;s output
*ProcessApi* | [**getTaskOutputs**](docs/ProcessApi.md#gettaskoutputs) | **GET** /proc/task/{TaskID}/outputs | Gets Task Output
*ProcessApi* | [**getTaskSyncBacklog**](docs/ProcessApi.md#gettasksyncbacklog) | **GET** /proc/tasks/sync_backlog | Gets task sync backlog in a time-range
*ProcessApi* | [**getTasks**](docs/ProcessApi.md#gettasks) | **GET** /proc/tasks | This gets a list of tasks based on the provided criteria
*ProcessApi* | [**getTasksErrorTypeCountByEngine**](docs/ProcessApi.md#gettaskserrortypecountbyengine) | **GET** /proc/tasks/error/count_type_by_engine | This gets error type count by engines
*ProcessApi* | [**getTasksErrors**](docs/ProcessApi.md#gettaskserrors) | **GET** /proc/tasks/errors | This provides a error list in a time range
*ProcessApi* | [**getTasksInstances**](docs/ProcessApi.md#gettasksinstances) | **GET** /proc/tasks/instances/by_category_host | This gets processing stats of the tasks
*ProcessApi* | [**getTasksStats**](docs/ProcessApi.md#gettasksstats) | **GET** /proc/tasks/stats | This gets processing stats of the tasks
*ProcessApi* | [**getTasksStatsCategories**](docs/ProcessApi.md#gettasksstatscategories) | **GET** /proc/tasks/stats/categories | This gets processing stats of the tasks grouped by engine categories
*ProcessApi* | [**getTasksStatsEngines**](docs/ProcessApi.md#gettasksstatsengines) | **GET** /proc/tasks/stats/engines | This gets processing stats of the tasks grouped by engine
*ProcessApi* | [**getTasksStatsOrganizations**](docs/ProcessApi.md#gettasksstatsorganizations) | **GET** /proc/tasks/stats/organizations | This gets processing stats of the tasks grouped by engine, filter by organizations
*ProcessApi* | [**getTasksStatsTimeRanges**](docs/ProcessApi.md#gettasksstatstimeranges) | **GET** /proc/tasks/stats/time_ranges | This gets processing stats of the tasks grouped by time ranges and sorted by a range start time
*ProcessApi* | [**getTotalPendingScheduledJobs**](docs/ProcessApi.md#gettotalpendingscheduledjobs) | **GET** /proc/scheduled_jobs/total_pending_time_ranges | This gets the total pending scheduled jobs by time ranges
*ProcessApi* | [**getWorkRequest**](docs/ProcessApi.md#getworkrequest) | **GET** /proc/workrequest/{WorkRequestID}/detail | This provides detail of workrequest
*ProcessApi* | [**launchJobTemplate**](docs/ProcessApi.md#launchjobtemplate) | **POST** /proc/template/{TemplateID}/launch | This launch a job based on the given job template
*ProcessApi* | [**pushContentToEndpoint**](docs/ProcessApi.md#pushcontenttoendpoint) | **POST** /proc/endpoint/{Endpoint} | Whatever is posted to this endpoint will be added to the child input folder(s) for the task_routes that have this endpoint.  If more than one task_routes have this endpoint, it will be added to all child input folders.
*ProcessApi* | [**recheckJobStatus**](docs/ProcessApi.md#recheckjobstatus) | **GET** /proc/job/{JobID}/recheck_status | Recheck Job Status
*ProcessApi* | [**tasksStatusExport**](docs/ProcessApi.md#tasksstatusexport) | **GET** /proc/tasks/stats/export | Export a task status report as a excel file
*ProcessApi* | [**updateTaskStatus**](docs/ProcessApi.md#updatetaskstatus) | **POST** /proc/tasks/update_status | This updates the status for a bulk of tasks by taskID
*ServiceApi* | [**createServiceInstance**](docs/ServiceApi.md#createserviceinstance) | **POST** /service/instance/create | This creates a new service instance
*ServiceApi* | [**deleteServiceInstance**](docs/ServiceApi.md#deleteserviceinstance) | **POST** /service/instance/{ServiceInstanceID}/delete | This deletes a service instance
*ServiceApi* | [**getResourcesForServiceInstance**](docs/ServiceApi.md#getresourcesforserviceinstance) | **GET** /service/instance/{ServiceInstanceID}/resources | Get resources for service instance


## Documentation For Models

 - [AddEngineForResourceRequest](docs/AddEngineForResourceRequest.md)
 - [AddEngineForResourceResponse](docs/AddEngineForResourceResponse.md)
 - [AddEngineForResourceResponseResult](docs/AddEngineForResourceResponseResult.md)
 - [AddServersToServerTypeRequest](docs/AddServersToServerTypeRequest.md)
 - [AddServiceForResourceRequest](docs/AddServiceForResourceRequest.md)
 - [AddServiceForResourceResponse](docs/AddServiceForResourceResponse.md)
 - [AddServiceForResourceResponseResult](docs/AddServiceForResourceResponseResult.md)
 - [AddTaskRequest](docs/AddTaskRequest.md)
 - [AddTaskResponse](docs/AddTaskResponse.md)
 - [AddTaskRouteDetail](docs/AddTaskRouteDetail.md)
 - [AddTaskRouteRequest](docs/AddTaskRouteRequest.md)
 - [AddTaskRouteResponse](docs/AddTaskRouteResponse.md)
 - [AdminApplicationCreateRequest](docs/AdminApplicationCreateRequest.md)
 - [AdminApplicationCreateResponse](docs/AdminApplicationCreateResponse.md)
 - [AdminApplicationDeleteResponse](docs/AdminApplicationDeleteResponse.md)
 - [AdminApplicationGetDetailResponse](docs/AdminApplicationGetDetailResponse.md)
 - [AdminApplicationUpdateRequest](docs/AdminApplicationUpdateRequest.md)
 - [AdminApplicationUpdateResponse](docs/AdminApplicationUpdateResponse.md)
 - [AdminApplicationsGetResponse](docs/AdminApplicationsGetResponse.md)
 - [AdminAuthRequest](docs/AdminAuthRequest.md)
 - [AdminAuthRequestAuth](docs/AdminAuthRequestAuth.md)
 - [AdminAuthResponse](docs/AdminAuthResponse.md)
 - [AdminAuthResponseResult](docs/AdminAuthResponseResult.md)
 - [AdminConfigResponse](docs/AdminConfigResponse.md)
 - [AdminConfigSectionKeyResponse](docs/AdminConfigSectionKeyResponse.md)
 - [AdminConfigSectionResponse](docs/AdminConfigSectionResponse.md)
 - [AdminConfigUpdateRequest](docs/AdminConfigUpdateRequest.md)
 - [AdminConfigUpdateResponse](docs/AdminConfigUpdateResponse.md)
 - [AdminConfigUpdateSectionKeyRequest](docs/AdminConfigUpdateSectionKeyRequest.md)
 - [AdminConfigUpdateSectionKeyResponse](docs/AdminConfigUpdateSectionKeyResponse.md)
 - [AdminConfigUpdateSectionRequest](docs/AdminConfigUpdateSectionRequest.md)
 - [AdminConfigUpdateSectionResponse](docs/AdminConfigUpdateSectionResponse.md)
 - [AdminCoreCreateRequest](docs/AdminCoreCreateRequest.md)
 - [AdminCoreCreateResponse](docs/AdminCoreCreateResponse.md)
 - [AdminCoreGetDetailResponse](docs/AdminCoreGetDetailResponse.md)
 - [AdminEngineConfigSectionKeyResponse](docs/AdminEngineConfigSectionKeyResponse.md)
 - [AdminGetTokensResponse](docs/AdminGetTokensResponse.md)
 - [AdminHostsGetResponse](docs/AdminHostsGetResponse.md)
 - [AdminOperationRequest](docs/AdminOperationRequest.md)
 - [AdminOperationResponse](docs/AdminOperationResponse.md)
 - [AdminOrganizationCreateRequest](docs/AdminOrganizationCreateRequest.md)
 - [AdminOrganizationCreateResponse](docs/AdminOrganizationCreateResponse.md)
 - [AdminOrganizationGetDetailResponse](docs/AdminOrganizationGetDetailResponse.md)
 - [AdminOrganizationGetTokensResponse](docs/AdminOrganizationGetTokensResponse.md)
 - [AdminOrganizationUpdateRequest](docs/AdminOrganizationUpdateRequest.md)
 - [AdminOrganizationUpdateResponse](docs/AdminOrganizationUpdateResponse.md)
 - [AdminOrganizationsGetResponse](docs/AdminOrganizationsGetResponse.md)
 - [AdminPermissionCreateRequest](docs/AdminPermissionCreateRequest.md)
 - [AdminPermissionCreateResponse](docs/AdminPermissionCreateResponse.md)
 - [AdminPermissionDetailResponse](docs/AdminPermissionDetailResponse.md)
 - [AdminPermissionUpdateRequest](docs/AdminPermissionUpdateRequest.md)
 - [AdminPermissionUpdateResponse](docs/AdminPermissionUpdateResponse.md)
 - [AdminRoleCreateRequest](docs/AdminRoleCreateRequest.md)
 - [AdminRoleCreateResponse](docs/AdminRoleCreateResponse.md)
 - [AdminRoleDeleteResponse](docs/AdminRoleDeleteResponse.md)
 - [AdminRoleDetailResponse](docs/AdminRoleDetailResponse.md)
 - [AdminRoleUpdateRequest](docs/AdminRoleUpdateRequest.md)
 - [AdminRoleUpdateResponse](docs/AdminRoleUpdateResponse.md)
 - [AdminServiceConfigResponse](docs/AdminServiceConfigResponse.md)
 - [AdminServiceConfigSectionKeyResponse](docs/AdminServiceConfigSectionKeyResponse.md)
 - [AdminServiceConfigSectionResponse](docs/AdminServiceConfigSectionResponse.md)
 - [AdminStatusDetail](docs/AdminStatusDetail.md)
 - [AdminTokenCreateRequest](docs/AdminTokenCreateRequest.md)
 - [AdminTokenCreateResponse](docs/AdminTokenCreateResponse.md)
 - [AdminTokenDeleteResponse](docs/AdminTokenDeleteResponse.md)
 - [AdminTokenPermissionsGetResponse](docs/AdminTokenPermissionsGetResponse.md)
 - [AdminTokenUpdateRequest](docs/AdminTokenUpdateRequest.md)
 - [AdminTokenUpdateResponse](docs/AdminTokenUpdateResponse.md)
 - [AdminUserCreateRequest](docs/AdminUserCreateRequest.md)
 - [AdminUserCreateResponse](docs/AdminUserCreateResponse.md)
 - [AdminUserDeleteResponse](docs/AdminUserDeleteResponse.md)
 - [AdminUserGetDetailResponse](docs/AdminUserGetDetailResponse.md)
 - [AdminUserGetTokensResponse](docs/AdminUserGetTokensResponse.md)
 - [AdminUserLoginRequest](docs/AdminUserLoginRequest.md)
 - [AdminUserLoginResponse](docs/AdminUserLoginResponse.md)
 - [AdminUserOAuth2LoginRequest](docs/AdminUserOAuth2LoginRequest.md)
 - [AdminUserPasswordForgotRequest](docs/AdminUserPasswordForgotRequest.md)
 - [AdminUserPasswordForgotResponse](docs/AdminUserPasswordForgotResponse.md)
 - [AdminUserPasswordResetRequest](docs/AdminUserPasswordResetRequest.md)
 - [AdminUserPasswordResetResponse](docs/AdminUserPasswordResetResponse.md)
 - [AdminUserPasswordUpdateRequest](docs/AdminUserPasswordUpdateRequest.md)
 - [AdminUserPasswordUpdateResponse](docs/AdminUserPasswordUpdateResponse.md)
 - [AdminUserPermissionsGetResponse](docs/AdminUserPermissionsGetResponse.md)
 - [AdminUserRegisterRequest](docs/AdminUserRegisterRequest.md)
 - [AdminUserRegisterResponse](docs/AdminUserRegisterResponse.md)
 - [AdminUserUpdateRequest](docs/AdminUserUpdateRequest.md)
 - [AdminUserUpdateResponse](docs/AdminUserUpdateResponse.md)
 - [AdminUsersGetResponse](docs/AdminUsersGetResponse.md)
 - [AdminUsersPermissionsGetResponse](docs/AdminUsersPermissionsGetResponse.md)
 - [AdminUsersRolesGetResponse](docs/AdminUsersRolesGetResponse.md)
 - [ApplicationDetail](docs/ApplicationDetail.md)
 - [ApplicationStatusEnum](docs/ApplicationStatusEnum.md)
 - [ApplicationTypeEnum](docs/ApplicationTypeEnum.md)
 - [AuthActionEnum](docs/AuthActionEnum.md)
 - [BacklogSummaryDetail](docs/BacklogSummaryDetail.md)
 - [BuildDetail](docs/BuildDetail.md)
 - [ChartTypeEnum](docs/ChartTypeEnum.md)
 - [ChunkCountInfo](docs/ChunkCountInfo.md)
 - [ConfigSection](docs/ConfigSection.md)
 - [ConfigSectionEnum](docs/ConfigSectionEnum.md)
 - [ConfigSectionKey](docs/ConfigSectionKey.md)
 - [ContainerStatus](docs/ContainerStatus.md)
 - [ContainerTypeEnum](docs/ContainerTypeEnum.md)
 - [CoreDetail](docs/CoreDetail.md)
 - [CreateApplicationDetail](docs/CreateApplicationDetail.md)
 - [CreateBuildDetail](docs/CreateBuildDetail.md)
 - [CreateBuildRequest](docs/CreateBuildRequest.md)
 - [CreateBuildResponse](docs/CreateBuildResponse.md)
 - [CreateCoreDetail](docs/CreateCoreDetail.md)
 - [CreateEngineCategoryDetail](docs/CreateEngineCategoryDetail.md)
 - [CreateEngineCategoryResponse](docs/CreateEngineCategoryResponse.md)
 - [CreateEngineDetail](docs/CreateEngineDetail.md)
 - [CreateEngineRequest](docs/CreateEngineRequest.md)
 - [CreateEngineResponse](docs/CreateEngineResponse.md)
 - [CreateJobDetail](docs/CreateJobDetail.md)
 - [CreateJobRequest](docs/CreateJobRequest.md)
 - [CreateJobResponse](docs/CreateJobResponse.md)
 - [CreateJobsAction](docs/CreateJobsAction.md)
 - [CreateLicenseDetail](docs/CreateLicenseDetail.md)
 - [CreateNodRedContainerDetail](docs/CreateNodRedContainerDetail.md)
 - [CreateOrganizationDetail](docs/CreateOrganizationDetail.md)
 - [CreatePermissionDetail](docs/CreatePermissionDetail.md)
 - [CreateResourceDetail](docs/CreateResourceDetail.md)
 - [CreateResourceRequest](docs/CreateResourceRequest.md)
 - [CreateResourceResponse](docs/CreateResourceResponse.md)
 - [CreateRoleDetail](docs/CreateRoleDetail.md)
 - [CreateServerTypeDetail](docs/CreateServerTypeDetail.md)
 - [CreateServerTypeEngineRunningDetail](docs/CreateServerTypeEngineRunningDetail.md)
 - [CreateServerTypeEngineRunningRequest](docs/CreateServerTypeEngineRunningRequest.md)
 - [CreateServerTypeEngineRunningResponse](docs/CreateServerTypeEngineRunningResponse.md)
 - [CreateServerTypeRequest](docs/CreateServerTypeRequest.md)
 - [CreateServerTypeResponse](docs/CreateServerTypeResponse.md)
 - [CreateServiceInstanceDetail](docs/CreateServiceInstanceDetail.md)
 - [CreateTDODetail](docs/CreateTDODetail.md)
 - [CreateTaskDetail](docs/CreateTaskDetail.md)
 - [CreateTaskIOInfo](docs/CreateTaskIOInfo.md)
 - [CreateTokenDetail](docs/CreateTokenDetail.md)
 - [CreateUserDetail](docs/CreateUserDetail.md)
 - [DeleteJobRequest](docs/DeleteJobRequest.md)
 - [DeleteServerTypeRequest](docs/DeleteServerTypeRequest.md)
 - [DesiredServersToServerTypeRequest](docs/DesiredServersToServerTypeRequest.md)
 - [DockerRegistry](docs/DockerRegistry.md)
 - [DrainHostRequest](docs/DrainHostRequest.md)
 - [EngineBuildStateEnum](docs/EngineBuildStateEnum.md)
 - [EngineCategoryDetail](docs/EngineCategoryDetail.md)
 - [EngineContainerCount](docs/EngineContainerCount.md)
 - [EngineContainerGroupByEnum](docs/EngineContainerGroupByEnum.md)
 - [EngineDetail](docs/EngineDetail.md)
 - [EngineErrorChartTypeEnum](docs/EngineErrorChartTypeEnum.md)
 - [EngineErrorTimeRangesCountsInfo](docs/EngineErrorTimeRangesCountsInfo.md)
 - [EngineInstanceActionEnum](docs/EngineInstanceActionEnum.md)
 - [EngineInstanceInfo](docs/EngineInstanceInfo.md)
 - [EngineInstanceRegistrationInfo](docs/EngineInstanceRegistrationInfo.md)
 - [EngineInstanceStatus](docs/EngineInstanceStatus.md)
 - [EngineInstanceStatusModeEnum](docs/EngineInstanceStatusModeEnum.md)
 - [EngineInstanceWorkDetailsResponse](docs/EngineInstanceWorkDetailsResponse.md)
 - [EngineInstanceWorkDetailsResponseResult](docs/EngineInstanceWorkDetailsResponseResult.md)
 - [EngineInstanceWorkItem](docs/EngineInstanceWorkItem.md)
 - [EngineInstanceWorkRequest](docs/EngineInstanceWorkRequest.md)
 - [EngineInstanceWorkRequestResponse](docs/EngineInstanceWorkRequestResponse.md)
 - [EngineInstanceWorkRequestResponseResult](docs/EngineInstanceWorkRequestResponseResult.md)
 - [EngineLaunchDetail](docs/EngineLaunchDetail.md)
 - [EngineRegistrationActionEnum](docs/EngineRegistrationActionEnum.md)
 - [EngineStateEnum](docs/EngineStateEnum.md)
 - [EngineStatusEnum](docs/EngineStatusEnum.md)
 - [EngineTypeEnum](docs/EngineTypeEnum.md)
 - [EnvKeyValue](docs/EnvKeyValue.md)
 - [Error](docs/Error.md)
 - [FailureReasonEnum](docs/FailureReasonEnum.md)
 - [GPUEnum](docs/GPUEnum.md)
 - [GetAdminServiceInstancesResponse](docs/GetAdminServiceInstancesResponse.md)
 - [GetAdminServicesResponse](docs/GetAdminServicesResponse.md)
 - [GetApplicationsResponse](docs/GetApplicationsResponse.md)
 - [GetBacklogSummaryResponse](docs/GetBacklogSummaryResponse.md)
 - [GetCoresResponse](docs/GetCoresResponse.md)
 - [GetEngineBuildByStateResponse](docs/GetEngineBuildByStateResponse.md)
 - [GetEngineBuildResponse](docs/GetEngineBuildResponse.md)
 - [GetEngineBuildsResponse](docs/GetEngineBuildsResponse.md)
 - [GetEngineCategoriesResponse](docs/GetEngineCategoriesResponse.md)
 - [GetEngineCategoryDetailResponse](docs/GetEngineCategoryDetailResponse.md)
 - [GetEngineContainerCountResponse](docs/GetEngineContainerCountResponse.md)
 - [GetEngineDetailResponse](docs/GetEngineDetailResponse.md)
 - [GetEngineErrorTimeRangesResponse](docs/GetEngineErrorTimeRangesResponse.md)
 - [GetEngineInstanceListResponse](docs/GetEngineInstanceListResponse.md)
 - [GetEngineInstancesResponse](docs/GetEngineInstancesResponse.md)
 - [GetEngineLaunchResponse](docs/GetEngineLaunchResponse.md)
 - [GetEngineLaunchesResponse](docs/GetEngineLaunchesResponse.md)
 - [GetEnginesForResourceResponse](docs/GetEnginesForResourceResponse.md)
 - [GetEnginesResponse](docs/GetEnginesResponse.md)
 - [GetHostCPUUsageResponse](docs/GetHostCPUUsageResponse.md)
 - [GetHostLaunchResponse](docs/GetHostLaunchResponse.md)
 - [GetHostMemoryUsageResponse](docs/GetHostMemoryUsageResponse.md)
 - [GetJobDetailResponse](docs/GetJobDetailResponse.md)
 - [GetJobListResponse](docs/GetJobListResponse.md)
 - [GetJobOutputResponse](docs/GetJobOutputResponse.md)
 - [GetJobOutputsResponse](docs/GetJobOutputsResponse.md)
 - [GetJobPerformanceResponse](docs/GetJobPerformanceResponse.md)
 - [GetJobStatusResponse](docs/GetJobStatusResponse.md)
 - [GetJobWorkRequestResponse](docs/GetJobWorkRequestResponse.md)
 - [GetJobsBacklogCountResponse](docs/GetJobsBacklogCountResponse.md)
 - [GetJobsOrganizationStatsResponse](docs/GetJobsOrganizationStatsResponse.md)
 - [GetJobsPerformanceResponse](docs/GetJobsPerformanceResponse.md)
 - [GetJobsStatsResponse](docs/GetJobsStatsResponse.md)
 - [GetJobsTimeRangesStatsResponse](docs/GetJobsTimeRangesStatsResponse.md)
 - [GetLicensesResponse](docs/GetLicensesResponse.md)
 - [GetRatePendingScheduledJobsResponse](docs/GetRatePendingScheduledJobsResponse.md)
 - [GetResourceResponse](docs/GetResourceResponse.md)
 - [GetResourcesForEngineInstanceResponse](docs/GetResourcesForEngineInstanceResponse.md)
 - [GetResourcesForEngineInstanceResponseResult](docs/GetResourcesForEngineInstanceResponseResult.md)
 - [GetResourcesForEngineResponse](docs/GetResourcesForEngineResponse.md)
 - [GetResourcesForHostResponse](docs/GetResourcesForHostResponse.md)
 - [GetResourcesForServiceInstanceResponse](docs/GetResourcesForServiceInstanceResponse.md)
 - [GetResourcesForServiceResponse](docs/GetResourcesForServiceResponse.md)
 - [GetResourcesResponse](docs/GetResourcesResponse.md)
 - [GetScheduledJobDetailResponse](docs/GetScheduledJobDetailResponse.md)
 - [GetScheduledJobsResponse](docs/GetScheduledJobsResponse.md)
 - [GetServerErrorCountsResponse](docs/GetServerErrorCountsResponse.md)
 - [GetServerTypeResponse](docs/GetServerTypeResponse.md)
 - [GetServerTypeRunningEngineDetailResponse](docs/GetServerTypeRunningEngineDetailResponse.md)
 - [GetServerTypeRunningEnginesResponse](docs/GetServerTypeRunningEnginesResponse.md)
 - [GetServerTypesResponse](docs/GetServerTypesResponse.md)
 - [GetServiceInstancesResponse](docs/GetServiceInstancesResponse.md)
 - [GetTaskDetailResponse](docs/GetTaskDetailResponse.md)
 - [GetTaskErrorsResponse](docs/GetTaskErrorsResponse.md)
 - [GetTaskOutputResponse](docs/GetTaskOutputResponse.md)
 - [GetTaskOutputsResponse](docs/GetTaskOutputsResponse.md)
 - [GetTaskSyncBacklogResponse](docs/GetTaskSyncBacklogResponse.md)
 - [GetTaskWorkRequestResponse](docs/GetTaskWorkRequestResponse.md)
 - [GetTasksCategoriesStatsResponse](docs/GetTasksCategoriesStatsResponse.md)
 - [GetTasksEnginesStatsResponse](docs/GetTasksEnginesStatsResponse.md)
 - [GetTasksErrorTypeCountByEngineResponse](docs/GetTasksErrorTypeCountByEngineResponse.md)
 - [GetTasksInstancesResponse](docs/GetTasksInstancesResponse.md)
 - [GetTasksResponse](docs/GetTasksResponse.md)
 - [GetTasksStatsOrganizationsResponse](docs/GetTasksStatsOrganizationsResponse.md)
 - [GetTasksStatsResponse](docs/GetTasksStatsResponse.md)
 - [GetTasksTimeRangesStatsResponse](docs/GetTasksTimeRangesStatsResponse.md)
 - [GetTotalPendingScheduledJobsResponse](docs/GetTotalPendingScheduledJobsResponse.md)
 - [HostAction](docs/HostAction.md)
 - [HostActionEnum](docs/HostActionEnum.md)
 - [HostActionLaunch](docs/HostActionLaunch.md)
 - [HostActionLaunchContainerConfig](docs/HostActionLaunchContainerConfig.md)
 - [HostActionModeEnum](docs/HostActionModeEnum.md)
 - [HostActionNodeRedLaunch](docs/HostActionNodeRedLaunch.md)
 - [HostActionNodeRedTerminate](docs/HostActionNodeRedTerminate.md)
 - [HostActionTerminate](docs/HostActionTerminate.md)
 - [HostAlertRequest](docs/HostAlertRequest.md)
 - [HostCPUUsageInfo](docs/HostCPUUsageInfo.md)
 - [HostDetail](docs/HostDetail.md)
 - [HostDrainReasonEnum](docs/HostDrainReasonEnum.md)
 - [HostLaunchConfig](docs/HostLaunchConfig.md)
 - [HostLaunchControllerConfig](docs/HostLaunchControllerConfig.md)
 - [HostLaunchDetail](docs/HostLaunchDetail.md)
 - [HostLaunchNFSConfig](docs/HostLaunchNFSConfig.md)
 - [HostLaunchPostgresConfig](docs/HostLaunchPostgresConfig.md)
 - [HostLaunchRegistryConfig](docs/HostLaunchRegistryConfig.md)
 - [HostMemoryUsageInfo](docs/HostMemoryUsageInfo.md)
 - [HostMountInfo](docs/HostMountInfo.md)
 - [HostMountTypeEnum](docs/HostMountTypeEnum.md)
 - [HostPreloadEngine](docs/HostPreloadEngine.md)
 - [HostRegisterRequest](docs/HostRegisterRequest.md)
 - [HostRegisterResponse](docs/HostRegisterResponse.md)
 - [HostRegisterResponseConfigProperties](docs/HostRegisterResponseConfigProperties.md)
 - [HostStatus](docs/HostStatus.md)
 - [HostStatusContainer](docs/HostStatusContainer.md)
 - [HostTerminationReasonEnum](docs/HostTerminationReasonEnum.md)
 - [HostsCountByType](docs/HostsCountByType.md)
 - [HostsCounts](docs/HostsCounts.md)
 - [HostsCountsByTypeResponse](docs/HostsCountsByTypeResponse.md)
 - [HostsCountsResponse](docs/HostsCountsResponse.md)
 - [JobBacklogCount](docs/JobBacklogCount.md)
 - [JobDetail](docs/JobDetail.md)
 - [JobOutput](docs/JobOutput.md)
 - [JobOutputs](docs/JobOutputs.md)
 - [JobPerformanceInfo](docs/JobPerformanceInfo.md)
 - [JobStatus](docs/JobStatus.md)
 - [JobStatusEnum](docs/JobStatusEnum.md)
 - [JobTaskStatusChartTypeEnum](docs/JobTaskStatusChartTypeEnum.md)
 - [JobWorkRequest](docs/JobWorkRequest.md)
 - [JobsCountsInfo](docs/JobsCountsInfo.md)
 - [JobsEnginesCountsInfo](docs/JobsEnginesCountsInfo.md)
 - [JobsHostsCountsInfo](docs/JobsHostsCountsInfo.md)
 - [JobsOrganizationCountsInfo](docs/JobsOrganizationCountsInfo.md)
 - [JobsTimeRangesCountsInfo](docs/JobsTimeRangesCountsInfo.md)
 - [LaunchActionEnum](docs/LaunchActionEnum.md)
 - [LaunchHostRequest](docs/LaunchHostRequest.md)
 - [LaunchJobTemplateRequest](docs/LaunchJobTemplateRequest.md)
 - [LaunchJobTemplateResponse](docs/LaunchJobTemplateResponse.md)
 - [LaunchStatusEnum](docs/LaunchStatusEnum.md)
 - [LicenseDetail](docs/LicenseDetail.md)
 - [OrganizationDetail](docs/OrganizationDetail.md)
 - [PauseEngineRequest](docs/PauseEngineRequest.md)
 - [PermissionDetail](docs/PermissionDetail.md)
 - [PermissionTypeEnum](docs/PermissionTypeEnum.md)
 - [RatePendingScheduledJobInfo](docs/RatePendingScheduledJobInfo.md)
 - [RecheckJobStatusResponse](docs/RecheckJobStatusResponse.md)
 - [RegisterUserDetail](docs/RegisterUserDetail.md)
 - [RemoveEngineForResourceRequest](docs/RemoveEngineForResourceRequest.md)
 - [RemoveEngineForResourceResponse](docs/RemoveEngineForResourceResponse.md)
 - [RemoveServersToServerTypeRequest](docs/RemoveServersToServerTypeRequest.md)
 - [ReplaceEngineRequest](docs/ReplaceEngineRequest.md)
 - [ResourceBindingTypeEnum](docs/ResourceBindingTypeEnum.md)
 - [ResourceDetail](docs/ResourceDetail.md)
 - [ResourceStateEnum](docs/ResourceStateEnum.md)
 - [ResourceTypeEnum](docs/ResourceTypeEnum.md)
 - [ResumeEngineRequest](docs/ResumeEngineRequest.md)
 - [RoleDetail](docs/RoleDetail.md)
 - [RunModeEnum](docs/RunModeEnum.md)
 - [SchedulePartDetail](docs/SchedulePartDetail.md)
 - [SchedulePartsDayEnum](docs/SchedulePartsDayEnum.md)
 - [SchedulePartsTypeEnum](docs/SchedulePartsTypeEnum.md)
 - [ScheduleRepeatIntervalEnum](docs/ScheduleRepeatIntervalEnum.md)
 - [ScheduleRunModeEnum](docs/ScheduleRunModeEnum.md)
 - [ScheduledJobDetail](docs/ScheduledJobDetail.md)
 - [ScheduledProcessDetail](docs/ScheduledProcessDetail.md)
 - [ScheduledProcessTypeEnum](docs/ScheduledProcessTypeEnum.md)
 - [ServerErrorChartTypeEnum](docs/ServerErrorChartTypeEnum.md)
 - [ServerErrorCountInfo](docs/ServerErrorCountInfo.md)
 - [ServerProviderEnum](docs/ServerProviderEnum.md)
 - [ServerTypeDetail](docs/ServerTypeDetail.md)
 - [ServerTypeEngineRunningDetail](docs/ServerTypeEngineRunningDetail.md)
 - [ServiceDetail](docs/ServiceDetail.md)
 - [ServiceInstanceCreateRequest](docs/ServiceInstanceCreateRequest.md)
 - [ServiceInstanceCreateResponse](docs/ServiceInstanceCreateResponse.md)
 - [ServiceInstanceDeleteResponse](docs/ServiceInstanceDeleteResponse.md)
 - [ServiceInstanceDetail](docs/ServiceInstanceDetail.md)
 - [ServiceTypeEnum](docs/ServiceTypeEnum.md)
 - [SortOrderEnum](docs/SortOrderEnum.md)
 - [StatusFormatEnum](docs/StatusFormatEnum.md)
 - [TaskActionEnum](docs/TaskActionEnum.md)
 - [TaskDetail](docs/TaskDetail.md)
 - [TaskErrorInfo](docs/TaskErrorInfo.md)
 - [TaskIO](docs/TaskIO.md)
 - [TaskIOFolder](docs/TaskIOFolder.md)
 - [TaskIOInfo](docs/TaskIOInfo.md)
 - [TaskIOModeEnum](docs/TaskIOModeEnum.md)
 - [TaskIOStatus](docs/TaskIOStatus.md)
 - [TaskIOTypeEnum](docs/TaskIOTypeEnum.md)
 - [TaskOutput](docs/TaskOutput.md)
 - [TaskOutputs](docs/TaskOutputs.md)
 - [TaskProcessedStats](docs/TaskProcessedStats.md)
 - [TaskRouteDetail](docs/TaskRouteDetail.md)
 - [TaskStatusDetail](docs/TaskStatusDetail.md)
 - [TaskStatusEnum](docs/TaskStatusEnum.md)
 - [TaskSyncBacklogInfo](docs/TaskSyncBacklogInfo.md)
 - [TaskWorkRequest](docs/TaskWorkRequest.md)
 - [TasksCategoriesCountsInfo](docs/TasksCategoriesCountsInfo.md)
 - [TasksCountsInfo](docs/TasksCountsInfo.md)
 - [TasksEnginesCountsInfo](docs/TasksEnginesCountsInfo.md)
 - [TasksErrorTypeCountByEngineInfo](docs/TasksErrorTypeCountByEngineInfo.md)
 - [TasksInstanceCountInfo](docs/TasksInstanceCountInfo.md)
 - [TasksOrganizationsStatsCount](docs/TasksOrganizationsStatsCount.md)
 - [TasksStatusUpdateRequest](docs/TasksStatusUpdateRequest.md)
 - [TasksStatusUpdateResponse](docs/TasksStatusUpdateResponse.md)
 - [TasksTimeRangesCountsInfo](docs/TasksTimeRangesCountsInfo.md)
 - [TerminateHostRequest](docs/TerminateHostRequest.md)
 - [TokenDetail](docs/TokenDetail.md)
 - [TokenTypeEnum](docs/TokenTypeEnum.md)
 - [TotalPendingScheduledJobInfo](docs/TotalPendingScheduledJobInfo.md)
 - [UpdateApplicationDetail](docs/UpdateApplicationDetail.md)
 - [UpdateBuildResponse](docs/UpdateBuildResponse.md)
 - [UpdateEngineBuildState](docs/UpdateEngineBuildState.md)
 - [UpdateEngineBuildStateRequest](docs/UpdateEngineBuildStateRequest.md)
 - [UpdateEngineCategoryResponse](docs/UpdateEngineCategoryResponse.md)
 - [UpdateEngineDetail](docs/UpdateEngineDetail.md)
 - [UpdateEngineRequest](docs/UpdateEngineRequest.md)
 - [UpdateEngineResponse](docs/UpdateEngineResponse.md)
 - [UpdateEnginesForResourceRequest](docs/UpdateEnginesForResourceRequest.md)
 - [UpdateEnginesForResourceResponse](docs/UpdateEnginesForResourceResponse.md)
 - [UpdateNodeRedRequestDetail](docs/UpdateNodeRedRequestDetail.md)
 - [UpdateOrganizationDetail](docs/UpdateOrganizationDetail.md)
 - [UpdatePermissionDetail](docs/UpdatePermissionDetail.md)
 - [UpdateResourceDetail](docs/UpdateResourceDetail.md)
 - [UpdateResourceRequest](docs/UpdateResourceRequest.md)
 - [UpdateResourceResponse](docs/UpdateResourceResponse.md)
 - [UpdateResourceStateRequest](docs/UpdateResourceStateRequest.md)
 - [UpdateResourceStateResponse](docs/UpdateResourceStateResponse.md)
 - [UpdateRoleDetail](docs/UpdateRoleDetail.md)
 - [UpdateServerTypeEngineRunningRequest](docs/UpdateServerTypeEngineRunningRequest.md)
 - [UpdateServerTypeEngineRunningResponse](docs/UpdateServerTypeEngineRunningResponse.md)
 - [UpdateServerTypeResponse](docs/UpdateServerTypeResponse.md)
 - [UpdateTokenDetail](docs/UpdateTokenDetail.md)
 - [UpdateUserDetail](docs/UpdateUserDetail.md)
 - [UserDetail](docs/UserDetail.md)
 - [UserStatusEnum](docs/UserStatusEnum.md)
 - [WorkRequestStatusEnum](docs/WorkRequestStatusEnum.md)


## Documentation For Authorization


## api_key


- **Type**: API key
- **API key parameter name**: api_key
- **Location**: HTTP header

