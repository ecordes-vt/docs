

# EngineInstanceWorkRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**containerStatus** | [**ContainerStatus**](ContainerStatus.md) |  |  [optional]
**engineToolkitVersion** | **String** | The version of engine toolkit format to be gitbranch:gitcommit:epochBuildDate |  [optional]
**hostAction** | [**HostActionEnum**](HostActionEnum.md) |  |  [optional]
**hostID** | [**UUID**](UUID.md) |  |  [optional]
**requestWorkForEngineIds** | **List&lt;String&gt;** | This is the set of engine ids that this instance will get work for.  Controller will return the highest priority task across the set of engine ids |  [optional]
**taskStatuses** | [**List&lt;TaskStatusDetail&gt;**](TaskStatusDetail.md) |  |  [optional]
**workRequestDetails** | **String** |  |  [optional]
**workRequestID** | [**UUID**](UUID.md) |  |  [optional]
**workRequestStatus** | [**WorkRequestStatusEnum**](WorkRequestStatusEnum.md) |  |  [optional]



