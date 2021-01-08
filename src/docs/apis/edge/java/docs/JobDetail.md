

# JobDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**abortedDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the task was aborted |  [optional]
**completedDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the job was completed |  [optional]
**coreID** | [**UUID**](UUID.md) |  |  [optional]
**coreJobID** | **String** | Core Job ID |  [optional]
**coreRecordingId** | **Long** | This is the recording id in the core of the content for this job |  [optional]
**coreScheduledJobId** | **Integer** | This is the core scheduled job id. |  [optional]
**coreSourceId** | **Long** | This is the Core Source Id |  [optional]
**createdDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the job was created |  [optional]
**currentRetries** | **Integer** | This is the current retries for the job |  [optional]
**dueDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the time the job is due to be complete.  This is used by edge to set the priorities. |  [optional]
**internalJobID** | [**UUID**](UUID.md) | Internal Job ID |  [optional]
**internalOrganizationID** | [**UUID**](UUID.md) |  |  [optional]
**internalScheduledJobId** | **String** | The internal scheduled job id. |  [optional]
**isTemplate** | **Boolean** | If true, this job is a template |  [optional]
**jobConfigJSON** | **String** | This is the job config expressed as JSON |  [optional]
**jobStatus** | [**JobStatusEnum**](JobStatusEnum.md) |  |  [optional]
**jobTemplateId** | **String** | If set, this job was created from this job template |  [optional]
**maxRetries** | **Integer** | This is the max retries for the job |  [optional]
**modifiedDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the job was last modified. |  [optional]
**priority** | **Integer** | The priority for the job.  Default is 0. |  [optional]
**scheduledDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | If from scheduled job, this is the date when the job should be launched. There is sometimes a difference between scheduled and start to allow for the edge to start processing at the right time if warmup is needed. If not, blank |  [optional]
**sendOutputToUris** | **List&lt;String&gt;** | A list of URIs to send processed chunks when the engine completes them. |  [optional]
**startDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | If from scheduled job, this is the date when the job should be started. This is a planning time not the actual whcih is startedDateTime.  If not, blank |  [optional]
**startedDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the job was started (actual) |  [optional]
**stopDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | If from scheduled job, this is the date when the job should be stopped. Start and Stop are used for recording from a stream.  If not, blank |  [optional]
**taskRoutes** | [**List&lt;TaskRouteDetail&gt;**](TaskRouteDetail.md) |  |  [optional]
**tasks** | [**List&lt;TaskDetail&gt;**](TaskDetail.md) |  |  [optional]



