# AiwareJsClient.ProcessApi

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



## addTask

> AddTaskResponse addTask(jobID, addTaskRequest, opts)

Adds a Task to a current job

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let jobID = null; // String | ID of Job
let addTaskRequest = new AiwareJsClient.AddTaskRequest(); // AddTaskRequest | Create Job API
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.addTask(jobID, addTaskRequest, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**String**](.md)| ID of Job | 
 **addTaskRequest** | [**AddTaskRequest**](AddTaskRequest.md)| Create Job API | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AddTaskResponse**](AddTaskResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## addTaskRoute

> AddTaskRouteResponse addTaskRoute(jobID, addTaskRouteRequest, opts)

Adds a Task Route to a current job

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let jobID = null; // String | ID of Job
let addTaskRouteRequest = new AiwareJsClient.AddTaskRouteRequest(); // AddTaskRouteRequest | Adds a Task Route
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.addTaskRoute(jobID, addTaskRouteRequest, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**String**](.md)| ID of Job | 
 **addTaskRouteRequest** | [**AddTaskRouteRequest**](AddTaskRouteRequest.md)| Adds a Task Route | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AddTaskRouteResponse**](AddTaskRouteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createJob

> CreateJobResponse createJob(createJobRequest, opts)

This creates a new Job

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let createJobRequest = new AiwareJsClient.CreateJobRequest(); // CreateJobRequest | Create Job API
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createJob(createJobRequest, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createJobRequest** | [**CreateJobRequest**](CreateJobRequest.md)| Create Job API | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateJobResponse**](CreateJobResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## deleteJob

> AdminOperationResponse deleteJob(jobID, opts)

This API deletes the specified job

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let jobID = null; // String | ID of Job
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'deleteJobRequest': new AiwareJsClient.DeleteJobRequest() // DeleteJobRequest | Request information to delete the specified job
};
apiInstance.deleteJob(jobID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**String**](.md)| ID of Job | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **deleteJobRequest** | [**DeleteJobRequest**](DeleteJobRequest.md)| Request information to delete the specified job | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## deleteTask

> AdminOperationResponse deleteTask(taskID, opts)

This API deletes the specified task

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let taskID = null; // String | ID of Task
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.deleteTask(taskID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**String**](.md)| ID of Task | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineErrorTimeRanges

> GetEngineErrorTimeRangesResponse getEngineErrorTimeRanges(opts)

This gets engine error count by error tasks grouped by time ranges and sorted by a range start time

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'chartType': new AiwareJsClient.EngineErrorChartTypeEnum(), // EngineErrorChartTypeEnum | It will help API to kmow the response should return
  'interval': 789, // Number | Interval in seconds for output time ranges
  'engineID': null // String | Filtering by engineID
};
apiInstance.getEngineErrorTimeRanges(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **chartType** | [**EngineErrorChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] 
 **interval** | **Number**| Interval in seconds for output time ranges | [optional] 
 **engineID** | [**String**](.md)| Filtering by engineID | [optional] 

### Return type

[**GetEngineErrorTimeRangesResponse**](GetEngineErrorTimeRangesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobDetail

> GetJobDetailResponse getJobDetail(jobID, opts)

Gets Job Detail

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let jobID = null; // String | ID of Job
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getJobDetail(jobID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**String**](.md)| ID of Job | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetJobDetailResponse**](GetJobDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobDownload

> [Blob] getJobDownload(jobID, jobOutputName, opts)

Returns the contents of the job&#39;s output

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let jobID = null; // String | ID of Job
let jobOutputName = "jobOutputName_example"; // String | Name of the job output, e.g. vtn-standard.json
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getJobDownload(jobID, jobOutputName, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**String**](.md)| ID of Job | 
 **jobOutputName** | **String**| Name of the job output, e.g. vtn-standard.json | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

**[Blob]**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobOutput

> GetJobOutputResponse getJobOutput(jobID, jobOutputName, opts)

Returns the contents of the job&#39;s output

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let jobID = null; // String | ID of Job
let jobOutputName = "jobOutputName_example"; // String | Name of the job output, e.g. vtn-standard.json
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getJobOutput(jobID, jobOutputName, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**String**](.md)| ID of Job | 
 **jobOutputName** | **String**| Name of the job output, e.g. vtn-standard.json | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetJobOutputResponse**](GetJobOutputResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobOutputs

> GetJobOutputsResponse getJobOutputs(jobID, opts)

Returns a list of output information about this job

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let jobID = null; // String | ID of Job
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getJobOutputs(jobID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**String**](.md)| ID of Job | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetJobOutputsResponse**](GetJobOutputsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobPerformance

> GetJobPerformanceResponse getJobPerformance(jobID, opts)

This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let jobID = null; // String | ID of Job
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'interval': 789, // Number | Interval in seconds for output time ranges
  'taskID': null, // String | Filter data by taskID
  'workRequestID': null // String | Filter data by workRequestID
};
apiInstance.getJobPerformance(jobID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**String**](.md)| ID of Job | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **interval** | **Number**| Interval in seconds for output time ranges | [optional] 
 **taskID** | [**String**](.md)| Filter data by taskID | [optional] 
 **workRequestID** | [**String**](.md)| Filter data by workRequestID | [optional] 

### Return type

[**GetJobPerformanceResponse**](GetJobPerformanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobStatus

> GetJobStatusResponse getJobStatus(jobID, opts)

Gets Job Status

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let jobID = null; // String | ID of Job
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getJobStatus(jobID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**String**](.md)| ID of Job | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetJobStatusResponse**](GetJobStatusResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobWorkRequests

> GetJobWorkRequestResponse getJobWorkRequests(jobID, opts)

This provides a list of workrequests of a job

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let jobID = null; // String | ID of Job
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'offset': 56, // Number | the number of records to skip before getting the result set
  'limit': 100, // Number | the number of records to return.
  'orderBy': "'createdDateTime'", // String | the field to sort. It should be in [createdDateTime, modifiedDateTime]
  'direction': "'DESC'", // String | the sort order
  'status': "status_example", // String | the value should be in [active, trial, inactive, deleted]
  'taskID': "taskID_example" // String | This is an internal task ID to get work request
};
apiInstance.getJobWorkRequests(jobID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**String**](.md)| ID of Job | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **offset** | **Number**| the number of records to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of records to return. | [optional] [default to 100]
 **orderBy** | **String**| the field to sort. It should be in [createdDateTime, modifiedDateTime] | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **String**| the sort order | [optional] [default to &#39;DESC&#39;]
 **status** | **String**| the value should be in [active, trial, inactive, deleted] | [optional] 
 **taskID** | **String**| This is an internal task ID to get work request | [optional] 

### Return type

[**GetJobWorkRequestResponse**](GetJobWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobs

> GetJobListResponse getJobs(opts)

This gets a list of jobs

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'status': new AiwareJsClient.JobStatusEnum(), // JobStatusEnum | If specified, this limits the jobs or tasks to follow status
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'orderBy': "'createdDateTime'", // String | the field to sort
  'direction': "'DESC'", // String | the sort order.  ASC or DESC.
  'coreID': null, // String | Filter by coreID
  'organizationID': null, // String | Filter by organizationID
  'recordingID': null, // String | Filter by recordingID
  'jobID': null, // String | Filter by jobID
  'coreJobID': "coreJobID_example", // String | Filter by coreJobID
  'modifiedBefore': 789, // Number | Filter by items modified before expressed as timestamp
  'modifiedAfter': 789, // Number | Filter by items modified after expressed as timestamp
  'createdBefore': 789, // Number | Filter items where created date is before this date
  'createdAfter': 789 // Number | Filter items where created date is after this date
};
apiInstance.getJobs(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**JobStatusEnum**](.md)| If specified, this limits the jobs or tasks to follow status | [optional] 
 **offset** | **Number**| the number of data to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of items to return. | [optional] [default to 10]
 **orderBy** | **String**| the field to sort | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **coreID** | [**String**](.md)| Filter by coreID | [optional] 
 **organizationID** | [**String**](.md)| Filter by organizationID | [optional] 
 **recordingID** | [**String**](.md)| Filter by recordingID | [optional] 
 **jobID** | [**String**](.md)| Filter by jobID | [optional] 
 **coreJobID** | **String**| Filter by coreJobID | [optional] 
 **modifiedBefore** | **Number**| Filter by items modified before expressed as timestamp | [optional] 
 **modifiedAfter** | **Number**| Filter by items modified after expressed as timestamp | [optional] 
 **createdBefore** | **Number**| Filter items where created date is before this date | [optional] 
 **createdAfter** | **Number**| Filter items where created date is after this date | [optional] 

### Return type

[**GetJobListResponse**](GetJobListResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobsOrganizationStats

> GetJobsOrganizationStatsResponse getJobsOrganizationStats(opts)

This gets processing stats of the jobs by organization

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'organizationIDs': "organizationIDs_example" // String | 
};
apiInstance.getJobsOrganizationStats(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **organizationIDs** | **String**|  | [optional] 

### Return type

[**GetJobsOrganizationStatsResponse**](GetJobsOrganizationStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobsPerformance

> GetJobsPerformanceResponse getJobsPerformance(opts)

This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'interval': 789 // Number | Interval in seconds for output time ranges
};
apiInstance.getJobsPerformance(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **interval** | **Number**| Interval in seconds for output time ranges | [optional] 

### Return type

[**GetJobsPerformanceResponse**](GetJobsPerformanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobsStats

> GetJobsStatsResponse getJobsStats(opts)

This gets processing stats of the jobs

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'chartType': new AiwareJsClient.JobTaskStatusChartTypeEnum(), // JobTaskStatusChartTypeEnum | It will help API to kmow the response should return
  'status': new AiwareJsClient.JobStatusEnum(), // JobStatusEnum | If specified, this limits the jobs or tasks to follow status
  'organizationIDs': "organizationIDs_example" // String | 
};
apiInstance.getJobsStats(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **chartType** | [**JobTaskStatusChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] 
 **status** | [**JobStatusEnum**](.md)| If specified, this limits the jobs or tasks to follow status | [optional] 
 **organizationIDs** | **String**|  | [optional] 

### Return type

[**GetJobsStatsResponse**](GetJobsStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobsTimeRangesStats

> GetJobsTimeRangesStatsResponse getJobsTimeRangesStats(opts)

This gets processing stats of the jobs grouped by time ranges and sorted by a range start time

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'status': new AiwareJsClient.JobStatusEnum(), // JobStatusEnum | If specified, this limits the jobs or tasks to follow status
  'interval': 789, // Number | Interval in seconds for output time ranges
  'organizationIDs': "organizationIDs_example", // String | 
  'engineCategoryID': null // String | 
};
apiInstance.getJobsTimeRangesStats(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**JobStatusEnum**](.md)| If specified, this limits the jobs or tasks to follow status | [optional] 
 **interval** | **Number**| Interval in seconds for output time ranges | [optional] 
 **organizationIDs** | **String**|  | [optional] 
 **engineCategoryID** | [**String**](.md)|  | [optional] 

### Return type

[**GetJobsTimeRangesStatsResponse**](GetJobsTimeRangesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getRatePendingScheduledJobs

> GetRatePendingScheduledJobsResponse getRatePendingScheduledJobs(opts)

This gets the rate of pending scheduled jobs by time ranges

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'interval': 789 // Number | Interval in seconds for output time ranges
};
apiInstance.getRatePendingScheduledJobs(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **interval** | **Number**| Interval in seconds for output time ranges | [optional] 

### Return type

[**GetRatePendingScheduledJobsResponse**](GetRatePendingScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getScheduledJobDetail

> GetScheduledJobDetailResponse getScheduledJobDetail(scheduledJobID, opts)

This gets scheduled job detail

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let scheduledJobID = null; // String | ID of Scheduled Job. It can be an internal ID or core ID
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getScheduledJobDetail(scheduledJobID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scheduledJobID** | [**String**](.md)| ID of Scheduled Job. It can be an internal ID or core ID | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetScheduledJobDetailResponse**](GetScheduledJobDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getScheduledJobs

> GetScheduledJobsResponse getScheduledJobs(opts)

This gets a list of scheduled jobs

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'direction': "'DESC'", // String | the sort order.  ASC or DESC.
  'scheduledJobID': "scheduledJobID_example", // String | Filter by internal scheduled Job ID(uuid) or core scheduled Job ID (integer)
  'internalOrganizationID': null, // String | Filter by internal organization id
  'coreID': null, // String | Filter by coreID
  'startStartTime': 789, // Number | 
  'endStartTime': 789, // Number | 
  'startStopTime': 789, // Number | 
  'endStopTime': 789, // Number | 
  'isActive': true, // Boolean | 
  'runMode': new AiwareJsClient.ScheduleRunModeEnum(), // ScheduleRunModeEnum | Filter by runMode
  'sourceID': 56, // Number | 
  'sourceType': "sourceType_example", // String | 
  'orderBy': "orderBy_example", // String | The value should be in [organizationID, runMode, createdTime, startTime, stopTime]
  'scheduledJobName': "scheduledJobName_example" // String | 
};
apiInstance.getScheduledJobs(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **offset** | **Number**| the number of data to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of items to return. | [optional] [default to 10]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **scheduledJobID** | **String**| Filter by internal scheduled Job ID(uuid) or core scheduled Job ID (integer) | [optional] 
 **internalOrganizationID** | [**String**](.md)| Filter by internal organization id | [optional] 
 **coreID** | [**String**](.md)| Filter by coreID | [optional] 
 **startStartTime** | **Number**|  | [optional] 
 **endStartTime** | **Number**|  | [optional] 
 **startStopTime** | **Number**|  | [optional] 
 **endStopTime** | **Number**|  | [optional] 
 **isActive** | **Boolean**|  | [optional] 
 **runMode** | [**ScheduleRunModeEnum**](.md)| Filter by runMode | [optional] 
 **sourceID** | **Number**|  | [optional] 
 **sourceType** | **String**|  | [optional] 
 **orderBy** | **String**| The value should be in [organizationID, runMode, createdTime, startTime, stopTime] | [optional] 
 **scheduledJobName** | **String**|  | [optional] 

### Return type

[**GetScheduledJobsResponse**](GetScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getServerErrorCounts

> GetServerErrorCountsResponse getServerErrorCounts(opts)

Get server error counts in a time-range

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'chartType': new AiwareJsClient.ServerErrorChartTypeEnum(), // ServerErrorChartTypeEnum | It will help API to kmow the response should return
  'service': "service_example", // String | Filter data by service name.
  'interval': 789 // Number | Interval in seconds for output time ranges
};
apiInstance.getServerErrorCounts(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **chartType** | [**ServerErrorChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] 
 **service** | **String**| Filter data by service name. | [optional] 
 **interval** | **Number**| Interval in seconds for output time ranges | [optional] 

### Return type

[**GetServerErrorCountsResponse**](GetServerErrorCountsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTaskDetail

> GetTaskDetailResponse getTaskDetail(taskID, opts)

Gets Task Detail

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let taskID = null; // String | ID of Task
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getTaskDetail(taskID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**String**](.md)| ID of Task | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetTaskDetailResponse**](GetTaskDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTaskDownload

> [ModelByte] getTaskDownload(taskID, taskOutputName, opts)

Returns the contents of the task&#39;s output

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let taskID = null; // String | ID of Task
let taskOutputName = "taskOutputName_example"; // String | Name of the task output, e.g. vtn-standard.json
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getTaskDownload(taskID, taskOutputName, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**String**](.md)| ID of Task | 
 **taskOutputName** | **String**| Name of the task output, e.g. vtn-standard.json | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**[ModelByte]**](ModelByte.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTaskLogs

> File getTaskLogs(taskID, opts)

Gets logs associated with a task

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let taskID = null; // String | ID of Task
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getTaskLogs(taskID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**String**](.md)| ID of Task | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

**File**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/zip, application/json


## getTaskOutput

> GetTaskOutputResponse getTaskOutput(taskID, taskOutputName, opts)

Returns the contents of the task&#39;s output

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let taskID = null; // String | ID of Task
let taskOutputName = "taskOutputName_example"; // String | Name of the task output, e.g. vtn-standard.json
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getTaskOutput(taskID, taskOutputName, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**String**](.md)| ID of Task | 
 **taskOutputName** | **String**| Name of the task output, e.g. vtn-standard.json | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetTaskOutputResponse**](GetTaskOutputResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTaskOutputs

> GetTaskOutputsResponse getTaskOutputs(taskID, opts)

Gets Task Output

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let taskID = null; // String | ID of Task
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getTaskOutputs(taskID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**String**](.md)| ID of Task | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetTaskOutputsResponse**](GetTaskOutputsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTaskSyncBacklog

> GetTaskSyncBacklogResponse getTaskSyncBacklog(opts)

Gets task sync backlog in a time-range

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'interval': 789 // Number | Interval in seconds for output time ranges
};
apiInstance.getTaskSyncBacklog(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **interval** | **Number**| Interval in seconds for output time ranges | [optional] 

### Return type

[**GetTaskSyncBacklogResponse**](GetTaskSyncBacklogResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTasks

> GetTasksResponse getTasks(opts)

This gets a list of tasks based on the provided criteria

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'orderBy': "'createdDateTime'", // String | the field to sort
  'direction': "'DESC'", // String | the sort order.  ASC or DESC.
  'status': new AiwareJsClient.TaskStatusEnum(), // TaskStatusEnum | Filtering by task Status
  'organizationID': "organizationID_example", // String | Filter by organization id
  'taskID': "taskID_example", // String | Filter by task id
  'coreTaskID': "coreTaskID_example", // String | Filter by coreTaskID
  'errorType': new AiwareJsClient.FailureReasonEnum(), // FailureReasonEnum | filter by errorType (failureReason)
  'jobID': "jobID_example", // String | Filter by job id
  'coreJobID': "coreJobID_example", // String | Filter by coreJobID
  'engineID': "engineID_example", // String | Filter by engine id
  'mediaSourceID': "mediaSourceID_example", // String | Filter by media source id
  'recordingID': 789, // Number | Filter tasks by the recording id
  'engineCategoryID': null, // String | Filtering by engineCategoryID
  'modifiedBefore': 789, // Number | Filter by items modified before expressed as timestamp
  'modifiedAfter': 789, // Number | Filter by items modified after expressed as timestamp
  'createdBefore': 789, // Number | Filter items where created date is before this date
  'createdAfter': 789, // Number | Filter items where created date is after this date
  'backlog': true, // Boolean | Filtering all tasks in backlog
  'alloc': true // Boolean | Filtering all tasks have alloc = true or not
};
apiInstance.getTasks(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **offset** | **Number**| the number of data to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of items to return. | [optional] [default to 10]
 **orderBy** | **String**| the field to sort | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **organizationID** | **String**| Filter by organization id | [optional] 
 **taskID** | **String**| Filter by task id | [optional] 
 **coreTaskID** | **String**| Filter by coreTaskID | [optional] 
 **errorType** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] 
 **jobID** | **String**| Filter by job id | [optional] 
 **coreJobID** | **String**| Filter by coreJobID | [optional] 
 **engineID** | **String**| Filter by engine id | [optional] 
 **mediaSourceID** | **String**| Filter by media source id | [optional] 
 **recordingID** | **Number**| Filter tasks by the recording id | [optional] 
 **engineCategoryID** | [**String**](.md)| Filtering by engineCategoryID | [optional] 
 **modifiedBefore** | **Number**| Filter by items modified before expressed as timestamp | [optional] 
 **modifiedAfter** | **Number**| Filter by items modified after expressed as timestamp | [optional] 
 **createdBefore** | **Number**| Filter items where created date is before this date | [optional] 
 **createdAfter** | **Number**| Filter items where created date is after this date | [optional] 
 **backlog** | **Boolean**| Filtering all tasks in backlog | [optional] 
 **alloc** | **Boolean**| Filtering all tasks have alloc &#x3D; true or not | [optional] 

### Return type

[**GetTasksResponse**](GetTasksResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTasksErrorTypeCountByEngine

> GetTasksErrorTypeCountByEngineResponse getTasksErrorTypeCountByEngine(opts)

This gets error type count by engines

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'engineID': "engineID_example", // String | Filter by engine id
  'status': new AiwareJsClient.TaskStatusEnum(), // TaskStatusEnum | Filtering by task Status
  'errorType': new AiwareJsClient.FailureReasonEnum() // FailureReasonEnum | filter by errorType (failureReason)
};
apiInstance.getTasksErrorTypeCountByEngine(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **engineID** | **String**| Filter by engine id | [optional] 
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **errorType** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] 

### Return type

[**GetTasksErrorTypeCountByEngineResponse**](GetTasksErrorTypeCountByEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTasksErrors

> GetTaskErrorsResponse getTasksErrors(opts)

This provides a error list in a time range

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'taskID': null, // String | filter by taskID
  'jobID': null, // String | filter by jobID
  'errorType': new AiwareJsClient.FailureReasonEnum(), // FailureReasonEnum | filter by errorType (failureReason)
  'offset': 56, // Number | the number of records to skip before getting the result set
  'limit': 100, // Number | the number of records to return.
  'orderBy': "'createdDateTime'", // String | the field to sort. It should be in [createdDateTime, modifiedDateTime]
  'direction': "'DESC'" // String | the sort order
};
apiInstance.getTasksErrors(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **taskID** | [**String**](.md)| filter by taskID | [optional] 
 **jobID** | [**String**](.md)| filter by jobID | [optional] 
 **errorType** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] 
 **offset** | **Number**| the number of records to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of records to return. | [optional] [default to 100]
 **orderBy** | **String**| the field to sort. It should be in [createdDateTime, modifiedDateTime] | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **String**| the sort order | [optional] [default to &#39;DESC&#39;]

### Return type

[**GetTaskErrorsResponse**](GetTaskErrorsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTasksInstances

> GetTasksInstancesResponse getTasksInstances(opts)

This gets processing stats of the tasks

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'status': new AiwareJsClient.EngineStatusEnum(), // EngineStatusEnum | If specified, this limits the engine instances to follow status
  'engineCategoryID': null // String | 
};
apiInstance.getTasksInstances(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**EngineStatusEnum**](.md)| If specified, this limits the engine instances to follow status | [optional] 
 **engineCategoryID** | [**String**](.md)|  | [optional] 

### Return type

[**GetTasksInstancesResponse**](GetTasksInstancesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTasksStats

> GetTasksStatsResponse getTasksStats(opts)

This gets processing stats of the tasks

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'chartType': new AiwareJsClient.JobTaskStatusChartTypeEnum(), // JobTaskStatusChartTypeEnum | It will help API to kmow the response should return
  'status': new AiwareJsClient.TaskStatusEnum(), // TaskStatusEnum | Filtering by task Status
  'organizationIDs': null, // String | 
  'engineIDs': null // String | 
};
apiInstance.getTasksStats(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **chartType** | [**JobTaskStatusChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] 
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **organizationIDs** | [**String**](.md)|  | [optional] 
 **engineIDs** | [**String**](.md)|  | [optional] 

### Return type

[**GetTasksStatsResponse**](GetTasksStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTasksStatsCategories

> GetTasksCategoriesStatsResponse getTasksStatsCategories(opts)

This gets processing stats of the tasks grouped by engine categories

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'status': new AiwareJsClient.TaskStatusEnum(), // TaskStatusEnum | Filtering by task Status
  'organizationIDs': null, // String | 
  'engineCategoryID': null // String | 
};
apiInstance.getTasksStatsCategories(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **organizationIDs** | [**String**](.md)|  | [optional] 
 **engineCategoryID** | [**String**](.md)|  | [optional] 

### Return type

[**GetTasksCategoriesStatsResponse**](GetTasksCategoriesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTasksStatsEngines

> GetTasksEnginesStatsResponse getTasksStatsEngines(opts)

This gets processing stats of the tasks grouped by engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'status': new AiwareJsClient.TaskStatusEnum(), // TaskStatusEnum | Filtering by task Status
  'organizationID': "organizationID_example", // String | Filter by  organization id
  'taskID': "taskID_example", // String | Filter by task id
  'errorType': new AiwareJsClient.FailureReasonEnum(), // FailureReasonEnum | filter by errorType (failureReason)
  'jobID': "jobID_example", // String | Filter by job id
  'engineID': "engineID_example", // String | Filter by engine id
  'mediaSourceID': "mediaSourceID_example", // String | Filter by media source id
  'recordingID': 789, // Number | Filter tasks by the recording id
  'engineCategoryID': null // String | Filtering by engineCategoryID
};
apiInstance.getTasksStatsEngines(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **organizationID** | **String**| Filter by  organization id | [optional] 
 **taskID** | **String**| Filter by task id | [optional] 
 **errorType** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] 
 **jobID** | **String**| Filter by job id | [optional] 
 **engineID** | **String**| Filter by engine id | [optional] 
 **mediaSourceID** | **String**| Filter by media source id | [optional] 
 **recordingID** | **Number**| Filter tasks by the recording id | [optional] 
 **engineCategoryID** | [**String**](.md)| Filtering by engineCategoryID | [optional] 

### Return type

[**GetTasksEnginesStatsResponse**](GetTasksEnginesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTasksStatsOrganizations

> GetTasksStatsOrganizationsResponse getTasksStatsOrganizations(opts)

This gets processing stats of the tasks grouped by engine, filter by organizations

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'status': new AiwareJsClient.TaskStatusEnum(), // TaskStatusEnum | Filtering by task Status
  'organizationIDs': null, // String | Filter by organization IDs
  'engineID': null // String | Filter by engine ID
};
apiInstance.getTasksStatsOrganizations(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **organizationIDs** | [**String**](.md)| Filter by organization IDs | [optional] 
 **engineID** | [**String**](.md)| Filter by engine ID | [optional] 

### Return type

[**GetTasksStatsOrganizationsResponse**](GetTasksStatsOrganizationsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTasksStatsTimeRanges

> GetTasksTimeRangesStatsResponse getTasksStatsTimeRanges(opts)

This gets processing stats of the tasks grouped by time ranges and sorted by a range start time

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'status': new AiwareJsClient.TaskStatusEnum(), // TaskStatusEnum | Filtering by task Status
  'interval': 789, // Number | Interval in seconds for output time ranges
  'engineCategoryID': null, // String | Filtering by engineCategoryID
  'organizationIDs': "organizationIDs_example" // String | 
};
apiInstance.getTasksStatsTimeRanges(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **interval** | **Number**| Interval in seconds for output time ranges | [optional] 
 **engineCategoryID** | [**String**](.md)| Filtering by engineCategoryID | [optional] 
 **organizationIDs** | **String**|  | [optional] 

### Return type

[**GetTasksTimeRangesStatsResponse**](GetTasksTimeRangesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getTotalPendingScheduledJobs

> GetTotalPendingScheduledJobsResponse getTotalPendingScheduledJobs(opts)

This gets the total pending scheduled jobs by time ranges

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'interval': 789 // Number | Interval in seconds for output time ranges
};
apiInstance.getTotalPendingScheduledJobs(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **interval** | **Number**| Interval in seconds for output time ranges | [optional] 

### Return type

[**GetTotalPendingScheduledJobsResponse**](GetTotalPendingScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getWorkRequest

> GetTaskWorkRequestResponse getWorkRequest(workRequestID, opts)

This provides detail of workrequest

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let workRequestID = null; // String | ID of Work request
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getWorkRequest(workRequestID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workRequestID** | [**String**](.md)| ID of Work request | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetTaskWorkRequestResponse**](GetTaskWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## launchJobTemplate

> LaunchJobTemplateResponse launchJobTemplate(templateID, launchJobTemplateRequest, opts)

This launch a job based on the given job template

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let templateID = "templateID_example"; // String | ID of Job
let launchJobTemplateRequest = new AiwareJsClient.LaunchJobTemplateRequest(); // LaunchJobTemplateRequest | Launch Job Template API
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.launchJobTemplate(templateID, launchJobTemplateRequest, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **templateID** | **String**| ID of Job | 
 **launchJobTemplateRequest** | [**LaunchJobTemplateRequest**](LaunchJobTemplateRequest.md)| Launch Job Template API | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**LaunchJobTemplateResponse**](LaunchJobTemplateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## pushContentToEndpoint

> CreateJobResponse pushContentToEndpoint(endpoint, body, opts)

Whatever is posted to this endpoint will be added to the child input folder(s) for the task_routes that have this endpoint.  If more than one task_routes have this endpoint, it will be added to all child input folders.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let endpoint = null; // String | Endpoint UUID to push this chunk towards
let body = "body_example"; // String | How to push content into a child input folder(s).
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.pushContentToEndpoint(endpoint, body, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **endpoint** | [**String**](.md)| Endpoint UUID to push this chunk towards | 
 **body** | **String**| How to push content into a child input folder(s). | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateJobResponse**](CreateJobResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json, application/octet-stream, audio/_*, image/_*, text/html, text/plain, text/xml, video/_*
- **Accept**: application/json


## recheckJobStatus

> RecheckJobStatusResponse recheckJobStatus(jobID, opts)

Recheck Job Status

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let jobID = null; // String | ID of Job
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.recheckJobStatus(jobID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**String**](.md)| ID of Job | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**RecheckJobStatusResponse**](RecheckJobStatusResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tasksStatusExport

> File tasksStatusExport(opts)

Export a task status report as a excel file

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'orderBy': "'createdDateTime'", // String | the field to sort
  'direction': "'DESC'", // String | the sort order.  ASC or DESC.
  'status': new AiwareJsClient.TaskStatusEnum(), // TaskStatusEnum | Filtering by task Status
  'organizationID': "organizationID_example", // String | Filter by organization id
  'taskID': "taskID_example", // String | Filter by task id
  'coreTaskID': "coreTaskID_example", // String | Filter by coreTaskID
  'errorType': new AiwareJsClient.FailureReasonEnum(), // FailureReasonEnum | filter by errorType (failureReason)
  'jobID': "jobID_example", // String | Filter by job id
  'coreJobID': "coreJobID_example", // String | Filter by coreJobID
  'engineID': "engineID_example", // String | Filter by engine id
  'mediaSourceID': "mediaSourceID_example", // String | Filter by media source id
  'recordingID': 789, // Number | Filter tasks by the recording id
  'engineCategoryID': null, // String | Filtering by engineCategoryID
  'modifiedBefore': 789, // Number | Filter by items modified before expressed as timestamp
  'modifiedAfter': 789, // Number | Filter by items modified after expressed as timestamp
  'createdBefore': 789, // Number | Filter items where created date is before this date
  'createdAfter': 789, // Number | Filter items where created date is after this date
  'backlog': true, // Boolean | Filtering all tasks in backlog
  'alloc': true // Boolean | Filtering all tasks have alloc = true or not
};
apiInstance.tasksStatusExport(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **offset** | **Number**| the number of data to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of items to return. | [optional] [default to 10]
 **orderBy** | **String**| the field to sort | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **organizationID** | **String**| Filter by organization id | [optional] 
 **taskID** | **String**| Filter by task id | [optional] 
 **coreTaskID** | **String**| Filter by coreTaskID | [optional] 
 **errorType** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] 
 **jobID** | **String**| Filter by job id | [optional] 
 **coreJobID** | **String**| Filter by coreJobID | [optional] 
 **engineID** | **String**| Filter by engine id | [optional] 
 **mediaSourceID** | **String**| Filter by media source id | [optional] 
 **recordingID** | **Number**| Filter tasks by the recording id | [optional] 
 **engineCategoryID** | [**String**](.md)| Filtering by engineCategoryID | [optional] 
 **modifiedBefore** | **Number**| Filter by items modified before expressed as timestamp | [optional] 
 **modifiedAfter** | **Number**| Filter by items modified after expressed as timestamp | [optional] 
 **createdBefore** | **Number**| Filter items where created date is before this date | [optional] 
 **createdAfter** | **Number**| Filter items where created date is after this date | [optional] 
 **backlog** | **Boolean**| Filtering all tasks in backlog | [optional] 
 **alloc** | **Boolean**| Filtering all tasks have alloc &#x3D; true or not | [optional] 

### Return type

**File**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet, application/json


## updateTaskStatus

> TasksStatusUpdateResponse updateTaskStatus(tasksStatusUpdateRequest, opts)

This updates the status for a bulk of tasks by taskID

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ProcessApi();
let tasksStatusUpdateRequest = new AiwareJsClient.TasksStatusUpdateRequest(); // TasksStatusUpdateRequest | The input for updateTaskStatus
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateTaskStatus(tasksStatusUpdateRequest, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tasksStatusUpdateRequest** | [**TasksStatusUpdateRequest**](TasksStatusUpdateRequest.md)| The input for updateTaskStatus | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**TasksStatusUpdateResponse**](TasksStatusUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

