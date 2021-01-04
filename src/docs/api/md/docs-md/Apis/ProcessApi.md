# ProcessApi

All URIs are relative to *https://api.aiware.com/edge/v1*

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


<a name="addTask"></a>
# **addTask**
> AddTaskResponse addTask(JobID, AddTaskRequest, X-Correlation-Id)

Adds a Task to a current job

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobID** | [**UUID**](../Models/.md)| ID of Job | [default to null]
 **AddTaskRequest** | [**AddTaskRequest**](../Models/AddTaskRequest.md)| Create Job API |
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AddTaskResponse**](../Models/AddTaskResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="addTaskRoute"></a>
# **addTaskRoute**
> AddTaskRouteResponse addTaskRoute(JobID, AddTaskRouteRequest, X-Correlation-Id)

Adds a Task Route to a current job

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobID** | [**UUID**](../Models/.md)| ID of Job | [default to null]
 **AddTaskRouteRequest** | [**AddTaskRouteRequest**](../Models/AddTaskRouteRequest.md)| Adds a Task Route |
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AddTaskRouteResponse**](../Models/AddTaskRouteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="createJob"></a>
# **createJob**
> CreateJobResponse createJob(CreateJobRequest, X-Correlation-Id)

This creates a new Job

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateJobRequest** | [**CreateJobRequest**](../Models/CreateJobRequest.md)| Create Job API |
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**CreateJobResponse**](../Models/CreateJobResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deleteJob"></a>
# **deleteJob**
> AdminOperationResponse deleteJob(JobID, X-Correlation-Id, DeleteJobRequest)

This API deletes the specified job

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobID** | [**UUID**](../Models/.md)| ID of Job | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **DeleteJobRequest** | [**DeleteJobRequest**](../Models/DeleteJobRequest.md)| Request information to delete the specified job | [optional]

### Return type

[**AdminOperationResponse**](../Models/AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deleteTask"></a>
# **deleteTask**
> AdminOperationResponse deleteTask(TaskID, X-Correlation-Id)

This API deletes the specified task

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TaskID** | [**UUID**](../Models/.md)| ID of Task | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](../Models/AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getEngineErrorTimeRanges"></a>
# **getEngineErrorTimeRanges**
> GetEngineErrorTimeRangesResponse getEngineErrorTimeRanges(X-Correlation-Id, startTime, endTime, chartType, interval, engineID)

This gets engine error count by error tasks grouped by time ranges and sorted by a range start time

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **chartType** | [**EngineErrorChartTypeEnum**](../Models/.md)| It will help API to kmow the response should return | [optional] [default to null] [enum: total_engine_errors, total_failed_task_by_engine]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional] [default to null]
 **engineID** | [**UUID**](../Models/.md)| Filtering by engineID | [optional] [default to null]

### Return type

[**GetEngineErrorTimeRangesResponse**](../Models/GetEngineErrorTimeRangesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getJobDetail"></a>
# **getJobDetail**
> GetJobDetailResponse getJobDetail(JobID, X-Correlation-Id)

Gets Job Detail

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobID** | [**UUID**](../Models/.md)| ID of Job | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetJobDetailResponse**](../Models/GetJobDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getJobDownload"></a>
# **getJobDownload**
> List getJobDownload(JobID, JobOutputName, X-Correlation-Id)

Returns the contents of the job&#39;s output

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobID** | [**UUID**](../Models/.md)| ID of Job | [default to null]
 **JobOutputName** | **String**| Name of the job output, e.g. vtn-standard.json | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**List**](../Models/ByteArray.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getJobOutput"></a>
# **getJobOutput**
> GetJobOutputResponse getJobOutput(JobID, JobOutputName, X-Correlation-Id)

Returns the contents of the job&#39;s output

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobID** | [**UUID**](../Models/.md)| ID of Job | [default to null]
 **JobOutputName** | **String**| Name of the job output, e.g. vtn-standard.json | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetJobOutputResponse**](../Models/GetJobOutputResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getJobOutputs"></a>
# **getJobOutputs**
> GetJobOutputsResponse getJobOutputs(JobID, X-Correlation-Id)

Returns a list of output information about this job

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobID** | [**UUID**](../Models/.md)| ID of Job | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetJobOutputsResponse**](../Models/GetJobOutputsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getJobPerformance"></a>
# **getJobPerformance**
> GetJobPerformanceResponse getJobPerformance(JobID, X-Correlation-Id, interval, taskID, workRequestID)

This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobID** | [**UUID**](../Models/.md)| ID of Job | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional] [default to null]
 **taskID** | [**UUID**](../Models/.md)| Filter data by taskID | [optional] [default to null]
 **workRequestID** | [**UUID**](../Models/.md)| Filter data by workRequestID | [optional] [default to null]

### Return type

[**GetJobPerformanceResponse**](../Models/GetJobPerformanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getJobStatus"></a>
# **getJobStatus**
> GetJobStatusResponse getJobStatus(JobID, X-Correlation-Id)

Gets Job Status

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobID** | [**UUID**](../Models/.md)| ID of Job | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetJobStatusResponse**](../Models/GetJobStatusResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getJobWorkRequests"></a>
# **getJobWorkRequests**
> GetJobWorkRequestResponse getJobWorkRequests(JobID, X-Correlation-Id, offset, limit, orderBy, direction, status, taskID)

This provides a list of workrequests of a job

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobID** | [**UUID**](../Models/.md)| ID of Job | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **offset** | **Integer**| the number of records to skip before getting the result set | [optional] [default to null]
 **limit** | **Integer**| the number of records to return. | [optional] [default to 100]
 **orderBy** | **String**| the field to sort. It should be in [createdDateTime, modifiedDateTime] | [optional] [default to createdDateTime]
 **direction** | **String**| the sort order | [optional] [default to DESC]
 **status** | **String**| the value should be in [active, trial, inactive, deleted] | [optional] [default to null]
 **taskID** | **String**| This is an internal task ID to get work request | [optional] [default to null]

### Return type

[**GetJobWorkRequestResponse**](../Models/GetJobWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getJobs"></a>
# **getJobs**
> GetJobListResponse getJobs(X-Correlation-Id, startTime, endTime, status, offset, limit, orderBy, direction, coreID, organizationID, recordingID, jobID, coreJobID, modifiedBefore, modifiedAfter, CreatedBefore, CreatedAfter)

This gets a list of jobs

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**JobStatusEnum**](../Models/.md)| If specified, this limits the jobs or tasks to follow status | [optional] [default to null] [enum: scheduled, pending, queued, running, complete, aborted, failed, rejected, reprocessing]
 **offset** | **Long**| the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10]
 **orderBy** | **String**| the field to sort | [optional] [default to createdDateTime]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to DESC]
 **coreID** | [**UUID**](../Models/.md)| Filter by coreID | [optional] [default to null]
 **organizationID** | [**UUID**](../Models/.md)| Filter by organizationID | [optional] [default to null]
 **recordingID** | [**UUID**](../Models/.md)| Filter by recordingID | [optional] [default to null]
 **jobID** | [**UUID**](../Models/.md)| Filter by jobID | [optional] [default to null]
 **coreJobID** | **String**| Filter by coreJobID | [optional] [default to null]
 **modifiedBefore** | **Long**| Filter by items modified before expressed as timestamp | [optional] [default to null]
 **modifiedAfter** | **Long**| Filter by items modified after expressed as timestamp | [optional] [default to null]
 **CreatedBefore** | **Long**| Filter items where created date is before this date | [optional] [default to null]
 **CreatedAfter** | **Long**| Filter items where created date is after this date | [optional] [default to null]

