

# EngineInstanceStatus

payload for updateEngineInstanceStatus API -
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**containerStatus** | [**ContainerStatus**](ContainerStatus.md) |  |  [optional]
**hostID** | [**UUID**](UUID.md) |  |  [optional]
**mode** | [**EngineInstanceStatusModeEnum**](EngineInstanceStatusModeEnum.md) |  |  [optional]
**priorTimestamp** | **Long** | UTC Timestamp of last status update or start of new task |  [optional]
**secondsToTTL** | **Integer** |  |  [optional]
**taskStatuses** | [**List&lt;TaskStatusDetail&gt;**](TaskStatusDetail.md) |  |  [optional]
**timestamp** | **Long** | UTC Timestamp of NOW() |  [optional]
**workRequestDetails** | **String** |  |  [optional]
**workRequestID** | [**UUID**](UUID.md) |  |  [optional]
**workRequestStatus** | [**WorkRequestStatusEnum**](WorkRequestStatusEnum.md) |  |  [optional]



