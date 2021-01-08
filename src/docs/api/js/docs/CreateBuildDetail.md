# AiwareJsClient.CreateBuildDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**buildDefaultTTL** | **Number** | The seconds on average a build should live if utilized | [optional] 
**buildID** | **String** |  | [optional] 
**buildState** | [**EngineBuildStateEnum**](EngineBuildStateEnum.md) |  | [optional] 
**diskFreeBytes** | **Number** | The number of free bytes required to launch engine | [optional] 
**dockerImage** | **String** | docker image | [optional] 
**engineID** | **String** |  | [optional] 
**licenseExpirationTimestamp** | **Number** | The unix timestamp on when the license for the engine expires.  If 0, then it does not expire | [optional] 
**manifestClusterSize** | **String** | Engine Size from the Manifest | [optional] 
**manifestCustomProfile** | **String** | Engine Custom Profile from the Manifest | [optional] 
**manifestEngineMode** | **String** | Engine Mode from the Manifest | [optional] 
**manifestEngineName** | **String** | Name of the Engine from the Manifest | [optional] 
**manifestGPUSupported** | [**GPUEnum**](GPUEnum.md) |  | [optional] 
**manifestRequireEC2** | **Boolean** | Does the engine require EC2 | [optional] 
**runtime** | **String** | JSON Data for runtime | [optional] 
**softGPULimit** | **Number** | The number of GPU required to launch engine | [optional] 
**softMemoryBytesLimit** | **Number** | The number of bytes required to launch this engine | [optional] 
**softVCPULimit** | **Number** | The number of VCPU based on 1024 required to launch engine | [optional] 
**version** | **Number** | version of the engine | [optional] 


