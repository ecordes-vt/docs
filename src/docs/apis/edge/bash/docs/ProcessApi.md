# ProcessApi

All URIs are relative to */edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addTask**](ProcessApi.md#addTask) | **POST** /proc/job/{JobID}/addtask | Adds a Task to a current job
[**addTaskRoute**](ProcessApi.md#addTaskRoute) | **POST** /proc/job/{JobID}/addtaskroute | Adds a Task Route to a current job
[**createJob**](ProcessApi.md#createJob) | **POST** /proc/job/create | This creates a new Job
[**deleteJob**](ProcessApi.md#deleteJob) | **POST** /proc/job/{JobID}/delete | This API deletes the specified job
[**deleteTask**](ProcessApi.md#deleteTask) | **POST** /proc/task/{TaskID}/delete | This API deletes the specified task
[**getEngineErrorTimeRanges**](ProcessApi.md#getEngineErrorTimeRanges) | **GET** /proc/tasks/error/engine_error_time_ranges | This gets engine error count by error tasks grouped by time ranges and sorted by a range start time
[**getJobDetail**](ProcessApi.md#getJobDetail) | **GET** /proc/job/{JobID}/detail | Gets Job Detail
[**getJobDownload**](ProcessApi.md#getJobDownload) | **GET** /proc/job/{JobID}/download/{JobOutputName} | Returns the contents of the job&#39;s output
[**getJobOutput**](ProcessApi.md#getJobOutput) | **GET** /proc/job/{JobID}/output/{JobOutputName} | Returns the contents of the job&#39;s output
[**getJobOutputs**](ProcessApi.md#getJobOutputs) | **GET** /proc/job/{JobID}/outputs | Returns a list of output information about this job
[**getJobPerformance**](ProcessApi.md#getJobPerformance) | **GET** /proc/job/{JobID}/performance | This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time
[**getJobStatus**](ProcessApi.md#getJobStatus) | **GET** /proc/job/{JobID}/status | Gets Job Status
[**getJobWorkRequests**](ProcessApi.md#getJobWorkRequests) | **GET** /proc/job/{JobID}/workrequests | This provides a list of workrequests of a job
[**getJobs**](ProcessApi.md#getJobs) | **GET** /proc/jobs | This gets a list of jobs
[**getJobsOrganizationStats**](ProcessApi.md#getJobsOrganizationStats) | **GET** /proc/jobs/stats/organization | This gets processing stats of the jobs by organization
[**getJobsPerformance**](ProcessApi.md#getJobsPerformance) | **GET** /proc/jobs/performance | This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time
[**getJobsStats**](ProcessApi.md#getJobsStats) | **GET** /proc/jobs/stats | This gets processing stats of the jobs
[**getJobsTimeRangesStats**](ProcessApi.md#getJobsTimeRangesStats) | **GET** /proc/jobs/stats/time_ranges | This gets processing stats of the jobs grouped by time ranges and sorted by a range start time
[**getRatePendingScheduledJobs**](ProcessApi.md#getRatePendingScheduledJobs) | **GET** /proc/scheduled_jobs/rate_pending_time_ranges | This gets the rate of pending scheduled jobs by time ranges
[**getScheduledJobDetail**](ProcessApi.md#getScheduledJobDetail) | **GET** /proc/scheduled_job/{ScheduledJobID}/detail | This gets scheduled job detail
[**getScheduledJobs**](ProcessApi.md#getScheduledJobs) | **GET** /proc/scheduled_jobs | This gets a list of scheduled jobs
[**getServerErrorCounts**](ProcessApi.md#getServerErrorCounts) | **GET** /proc/tasks/error/server_error_counts | Get server error counts in a time-range
[**getTaskDetail**](ProcessApi.md#getTaskDetail) | **GET** /proc/task/{TaskID}/detail | Gets Task Detail
[**getTaskDownload**](ProcessApi.md#getTaskDownload) | **GET** /proc/task/{TaskID}/download/{TaskOutputName} | Returns the contents of the task&#39;s output
[**getTaskLogs**](ProcessApi.md#getTaskLogs) | **GET** /proc/task/{TaskID}/logs | Gets logs associated with a task
[**getTaskOutput**](ProcessApi.md#getTaskOutput) | **GET** /proc/task/{TaskID}/output/{TaskOutputName} | Returns the contents of the task&#39;s output
[**getTaskOutputs**](ProcessApi.md#getTaskOutputs) | **GET** /proc/task/{TaskID}/outputs | Gets Task Output
[**getTaskSyncBacklog**](ProcessApi.md#getTaskSyncBacklog) | **GET** /proc/tasks/sync_backlog | Gets task sync backlog in a time-range
[**getTasks**](ProcessApi.md#getTasks) | **GET** /proc/tasks | This gets a list of tasks based on the provided criteria
[**getTasksErrorTypeCountByEngine**](ProcessApi.md#getTasksErrorTypeCountByEngine) | **GET** /proc/tasks/error/count_type_by_engine | This gets error type count by engines
[**getTasksErrors**](ProcessApi.md#getTasksErrors) | **GET** /proc/tasks/errors | This provides a error list in a time range
[**getTasksInstances**](ProcessApi.md#getTasksInstances) | **GET** /proc/tasks/instances/by_category_host | This gets processing stats of the tasks
[**getTasksStats**](ProcessApi.md#getTasksStats) | **GET** /proc/tasks/stats | This gets processing stats of the tasks
[**getTasksStatsCategories**](ProcessApi.md#getTasksStatsCategories) | **GET** /proc/tasks/stats/categories | This gets processing stats of the tasks grouped by engine categories
[**getTasksStatsEngines**](ProcessApi.md#getTasksStatsEngines) | **GET** /proc/tasks/stats/engines | This gets processing stats of the tasks grouped by engine
[**getTasksStatsOrganizations**](ProcessApi.md#getTasksStatsOrganizations) | **GET** /proc/tasks/stats/organizations | This gets processing stats of the tasks grouped by engine, filter by organizations
[**getTasksStatsTimeRanges**](ProcessApi.md#getTasksStatsTimeRanges) | **GET** /proc/tasks/stats/time_ranges | This gets processing stats of the tasks grouped by time ranges and sorted by a range start time
[**getTotalPendingScheduledJobs**](ProcessApi.md#getTotalPendingScheduledJobs) | **GET** /proc/scheduled_jobs/total_pending_time_ranges | This gets the total pending scheduled jobs by time ranges
[**getWorkRequest**](ProcessApi.md#getWorkRequest) | **GET** /proc/workrequest/{WorkRequestID}/detail | This provides detail of workrequest
[**launchJobTemplate**](ProcessApi.md#launchJobTemplate) | **POST** /proc/template/{TemplateID}/launch | This launch a job based on the given job template
[**pushContentToEndpoint**](ProcessApi.md#pushContentToEndpoint) | **POST** /proc/endpoint/{Endpoint} | Whatever is posted to this endpoint will be added to the child input folder(s) for the task_routes that have this endpoint.  If more than one task_routes have this endpoint, it will be added to all child input folders.
[**recheckJobStatus**](ProcessApi.md#recheckJobStatus) | **GET** /proc/job/{JobID}/recheck_status | Recheck Job Status
[**tasksStatusExport**](ProcessApi.md#tasksStatusExport) | **GET** /proc/tasks/stats/export | Export a task status report as a excel file
[**updateTaskStatus**](ProcessApi.md#updateTaskStatus) | **POST** /proc/tasks/update_status | This updates the status for a bulk of tasks by taskID



## addTask

Adds a Task to a current job

### Example

```bash
aiware addTask JobID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**string**](.md) | ID of Job | [default to null]
 **addTaskRequest** | [**AddTaskRequest**](AddTaskRequest.md) | Create Job API |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AddTaskResponse**](AddTaskResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## addTaskRoute

Adds a Task Route to a current job

### Example

```bash
aiware addTaskRoute JobID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**string**](.md) | ID of Job | [default to null]
 **addTaskRouteRequest** | [**AddTaskRouteRequest**](AddTaskRouteRequest.md) | Adds a Task Route |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AddTaskRouteResponse**](AddTaskRouteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## createJob

This creates a new Job

### Example

```bash
aiware createJob X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createJobRequest** | [**CreateJobRequest**](CreateJobRequest.md) | Create Job API |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**CreateJobResponse**](CreateJobResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deleteJob

This API deletes the specified job

### Example

```bash
aiware deleteJob JobID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**string**](.md) | ID of Job | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **deleteJobRequest** | [**DeleteJobRequest**](DeleteJobRequest.md) | Request information to delete the specified job | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deleteTask

This API deletes the specified task

### Example

```bash
aiware deleteTask TaskID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**string**](.md) | ID of Task | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineErrorTimeRanges

This gets engine error count by error tasks grouped by time ranges and sorted by a range start time

### Example

```bash
aiware getEngineErrorTimeRanges X-Correlation-Id:value  startTime=value  endTime=value  chartType=value  interval=value  engineID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **chartType** | [**EngineErrorChartTypeEnum**](.md) | It will help API to kmow the response should return | [optional] [default to null]
 **interval** | **integer** | Interval in seconds for output time ranges | [optional] [default to null]
 **engineID** | [**string**](.md) | Filtering by engineID | [optional] [default to null]

### Return type

[**GetEngineErrorTimeRangesResponse**](GetEngineErrorTimeRangesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobDetail

Gets Job Detail

### Example

```bash
aiware getJobDetail JobID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**string**](.md) | ID of Job | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetJobDetailResponse**](GetJobDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobDownload

Returns the contents of the job's output

### Example

```bash
aiware getJobDownload JobID=value JobOutputName=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**string**](.md) | ID of Job | [default to null]
 **jobOutputName** | **string** | Name of the job output, e.g. vtn-standard.json | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

**array[string]**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobOutput

Returns the contents of the job's output

### Example

```bash
aiware getJobOutput JobID=value JobOutputName=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**string**](.md) | ID of Job | [default to null]
 **jobOutputName** | **string** | Name of the job output, e.g. vtn-standard.json | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetJobOutputResponse**](GetJobOutputResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobOutputs

Returns a list of output information about this job

### Example

```bash
aiware getJobOutputs JobID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**string**](.md) | ID of Job | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetJobOutputsResponse**](GetJobOutputsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobPerformance

This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time

### Example

```bash
aiware getJobPerformance JobID=value X-Correlation-Id:value  interval=value  taskID=value  workRequestID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**string**](.md) | ID of Job | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **interval** | **integer** | Interval in seconds for output time ranges | [optional] [default to null]
 **taskID** | [**string**](.md) | Filter data by taskID | [optional] [default to null]
 **workRequestID** | [**string**](.md) | Filter data by workRequestID | [optional] [default to null]

### Return type

[**GetJobPerformanceResponse**](GetJobPerformanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobStatus

Gets Job Status

### Example

```bash
aiware getJobStatus JobID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**string**](.md) | ID of Job | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetJobStatusResponse**](GetJobStatusResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobWorkRequests

This provides a list of workrequests of a job

### Example

```bash
aiware getJobWorkRequests JobID=value X-Correlation-Id:value  offset=value  limit=value  orderBy=value  direction=value  status=value  taskID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**string**](.md) | ID of Job | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **offset** | **integer** | the number of records to skip before getting the result set | [optional] [default to null]
 **limit** | **integer** | the number of records to return. | [optional] [default to 100]
 **orderBy** | **string** | the field to sort. It should be in [createdDateTime, modifiedDateTime] | [optional] [default to createdDateTime]
 **direction** | **string** | the sort order | [optional] [default to DESC]
 **status** | **string** | the value should be in [active, trial, inactive, deleted] | [optional] [default to null]
 **taskID** | **string** | This is an internal task ID to get work request | [optional] [default to null]

### Return type

[**GetJobWorkRequestResponse**](GetJobWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobs

This gets a list of jobs

### Example

```bash
aiware getJobs X-Correlation-Id:value  startTime=value  endTime=value  status=value  offset=value  limit=value  orderBy=value  direction=value  coreID=value  organizationID=value  recordingID=value  jobID=value  coreJobID=value  modifiedBefore=value  modifiedAfter=value  CreatedBefore=value  CreatedAfter=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**JobStatusEnum**](.md) | If specified, this limits the jobs or tasks to follow status | [optional] [default to null]
 **offset** | **integer** | the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **integer** | the number of items to return. | [optional] [default to 10]
 **orderBy** | **string** | the field to sort | [optional] [default to createdDateTime]
 **direction** | **string** | the sort order.  ASC or DESC. | [optional] [default to DESC]
 **coreID** | [**string**](.md) | Filter by coreID | [optional] [default to null]
 **organizationID** | [**string**](.md) | Filter by organizationID | [optional] [default to null]
 **recordingID** | [**string**](.md) | Filter by recordingID | [optional] [default to null]
 **jobID** | [**string**](.md) | Filter by jobID | [optional] [default to null]
 **coreJobID** | **string** | Filter by coreJobID | [optional] [default to null]
 **modifiedBefore** | **integer** | Filter by items modified before expressed as timestamp | [optional] [default to null]
 **modifiedAfter** | **integer** | Filter by items modified after expressed as timestamp | [optional] [default to null]
 **createdBefore** | **integer** | Filter items where created date is before this date | [optional] [default to null]
 **createdAfter** | **integer** | Filter items where created date is after this date | [optional] [default to null]

### Return type

[**GetJobListResponse**](GetJobListResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobsOrganizationStats

This gets processing stats of the jobs by organization

### Example

```bash
aiware getJobsOrganizationStats X-Correlation-Id:value  startTime=value  endTime=value  organizationIDs=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **organizationIDs** | **string** |  | [optional] [default to null]

### Return type

[**GetJobsOrganizationStatsResponse**](GetJobsOrganizationStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobsPerformance

This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time

### Example

```bash
aiware getJobsPerformance X-Correlation-Id:value  startTime=value  endTime=value  interval=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **interval** | **integer** | Interval in seconds for output time ranges | [optional] [default to null]

### Return type

[**GetJobsPerformanceResponse**](GetJobsPerformanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobsStats

This gets processing stats of the jobs

### Example

```bash
aiware getJobsStats X-Correlation-Id:value  startTime=value  endTime=value  chartType=value  status=value  organizationIDs=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **chartType** | [**JobTaskStatusChartTypeEnum**](.md) | It will help API to kmow the response should return | [optional] [default to null]
 **status** | [**JobStatusEnum**](.md) | If specified, this limits the jobs or tasks to follow status | [optional] [default to null]
 **organizationIDs** | **string** |  | [optional] [default to null]

### Return type

[**GetJobsStatsResponse**](GetJobsStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobsTimeRangesStats

This gets processing stats of the jobs grouped by time ranges and sorted by a range start time

### Example

```bash
aiware getJobsTimeRangesStats X-Correlation-Id:value  startTime=value  endTime=value  status=value  interval=value  organizationIDs=value  engineCategoryID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**JobStatusEnum**](.md) | If specified, this limits the jobs or tasks to follow status | [optional] [default to null]
 **interval** | **integer** | Interval in seconds for output time ranges | [optional] [default to null]
 **organizationIDs** | **string** |  | [optional] [default to null]
 **engineCategoryID** | [**string**](.md) |  | [optional] [default to null]

### Return type

[**GetJobsTimeRangesStatsResponse**](GetJobsTimeRangesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getRatePendingScheduledJobs

This gets the rate of pending scheduled jobs by time ranges

### Example

```bash
aiware getRatePendingScheduledJobs X-Correlation-Id:value  startTime=value  endTime=value  interval=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **interval** | **integer** | Interval in seconds for output time ranges | [optional] [default to null]

### Return type

[**GetRatePendingScheduledJobsResponse**](GetRatePendingScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getScheduledJobDetail

This gets scheduled job detail

### Example

```bash
aiware getScheduledJobDetail ScheduledJobID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scheduledJobID** | [**string**](.md) | ID of Scheduled Job. It can be an internal ID or core ID | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetScheduledJobDetailResponse**](GetScheduledJobDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getScheduledJobs

This gets a list of scheduled jobs

### Example

```bash
aiware getScheduledJobs X-Correlation-Id:value  startTime=value  endTime=value  offset=value  limit=value  direction=value  scheduledJobID=value  internalOrganizationID=value  coreID=value  startStartTime=value  endStartTime=value  startStopTime=value  endStopTime=value  isActive=value  runMode=value  sourceID=value  sourceType=value  orderBy=value  scheduledJobName=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **offset** | **integer** | the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **integer** | the number of items to return. | [optional] [default to 10]
 **direction** | **string** | the sort order.  ASC or DESC. | [optional] [default to DESC]
 **scheduledJobID** | **string** | Filter by internal scheduled Job ID(uuid) or core scheduled Job ID (integer) | [optional] [default to null]
 **internalOrganizationID** | [**string**](.md) | Filter by internal organization id | [optional] [default to null]
 **coreID** | [**string**](.md) | Filter by coreID | [optional] [default to null]
 **startStartTime** | **integer** |  | [optional] [default to null]
 **endStartTime** | **integer** |  | [optional] [default to null]
 **startStopTime** | **integer** |  | [optional] [default to null]
 **endStopTime** | **integer** |  | [optional] [default to null]
 **isActive** | **boolean** |  | [optional] [default to null]
 **runMode** | [**ScheduleRunModeEnum**](.md) | Filter by runMode | [optional] [default to null]
 **sourceID** | **integer** |  | [optional] [default to null]
 **sourceType** | **string** |  | [optional] [default to null]
 **orderBy** | **string** | The value should be in [organizationID, runMode, createdTime, startTime, stopTime] | [optional] [default to null]
 **scheduledJobName** | **string** |  | [optional] [default to null]

### Return type

[**GetScheduledJobsResponse**](GetScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getServerErrorCounts

Get server error counts in a time-range

### Example

```bash
aiware getServerErrorCounts X-Correlation-Id:value  startTime=value  endTime=value  chartType=value  service=value  interval=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **chartType** | [**ServerErrorChartTypeEnum**](.md) | It will help API to kmow the response should return | [optional] [default to null]
 **service** | **string** | Filter data by service name. | [optional] [default to null]
 **interval** | **integer** | Interval in seconds for output time ranges | [optional] [default to null]

### Return type

[**GetServerErrorCountsResponse**](GetServerErrorCountsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTaskDetail

Gets Task Detail

### Example

```bash
aiware getTaskDetail TaskID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**string**](.md) | ID of Task | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetTaskDetailResponse**](GetTaskDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTaskDownload

Returns the contents of the task's output

### Example

```bash
aiware getTaskDownload TaskID=value TaskOutputName=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**string**](.md) | ID of Task | [default to null]
 **taskOutputName** | **string** | Name of the task output, e.g. vtn-standard.json | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**array[Byte]**](Byte.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTaskLogs

Gets logs associated with a task

### Example

```bash
aiware getTaskLogs TaskID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**string**](.md) | ID of Task | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

**binary**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/zip, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTaskOutput

Returns the contents of the task's output

### Example

```bash
aiware getTaskOutput TaskID=value TaskOutputName=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**string**](.md) | ID of Task | [default to null]
 **taskOutputName** | **string** | Name of the task output, e.g. vtn-standard.json | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetTaskOutputResponse**](GetTaskOutputResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTaskOutputs

Gets Task Output

### Example

```bash
aiware getTaskOutputs TaskID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**string**](.md) | ID of Task | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetTaskOutputsResponse**](GetTaskOutputsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTaskSyncBacklog

Gets task sync backlog in a time-range

### Example

```bash
aiware getTaskSyncBacklog X-Correlation-Id:value  startTime=value  endTime=value  interval=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **interval** | **integer** | Interval in seconds for output time ranges | [optional] [default to null]

### Return type

[**GetTaskSyncBacklogResponse**](GetTaskSyncBacklogResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTasks

This gets a list of tasks based on the provided criteria

### Example

```bash
aiware getTasks X-Correlation-Id:value  startTime=value  endTime=value  offset=value  limit=value  orderBy=value  direction=value  status=value  organizationID=value  taskID=value  coreTaskID=value  errorType=value  jobID=value  coreJobID=value  engineID=value  mediaSourceID=value  recordingID=value  engineCategoryID=value  modifiedBefore=value  modifiedAfter=value  CreatedBefore=value  CreatedAfter=value  backlog=value  alloc=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **offset** | **integer** | the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **integer** | the number of items to return. | [optional] [default to 10]
 **orderBy** | **string** | the field to sort | [optional] [default to createdDateTime]
 **direction** | **string** | the sort order.  ASC or DESC. | [optional] [default to DESC]
 **status** | [**TaskStatusEnum**](.md) | Filtering by task Status | [optional] [default to null]
 **organizationID** | **string** | Filter by organization id | [optional] [default to null]
 **taskID** | **string** | Filter by task id | [optional] [default to null]
 **coreTaskID** | **string** | Filter by coreTaskID | [optional] [default to null]
 **errorType** | [**FailureReasonEnum**](.md) | filter by errorType (failureReason) | [optional] [default to null]
 **jobID** | **string** | Filter by job id | [optional] [default to null]
 **coreJobID** | **string** | Filter by coreJobID | [optional] [default to null]
 **engineID** | **string** | Filter by engine id | [optional] [default to null]
 **mediaSourceID** | **string** | Filter by media source id | [optional] [default to null]
 **recordingID** | **integer** | Filter tasks by the recording id | [optional] [default to null]
 **engineCategoryID** | [**string**](.md) | Filtering by engineCategoryID | [optional] [default to null]
 **modifiedBefore** | **integer** | Filter by items modified before expressed as timestamp | [optional] [default to null]
 **modifiedAfter** | **integer** | Filter by items modified after expressed as timestamp | [optional] [default to null]
 **createdBefore** | **integer** | Filter items where created date is before this date | [optional] [default to null]
 **createdAfter** | **integer** | Filter items where created date is after this date | [optional] [default to null]
 **backlog** | **boolean** | Filtering all tasks in backlog | [optional] [default to null]
 **alloc** | **boolean** | Filtering all tasks have alloc = true or not | [optional] [default to null]

### Return type

[**GetTasksResponse**](GetTasksResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTasksErrorTypeCountByEngine

This gets error type count by engines

### Example

```bash
aiware getTasksErrorTypeCountByEngine X-Correlation-Id:value  startTime=value  endTime=value  engineID=value  status=value  errorType=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **engineID** | **string** | Filter by engine id | [optional] [default to null]
 **status** | [**TaskStatusEnum**](.md) | Filtering by task Status | [optional] [default to null]
 **errorType** | [**FailureReasonEnum**](.md) | filter by errorType (failureReason) | [optional] [default to null]

### Return type

[**GetTasksErrorTypeCountByEngineResponse**](GetTasksErrorTypeCountByEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTasksErrors

This provides a error list in a time range

### Example

```bash
aiware getTasksErrors X-Correlation-Id:value  startTime=value  endTime=value  taskID=value  jobID=value  errorType=value  offset=value  limit=value  orderBy=value  direction=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **taskID** | [**string**](.md) | filter by taskID | [optional] [default to null]
 **jobID** | [**string**](.md) | filter by jobID | [optional] [default to null]
 **errorType** | [**FailureReasonEnum**](.md) | filter by errorType (failureReason) | [optional] [default to null]
 **offset** | **integer** | the number of records to skip before getting the result set | [optional] [default to null]
 **limit** | **integer** | the number of records to return. | [optional] [default to 100]
 **orderBy** | **string** | the field to sort. It should be in [createdDateTime, modifiedDateTime] | [optional] [default to createdDateTime]
 **direction** | **string** | the sort order | [optional] [default to DESC]

### Return type

[**GetTaskErrorsResponse**](GetTaskErrorsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTasksInstances

This gets processing stats of the tasks

### Example

```bash
aiware getTasksInstances X-Correlation-Id:value  startTime=value  endTime=value  status=value  engineCategoryID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**EngineStatusEnum**](.md) | If specified, this limits the engine instances to follow status | [optional] [default to null]
 **engineCategoryID** | [**string**](.md) |  | [optional] [default to null]

### Return type

[**GetTasksInstancesResponse**](GetTasksInstancesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTasksStats

This gets processing stats of the tasks

### Example

```bash
aiware getTasksStats X-Correlation-Id:value  startTime=value  endTime=value  chartType=value  status=value  organizationIDs=value  engineIDs=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **chartType** | [**JobTaskStatusChartTypeEnum**](.md) | It will help API to kmow the response should return | [optional] [default to null]
 **status** | [**TaskStatusEnum**](.md) | Filtering by task Status | [optional] [default to null]
 **organizationIDs** | [**string**](.md) |  | [optional] [default to null]
 **engineIDs** | [**string**](.md) |  | [optional] [default to null]

### Return type

[**GetTasksStatsResponse**](GetTasksStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTasksStatsCategories

This gets processing stats of the tasks grouped by engine categories

### Example

```bash
aiware getTasksStatsCategories X-Correlation-Id:value  startTime=value  endTime=value  status=value  organizationIDs=value  engineCategoryID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**TaskStatusEnum**](.md) | Filtering by task Status | [optional] [default to null]
 **organizationIDs** | [**string**](.md) |  | [optional] [default to null]
 **engineCategoryID** | [**string**](.md) |  | [optional] [default to null]

### Return type

[**GetTasksCategoriesStatsResponse**](GetTasksCategoriesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTasksStatsEngines

This gets processing stats of the tasks grouped by engine

### Example

```bash
aiware getTasksStatsEngines X-Correlation-Id:value  startTime=value  endTime=value  status=value  organizationID=value  taskID=value  errorType=value  jobID=value  engineID=value  mediaSourceID=value  recordingID=value  engineCategoryID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**TaskStatusEnum**](.md) | Filtering by task Status | [optional] [default to null]
 **organizationID** | **string** | Filter by  organization id | [optional] [default to null]
 **taskID** | **string** | Filter by task id | [optional] [default to null]
 **errorType** | [**FailureReasonEnum**](.md) | filter by errorType (failureReason) | [optional] [default to null]
 **jobID** | **string** | Filter by job id | [optional] [default to null]
 **engineID** | **string** | Filter by engine id | [optional] [default to null]
 **mediaSourceID** | **string** | Filter by media source id | [optional] [default to null]
 **recordingID** | **integer** | Filter tasks by the recording id | [optional] [default to null]
 **engineCategoryID** | [**string**](.md) | Filtering by engineCategoryID | [optional] [default to null]

### Return type

[**GetTasksEnginesStatsResponse**](GetTasksEnginesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTasksStatsOrganizations

This gets processing stats of the tasks grouped by engine, filter by organizations

### Example

```bash
aiware getTasksStatsOrganizations X-Correlation-Id:value  startTime=value  endTime=value  status=value  organizationIDs=value  engineID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**TaskStatusEnum**](.md) | Filtering by task Status | [optional] [default to null]
 **organizationIDs** | [**string**](.md) | Filter by organization IDs | [optional] [default to null]
 **engineID** | [**string**](.md) | Filter by engine ID | [optional] [default to null]

### Return type

[**GetTasksStatsOrganizationsResponse**](GetTasksStatsOrganizationsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTasksStatsTimeRanges

This gets processing stats of the tasks grouped by time ranges and sorted by a range start time

### Example

```bash
aiware getTasksStatsTimeRanges X-Correlation-Id:value  startTime=value  endTime=value  status=value  interval=value  engineCategoryID=value  organizationIDs=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**TaskStatusEnum**](.md) | Filtering by task Status | [optional] [default to null]
 **interval** | **integer** | Interval in seconds for output time ranges | [optional] [default to null]
 **engineCategoryID** | [**string**](.md) | Filtering by engineCategoryID | [optional] [default to null]
 **organizationIDs** | **string** |  | [optional] [default to null]

### Return type

[**GetTasksTimeRangesStatsResponse**](GetTasksTimeRangesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTotalPendingScheduledJobs

This gets the total pending scheduled jobs by time ranges

### Example

```bash
aiware getTotalPendingScheduledJobs X-Correlation-Id:value  startTime=value  endTime=value  interval=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **interval** | **integer** | Interval in seconds for output time ranges | [optional] [default to null]

### Return type

[**GetTotalPendingScheduledJobsResponse**](GetTotalPendingScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getWorkRequest

This provides detail of workrequest

### Example

```bash
aiware getWorkRequest WorkRequestID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workRequestID** | [**string**](.md) | ID of Work request | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetTaskWorkRequestResponse**](GetTaskWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## launchJobTemplate

This launch a job based on the given job template

### Example

```bash
aiware launchJobTemplate TemplateID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **templateID** | **string** | ID of Job | [default to null]
 **launchJobTemplateRequest** | [**LaunchJobTemplateRequest**](LaunchJobTemplateRequest.md) | Launch Job Template API |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**LaunchJobTemplateResponse**](LaunchJobTemplateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pushContentToEndpoint

Whatever is posted to this endpoint will be added to the child input folder(s) for the task_routes that have this endpoint.  If more than one task_routes have this endpoint, it will be added to all child input folders.

### Example

```bash
aiware pushContentToEndpoint Endpoint=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **endpoint** | [**string**](.md) | Endpoint UUID to push this chunk towards | [default to null]
 **body** | **string** | How to push content into a child input folder(s). |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**CreateJobResponse**](CreateJobResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json, application/octet-stream, audio/*, image/*, text/html, text/plain, text/xml, video/*
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## recheckJobStatus

Recheck Job Status

### Example

```bash
aiware recheckJobStatus JobID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**string**](.md) | ID of Job | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**RecheckJobStatusResponse**](RecheckJobStatusResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tasksStatusExport

Export a task status report as a excel file

### Example

```bash
aiware tasksStatusExport X-Correlation-Id:value  startTime=value  endTime=value  offset=value  limit=value  orderBy=value  direction=value  status=value  organizationID=value  taskID=value  coreTaskID=value  errorType=value  jobID=value  coreJobID=value  engineID=value  mediaSourceID=value  recordingID=value  engineCategoryID=value  modifiedBefore=value  modifiedAfter=value  CreatedBefore=value  CreatedAfter=value  backlog=value  alloc=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **offset** | **integer** | the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **integer** | the number of items to return. | [optional] [default to 10]
 **orderBy** | **string** | the field to sort | [optional] [default to createdDateTime]
 **direction** | **string** | the sort order.  ASC or DESC. | [optional] [default to DESC]
 **status** | [**TaskStatusEnum**](.md) | Filtering by task Status | [optional] [default to null]
 **organizationID** | **string** | Filter by organization id | [optional] [default to null]
 **taskID** | **string** | Filter by task id | [optional] [default to null]
 **coreTaskID** | **string** | Filter by coreTaskID | [optional] [default to null]
 **errorType** | [**FailureReasonEnum**](.md) | filter by errorType (failureReason) | [optional] [default to null]
 **jobID** | **string** | Filter by job id | [optional] [default to null]
 **coreJobID** | **string** | Filter by coreJobID | [optional] [default to null]
 **engineID** | **string** | Filter by engine id | [optional] [default to null]
 **mediaSourceID** | **string** | Filter by media source id | [optional] [default to null]
 **recordingID** | **integer** | Filter tasks by the recording id | [optional] [default to null]
 **engineCategoryID** | [**string**](.md) | Filtering by engineCategoryID | [optional] [default to null]
 **modifiedBefore** | **integer** | Filter by items modified before expressed as timestamp | [optional] [default to null]
 **modifiedAfter** | **integer** | Filter by items modified after expressed as timestamp | [optional] [default to null]
 **createdBefore** | **integer** | Filter items where created date is before this date | [optional] [default to null]
 **createdAfter** | **integer** | Filter items where created date is after this date | [optional] [default to null]
 **backlog** | **boolean** | Filtering all tasks in backlog | [optional] [default to null]
 **alloc** | **boolean** | Filtering all tasks have alloc = true or not | [optional] [default to null]

### Return type

**binary**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateTaskStatus

This updates the status for a bulk of tasks by taskID

### Example

```bash
aiware updateTaskStatus X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tasksStatusUpdateRequest** | [**TasksStatusUpdateRequest**](TasksStatusUpdateRequest.md) | The input for updateTaskStatus |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**TasksStatusUpdateResponse**](TasksStatusUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

