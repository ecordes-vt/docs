# AiwareJsClient.EngineInstanceWorkItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**engineID** | **String** |  | [optional] 
**engineType** | [**EngineTypeEnum**](EngineTypeEnum.md) |  | [optional] 
**internalJobID** | **String** | Internal Job ID | [optional] 
**internalOrganizationID** | **String** |  | [optional] 
**internalTaskID** | **String** | Internal Task ID | [optional] 
**isRetry** | **Boolean** | If true, a prior version of this task has failed.  The outputs and inputs have to be reset based on the work that has been processed by the downstream tasks | [optional] 
**jobID** | **String** | Core Job ID | [optional] 
**maxProcessingSecondsPerWorkItem** | **Number** | The number of seconds a work item can take to process the chunks.  This will not interrupt a chunk processing time. | [optional] 
**maxWaitSecondsForChunk** | **Number** | The max time to wait for a chunk. Default is 0. | [optional] 
**numChunksPerWorkItem** | **Number** | The number of units to process. Applicable to chunk engines, number of chunks to work on this task | [optional] 
**organizationID** | **Number** | This is the organization id in core (int), not the internal organization id | [optional] 
**sendOutputToUris** | **[String]** | A list of URIs to send processed chunks when the engine completes them. | [optional] 
**taskID** | **String** | Core Task ID | [optional] 
**taskIOs** | [**[TaskIO]**](TaskIO.md) |  | [optional] 
**taskParentStatus** | [**TaskStatusEnum**](TaskStatusEnum.md) |  | [optional] 
**taskPayload** | **Object** |  | [optional] 
**taskRouteID** | **String** | the task route associated with this work item | [optional] 


