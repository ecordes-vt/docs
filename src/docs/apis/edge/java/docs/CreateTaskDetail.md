

# CreateTaskDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**coreTaskId** | **String** | This is the core task id associated with this job |  [optional]
**correlationTaskId** | **String** | Correlation Task Id.  On create, this will be used instead of internalTaskId or coreTaskId on routes |  [optional]
**dueDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the time the task is due to be complete.  This is used by edge to set the priorities. |  [optional]
**engineId** | [**UUID**](UUID.md) | The engineId to use.  If the engine is not available on edge, this will return an exception | 
**ioFolders** | [**List&lt;CreateTaskIOInfo&gt;**](CreateTaskIOInfo.md) |  |  [optional]
**maxEngines** | **Integer** | The maximum number of engine instances to run against this task.  Defaults to 1 if parallelProcessing is false, or 2 otherwise. |  [optional]
**maxProcessingSecondsPerWorkItem** | **Long** | The maximum number of seconds a work item can take.  If an engine instance is processing a chunk, engine toolkit will wait till the chunk is complete. |  [optional]
**maxRetries** | **Integer** | This is the max retries for the task |  [optional]
**maxWaitSecondsForChunk** | **Long** | The maximum number of seconds to wait for a new chunk before completing. |  [optional]
**numChunksPerWorkItem** | **Long** | The maximum number of chunks to process per work item |  [optional]
**parallelProcessing** | **Boolean** | If true, multiple engine instances can process this task in parallel.  If false, maxEngines will be 1. |  [optional]
**parentMustBeCompleteBeforeStarting** | **Boolean** | If true, this task won&#39;t start until the parent is complete |  [optional]
**payloadJSON** | **String** | This is the payload encoded as a JSON string |  [optional]
**priority** | **Integer** | The priority for the task. Default is 0. |  [optional]
**sendOutputToUris** | **List&lt;String&gt;** | A list of URIs to send processed chunks when the engine completes them. |  [optional]
**taskPayloadJSON** | **String** | This is the taskPayload as a JSON string |  [optional]
**taskStatus** | [**JobStatusEnum**](JobStatusEnum.md) |  |  [optional]



