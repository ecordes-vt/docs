# AiwareJsClient.JobDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**abortedDateTime** | **Date** | This is the datetime the task was aborted | [optional] 
**completedDateTime** | **Date** | This is the datetime the job was completed | [optional] 
**coreID** | **String** |  | [optional] 
**coreJobID** | **String** | Core Job ID | [optional] 
**coreRecordingId** | **Number** | This is the recording id in the core of the content for this job | [optional] 
**coreScheduledJobId** | **Number** | This is the core scheduled job id. | [optional] 
**coreSourceId** | **Number** | This is the Core Source Id | [optional] [default to 0]
**createdDateTime** | **Date** | This is the datetime the job was created | [optional] 
**currentRetries** | **Number** | This is the current retries for the job | [optional] [default to 0]
**dueDateTime** | **Date** | This is the time the job is due to be complete.  This is used by edge to set the priorities. | [optional] 
**internalJobID** | **String** | Internal Job ID | [optional] 
**internalOrganizationID** | **String** |  | [optional] 
**internalScheduledJobId** | **String** | The internal scheduled job id. | [optional] 
**isTemplate** | **Boolean** | If true, this job is a template | [optional] 
**jobConfigJSON** | **String** | This is the job config expressed as JSON | [optional] 
**jobStatus** | [**JobStatusEnum**](JobStatusEnum.md) |  | [optional] 
**jobTemplateId** | **String** | If set, this job was created from this job template | [optional] 
**maxRetries** | **Number** | This is the max retries for the job | [optional] [default to 0]
**modifiedDateTime** | **Date** | This is the datetime the job was last modified. | [optional] 
**priority** | **Number** | The priority for the job.  Default is 0. | [optional] [default to 0]
**scheduledDateTime** | **Date** | If from scheduled job, this is the date when the job should be launched. There is sometimes a difference between scheduled and start to allow for the edge to start processing at the right time if warmup is needed. If not, blank | [optional] 
**sendOutputToUris** | **[String]** | A list of URIs to send processed chunks when the engine completes them. | [optional] 
**startDateTime** | **Date** | If from scheduled job, this is the date when the job should be started. This is a planning time not the actual whcih is startedDateTime.  If not, blank | [optional] 
**startedDateTime** | **Date** | This is the datetime the job was started (actual) | [optional] 
**stopDateTime** | **Date** | If from scheduled job, this is the date when the job should be stopped. Start and Stop are used for recording from a stream.  If not, blank | [optional] 
**taskRoutes** | [**[TaskRouteDetail]**](TaskRouteDetail.md) |  | [optional] 
**tasks** | [**[TaskDetail]**](TaskDetail.md) |  | [optional] 


