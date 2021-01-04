

# TaskStatusDetail

Represent a task status as being worked on by an engine instance.  This can be sent as part of heartbeat status update or when getting new work. The updates are deltas since last post
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**createJobsAction** | [**List&lt;CreateJobsAction&gt;**](CreateJobsAction.md) |  |  [optional]
**engineID** | [**UUID**](UUID.md) |  |  [optional]
**errorCount** | **Integer** | How many errors since last error update |  [optional]
**errorDetails** | **String** | JSON string containing an array of JSON Object to describe indvidiual errors e.g. [{\&quot;id\&quot;:\&quot;xxx\&quot;, \&quot;msg\&quot;:\&quot;xxx\&quot;},..] |  [optional]
**failureReason** | [**FailureReasonEnum**](FailureReasonEnum.md) |  |  [optional]
**inputs** | [**List&lt;TaskIOStatus&gt;**](TaskIOStatus.md) |  |  [optional]
**internalJobID** | [**UUID**](UUID.md) | Internal Job ID |  [optional]
**internalTaskID** | [**UUID**](UUID.md) | Internal Task ID |  [optional]
**outputs** | [**List&lt;TaskIOStatus&gt;**](TaskIOStatus.md) |  |  [optional]
**priorTimestamp** | **Long** | UTC Timestamp of last status update or start of new task |  [optional]
**processedStats** | [**TaskProcessedStats**](TaskProcessedStats.md) |  |  [optional]
**retryCount** | **Integer** | How many retries since last status update |  [optional]
**taskAction** | [**TaskActionEnum**](TaskActionEnum.md) |  |  [optional]
**taskOutput** | **Object** | available at the end of a batch, when getting the next batch to work, or last heartbeat before exiting. May not present in heartbeat update |  [optional]
**taskRouteID** | **String** | the task route associated with this work item |  [optional]
**taskStatus** | [**JobStatusEnum**](JobStatusEnum.md) |  |  [optional]
**timestamp** | **Long** | UTC Timestamp of NOW() |  [optional]
**workRequestID** | [**UUID**](UUID.md) |  |  [optional]



