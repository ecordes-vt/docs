# AiwareJsClient.TaskDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**abortedDateTime** | **Date** | This is the datetime the task was aborted | [optional] 
**buildID** | **String** |  | [optional] 
**childTaskIDs** | **[String]** | Array of Internal Child Task Id | [optional] 
**chunkCountInfo** | [**ChunkCountInfo**](ChunkCountInfo.md) |  | [optional] 
**completedDateTime** | **Date** | This is the datetime the task was completed | [optional] 
**coreJobID** | **String** | This is the core job id associated with this job | [optional] 
**coreRecordingID** | **Number** | This is the recording id in the core of the content for this job | [optional] 
**coreTaskID** | **String** | This is the core task id associated with this job | [optional] 
**createdDateTime** | **Date** | This is the datetime the core was created | [optional] 
**currentRetries** | **Number** | This is the current retries for the task | [optional] [default to 0]
**dueDateTime** | **Date** | This is the time the task is due to be complete.  This is used by edge to set the priorities. | [optional] 
**engineCategoryID** | **String** | Category Id | [optional] 
**engineCategoryName** | **String** | Category name | [optional] 
**engineID** | **String** |  | [optional] 
**engineName** | **String** | Engine name | [optional] 
**errorCount** | **Number** | This is the error count for the task | [optional] 
**failureDetail** | **String** | If there is an error, the detail will be set here. | [optional] 
**failureReason** | [**FailureReasonEnum**](FailureReasonEnum.md) |  | [optional] 
**internalJobID** | **String** | Internal Job ID | [optional] 
**internalOrganizationID** | **String** |  | [optional] 
**internalTaskID** | **String** | Internal Task ID | [optional] 
**ioFolders** | [**[TaskIOInfo]**](TaskIOInfo.md) |  | [optional] 
**isTemplate** | **Boolean** | If true, this job is a template | [optional] 
**maxEngines** | **Number** | The maximum number of engine instances to run against this task.  Defaults to 1 if parallelProcessing is false, or 2 otherwise. | [optional] 
**maxRetries** | **Number** | This is the max retries for the task | [optional] 
**modifiedDateTime** | **Date** | This is the datetime the core was last modified. | [optional] 
**parallelProcessing** | **Boolean** | If true, multiple engine instances can process this task in parallel.  If false, maxEngines will be 1. | [optional] 
**parentMustBeCompleteBeforeStarting** | **Boolean** | If true, this task won&#39;t start until the parent is complete | [optional] 
**parentTaskID** | **String** | Internal Parent Task Id | [optional] 
**payloadJSON** | **String** | This is the payload encoded as a JSON string | [optional] 
**scheduledDateTime** | **Date** | If from scheduled job, this is the date when the task should be launched. There is sometimes a difference between scheduled and start to allow for the edge to start processing at the right time if warmup is needed. If not, blank | [optional] 
**sendOutputToUris** | **[String]** | A list of URIs to send processed chunks when the engine completes them. | [optional] 
**startDateTime** | **Date** | If from scheduled job, this is the date when the task should be started. This is a planning time not the actual which is startedDateTime.  If not, blank | [optional] 
**startedDateTime** | **Date** | This is the datetime the task was started (actual) | [optional] 
**stopDateTime** | **Date** | If from scheduled job, this is the date when the task should be stopped. Start and Stop are used for recording from a stream.  If not, blank | [optional] 
**taskOutputSON** | **String** | This is the taskOutput as a JSON string | [optional] 
**taskPayloadJSON** | **String** | This is the taskPayload as a JSON string | [optional] 
**taskStatus** | [**JobStatusEnum**](JobStatusEnum.md) |  | [optional] 
**taskTemplateID** | **String** | If set, this task was created from this task template. | [optional] 


