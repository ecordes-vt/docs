# AiwareJsClient.CreateJobDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**coreID** | **String** |  | [optional] 
**coreJobID** | **String** | This is the core job id associated with this job | [optional] 
**coreRecordingID** | **Number** | This is the recording id in the core of the content for this job | [optional] 
**coreSourceID** | **Number** | This is the Core Source Id | [optional] [default to 0]
**currentRetries** | **Number** | This is the current retries for the job | [optional] [default to 0]
**dueDateTime** | **Date** | This is the time the job is due to be complete.  This is used by edge to set the priorities. | [optional] 
**internalOrganizationID** | **String** |  | 
**jobConfigJSON** | **String** | This is the job config expressed as JSON | [optional] 
**jobStatus** | [**JobStatusEnum**](JobStatusEnum.md) |  | [optional] 
**sendOutputToUris** | **[String]** | A list of URIs to send processed chunks when the engine completes them. | [optional] 
**taskRoutes** | [**[TaskRouteDetail]**](TaskRouteDetail.md) |  | [optional] 
**tasks** | [**[CreateTaskDetail]**](CreateTaskDetail.md) |  | [optional] 


