# AiwareJsClient.EngineInstanceWorkRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**containerStatus** | [**ContainerStatus**](ContainerStatus.md) |  | [optional] 
**engineToolkitVersion** | **String** | The version of engine toolkit format to be gitbranch:gitcommit:epochBuildDate | [optional] 
**hostAction** | [**HostActionEnum**](HostActionEnum.md) |  | [optional] 
**hostID** | **String** |  | [optional] 
**requestWorkForEngineIds** | **[String]** | This is the set of engine ids that this instance will get work for.  Controller will return the highest priority task across the set of engine ids | [optional] 
**taskStatuses** | [**[TaskStatusDetail]**](TaskStatusDetail.md) |  | [optional] 
**workRequestDetails** | **String** |  | [optional] 
**workRequestID** | **String** |  | [optional] 
**workRequestStatus** | [**WorkRequestStatusEnum**](WorkRequestStatusEnum.md) |  | [optional] 


