# \ProcessApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddTask**](ProcessApi.md#AddTask) | **Post** /proc/job/{JobID}/addtask | Adds a Task to a current job
[**AddTaskRoute**](ProcessApi.md#AddTaskRoute) | **Post** /proc/job/{JobID}/addtaskroute | Adds a Task Route to a current job
[**CreateJob**](ProcessApi.md#CreateJob) | **Post** /proc/job/create | This creates a new Job
[**DeleteJob**](ProcessApi.md#DeleteJob) | **Post** /proc/job/{JobID}/delete | This API deletes the specified job
[**DeleteTask**](ProcessApi.md#DeleteTask) | **Post** /proc/task/{TaskID}/delete | This API deletes the specified task
[**GetEngineErrorTimeRanges**](ProcessApi.md#GetEngineErrorTimeRanges) | **Get** /proc/tasks/error/engine_error_time_ranges | This gets engine error count by error tasks grouped by time ranges and sorted by a range start time
[**GetJobDetail**](ProcessApi.md#GetJobDetail) | **Get** /proc/job/{JobID}/detail | Gets Job Detail
[**GetJobDownload**](ProcessApi.md#GetJobDownload) | **Get** /proc/job/{JobID}/download/{JobOutputName} | Returns the contents of the job&#39;s output
[**GetJobOutput**](ProcessApi.md#GetJobOutput) | **Get** /proc/job/{JobID}/output/{JobOutputName} | Returns the contents of the job&#39;s output
[**GetJobOutputs**](ProcessApi.md#GetJobOutputs) | **Get** /proc/job/{JobID}/outputs | Returns a list of output information about this job
[**GetJobPerformance**](ProcessApi.md#GetJobPerformance) | **Get** /proc/job/{JobID}/performance | This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time
[**GetJobStatus**](ProcessApi.md#GetJobStatus) | **Get** /proc/job/{JobID}/status | Gets Job Status
[**GetJobWorkRequests**](ProcessApi.md#GetJobWorkRequests) | **Get** /proc/job/{JobID}/workrequests | This provides a list of workrequests of a job
[**GetJobs**](ProcessApi.md#GetJobs) | **Get** /proc/jobs | This gets a list of jobs
[**GetJobsOrganizationStats**](ProcessApi.md#GetJobsOrganizationStats) | **Get** /proc/jobs/stats/organization | This gets processing stats of the jobs by organization
[**GetJobsPerformance**](ProcessApi.md#GetJobsPerformance) | **Get** /proc/jobs/performance | This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time
[**GetJobsStats**](ProcessApi.md#GetJobsStats) | **Get** /proc/jobs/stats | This gets processing stats of the jobs
[**GetJobsTimeRangesStats**](ProcessApi.md#GetJobsTimeRangesStats) | **Get** /proc/jobs/stats/time_ranges | This gets processing stats of the jobs grouped by time ranges and sorted by a range start time
[**GetRatePendingScheduledJobs**](ProcessApi.md#GetRatePendingScheduledJobs) | **Get** /proc/scheduled_jobs/rate_pending_time_ranges | This gets the rate of pending scheduled jobs by time ranges
[**GetScheduledJobDetail**](ProcessApi.md#GetScheduledJobDetail) | **Get** /proc/scheduled_job/{ScheduledJobID}/detail | This gets scheduled job detail
[**GetScheduledJobs**](ProcessApi.md#GetScheduledJobs) | **Get** /proc/scheduled_jobs | This gets a list of scheduled jobs
[**GetServerErrorCounts**](ProcessApi.md#GetServerErrorCounts) | **Get** /proc/tasks/error/server_error_counts | Get server error counts in a time-range
[**GetTaskDetail**](ProcessApi.md#GetTaskDetail) | **Get** /proc/task/{TaskID}/detail | Gets Task Detail
[**GetTaskDownload**](ProcessApi.md#GetTaskDownload) | **Get** /proc/task/{TaskID}/download/{TaskOutputName} | Returns the contents of the task&#39;s output
[**GetTaskLogs**](ProcessApi.md#GetTaskLogs) | **Get** /proc/task/{TaskID}/logs | Gets logs associated with a task
[**GetTaskOutput**](ProcessApi.md#GetTaskOutput) | **Get** /proc/task/{TaskID}/output/{TaskOutputName} | Returns the contents of the task&#39;s output
[**GetTaskOutputs**](ProcessApi.md#GetTaskOutputs) | **Get** /proc/task/{TaskID}/outputs | Gets Task Output
[**GetTaskSyncBacklog**](ProcessApi.md#GetTaskSyncBacklog) | **Get** /proc/tasks/sync_backlog | Gets task sync backlog in a time-range
[**GetTasks**](ProcessApi.md#GetTasks) | **Get** /proc/tasks | This gets a list of tasks based on the provided criteria
[**GetTasksErrorTypeCountByEngine**](ProcessApi.md#GetTasksErrorTypeCountByEngine) | **Get** /proc/tasks/error/count_type_by_engine | This gets error type count by engines
[**GetTasksErrors**](ProcessApi.md#GetTasksErrors) | **Get** /proc/tasks/errors | This provides a error list in a time range
[**GetTasksInstances**](ProcessApi.md#GetTasksInstances) | **Get** /proc/tasks/instances/by_category_host | This gets processing stats of the tasks
[**GetTasksStats**](ProcessApi.md#GetTasksStats) | **Get** /proc/tasks/stats | This gets processing stats of the tasks
[**GetTasksStatsCategories**](ProcessApi.md#GetTasksStatsCategories) | **Get** /proc/tasks/stats/categories | This gets processing stats of the tasks grouped by engine categories
[**GetTasksStatsEngines**](ProcessApi.md#GetTasksStatsEngines) | **Get** /proc/tasks/stats/engines | This gets processing stats of the tasks grouped by engine
[**GetTasksStatsOrganizations**](ProcessApi.md#GetTasksStatsOrganizations) | **Get** /proc/tasks/stats/organizations | This gets processing stats of the tasks grouped by engine, filter by organizations
[**GetTasksStatsTimeRanges**](ProcessApi.md#GetTasksStatsTimeRanges) | **Get** /proc/tasks/stats/time_ranges | This gets processing stats of the tasks grouped by time ranges and sorted by a range start time
[**GetTotalPendingScheduledJobs**](ProcessApi.md#GetTotalPendingScheduledJobs) | **Get** /proc/scheduled_jobs/total_pending_time_ranges | This gets the total pending scheduled jobs by time ranges
[**GetWorkRequest**](ProcessApi.md#GetWorkRequest) | **Get** /proc/workrequest/{WorkRequestID}/detail | This provides detail of workrequest
[**LaunchJobTemplate**](ProcessApi.md#LaunchJobTemplate) | **Post** /proc/template/{TemplateID}/launch | This launch a job based on the given job template
[**PushContentToEndpoint**](ProcessApi.md#PushContentToEndpoint) | **Post** /proc/endpoint/{Endpoint} | Whatever is posted to this endpoint will be added to the child input folder(s) for the task_routes that have this endpoint.  If more than one task_routes have this endpoint, it will be added to all child input folders.
[**RecheckJobStatus**](ProcessApi.md#RecheckJobStatus) | **Get** /proc/job/{JobID}/recheck_status | Recheck Job Status
[**TasksStatusExport**](ProcessApi.md#TasksStatusExport) | **Get** /proc/tasks/stats/export | Export a task status report as a excel file
[**UpdateTaskStatus**](ProcessApi.md#UpdateTaskStatus) | **Post** /proc/tasks/update_status | This updates the status for a bulk of tasks by taskID



## AddTask

> AddTaskResponse AddTask(ctx, jobID, addTaskRequest, optional)

Adds a Task to a current job

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**jobID** | [**string**](.md)| ID of Job | 
**addTaskRequest** | [**AddTaskRequest**](AddTaskRequest.md)| Create Job API | 
 **optional** | ***AddTaskOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a AddTaskOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AddTaskResponse**](AddTaskResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## AddTaskRoute

> AddTaskRouteResponse AddTaskRoute(ctx, jobID, addTaskRouteRequest, optional)

Adds a Task Route to a current job

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**jobID** | [**string**](.md)| ID of Job | 
**addTaskRouteRequest** | [**AddTaskRouteRequest**](AddTaskRouteRequest.md)| Adds a Task Route | 
 **optional** | ***AddTaskRouteOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a AddTaskRouteOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AddTaskRouteResponse**](AddTaskRouteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateJob

> CreateJobResponse CreateJob(ctx, createJobRequest, optional)

This creates a new Job

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**createJobRequest** | [**CreateJobRequest**](CreateJobRequest.md)| Create Job API | 
 **optional** | ***CreateJobOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateJobOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**CreateJobResponse**](CreateJobResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteJob

> AdminOperationResponse DeleteJob(ctx, jobID, optional)

This API deletes the specified job

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**jobID** | [**string**](.md)| ID of Job | 
 **optional** | ***DeleteJobOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteJobOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **deleteJobRequest** | [**optional.Interface of DeleteJobRequest**](DeleteJobRequest.md)| Request information to delete the specified job | 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteTask

> AdminOperationResponse DeleteTask(ctx, taskID, optional)

This API deletes the specified task

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**taskID** | [**string**](.md)| ID of Task | 
 **optional** | ***DeleteTaskOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteTaskOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineErrorTimeRanges

> GetEngineErrorTimeRangesResponse GetEngineErrorTimeRanges(ctx, optional)

This gets engine error count by error tasks grouped by time ranges and sorted by a range start time

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetEngineErrorTimeRangesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineErrorTimeRangesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **chartType** | [**optional.Interface of EngineErrorChartTypeEnum**](.md)| It will help API to kmow the response should return | 
 **interval** | **optional.Int64**| Interval in seconds for output time ranges | 
 **engineID** | [**optional.Interface of string**](.md)| Filtering by engineID | 

### Return type

[**GetEngineErrorTimeRangesResponse**](GetEngineErrorTimeRangesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobDetail

> GetJobDetailResponse GetJobDetail(ctx, jobID, optional)

Gets Job Detail

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**jobID** | [**string**](.md)| ID of Job | 
 **optional** | ***GetJobDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetJobDetailResponse**](GetJobDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobDownload

> []string GetJobDownload(ctx, jobID, jobOutputName, optional)

Returns the contents of the job's output

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**jobID** | [**string**](.md)| ID of Job | 
**jobOutputName** | **string**| Name of the job output, e.g. vtn-standard.json | 
 **optional** | ***GetJobDownloadOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobDownloadOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

**[]string**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobOutput

> GetJobOutputResponse GetJobOutput(ctx, jobID, jobOutputName, optional)

Returns the contents of the job's output

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**jobID** | [**string**](.md)| ID of Job | 
**jobOutputName** | **string**| Name of the job output, e.g. vtn-standard.json | 
 **optional** | ***GetJobOutputOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobOutputOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetJobOutputResponse**](GetJobOutputResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobOutputs

> GetJobOutputsResponse GetJobOutputs(ctx, jobID, optional)

Returns a list of output information about this job

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**jobID** | [**string**](.md)| ID of Job | 
 **optional** | ***GetJobOutputsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobOutputsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetJobOutputsResponse**](GetJobOutputsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobPerformance

> GetJobPerformanceResponse GetJobPerformance(ctx, jobID, optional)

This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**jobID** | [**string**](.md)| ID of Job | 
 **optional** | ***GetJobPerformanceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobPerformanceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **interval** | **optional.Int64**| Interval in seconds for output time ranges | 
 **taskID** | [**optional.Interface of string**](.md)| Filter data by taskID | 
 **workRequestID** | [**optional.Interface of string**](.md)| Filter data by workRequestID | 

### Return type

[**GetJobPerformanceResponse**](GetJobPerformanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobStatus

> GetJobStatusResponse GetJobStatus(ctx, jobID, optional)

Gets Job Status

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**jobID** | [**string**](.md)| ID of Job | 
 **optional** | ***GetJobStatusOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobStatusOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetJobStatusResponse**](GetJobStatusResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobWorkRequests

> GetJobWorkRequestResponse GetJobWorkRequests(ctx, jobID, optional)

This provides a list of workrequests of a job

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**jobID** | [**string**](.md)| ID of Job | 
 **optional** | ***GetJobWorkRequestsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobWorkRequestsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **offset** | **optional.Int32**| the number of records to skip before getting the result set | 
 **limit** | **optional.Int32**| the number of records to return. | [default to 100]
 **orderBy** | **optional.String**| the field to sort. It should be in [createdDateTime, modifiedDateTime] | [default to createdDateTime]
 **direction** | **optional.String**| the sort order | [default to DESC]
 **status** | **optional.String**| the value should be in [active, trial, inactive, deleted] | 
 **taskID** | **optional.String**| This is an internal task ID to get work request | 

### Return type

[**GetJobWorkRequestResponse**](GetJobWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobs

> GetJobListResponse GetJobs(ctx, optional)

This gets a list of jobs

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetJobsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **status** | [**optional.Interface of JobStatusEnum**](.md)| If specified, this limits the jobs or tasks to follow status | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **orderBy** | **optional.String**| the field to sort | [default to createdDateTime]
 **direction** | **optional.String**| the sort order.  ASC or DESC. | [default to DESC]
 **coreID** | [**optional.Interface of string**](.md)| Filter by coreID | 
 **organizationID** | [**optional.Interface of string**](.md)| Filter by organizationID | 
 **recordingID** | [**optional.Interface of string**](.md)| Filter by recordingID | 
 **jobID** | [**optional.Interface of string**](.md)| Filter by jobID | 
 **coreJobID** | **optional.String**| Filter by coreJobID | 
 **modifiedBefore** | **optional.Int64**| Filter by items modified before expressed as timestamp | 
 **modifiedAfter** | **optional.Int64**| Filter by items modified after expressed as timestamp | 
 **createdBefore** | **optional.Int64**| Filter items where created date is before this date | 
 **createdAfter** | **optional.Int64**| Filter items where created date is after this date | 

### Return type

[**GetJobListResponse**](GetJobListResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobsOrganizationStats

> GetJobsOrganizationStatsResponse GetJobsOrganizationStats(ctx, optional)

This gets processing stats of the jobs by organization

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetJobsOrganizationStatsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobsOrganizationStatsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **organizationIDs** | **optional.String**|  | 

### Return type

[**GetJobsOrganizationStatsResponse**](GetJobsOrganizationStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobsPerformance

> GetJobsPerformanceResponse GetJobsPerformance(ctx, optional)

This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetJobsPerformanceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobsPerformanceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **interval** | **optional.Int64**| Interval in seconds for output time ranges | 

### Return type

[**GetJobsPerformanceResponse**](GetJobsPerformanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobsStats

> GetJobsStatsResponse GetJobsStats(ctx, optional)

This gets processing stats of the jobs

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetJobsStatsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobsStatsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **chartType** | [**optional.Interface of JobTaskStatusChartTypeEnum**](.md)| It will help API to kmow the response should return | 
 **status** | [**optional.Interface of JobStatusEnum**](.md)| If specified, this limits the jobs or tasks to follow status | 
 **organizationIDs** | **optional.String**|  | 

### Return type

[**GetJobsStatsResponse**](GetJobsStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobsTimeRangesStats

> GetJobsTimeRangesStatsResponse GetJobsTimeRangesStats(ctx, optional)

This gets processing stats of the jobs grouped by time ranges and sorted by a range start time

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetJobsTimeRangesStatsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobsTimeRangesStatsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **status** | [**optional.Interface of JobStatusEnum**](.md)| If specified, this limits the jobs or tasks to follow status | 
 **interval** | **optional.Int64**| Interval in seconds for output time ranges | 
 **organizationIDs** | **optional.String**|  | 
 **engineCategoryID** | [**optional.Interface of string**](.md)|  | 

### Return type

[**GetJobsTimeRangesStatsResponse**](GetJobsTimeRangesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetRatePendingScheduledJobs

> GetRatePendingScheduledJobsResponse GetRatePendingScheduledJobs(ctx, optional)

This gets the rate of pending scheduled jobs by time ranges

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetRatePendingScheduledJobsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetRatePendingScheduledJobsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **interval** | **optional.Int64**| Interval in seconds for output time ranges | 

### Return type

[**GetRatePendingScheduledJobsResponse**](GetRatePendingScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetScheduledJobDetail

> GetScheduledJobDetailResponse GetScheduledJobDetail(ctx, scheduledJobID, optional)

This gets scheduled job detail

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**scheduledJobID** | [**string**](.md)| ID of Scheduled Job. It can be an internal ID or core ID | 
 **optional** | ***GetScheduledJobDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetScheduledJobDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetScheduledJobDetailResponse**](GetScheduledJobDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetScheduledJobs

> GetScheduledJobsResponse GetScheduledJobs(ctx, optional)

This gets a list of scheduled jobs

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetScheduledJobsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetScheduledJobsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **direction** | **optional.String**| the sort order.  ASC or DESC. | [default to DESC]
 **scheduledJobID** | **optional.String**| Filter by internal scheduled Job ID(uuid) or core scheduled Job ID (integer) | 
 **internalOrganizationID** | [**optional.Interface of string**](.md)| Filter by internal organization id | 
 **coreID** | [**optional.Interface of string**](.md)| Filter by coreID | 
 **startStartTime** | **optional.Int64**|  | 
 **endStartTime** | **optional.Int64**|  | 
 **startStopTime** | **optional.Int64**|  | 
 **endStopTime** | **optional.Int64**|  | 
 **isActive** | **optional.Bool**|  | 
 **runMode** | [**optional.Interface of ScheduleRunModeEnum**](.md)| Filter by runMode | 
 **sourceID** | **optional.Int32**|  | 
 **sourceType** | **optional.String**|  | 
 **orderBy** | **optional.String**| The value should be in [organizationID, runMode, createdTime, startTime, stopTime] | 
 **scheduledJobName** | **optional.String**|  | 

### Return type

[**GetScheduledJobsResponse**](GetScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetServerErrorCounts

> GetServerErrorCountsResponse GetServerErrorCounts(ctx, optional)

Get server error counts in a time-range

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetServerErrorCountsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetServerErrorCountsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **chartType** | [**optional.Interface of ServerErrorChartTypeEnum**](.md)| It will help API to kmow the response should return | 
 **service** | **optional.String**| Filter data by service name. | 
 **interval** | **optional.Int64**| Interval in seconds for output time ranges | 

### Return type

[**GetServerErrorCountsResponse**](GetServerErrorCountsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTaskDetail

> GetTaskDetailResponse GetTaskDetail(ctx, taskID, optional)

Gets Task Detail

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**taskID** | [**string**](.md)| ID of Task | 
 **optional** | ***GetTaskDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTaskDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetTaskDetailResponse**](GetTaskDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTaskDownload

> []byte GetTaskDownload(ctx, taskID, taskOutputName, optional)

Returns the contents of the task's output

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**taskID** | [**string**](.md)| ID of Task | 
**taskOutputName** | **string**| Name of the task output, e.g. vtn-standard.json | 
 **optional** | ***GetTaskDownloadOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTaskDownloadOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

**[]byte**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTaskLogs

> *os.File GetTaskLogs(ctx, taskID, optional)

Gets logs associated with a task

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**taskID** | [**string**](.md)| ID of Task | 
 **optional** | ***GetTaskLogsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTaskLogsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[***os.File**](*os.File.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/zip, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTaskOutput

> GetTaskOutputResponse GetTaskOutput(ctx, taskID, taskOutputName, optional)

Returns the contents of the task's output

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**taskID** | [**string**](.md)| ID of Task | 
**taskOutputName** | **string**| Name of the task output, e.g. vtn-standard.json | 
 **optional** | ***GetTaskOutputOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTaskOutputOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetTaskOutputResponse**](GetTaskOutputResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTaskOutputs

> GetTaskOutputsResponse GetTaskOutputs(ctx, taskID, optional)

Gets Task Output

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**taskID** | [**string**](.md)| ID of Task | 
 **optional** | ***GetTaskOutputsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTaskOutputsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetTaskOutputsResponse**](GetTaskOutputsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTaskSyncBacklog

> GetTaskSyncBacklogResponse GetTaskSyncBacklog(ctx, optional)

Gets task sync backlog in a time-range

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetTaskSyncBacklogOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTaskSyncBacklogOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **interval** | **optional.Int64**| Interval in seconds for output time ranges | 

### Return type

[**GetTaskSyncBacklogResponse**](GetTaskSyncBacklogResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTasks

> GetTasksResponse GetTasks(ctx, optional)

This gets a list of tasks based on the provided criteria

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetTasksOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTasksOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **orderBy** | **optional.String**| the field to sort | [default to createdDateTime]
 **direction** | **optional.String**| the sort order.  ASC or DESC. | [default to DESC]
 **status** | [**optional.Interface of TaskStatusEnum**](.md)| Filtering by task Status | 
 **organizationID** | **optional.String**| Filter by organization id | 
 **taskID** | **optional.String**| Filter by task id | 
 **coreTaskID** | **optional.String**| Filter by coreTaskID | 
 **errorType** | [**optional.Interface of FailureReasonEnum**](.md)| filter by errorType (failureReason) | 
 **jobID** | **optional.String**| Filter by job id | 
 **coreJobID** | **optional.String**| Filter by coreJobID | 
 **engineID** | **optional.String**| Filter by engine id | 
 **mediaSourceID** | **optional.String**| Filter by media source id | 
 **recordingID** | **optional.Int64**| Filter tasks by the recording id | 
 **engineCategoryID** | [**optional.Interface of string**](.md)| Filtering by engineCategoryID | 
 **modifiedBefore** | **optional.Int64**| Filter by items modified before expressed as timestamp | 
 **modifiedAfter** | **optional.Int64**| Filter by items modified after expressed as timestamp | 
 **createdBefore** | **optional.Int64**| Filter items where created date is before this date | 
 **createdAfter** | **optional.Int64**| Filter items where created date is after this date | 
 **backlog** | **optional.Bool**| Filtering all tasks in backlog | 
 **alloc** | **optional.Bool**| Filtering all tasks have alloc &#x3D; true or not | 

### Return type

[**GetTasksResponse**](GetTasksResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTasksErrorTypeCountByEngine

> GetTasksErrorTypeCountByEngineResponse GetTasksErrorTypeCountByEngine(ctx, optional)

This gets error type count by engines

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetTasksErrorTypeCountByEngineOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTasksErrorTypeCountByEngineOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **engineID** | **optional.String**| Filter by engine id | 
 **status** | [**optional.Interface of TaskStatusEnum**](.md)| Filtering by task Status | 
 **errorType** | [**optional.Interface of FailureReasonEnum**](.md)| filter by errorType (failureReason) | 

### Return type

[**GetTasksErrorTypeCountByEngineResponse**](GetTasksErrorTypeCountByEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTasksErrors

> GetTaskErrorsResponse GetTasksErrors(ctx, optional)

This provides a error list in a time range

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetTasksErrorsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTasksErrorsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **taskID** | [**optional.Interface of string**](.md)| filter by taskID | 
 **jobID** | [**optional.Interface of string**](.md)| filter by jobID | 
 **errorType** | [**optional.Interface of FailureReasonEnum**](.md)| filter by errorType (failureReason) | 
 **offset** | **optional.Int32**| the number of records to skip before getting the result set | 
 **limit** | **optional.Int32**| the number of records to return. | [default to 100]
 **orderBy** | **optional.String**| the field to sort. It should be in [createdDateTime, modifiedDateTime] | [default to createdDateTime]
 **direction** | **optional.String**| the sort order | [default to DESC]

### Return type

[**GetTaskErrorsResponse**](GetTaskErrorsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTasksInstances

> GetTasksInstancesResponse GetTasksInstances(ctx, optional)

This gets processing stats of the tasks

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetTasksInstancesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTasksInstancesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **status** | [**optional.Interface of EngineStatusEnum**](.md)| If specified, this limits the engine instances to follow status | 
 **engineCategoryID** | [**optional.Interface of string**](.md)|  | 

### Return type

[**GetTasksInstancesResponse**](GetTasksInstancesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTasksStats

> GetTasksStatsResponse GetTasksStats(ctx, optional)

This gets processing stats of the tasks

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetTasksStatsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTasksStatsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **chartType** | [**optional.Interface of JobTaskStatusChartTypeEnum**](.md)| It will help API to kmow the response should return | 
 **status** | [**optional.Interface of TaskStatusEnum**](.md)| Filtering by task Status | 
 **organizationIDs** | [**optional.Interface of string**](.md)|  | 
 **engineIDs** | [**optional.Interface of string**](.md)|  | 

### Return type

[**GetTasksStatsResponse**](GetTasksStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTasksStatsCategories

> GetTasksCategoriesStatsResponse GetTasksStatsCategories(ctx, optional)

This gets processing stats of the tasks grouped by engine categories

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetTasksStatsCategoriesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTasksStatsCategoriesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **status** | [**optional.Interface of TaskStatusEnum**](.md)| Filtering by task Status | 
 **organizationIDs** | [**optional.Interface of string**](.md)|  | 
 **engineCategoryID** | [**optional.Interface of string**](.md)|  | 

### Return type

[**GetTasksCategoriesStatsResponse**](GetTasksCategoriesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTasksStatsEngines

> GetTasksEnginesStatsResponse GetTasksStatsEngines(ctx, optional)

This gets processing stats of the tasks grouped by engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetTasksStatsEnginesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTasksStatsEnginesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **status** | [**optional.Interface of TaskStatusEnum**](.md)| Filtering by task Status | 
 **organizationID** | **optional.String**| Filter by  organization id | 
 **taskID** | **optional.String**| Filter by task id | 
 **errorType** | [**optional.Interface of FailureReasonEnum**](.md)| filter by errorType (failureReason) | 
 **jobID** | **optional.String**| Filter by job id | 
 **engineID** | **optional.String**| Filter by engine id | 
 **mediaSourceID** | **optional.String**| Filter by media source id | 
 **recordingID** | **optional.Int64**| Filter tasks by the recording id | 
 **engineCategoryID** | [**optional.Interface of string**](.md)| Filtering by engineCategoryID | 

### Return type

[**GetTasksEnginesStatsResponse**](GetTasksEnginesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTasksStatsOrganizations

> GetTasksStatsOrganizationsResponse GetTasksStatsOrganizations(ctx, optional)

This gets processing stats of the tasks grouped by engine, filter by organizations

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetTasksStatsOrganizationsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTasksStatsOrganizationsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **status** | [**optional.Interface of TaskStatusEnum**](.md)| Filtering by task Status | 
 **organizationIDs** | [**optional.Interface of string**](.md)| Filter by organization IDs | 
 **engineID** | [**optional.Interface of string**](.md)| Filter by engine ID | 

### Return type

[**GetTasksStatsOrganizationsResponse**](GetTasksStatsOrganizationsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTasksStatsTimeRanges

> GetTasksTimeRangesStatsResponse GetTasksStatsTimeRanges(ctx, optional)

This gets processing stats of the tasks grouped by time ranges and sorted by a range start time

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetTasksStatsTimeRangesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTasksStatsTimeRangesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **status** | [**optional.Interface of TaskStatusEnum**](.md)| Filtering by task Status | 
 **interval** | **optional.Int64**| Interval in seconds for output time ranges | 
 **engineCategoryID** | [**optional.Interface of string**](.md)| Filtering by engineCategoryID | 
 **organizationIDs** | **optional.String**|  | 

### Return type

[**GetTasksTimeRangesStatsResponse**](GetTasksTimeRangesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTotalPendingScheduledJobs

> GetTotalPendingScheduledJobsResponse GetTotalPendingScheduledJobs(ctx, optional)

This gets the total pending scheduled jobs by time ranges

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetTotalPendingScheduledJobsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetTotalPendingScheduledJobsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **interval** | **optional.Int64**| Interval in seconds for output time ranges | 

### Return type

[**GetTotalPendingScheduledJobsResponse**](GetTotalPendingScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetWorkRequest

> GetTaskWorkRequestResponse GetWorkRequest(ctx, workRequestID, optional)

This provides detail of workrequest

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**workRequestID** | [**string**](.md)| ID of Work request | 
 **optional** | ***GetWorkRequestOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetWorkRequestOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetTaskWorkRequestResponse**](GetTaskWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## LaunchJobTemplate

> LaunchJobTemplateResponse LaunchJobTemplate(ctx, templateID, launchJobTemplateRequest, optional)

This launch a job based on the given job template

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**templateID** | **string**| ID of Job | 
**launchJobTemplateRequest** | [**LaunchJobTemplateRequest**](LaunchJobTemplateRequest.md)| Launch Job Template API | 
 **optional** | ***LaunchJobTemplateOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a LaunchJobTemplateOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**LaunchJobTemplateResponse**](LaunchJobTemplateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PushContentToEndpoint

> CreateJobResponse PushContentToEndpoint(ctx, endpoint, body, optional)

Whatever is posted to this endpoint will be added to the child input folder(s) for the task_routes that have this endpoint.  If more than one task_routes have this endpoint, it will be added to all child input folders.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**endpoint** | [**string**](.md)| Endpoint UUID to push this chunk towards | 
**body** | **string**| How to push content into a child input folder(s). | 
 **optional** | ***PushContentToEndpointOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a PushContentToEndpointOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**CreateJobResponse**](CreateJobResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json, application/octet-stream, audio/_*, image/_*, text/html, text/plain, text/xml, video/_*
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RecheckJobStatus

> RecheckJobStatusResponse RecheckJobStatus(ctx, jobID, optional)

Recheck Job Status

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**jobID** | [**string**](.md)| ID of Job | 
 **optional** | ***RecheckJobStatusOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a RecheckJobStatusOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**RecheckJobStatusResponse**](RecheckJobStatusResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## TasksStatusExport

> *os.File TasksStatusExport(ctx, optional)

Export a task status report as a excel file

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***TasksStatusExportOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a TasksStatusExportOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **orderBy** | **optional.String**| the field to sort | [default to createdDateTime]
 **direction** | **optional.String**| the sort order.  ASC or DESC. | [default to DESC]
 **status** | [**optional.Interface of TaskStatusEnum**](.md)| Filtering by task Status | 
 **organizationID** | **optional.String**| Filter by organization id | 
 **taskID** | **optional.String**| Filter by task id | 
 **coreTaskID** | **optional.String**| Filter by coreTaskID | 
 **errorType** | [**optional.Interface of FailureReasonEnum**](.md)| filter by errorType (failureReason) | 
 **jobID** | **optional.String**| Filter by job id | 
 **coreJobID** | **optional.String**| Filter by coreJobID | 
 **engineID** | **optional.String**| Filter by engine id | 
 **mediaSourceID** | **optional.String**| Filter by media source id | 
 **recordingID** | **optional.Int64**| Filter tasks by the recording id | 
 **engineCategoryID** | [**optional.Interface of string**](.md)| Filtering by engineCategoryID | 
 **modifiedBefore** | **optional.Int64**| Filter by items modified before expressed as timestamp | 
 **modifiedAfter** | **optional.Int64**| Filter by items modified after expressed as timestamp | 
 **createdBefore** | **optional.Int64**| Filter items where created date is before this date | 
 **createdAfter** | **optional.Int64**| Filter items where created date is after this date | 
 **backlog** | **optional.Bool**| Filtering all tasks in backlog | 
 **alloc** | **optional.Bool**| Filtering all tasks have alloc &#x3D; true or not | 

### Return type

[***os.File**](*os.File.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateTaskStatus

> TasksStatusUpdateResponse UpdateTaskStatus(ctx, tasksStatusUpdateRequest, optional)

This updates the status for a bulk of tasks by taskID

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**tasksStatusUpdateRequest** | [**TasksStatusUpdateRequest**](TasksStatusUpdateRequest.md)| The input for updateTaskStatus | 
 **optional** | ***UpdateTaskStatusOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateTaskStatusOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**TasksStatusUpdateResponse**](TasksStatusUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

