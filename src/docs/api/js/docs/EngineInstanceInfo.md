# AiwareJsClient.EngineInstanceInfo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**additionalEngineIDs** | **[String]** | This is a list of additional engines this instance can handle | [optional] 
**buildID** | **String** |  | [optional] 
**createdDateTime** | **Date** | This is the datetime the core was created | [optional] 
**dockerContainerID** | **String** | The docker container PID | [optional] 
**drain** | **Boolean** | The current engine instance is draining or not | [optional] 
**engineID** | **String** |  | [optional] 
**engineInstanceID** | **String** |  | [optional] 
**engineToolkitVersion** | **String** | The engine toolkit version | [optional] 
**errors** | [**[Error]**](Error.md) |  | [optional] 
**hostID** | **String** |  | [optional] 
**lastUpdate** | **Date** |  | [optional] 
**launchEnvVariables** | **Object** |  | [optional] 
**launchID** | **String** |  | [optional] 
**launchStatus** | [**LaunchStatusEnum**](LaunchStatusEnum.md) |  | [optional] 
**launchStatusInfo** | **String** | Additional to log about launch status | [optional] 
**licenseExpirationSeconds** | **Number** | Seconds till the license expires | [optional] 
**modifiedDateTime** | **Date** | This is the datetime the core was last modified. | [optional] 
**runtimeExpirationSeconds** | **Number** | Seconds till runtime should expire | [optional] 
**startupTimestamp** | **Number** | Timestamp of engine instance startup in UTC | [optional] 
**status** | [**EngineStatusEnum**](EngineStatusEnum.md) |  | [optional] 
**warnings** | [**[Error]**](Error.md) |  | [optional] 
**workRequestID** | **String** |  | [optional] 


