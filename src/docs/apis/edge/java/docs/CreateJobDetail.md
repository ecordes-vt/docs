

# CreateJobDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**coreID** | [**UUID**](UUID.md) |  |  [optional]
**coreJobID** | **String** | This is the core job id associated with this job |  [optional]
**coreRecordingID** | **Long** | This is the recording id in the core of the content for this job |  [optional]
**coreSourceID** | **Long** | This is the Core Source Id |  [optional]
**currentRetries** | **Integer** | This is the current retries for the job |  [optional]
**dueDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the time the job is due to be complete.  This is used by edge to set the priorities. |  [optional]
**internalOrganizationID** | [**UUID**](UUID.md) |  | 
**jobConfigJSON** | **String** | This is the job config expressed as JSON |  [optional]
**jobStatus** | [**JobStatusEnum**](JobStatusEnum.md) |  |  [optional]
**sendOutputToUris** | **List&lt;String&gt;** | A list of URIs to send processed chunks when the engine completes them. |  [optional]
**taskRoutes** | [**List&lt;TaskRouteDetail&gt;**](TaskRouteDetail.md) |  |  [optional]
**tasks** | [**List&lt;CreateTaskDetail&gt;**](CreateTaskDetail.md) |  |  [optional]



