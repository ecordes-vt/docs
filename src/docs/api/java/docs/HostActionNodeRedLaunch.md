

# HostActionNodeRedLaunch

Launch request
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**buildId** | **String** | the buildId for the engine |  [optional]
**containerConfig** | [**HostActionLaunchContainerConfig**](HostActionLaunchContainerConfig.md) |  |  [optional]
**containerType** | [**ContainerTypeEnum**](ContainerTypeEnum.md) |  |  [optional]
**coreID** | **String** | core system id of graphql |  [optional]
**coreToken** | **String** | The core token of the current user. |  [optional]
**dockerContainerName** | **String** | Docker container name to launch |  [optional]
**dockerImage** | **String** | Docker image to launch |  [optional]
**engineId** | **String** | The id of the engine to launch |  [optional]
**env** | [**List&lt;EnvKeyValue&gt;**](EnvKeyValue.md) |  |  [optional]
**hostId** | **String** | HostID of the node-red container |  [optional]
**launchId** | [**UUID**](UUID.md) | The Launch ID to use for the launch |  [optional]
**name** | **String** | The name of the engine or process to launch. This is informational only. |  [optional]
**port** | **String** | Port of the node-red container |  [optional]
**runtimeTTL** | **Integer** | Seconds to run |  [optional]
**softMinMemory** | **Long** |  |  [optional]
**softMinvCPU** | **Integer** |  |  [optional]



