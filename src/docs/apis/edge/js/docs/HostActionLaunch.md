# AiwareJsClient.HostActionLaunch

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**buildId** | **String** | the buildId for the engine | [optional] 
**containerConfig** | [**HostActionLaunchContainerConfig**](HostActionLaunchContainerConfig.md) |  | [optional] 
**containerType** | [**ContainerTypeEnum**](ContainerTypeEnum.md) |  | [optional] 
**dockerImage** | **String** | Docker image to launch | [optional] 
**engineId** | **String** | The id of the engine to launch | [optional] 
**env** | [**[EnvKeyValue]**](EnvKeyValue.md) |  | [optional] 
**gpuType** | [**GPUEnum**](GPUEnum.md) |  | [optional] 
**isGPU** | **Boolean** | If true, this requires a GPU | [optional] 
**launchId** | **String** | The Launch ID to use for the launch | [optional] 
**name** | **String** | The name of the engine or process to launch. This is informational only. | [optional] 
**runtime** | **String** | the runtime for the build | [optional] 
**runtimeTTL** | **Number** | Seconds to run | [optional] 
**softMinMemory** | **Number** |  | [optional] 
**softMinvCPU** | **Number** |  | [optional] 