### Return type

[**GetJobListResponse**](../Models/GetJobListResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getJobsOrganizationStats"></a>
# **getJobsOrganizationStats**
> GetJobsOrganizationStatsResponse getJobsOrganizationStats(X-Correlation-Id, startTime, endTime, organizationIDs)

This gets processing stats of the jobs by organization

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **organizationIDs** | **String**|  | [optional] [default to null]

### Return type

[**GetJobsOrganizationStatsResponse**](../Models/GetJobsOrganizationStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getJobsPerformance"></a>
# **getJobsPerformance**
> GetJobsPerformanceResponse getJobsPerformance(X-Correlation-Id, startTime, endTime, interval)

This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional] [default to null]

### Return type

[**GetJobsPerformanceResponse**](../Models/GetJobsPerformanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getJobsStats"></a>
# **getJobsStats**
> GetJobsStatsResponse getJobsStats(X-Correlation-Id, startTime, endTime, chartType, status, organizationIDs)

This gets processing stats of the jobs

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **chartType** | [**JobTaskStatusChartTypeEnum**](../Models/.md)| It will help API to kmow the response should return | [optional] [default to null] [enum: total, total_by_time_range]
 **status** | [**JobStatusEnum**](../Models/.md)| If specified, this limits the jobs or tasks to follow status | [optional] [default to null] [enum: scheduled, pending, queued, running, complete, aborted, failed, rejected, reprocessing]
 **organizationIDs** | **String**|  | [optional] [default to null]

### Return type

[**GetJobsStatsResponse**](../Models/GetJobsStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getJobsTimeRangesStats"></a>
# **getJobsTimeRangesStats**
> GetJobsTimeRangesStatsResponse getJobsTimeRangesStats(X-Correlation-Id, startTime, endTime, status, interval, organizationIDs, engineCategoryID)

This gets processing stats of the jobs grouped by time ranges and sorted by a range start time

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**JobStatusEnum**](../Models/.md)| If specified, this limits the jobs or tasks to follow status | [optional] [default to null] [enum: scheduled, pending, queued, running, complete, aborted, failed, rejected, reprocessing]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional] [default to null]
 **organizationIDs** | **String**|  | [optional] [default to null]
 **engineCategoryID** | [**UUID**](../Models/.md)|  | [optional] [default to null]

### Return type

[**GetJobsTimeRangesStatsResponse**](../Models/GetJobsTimeRangesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getRatePendingScheduledJobs"></a>
# **getRatePendingScheduledJobs**
> GetRatePendingScheduledJobsResponse getRatePendingScheduledJobs(X-Correlation-Id, startTime, endTime, interval)

This gets the rate of pending scheduled jobs by time ranges

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional] [default to null]

### Return type

[**GetRatePendingScheduledJobsResponse**](../Models/GetRatePendingScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getScheduledJobDetail"></a>
# **getScheduledJobDetail**
> GetScheduledJobDetailResponse getScheduledJobDetail(ScheduledJobID, X-Correlation-Id)

This gets scheduled job detail

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ScheduledJobID** | [**UUID**](../Models/.md)| ID of Scheduled Job. It can be an internal ID or core ID | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetScheduledJobDetailResponse**](../Models/GetScheduledJobDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getScheduledJobs"></a>
# **getScheduledJobs**
> GetScheduledJobsResponse getScheduledJobs(X-Correlation-Id, startTime, endTime, offset, limit, direction, scheduledJobID, internalOrganizationID, coreID, startStartTime, endStartTime, startStopTime, endStopTime, isActive, runMode, sourceID, sourceType, orderBy, scheduledJobName)

This gets a list of scheduled jobs

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **offset** | **Long**| the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to DESC]
 **scheduledJobID** | **String**| Filter by internal scheduled Job ID(uuid) or core scheduled Job ID (integer) | [optional] [default to null]
 **internalOrganizationID** | [**UUID**](../Models/.md)| Filter by internal organization id | [optional] [default to null]
 **coreID** | [**UUID**](../Models/.md)| Filter by coreID | [optional] [default to null]
 **startStartTime** | **Long**|  | [optional] [default to null]
 **endStartTime** | **Long**|  | [optional] [default to null]
 **startStopTime** | **Long**|  | [optional] [default to null]
 **endStopTime** | **Long**|  | [optional] [default to null]
 **isActive** | **Boolean**|  | [optional] [default to null]
 **runMode** | [**ScheduleRunModeEnum**](../Models/.md)| Filter by runMode | [optional] [default to null] [enum: continuous, recurring, now, once]
 **sourceID** | **Integer**|  | [optional] [default to null]
 **sourceType** | **String**|  | [optional] [default to null]
 **orderBy** | **String**| The value should be in [organizationID, runMode, createdTime, startTime, stopTime] | [optional] [default to null]
 **scheduledJobName** | **String**|  | [optional] [default to null]

### Return type

[**GetScheduledJobsResponse**](../Models/GetScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getServerErrorCounts"></a>
# **getServerErrorCounts**
> GetServerErrorCountsResponse getServerErrorCounts(X-Correlation-Id, startTime, endTime, chartType, service, interval)

Get server error counts in a time-range

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **chartType** | [**ServerErrorChartTypeEnum**](../Models/.md)| It will help API to kmow the response should return | [optional] [default to null] [enum: total, pie, time_range]
 **service** | **String**| Filter data by service name. | [optional] [default to null]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional] [default to null]

### Return type

[**GetServerErrorCountsResponse**](../Models/GetServerErrorCountsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTaskDetail"></a>
# **getTaskDetail**
> GetTaskDetailResponse getTaskDetail(TaskID, X-Correlation-Id)

Gets Task Detail

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TaskID** | [**UUID**](../Models/.md)| ID of Task | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetTaskDetailResponse**](../Models/GetTaskDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTaskDownload"></a>
# **getTaskDownload**
> List getTaskDownload(TaskID, TaskOutputName, X-Correlation-Id)

Returns the contents of the task&#39;s output

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TaskID** | [**UUID**](../Models/.md)| ID of Task | [default to null]
 **TaskOutputName** | **String**| Name of the task output, e.g. vtn-standard.json | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**List**](../Models/byte.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTaskLogs"></a>
# **getTaskLogs**
> File getTaskLogs(TaskID, X-Correlation-Id)

Gets logs associated with a task

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TaskID** | [**UUID**](../Models/.md)| ID of Task | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**File**](../Models/file.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/zip, application/json

<a name="getTaskOutput"></a>
# **getTaskOutput**
> GetTaskOutputResponse getTaskOutput(TaskID, TaskOutputName, X-Correlation-Id)

Returns the contents of the task&#39;s output

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TaskID** | [**UUID**](../Models/.md)| ID of Task | [default to null]
 **TaskOutputName** | **String**| Name of the task output, e.g. vtn-standard.json | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetTaskOutputResponse**](../Models/GetTaskOutputResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTaskOutputs"></a>
# **getTaskOutputs**
> GetTaskOutputsResponse getTaskOutputs(TaskID, X-Correlation-Id)

Gets Task Output

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TaskID** | [**UUID**](../Models/.md)| ID of Task | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetTaskOutputsResponse**](../Models/GetTaskOutputsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTaskSyncBacklog"></a>
# **getTaskSyncBacklog**
> GetTaskSyncBacklogResponse getTaskSyncBacklog(X-Correlation-Id, startTime, endTime, interval)

Gets task sync backlog in a time-range

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional] [default to null]

### Return type

[**GetTaskSyncBacklogResponse**](../Models/GetTaskSyncBacklogResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTasks"></a>
# **getTasks**
> GetTasksResponse getTasks(X-Correlation-Id, startTime, endTime, offset, limit, orderBy, direction, status, organizationID, taskID, coreTaskID, errorType, jobID, coreJobID, engineID, mediaSourceID, recordingID, engineCategoryID, modifiedBefore, modifiedAfter, CreatedBefore, CreatedAfter, backlog, alloc)

This gets a list of tasks based on the provided criteria

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **offset** | **Long**| the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10]
 **orderBy** | **String**| the field to sort | [optional] [default to createdDateTime]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to DESC]
 **status** | [**TaskStatusEnum**](../Models/.md)| Filtering by task Status | [optional] [default to null] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **organizationID** | **String**| Filter by organization id | [optional] [default to null]
 **taskID** | **String**| Filter by task id | [optional] [default to null]
 **coreTaskID** | **String**| Filter by coreTaskID | [optional] [default to null]
 **errorType** | [**FailureReasonEnum**](../Models/.md)| filter by errorType (failureReason) | [optional] [default to null] [enum: internal_error, unknown, connection, rate_limited, unauthorized, api, resources, not_found, core_api, bad_data, none]
 **jobID** | **String**| Filter by job id | [optional] [default to null]
 **coreJobID** | **String**| Filter by coreJobID | [optional] [default to null]
 **engineID** | **String**| Filter by engine id | [optional] [default to null]
 **mediaSourceID** | **String**| Filter by media source id | [optional] [default to null]
 **recordingID** | **Long**| Filter tasks by the recording id | [optional] [default to null]
 **engineCategoryID** | [**UUID**](../Models/.md)| Filtering by engineCategoryID | [optional] [default to null]
 **modifiedBefore** | **Long**| Filter by items modified before expressed as timestamp | [optional] [default to null]
 **modifiedAfter** | **Long**| Filter by items modified after expressed as timestamp | [optional] [default to null]
 **CreatedBefore** | **Long**| Filter items where created date is before this date | [optional] [default to null]
 **CreatedAfter** | **Long**| Filter items where created date is after this date | [optional] [default to null]
 **backlog** | **Boolean**| Filtering all tasks in backlog | [optional] [default to null]
 **alloc** | **Boolean**| Filtering all tasks have alloc &#x3D; true or not | [optional] [default to null]

