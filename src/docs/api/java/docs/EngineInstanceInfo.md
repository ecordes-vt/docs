

# EngineInstanceInfo

EngineInstance Information
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**additionalEngineIDs** | **List&lt;String&gt;** | This is a list of additional engines this instance can handle |  [optional]
**buildID** | [**UUID**](UUID.md) |  |  [optional]
**createdDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the core was created |  [optional]
**dockerContainerID** | **String** | The docker container PID |  [optional]
**drain** | **Boolean** | The current engine instance is draining or not |  [optional]
**engineID** | [**UUID**](UUID.md) |  |  [optional]
**engineInstanceID** | [**UUID**](UUID.md) |  |  [optional]
**engineToolkitVersion** | **String** | The engine toolkit version |  [optional]
**errors** | [**List&lt;Error&gt;**](Error.md) |  |  [optional]
**hostID** | [**UUID**](UUID.md) |  |  [optional]
**lastUpdate** | [**OffsetDateTime**](OffsetDateTime.md) |  |  [optional]
**launchEnvVariables** | **Object** |  |  [optional]
**launchID** | [**UUID**](UUID.md) |  |  [optional]
**launchStatus** | [**LaunchStatusEnum**](LaunchStatusEnum.md) |  |  [optional]
**launchStatusInfo** | **String** | Additional to log about launch status |  [optional]
**licenseExpirationSeconds** | **Integer** | Seconds till the license expires |  [optional]
**modifiedDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the core was last modified. |  [optional]
**runtimeExpirationSeconds** | **Integer** | Seconds till runtime should expire |  [optional]
**startupTimestamp** | **Long** | Timestamp of engine instance startup in UTC |  [optional]
**status** | [**EngineStatusEnum**](EngineStatusEnum.md) |  |  [optional]
**warnings** | [**List&lt;Error&gt;**](Error.md) |  |  [optional]
**workRequestID** | [**UUID**](UUID.md) |  |  [optional]



