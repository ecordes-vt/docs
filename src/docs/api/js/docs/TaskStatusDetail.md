# AiwareJsClient.TaskStatusDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**createJobsAction** | [**[CreateJobsAction]**](CreateJobsAction.md) |  | [optional] 
**engineID** | **String** |  | [optional] 
**errorCount** | **Number** | How many errors since last error update | [optional] 
**errorDetails** | **String** | JSON string containing an array of JSON Object to describe indvidiual errors e.g. [{\&quot;id\&quot;:\&quot;xxx\&quot;, \&quot;msg\&quot;:\&quot;xxx\&quot;},..] | [optional] 
**failureReason** | [**FailureReasonEnum**](FailureReasonEnum.md) |  | [optional] 
**inputs** | [**[TaskIOStatus]**](TaskIOStatus.md) |  | [optional] 
**internalJobID** | **String** | Internal Job ID | [optional] 
**internalTaskID** | **String** | Internal Task ID | [optional] 
**outputs** | [**[TaskIOStatus]**](TaskIOStatus.md) |  | [optional] 
**priorTimestamp** | **Number** | UTC Timestamp of last status update or start of new task | [optional] 
**processedStats** | [**TaskProcessedStats**](TaskProcessedStats.md) |  | [optional] 
**retryCount** | **Number** | How many retries since last status update | [optional] 
**taskAction** | [**TaskActionEnum**](TaskActionEnum.md) |  | [optional] 
**taskOutput** | **Object** | available at the end of a batch, when getting the next batch to work, or last heartbeat before exiting. May not present in heartbeat update | [optional] 
**taskRouteID** | **String** | the task route associated with this work item | [optional] 
**taskStatus** | [**JobStatusEnum**](JobStatusEnum.md) |  | [optional] 
**timestamp** | **Number** | UTC Timestamp of NOW() | [optional] 
**workRequestID** | **String** |  | [optional] 