### Return type

[**GetTasksResponse**](../Models/GetTasksResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTasksErrorTypeCountByEngine"></a>
# **getTasksErrorTypeCountByEngine**
> GetTasksErrorTypeCountByEngineResponse getTasksErrorTypeCountByEngine(X-Correlation-Id, startTime, endTime, engineID, status, errorType)

This gets error type count by engines

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **engineID** | **String**| Filter by engine id | [optional] [default to null]
 **status** | [**TaskStatusEnum**](../Models/.md)| Filtering by task Status | [optional] [default to null] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **errorType** | [**FailureReasonEnum**](../Models/.md)| filter by errorType (failureReason) | [optional] [default to null] [enum: internal_error, unknown, connection, rate_limited, unauthorized, api, resources, not_found, core_api, bad_data, none]

### Return type

[**GetTasksErrorTypeCountByEngineResponse**](../Models/GetTasksErrorTypeCountByEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTasksErrors"></a>
# **getTasksErrors**
> GetTaskErrorsResponse getTasksErrors(X-Correlation-Id, startTime, endTime, taskID, jobID, errorType, offset, limit, orderBy, direction)

This provides a error list in a time range

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **taskID** | [**UUID**](../Models/.md)| filter by taskID | [optional] [default to null]
 **jobID** | [**UUID**](../Models/.md)| filter by jobID | [optional] [default to null]
 **errorType** | [**FailureReasonEnum**](../Models/.md)| filter by errorType (failureReason) | [optional] [default to null] [enum: internal_error, unknown, connection, rate_limited, unauthorized, api, resources, not_found, core_api, bad_data, none]
 **offset** | **Integer**| the number of records to skip before getting the result set | [optional] [default to null]
 **limit** | **Integer**| the number of records to return. | [optional] [default to 100]
 **orderBy** | **String**| the field to sort. It should be in [createdDateTime, modifiedDateTime] | [optional] [default to createdDateTime]
 **direction** | **String**| the sort order | [optional] [default to DESC]

### Return type

[**GetTaskErrorsResponse**](../Models/GetTaskErrorsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTasksInstances"></a>
# **getTasksInstances**
> GetTasksInstancesResponse getTasksInstances(X-Correlation-Id, startTime, endTime, status, engineCategoryID)

This gets processing stats of the tasks

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**EngineStatusEnum**](../Models/.md)| If specified, this limits the engine instances to follow status | [optional] [default to null] [enum: active, terminated]
 **engineCategoryID** | [**UUID**](../Models/.md)|  | [optional] [default to null]

### Return type

[**GetTasksInstancesResponse**](../Models/GetTasksInstancesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTasksStats"></a>
# **getTasksStats**
> GetTasksStatsResponse getTasksStats(X-Correlation-Id, startTime, endTime, chartType, status, organizationIDs, engineIDs)

This gets processing stats of the tasks

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **chartType** | [**JobTaskStatusChartTypeEnum**](../Models/.md)| It will help API to kmow the response should return | [optional] [default to null] [enum: total, total_by_time_range]
 **status** | [**TaskStatusEnum**](../Models/.md)| Filtering by task Status | [optional] [default to null] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **organizationIDs** | [**UUID**](../Models/.md)|  | [optional] [default to null]
 **engineIDs** | [**UUID**](../Models/.md)|  | [optional] [default to null]

### Return type

[**GetTasksStatsResponse**](../Models/GetTasksStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTasksStatsCategories"></a>
# **getTasksStatsCategories**
> GetTasksCategoriesStatsResponse getTasksStatsCategories(X-Correlation-Id, startTime, endTime, status, organizationIDs, engineCategoryID)

This gets processing stats of the tasks grouped by engine categories

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**TaskStatusEnum**](../Models/.md)| Filtering by task Status | [optional] [default to null] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **organizationIDs** | [**UUID**](../Models/.md)|  | [optional] [default to null]
 **engineCategoryID** | [**UUID**](../Models/.md)|  | [optional] [default to null]

### Return type

[**GetTasksCategoriesStatsResponse**](../Models/GetTasksCategoriesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTasksStatsEngines"></a>
# **getTasksStatsEngines**
> GetTasksEnginesStatsResponse getTasksStatsEngines(X-Correlation-Id, startTime, endTime, status, organizationID, taskID, errorType, jobID, engineID, mediaSourceID, recordingID, engineCategoryID)

This gets processing stats of the tasks grouped by engine

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**TaskStatusEnum**](../Models/.md)| Filtering by task Status | [optional] [default to null] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **organizationID** | **String**| Filter by  organization id | [optional] [default to null]
 **taskID** | **String**| Filter by task id | [optional] [default to null]
 **errorType** | [**FailureReasonEnum**](../Models/.md)| filter by errorType (failureReason) | [optional] [default to null] [enum: internal_error, unknown, connection, rate_limited, unauthorized, api, resources, not_found, core_api, bad_data, none]
 **jobID** | **String**| Filter by job id | [optional] [default to null]
 **engineID** | **String**| Filter by engine id | [optional] [default to null]
 **mediaSourceID** | **String**| Filter by media source id | [optional] [default to null]
 **recordingID** | **Long**| Filter tasks by the recording id | [optional] [default to null]
 **engineCategoryID** | [**UUID**](../Models/.md)| Filtering by engineCategoryID | [optional] [default to null]

### Return type

[**GetTasksEnginesStatsResponse**](../Models/GetTasksEnginesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTasksStatsOrganizations"></a>
# **getTasksStatsOrganizations**
> GetTasksStatsOrganizationsResponse getTasksStatsOrganizations(X-Correlation-Id, startTime, endTime, status, organizationIDs, engineID)

This gets processing stats of the tasks grouped by engine, filter by organizations

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**TaskStatusEnum**](../Models/.md)| Filtering by task Status | [optional] [default to null] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **organizationIDs** | [**UUID**](../Models/.md)| Filter by organization IDs | [optional] [default to null]
 **engineID** | [**UUID**](../Models/.md)| Filter by engine ID | [optional] [default to null]

### Return type

[**GetTasksStatsOrganizationsResponse**](../Models/GetTasksStatsOrganizationsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTasksStatsTimeRanges"></a>
# **getTasksStatsTimeRanges**
> GetTasksTimeRangesStatsResponse getTasksStatsTimeRanges(X-Correlation-Id, startTime, endTime, status, interval, engineCategoryID, organizationIDs)

This gets processing stats of the tasks grouped by time ranges and sorted by a range start time

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **status** | [**TaskStatusEnum**](../Models/.md)| Filtering by task Status | [optional] [default to null] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional] [default to null]
 **engineCategoryID** | [**UUID**](../Models/.md)| Filtering by engineCategoryID | [optional] [default to null]
 **organizationIDs** | **String**|  | [optional] [default to null]

### Return type

[**GetTasksTimeRangesStatsResponse**](../Models/GetTasksTimeRangesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getTotalPendingScheduledJobs"></a>
# **getTotalPendingScheduledJobs**
> GetTotalPendingScheduledJobsResponse getTotalPendingScheduledJobs(X-Correlation-Id, startTime, endTime, interval)

This gets the total pending scheduled jobs by time ranges

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional] [default to null]

### Return type

[**GetTotalPendingScheduledJobsResponse**](../Models/GetTotalPendingScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getWorkRequest"></a>
# **getWorkRequest**
> GetTaskWorkRequestResponse getWorkRequest(WorkRequestID, X-Correlation-Id)

This provides detail of workrequest

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **WorkRequestID** | [**UUID**](../Models/.md)| ID of Work request | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetTaskWorkRequestResponse**](../Models/GetTaskWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="launchJobTemplate"></a>
# **launchJobTemplate**
> LaunchJobTemplateResponse launchJobTemplate(TemplateID, LaunchJobTemplateRequest, X-Correlation-Id)

This launch a job based on the given job template

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TemplateID** | **String**| ID of Job | [default to null]
 **LaunchJobTemplateRequest** | [**LaunchJobTemplateRequest**](../Models/LaunchJobTemplateRequest.md)| Launch Job Template API |
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**LaunchJobTemplateResponse**](../Models/LaunchJobTemplateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="pushContentToEndpoint"></a>
# **pushContentToEndpoint**
> CreateJobResponse pushContentToEndpoint(Endpoint, body, X-Correlation-Id)

Whatever is posted to this endpoint will be added to the child input folder(s) for the task_routes that have this endpoint.  If more than one task_routes have this endpoint, it will be added to all child input folders.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Endpoint** | [**UUID**](../Models/.md)| Endpoint UUID to push this chunk towards | [default to null]
 **body** | **String**| How to push content into a child input folder(s). |
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**CreateJobResponse**](../Models/CreateJobResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json, application/octet-stream, audio/*, image/*, text/html, text/plain, text/xml, video/*
- **Accept**: application/json

<a name="recheckJobStatus"></a>
# **recheckJobStatus**
> RecheckJobStatusResponse recheckJobStatus(JobID, X-Correlation-Id)

Recheck Job Status

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobID** | [**UUID**](../Models/.md)| ID of Job | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**RecheckJobStatusResponse**](../Models/RecheckJobStatusResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="tasksStatusExport"></a>
# **tasksStatusExport**
> File tasksStatusExport(X-Correlation-Id, startTime, endTime, offset, limit, orderBy, direction, status, organizationID, taskID, coreTaskID, errorType, jobID, coreJobID, engineID, mediaSourceID, recordingID, engineCategoryID, modifiedBefore, modifiedAfter, CreatedBefore, CreatedAfter, backlog, alloc)

Export a task status report as a excel file

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **offset** | **Long**| the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10]
 **orderBy** | **String**| the field to sort | [optional] [default to createdDateTime]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to DESC]
 **status** | [**TaskStatusEnum**](../Models/.md)| Filtering by task Status | [optional] [default to null] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **organizationID** | **String**| Filter by organization id | [optional] [default to null]
 **taskID** | **String**| Filter by task id | [optional] [default to null]
 **coreTaskID** | **String**| Filter by coreTaskID | [optional] [default to null]
 **errorType** | [**FailureReasonEnum**](../Models/.md)| filter by errorType (failureReason) | [optional] [default to null] [enum: internal_error, unknown, connection, rate_limited, unauthorized, api, resources, not_found, core_api, bad_data, none]
 **jobID** | **String**| Filter by job id | [optional] [default to null]
 **coreJobID** | **String**| Filter by coreJobID | [optional] [default to null]
 **engineID** | **String**| Filter by engine id | [optional] [default to null]
 **mediaSourceID** | **String**| Filter by media source id | [optional] [default to null]
 **recordingID** | **Long**| Filter tasks by the recording id | [optional] [default to null]
 **engineCategoryID** | [**UUID**](../Models/.md)| Filtering by engineCategoryID | [optional] [default to null]
 **modifiedBefore** | **Long**| Filter by items modified before expressed as timestamp | [optional] [default to null]
 **modifiedAfter** | **Long**| Filter by items modified after expressed as timestamp | [optional] [default to null]
 **CreatedBefore** | **Long**| Filter items where created date is before this date | [optional] [default to null]
 **CreatedAfter** | **Long**| Filter items where created date is after this date | [optional] [default to null]
 **backlog** | **Boolean**| Filtering all tasks in backlog | [optional] [default to null]
 **alloc** | **Boolean**| Filtering all tasks have alloc &#x3D; true or not | [optional] [default to null]

### Return type

[**File**](../Models/file.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet, application/json

<a name="updateTaskStatus"></a>
# **updateTaskStatus**
> TasksStatusUpdateResponse updateTaskStatus(TasksStatusUpdateRequest, X-Correlation-Id)

This updates the status for a bulk of tasks by taskID

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TasksStatusUpdateRequest** | [**TasksStatusUpdateRequest**](../Models/TasksStatusUpdateRequest.md)| The input for updateTaskStatus |
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**TasksStatusUpdateResponse**](../Models/TasksStatusUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

