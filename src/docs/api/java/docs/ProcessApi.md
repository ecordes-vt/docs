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
> AddTaskResponse addTask(jobID, addTaskRequest, xCorrelationId)

Adds a Task to a current job

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID jobID = new UUID(); // UUID | ID of Job
    AddTaskRequest addTaskRequest = new AddTaskRequest(); // AddTaskRequest | Create Job API
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AddTaskResponse result = apiInstance.addTask(jobID, addTaskRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#addTask");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**UUID**](.md)| ID of Job |
 **addTaskRequest** | [**AddTaskRequest**](AddTaskRequest.md)| Create Job API |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**AddTaskResponse**](AddTaskResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="addTaskRoute"></a>
# **addTaskRoute**
> AddTaskRouteResponse addTaskRoute(jobID, addTaskRouteRequest, xCorrelationId)

Adds a Task Route to a current job

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID jobID = new UUID(); // UUID | ID of Job
    AddTaskRouteRequest addTaskRouteRequest = new AddTaskRouteRequest(); // AddTaskRouteRequest | Adds a Task Route
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AddTaskRouteResponse result = apiInstance.addTaskRoute(jobID, addTaskRouteRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#addTaskRoute");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**UUID**](.md)| ID of Job |
 **addTaskRouteRequest** | [**AddTaskRouteRequest**](AddTaskRouteRequest.md)| Adds a Task Route |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**AddTaskRouteResponse**](AddTaskRouteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="createJob"></a>
# **createJob**
> CreateJobResponse createJob(createJobRequest, xCorrelationId)

This creates a new Job

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    CreateJobRequest createJobRequest = new CreateJobRequest(); // CreateJobRequest | Create Job API
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      CreateJobResponse result = apiInstance.createJob(createJobRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#createJob");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
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

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="deleteJob"></a>
# **deleteJob**
> AdminOperationResponse deleteJob(jobID, xCorrelationId, deleteJobRequest)

This API deletes the specified job

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID jobID = new UUID(); // UUID | ID of Job
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    DeleteJobRequest deleteJobRequest = new DeleteJobRequest(); // DeleteJobRequest | Request information to delete the specified job
    try {
      AdminOperationResponse result = apiInstance.deleteJob(jobID, xCorrelationId, deleteJobRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#deleteJob");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**UUID**](.md)| ID of Job |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **deleteJobRequest** | [**DeleteJobRequest**](DeleteJobRequest.md)| Request information to delete the specified job | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Delete a particular job |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="deleteTask"></a>
# **deleteTask**
> AdminOperationResponse deleteTask(taskID, xCorrelationId)

This API deletes the specified task

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID taskID = new UUID(); // UUID | ID of Task
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AdminOperationResponse result = apiInstance.deleteTask(taskID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#deleteTask");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**UUID**](.md)| ID of Task |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Delete a particular task |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineErrorTimeRanges"></a>
# **getEngineErrorTimeRanges**
> GetEngineErrorTimeRangesResponse getEngineErrorTimeRanges(xCorrelationId, startTime, endTime, chartType, interval, engineID)

This gets engine error count by error tasks grouped by time ranges and sorted by a range start time

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    EngineErrorChartTypeEnum chartType = new EngineErrorChartTypeEnum(); // EngineErrorChartTypeEnum | It will help API to kmow the response should return
    Long interval = 56L; // Long | Interval in seconds for output time ranges
    UUID engineID = new UUID(); // UUID | Filtering by engineID
    try {
      GetEngineErrorTimeRangesResponse result = apiInstance.getEngineErrorTimeRanges(xCorrelationId, startTime, endTime, chartType, interval, engineID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getEngineErrorTimeRanges");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **chartType** | [**EngineErrorChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] [enum: total_engine_errors, total_failed_task_by_engine]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional]
 **engineID** | [**UUID**](.md)| Filtering by engineID | [optional]

### Return type

[**GetEngineErrorTimeRangesResponse**](GetEngineErrorTimeRangesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobDetail"></a>
# **getJobDetail**
> GetJobDetailResponse getJobDetail(jobID, xCorrelationId)

Gets Job Detail

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID jobID = new UUID(); // UUID | ID of Job
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetJobDetailResponse result = apiInstance.getJobDetail(jobID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getJobDetail");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**UUID**](.md)| ID of Job |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetJobDetailResponse**](GetJobDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobDownload"></a>
# **getJobDownload**
> List&lt;byte[]&gt; getJobDownload(jobID, jobOutputName, xCorrelationId)

Returns the contents of the job&#39;s output

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID jobID = new UUID(); // UUID | ID of Job
    String jobOutputName = "jobOutputName_example"; // String | Name of the job output, e.g. vtn-standard.json
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      List<byte[]> result = apiInstance.getJobDownload(jobID, jobOutputName, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getJobDownload");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**UUID**](.md)| ID of Job |
 **jobOutputName** | **String**| Name of the job output, e.g. vtn-standard.json |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

**List&lt;byte[]&gt;**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobOutput"></a>
# **getJobOutput**
> GetJobOutputResponse getJobOutput(jobID, jobOutputName, xCorrelationId)

Returns the contents of the job&#39;s output

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID jobID = new UUID(); // UUID | ID of Job
    String jobOutputName = "jobOutputName_example"; // String | Name of the job output, e.g. vtn-standard.json
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetJobOutputResponse result = apiInstance.getJobOutput(jobID, jobOutputName, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getJobOutput");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**UUID**](.md)| ID of Job |
 **jobOutputName** | **String**| Name of the job output, e.g. vtn-standard.json |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetJobOutputResponse**](GetJobOutputResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobOutputs"></a>
# **getJobOutputs**
> GetJobOutputsResponse getJobOutputs(jobID, xCorrelationId)

Returns a list of output information about this job

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID jobID = new UUID(); // UUID | ID of Job
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetJobOutputsResponse result = apiInstance.getJobOutputs(jobID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getJobOutputs");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**UUID**](.md)| ID of Job |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetJobOutputsResponse**](GetJobOutputsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobPerformance"></a>
# **getJobPerformance**
> GetJobPerformanceResponse getJobPerformance(jobID, xCorrelationId, interval, taskID, workRequestID)

This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID jobID = new UUID(); // UUID | ID of Job
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long interval = 56L; // Long | Interval in seconds for output time ranges
    UUID taskID = new UUID(); // UUID | Filter data by taskID
    UUID workRequestID = new UUID(); // UUID | Filter data by workRequestID
    try {
      GetJobPerformanceResponse result = apiInstance.getJobPerformance(jobID, xCorrelationId, interval, taskID, workRequestID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getJobPerformance");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**UUID**](.md)| ID of Job |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional]
 **taskID** | [**UUID**](.md)| Filter data by taskID | [optional]
 **workRequestID** | [**UUID**](.md)| Filter data by workRequestID | [optional]

### Return type

[**GetJobPerformanceResponse**](GetJobPerformanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobStatus"></a>
# **getJobStatus**
> GetJobStatusResponse getJobStatus(jobID, xCorrelationId)

Gets Job Status

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID jobID = new UUID(); // UUID | ID of Job
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetJobStatusResponse result = apiInstance.getJobStatus(jobID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getJobStatus");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**UUID**](.md)| ID of Job |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetJobStatusResponse**](GetJobStatusResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobWorkRequests"></a>
# **getJobWorkRequests**
> GetJobWorkRequestResponse getJobWorkRequests(jobID, xCorrelationId, offset, limit, orderBy, direction, status, taskID)

This provides a list of workrequests of a job

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID jobID = new UUID(); // UUID | ID of Job
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Integer offset = 56; // Integer | the number of records to skip before getting the result set
    Integer limit = 100; // Integer | the number of records to return.
    String orderBy = "\"createdDateTime\""; // String | the field to sort. It should be in [createdDateTime, modifiedDateTime]
    String direction = "\"DESC\""; // String | the sort order
    String status = "status_example"; // String | the value should be in [active, trial, inactive, deleted]
    String taskID = "taskID_example"; // String | This is an internal task ID to get work request
    try {
      GetJobWorkRequestResponse result = apiInstance.getJobWorkRequests(jobID, xCorrelationId, offset, limit, orderBy, direction, status, taskID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getJobWorkRequests");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**UUID**](.md)| ID of Job |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **offset** | **Integer**| the number of records to skip before getting the result set | [optional]
 **limit** | **Integer**| the number of records to return. | [optional] [default to 100]
 **orderBy** | **String**| the field to sort. It should be in [createdDateTime, modifiedDateTime] | [optional] [default to &quot;createdDateTime&quot;]
 **direction** | **String**| the sort order | [optional] [default to &quot;DESC&quot;]
 **status** | **String**| the value should be in [active, trial, inactive, deleted] | [optional]
 **taskID** | **String**| This is an internal task ID to get work request | [optional]

### Return type

[**GetJobWorkRequestResponse**](GetJobWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobs"></a>
# **getJobs**
> GetJobListResponse getJobs(xCorrelationId, startTime, endTime, status, offset, limit, orderBy, direction, coreID, organizationID, recordingID, jobID, coreJobID, modifiedBefore, modifiedAfter, createdBefore, createdAfter)

This gets a list of jobs

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    JobStatusEnum status = new JobStatusEnum(); // JobStatusEnum | If specified, this limits the jobs or tasks to follow status
    Long offset = 56L; // Long | the number of data to skip before getting the result set
    Long limit = 10lL; // Long | the number of items to return.
    String orderBy = "\"createdDateTime\""; // String | the field to sort
    String direction = "\"DESC\""; // String | the sort order.  ASC or DESC.
    UUID coreID = new UUID(); // UUID | Filter by coreID
    UUID organizationID = new UUID(); // UUID | Filter by organizationID
    UUID recordingID = new UUID(); // UUID | Filter by recordingID
    UUID jobID = new UUID(); // UUID | Filter by jobID
    String coreJobID = "coreJobID_example"; // String | Filter by coreJobID
    Long modifiedBefore = 56L; // Long | Filter by items modified before expressed as timestamp
    Long modifiedAfter = 56L; // Long | Filter by items modified after expressed as timestamp
    Long createdBefore = 56L; // Long | Filter items where created date is before this date
    Long createdAfter = 56L; // Long | Filter items where created date is after this date
    try {
      GetJobListResponse result = apiInstance.getJobs(xCorrelationId, startTime, endTime, status, offset, limit, orderBy, direction, coreID, organizationID, recordingID, jobID, coreJobID, modifiedBefore, modifiedAfter, createdBefore, createdAfter);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getJobs");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **status** | [**JobStatusEnum**](.md)| If specified, this limits the jobs or tasks to follow status | [optional] [enum: scheduled, pending, queued, running, complete, aborted, failed, rejected, reprocessing]
 **offset** | **Long**| the number of data to skip before getting the result set | [optional]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10l]
 **orderBy** | **String**| the field to sort | [optional] [default to &quot;createdDateTime&quot;]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &quot;DESC&quot;]
 **coreID** | [**UUID**](.md)| Filter by coreID | [optional]
 **organizationID** | [**UUID**](.md)| Filter by organizationID | [optional]
 **recordingID** | [**UUID**](.md)| Filter by recordingID | [optional]
 **jobID** | [**UUID**](.md)| Filter by jobID | [optional]
 **coreJobID** | **String**| Filter by coreJobID | [optional]
 **modifiedBefore** | **Long**| Filter by items modified before expressed as timestamp | [optional]
 **modifiedAfter** | **Long**| Filter by items modified after expressed as timestamp | [optional]
 **createdBefore** | **Long**| Filter items where created date is before this date | [optional]
 **createdAfter** | **Long**| Filter items where created date is after this date | [optional]

### Return type

[**GetJobListResponse**](GetJobListResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobsOrganizationStats"></a>
# **getJobsOrganizationStats**
> GetJobsOrganizationStatsResponse getJobsOrganizationStats(xCorrelationId, startTime, endTime, organizationIDs)

This gets processing stats of the jobs by organization

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    String organizationIDs = "organizationIDs_example"; // String | 
    try {
      GetJobsOrganizationStatsResponse result = apiInstance.getJobsOrganizationStats(xCorrelationId, startTime, endTime, organizationIDs);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getJobsOrganizationStats");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **organizationIDs** | **String**|  | [optional]

### Return type

[**GetJobsOrganizationStatsResponse**](GetJobsOrganizationStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobsPerformance"></a>
# **getJobsPerformance**
> GetJobsPerformanceResponse getJobsPerformance(xCorrelationId, startTime, endTime, interval)

This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    Long interval = 56L; // Long | Interval in seconds for output time ranges
    try {
      GetJobsPerformanceResponse result = apiInstance.getJobsPerformance(xCorrelationId, startTime, endTime, interval);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getJobsPerformance");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional]

### Return type

[**GetJobsPerformanceResponse**](GetJobsPerformanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobsStats"></a>
# **getJobsStats**
> GetJobsStatsResponse getJobsStats(xCorrelationId, startTime, endTime, chartType, status, organizationIDs)

This gets processing stats of the jobs

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    JobTaskStatusChartTypeEnum chartType = new JobTaskStatusChartTypeEnum(); // JobTaskStatusChartTypeEnum | It will help API to kmow the response should return
    JobStatusEnum status = new JobStatusEnum(); // JobStatusEnum | If specified, this limits the jobs or tasks to follow status
    String organizationIDs = "organizationIDs_example"; // String | 
    try {
      GetJobsStatsResponse result = apiInstance.getJobsStats(xCorrelationId, startTime, endTime, chartType, status, organizationIDs);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getJobsStats");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **chartType** | [**JobTaskStatusChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] [enum: total, total_by_time_range]
 **status** | [**JobStatusEnum**](.md)| If specified, this limits the jobs or tasks to follow status | [optional] [enum: scheduled, pending, queued, running, complete, aborted, failed, rejected, reprocessing]
 **organizationIDs** | **String**|  | [optional]

### Return type

[**GetJobsStatsResponse**](GetJobsStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobsTimeRangesStats"></a>
# **getJobsTimeRangesStats**
> GetJobsTimeRangesStatsResponse getJobsTimeRangesStats(xCorrelationId, startTime, endTime, status, interval, organizationIDs, engineCategoryID)

This gets processing stats of the jobs grouped by time ranges and sorted by a range start time

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    JobStatusEnum status = new JobStatusEnum(); // JobStatusEnum | If specified, this limits the jobs or tasks to follow status
    Long interval = 56L; // Long | Interval in seconds for output time ranges
    String organizationIDs = "organizationIDs_example"; // String | 
    UUID engineCategoryID = new UUID(); // UUID | 
    try {
      GetJobsTimeRangesStatsResponse result = apiInstance.getJobsTimeRangesStats(xCorrelationId, startTime, endTime, status, interval, organizationIDs, engineCategoryID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getJobsTimeRangesStats");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **status** | [**JobStatusEnum**](.md)| If specified, this limits the jobs or tasks to follow status | [optional] [enum: scheduled, pending, queued, running, complete, aborted, failed, rejected, reprocessing]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional]
 **organizationIDs** | **String**|  | [optional]
 **engineCategoryID** | [**UUID**](.md)|  | [optional]

### Return type

[**GetJobsTimeRangesStatsResponse**](GetJobsTimeRangesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getRatePendingScheduledJobs"></a>
# **getRatePendingScheduledJobs**
> GetRatePendingScheduledJobsResponse getRatePendingScheduledJobs(xCorrelationId, startTime, endTime, interval)

This gets the rate of pending scheduled jobs by time ranges

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    Long interval = 56L; // Long | Interval in seconds for output time ranges
    try {
      GetRatePendingScheduledJobsResponse result = apiInstance.getRatePendingScheduledJobs(xCorrelationId, startTime, endTime, interval);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getRatePendingScheduledJobs");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional]

### Return type

[**GetRatePendingScheduledJobsResponse**](GetRatePendingScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getScheduledJobDetail"></a>
# **getScheduledJobDetail**
> GetScheduledJobDetailResponse getScheduledJobDetail(scheduledJobID, xCorrelationId)

This gets scheduled job detail

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID scheduledJobID = new UUID(); // UUID | ID of Scheduled Job. It can be an internal ID or core ID
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetScheduledJobDetailResponse result = apiInstance.getScheduledJobDetail(scheduledJobID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getScheduledJobDetail");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scheduledJobID** | [**UUID**](.md)| ID of Scheduled Job. It can be an internal ID or core ID |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetScheduledJobDetailResponse**](GetScheduledJobDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getScheduledJobs"></a>
# **getScheduledJobs**
> GetScheduledJobsResponse getScheduledJobs(xCorrelationId, startTime, endTime, offset, limit, direction, scheduledJobID, internalOrganizationID, coreID, startStartTime, endStartTime, startStopTime, endStopTime, isActive, runMode, sourceID, sourceType, orderBy, scheduledJobName)

This gets a list of scheduled jobs

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    Long offset = 56L; // Long | the number of data to skip before getting the result set
    Long limit = 10lL; // Long | the number of items to return.
    String direction = "\"DESC\""; // String | the sort order.  ASC or DESC.
    String scheduledJobID = "scheduledJobID_example"; // String | Filter by internal scheduled Job ID(uuid) or core scheduled Job ID (integer)
    UUID internalOrganizationID = new UUID(); // UUID | Filter by internal organization id
    UUID coreID = new UUID(); // UUID | Filter by coreID
    Long startStartTime = 56L; // Long | 
    Long endStartTime = 56L; // Long | 
    Long startStopTime = 56L; // Long | 
    Long endStopTime = 56L; // Long | 
    Boolean isActive = true; // Boolean | 
    ScheduleRunModeEnum runMode = new ScheduleRunModeEnum(); // ScheduleRunModeEnum | Filter by runMode
    Integer sourceID = 56; // Integer | 
    String sourceType = "sourceType_example"; // String | 
    String orderBy = "orderBy_example"; // String | The value should be in [organizationID, runMode, createdTime, startTime, stopTime]
    String scheduledJobName = "scheduledJobName_example"; // String | 
    try {
      GetScheduledJobsResponse result = apiInstance.getScheduledJobs(xCorrelationId, startTime, endTime, offset, limit, direction, scheduledJobID, internalOrganizationID, coreID, startStartTime, endStartTime, startStopTime, endStopTime, isActive, runMode, sourceID, sourceType, orderBy, scheduledJobName);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getScheduledJobs");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **offset** | **Long**| the number of data to skip before getting the result set | [optional]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10l]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &quot;DESC&quot;]
 **scheduledJobID** | **String**| Filter by internal scheduled Job ID(uuid) or core scheduled Job ID (integer) | [optional]
 **internalOrganizationID** | [**UUID**](.md)| Filter by internal organization id | [optional]
 **coreID** | [**UUID**](.md)| Filter by coreID | [optional]
 **startStartTime** | **Long**|  | [optional]
 **endStartTime** | **Long**|  | [optional]
 **startStopTime** | **Long**|  | [optional]
 **endStopTime** | **Long**|  | [optional]
 **isActive** | **Boolean**|  | [optional]
 **runMode** | [**ScheduleRunModeEnum**](.md)| Filter by runMode | [optional] [enum: continuous, recurring, now, once]
 **sourceID** | **Integer**|  | [optional]
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

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getServerErrorCounts"></a>
# **getServerErrorCounts**
> GetServerErrorCountsResponse getServerErrorCounts(xCorrelationId, startTime, endTime, chartType, service, interval)

Get server error counts in a time-range

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    ServerErrorChartTypeEnum chartType = new ServerErrorChartTypeEnum(); // ServerErrorChartTypeEnum | It will help API to kmow the response should return
    String service = "service_example"; // String | Filter data by service name.
    Long interval = 56L; // Long | Interval in seconds for output time ranges
    try {
      GetServerErrorCountsResponse result = apiInstance.getServerErrorCounts(xCorrelationId, startTime, endTime, chartType, service, interval);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getServerErrorCounts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **chartType** | [**ServerErrorChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] [enum: total, pie, time_range]
 **service** | **String**| Filter data by service name. | [optional]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional]

### Return type

[**GetServerErrorCountsResponse**](GetServerErrorCountsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTaskDetail"></a>
# **getTaskDetail**
> GetTaskDetailResponse getTaskDetail(taskID, xCorrelationId)

Gets Task Detail

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID taskID = new UUID(); // UUID | ID of Task
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetTaskDetailResponse result = apiInstance.getTaskDetail(taskID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTaskDetail");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**UUID**](.md)| ID of Task |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetTaskDetailResponse**](GetTaskDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTaskDownload"></a>
# **getTaskDownload**
> List&lt;ModelByte&gt; getTaskDownload(taskID, taskOutputName, xCorrelationId)

Returns the contents of the task&#39;s output

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID taskID = new UUID(); // UUID | ID of Task
    String taskOutputName = "taskOutputName_example"; // String | Name of the task output, e.g. vtn-standard.json
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      List<ModelByte> result = apiInstance.getTaskDownload(taskID, taskOutputName, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTaskDownload");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**UUID**](.md)| ID of Task |
 **taskOutputName** | **String**| Name of the task output, e.g. vtn-standard.json |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**List&lt;ModelByte&gt;**](ModelByte.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTaskLogs"></a>
# **getTaskLogs**
> File getTaskLogs(taskID, xCorrelationId)

Gets logs associated with a task

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID taskID = new UUID(); // UUID | ID of Task
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      File result = apiInstance.getTaskLogs(taskID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTaskLogs");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**UUID**](.md)| ID of Task |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**File**](File.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTaskOutput"></a>
# **getTaskOutput**
> GetTaskOutputResponse getTaskOutput(taskID, taskOutputName, xCorrelationId)

Returns the contents of the task&#39;s output

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID taskID = new UUID(); // UUID | ID of Task
    String taskOutputName = "taskOutputName_example"; // String | Name of the task output, e.g. vtn-standard.json
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetTaskOutputResponse result = apiInstance.getTaskOutput(taskID, taskOutputName, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTaskOutput");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**UUID**](.md)| ID of Task |
 **taskOutputName** | **String**| Name of the task output, e.g. vtn-standard.json |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetTaskOutputResponse**](GetTaskOutputResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTaskOutputs"></a>
# **getTaskOutputs**
> GetTaskOutputsResponse getTaskOutputs(taskID, xCorrelationId)

Gets Task Output

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID taskID = new UUID(); // UUID | ID of Task
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetTaskOutputsResponse result = apiInstance.getTaskOutputs(taskID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTaskOutputs");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **taskID** | [**UUID**](.md)| ID of Task |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetTaskOutputsResponse**](GetTaskOutputsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTaskSyncBacklog"></a>
# **getTaskSyncBacklog**
> GetTaskSyncBacklogResponse getTaskSyncBacklog(xCorrelationId, startTime, endTime, interval)

Gets task sync backlog in a time-range

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    Long interval = 56L; // Long | Interval in seconds for output time ranges
    try {
      GetTaskSyncBacklogResponse result = apiInstance.getTaskSyncBacklog(xCorrelationId, startTime, endTime, interval);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTaskSyncBacklog");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional]

### Return type

[**GetTaskSyncBacklogResponse**](GetTaskSyncBacklogResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTasks"></a>
# **getTasks**
> GetTasksResponse getTasks(xCorrelationId, startTime, endTime, offset, limit, orderBy, direction, status, organizationID, taskID, coreTaskID, errorType, jobID, coreJobID, engineID, mediaSourceID, recordingID, engineCategoryID, modifiedBefore, modifiedAfter, createdBefore, createdAfter, backlog, alloc)

This gets a list of tasks based on the provided criteria

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    Long offset = 56L; // Long | the number of data to skip before getting the result set
    Long limit = 10lL; // Long | the number of items to return.
    String orderBy = "\"createdDateTime\""; // String | the field to sort
    String direction = "\"DESC\""; // String | the sort order.  ASC or DESC.
    TaskStatusEnum status = new TaskStatusEnum(); // TaskStatusEnum | Filtering by task Status
    String organizationID = "organizationID_example"; // String | Filter by organization id
    String taskID = "taskID_example"; // String | Filter by task id
    String coreTaskID = "coreTaskID_example"; // String | Filter by coreTaskID
    FailureReasonEnum errorType = new FailureReasonEnum(); // FailureReasonEnum | filter by errorType (failureReason)
    String jobID = "jobID_example"; // String | Filter by job id
    String coreJobID = "coreJobID_example"; // String | Filter by coreJobID
    String engineID = "engineID_example"; // String | Filter by engine id
    String mediaSourceID = "mediaSourceID_example"; // String | Filter by media source id
    Long recordingID = 56L; // Long | Filter tasks by the recording id
    UUID engineCategoryID = new UUID(); // UUID | Filtering by engineCategoryID
    Long modifiedBefore = 56L; // Long | Filter by items modified before expressed as timestamp
    Long modifiedAfter = 56L; // Long | Filter by items modified after expressed as timestamp
    Long createdBefore = 56L; // Long | Filter items where created date is before this date
    Long createdAfter = 56L; // Long | Filter items where created date is after this date
    Boolean backlog = true; // Boolean | Filtering all tasks in backlog
    Boolean alloc = true; // Boolean | Filtering all tasks have alloc = true or not
    try {
      GetTasksResponse result = apiInstance.getTasks(xCorrelationId, startTime, endTime, offset, limit, orderBy, direction, status, organizationID, taskID, coreTaskID, errorType, jobID, coreJobID, engineID, mediaSourceID, recordingID, engineCategoryID, modifiedBefore, modifiedAfter, createdBefore, createdAfter, backlog, alloc);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTasks");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **offset** | **Long**| the number of data to skip before getting the result set | [optional]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10l]
 **orderBy** | **String**| the field to sort | [optional] [default to &quot;createdDateTime&quot;]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &quot;DESC&quot;]
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **organizationID** | **String**| Filter by organization id | [optional]
 **taskID** | **String**| Filter by task id | [optional]
 **coreTaskID** | **String**| Filter by coreTaskID | [optional]
 **errorType** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] [enum: internal_error, unknown, connection, rate_limited, unauthorized, api, resources, not_found, core_api, bad_data, scheduling, none]
 **jobID** | **String**| Filter by job id | [optional]
 **coreJobID** | **String**| Filter by coreJobID | [optional]
 **engineID** | **String**| Filter by engine id | [optional]
 **mediaSourceID** | **String**| Filter by media source id | [optional]
 **recordingID** | **Long**| Filter tasks by the recording id | [optional]
 **engineCategoryID** | [**UUID**](.md)| Filtering by engineCategoryID | [optional]
 **modifiedBefore** | **Long**| Filter by items modified before expressed as timestamp | [optional]
 **modifiedAfter** | **Long**| Filter by items modified after expressed as timestamp | [optional]
 **createdBefore** | **Long**| Filter items where created date is before this date | [optional]
 **createdAfter** | **Long**| Filter items where created date is after this date | [optional]
 **backlog** | **Boolean**| Filtering all tasks in backlog | [optional]
 **alloc** | **Boolean**| Filtering all tasks have alloc &#x3D; true or not | [optional]

### Return type

[**GetTasksResponse**](GetTasksResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTasksErrorTypeCountByEngine"></a>
# **getTasksErrorTypeCountByEngine**
> GetTasksErrorTypeCountByEngineResponse getTasksErrorTypeCountByEngine(xCorrelationId, startTime, endTime, engineID, status, errorType)

This gets error type count by engines

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    String engineID = "engineID_example"; // String | Filter by engine id
    TaskStatusEnum status = new TaskStatusEnum(); // TaskStatusEnum | Filtering by task Status
    FailureReasonEnum errorType = new FailureReasonEnum(); // FailureReasonEnum | filter by errorType (failureReason)
    try {
      GetTasksErrorTypeCountByEngineResponse result = apiInstance.getTasksErrorTypeCountByEngine(xCorrelationId, startTime, endTime, engineID, status, errorType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTasksErrorTypeCountByEngine");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **engineID** | **String**| Filter by engine id | [optional]
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **errorType** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] [enum: internal_error, unknown, connection, rate_limited, unauthorized, api, resources, not_found, core_api, bad_data, scheduling, none]

### Return type

[**GetTasksErrorTypeCountByEngineResponse**](GetTasksErrorTypeCountByEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTasksErrors"></a>
# **getTasksErrors**
> GetTaskErrorsResponse getTasksErrors(xCorrelationId, startTime, endTime, taskID, jobID, errorType, offset, limit, orderBy, direction)

This provides a error list in a time range

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    UUID taskID = new UUID(); // UUID | filter by taskID
    UUID jobID = new UUID(); // UUID | filter by jobID
    FailureReasonEnum errorType = new FailureReasonEnum(); // FailureReasonEnum | filter by errorType (failureReason)
    Integer offset = 56; // Integer | the number of records to skip before getting the result set
    Integer limit = 100; // Integer | the number of records to return.
    String orderBy = "\"createdDateTime\""; // String | the field to sort. It should be in [createdDateTime, modifiedDateTime]
    String direction = "\"DESC\""; // String | the sort order
    try {
      GetTaskErrorsResponse result = apiInstance.getTasksErrors(xCorrelationId, startTime, endTime, taskID, jobID, errorType, offset, limit, orderBy, direction);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTasksErrors");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **taskID** | [**UUID**](.md)| filter by taskID | [optional]
 **jobID** | [**UUID**](.md)| filter by jobID | [optional]
 **errorType** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] [enum: internal_error, unknown, connection, rate_limited, unauthorized, api, resources, not_found, core_api, bad_data, scheduling, none]
 **offset** | **Integer**| the number of records to skip before getting the result set | [optional]
 **limit** | **Integer**| the number of records to return. | [optional] [default to 100]
 **orderBy** | **String**| the field to sort. It should be in [createdDateTime, modifiedDateTime] | [optional] [default to &quot;createdDateTime&quot;]
 **direction** | **String**| the sort order | [optional] [default to &quot;DESC&quot;]

### Return type

[**GetTaskErrorsResponse**](GetTaskErrorsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTasksInstances"></a>
# **getTasksInstances**
> GetTasksInstancesResponse getTasksInstances(xCorrelationId, startTime, endTime, status, engineCategoryID)

This gets processing stats of the tasks

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    EngineStatusEnum status = new EngineStatusEnum(); // EngineStatusEnum | If specified, this limits the engine instances to follow status
    UUID engineCategoryID = new UUID(); // UUID | 
    try {
      GetTasksInstancesResponse result = apiInstance.getTasksInstances(xCorrelationId, startTime, endTime, status, engineCategoryID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTasksInstances");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **status** | [**EngineStatusEnum**](.md)| If specified, this limits the engine instances to follow status | [optional] [enum: active, terminated]
 **engineCategoryID** | [**UUID**](.md)|  | [optional]

### Return type

[**GetTasksInstancesResponse**](GetTasksInstancesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | This provides the output for the tasks instances call.  Rows that do not have data will be omitted. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTasksStats"></a>
# **getTasksStats**
> GetTasksStatsResponse getTasksStats(xCorrelationId, startTime, endTime, chartType, status, organizationIDs, engineIDs)

This gets processing stats of the tasks

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    JobTaskStatusChartTypeEnum chartType = new JobTaskStatusChartTypeEnum(); // JobTaskStatusChartTypeEnum | It will help API to kmow the response should return
    TaskStatusEnum status = new TaskStatusEnum(); // TaskStatusEnum | Filtering by task Status
    UUID organizationIDs = new UUID(); // UUID | 
    UUID engineIDs = new UUID(); // UUID | 
    try {
      GetTasksStatsResponse result = apiInstance.getTasksStats(xCorrelationId, startTime, endTime, chartType, status, organizationIDs, engineIDs);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTasksStats");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **chartType** | [**JobTaskStatusChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] [enum: total, total_by_time_range]
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **organizationIDs** | [**UUID**](.md)|  | [optional]
 **engineIDs** | [**UUID**](.md)|  | [optional]

### Return type

[**GetTasksStatsResponse**](GetTasksStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | This provides the output for the tasks stats call.  Rows that do not have data will be omitted. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTasksStatsCategories"></a>
# **getTasksStatsCategories**
> GetTasksCategoriesStatsResponse getTasksStatsCategories(xCorrelationId, startTime, endTime, status, organizationIDs, engineCategoryID)

This gets processing stats of the tasks grouped by engine categories

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    TaskStatusEnum status = new TaskStatusEnum(); // TaskStatusEnum | Filtering by task Status
    UUID organizationIDs = new UUID(); // UUID | 
    UUID engineCategoryID = new UUID(); // UUID | 
    try {
      GetTasksCategoriesStatsResponse result = apiInstance.getTasksStatsCategories(xCorrelationId, startTime, endTime, status, organizationIDs, engineCategoryID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTasksStatsCategories");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **organizationIDs** | [**UUID**](.md)|  | [optional]
 **engineCategoryID** | [**UUID**](.md)|  | [optional]

### Return type

[**GetTasksCategoriesStatsResponse**](GetTasksCategoriesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTasksStatsEngines"></a>
# **getTasksStatsEngines**
> GetTasksEnginesStatsResponse getTasksStatsEngines(xCorrelationId, startTime, endTime, status, organizationID, taskID, errorType, jobID, engineID, mediaSourceID, recordingID, engineCategoryID)

This gets processing stats of the tasks grouped by engine

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    TaskStatusEnum status = new TaskStatusEnum(); // TaskStatusEnum | Filtering by task Status
    String organizationID = "organizationID_example"; // String | Filter by  organization id
    String taskID = "taskID_example"; // String | Filter by task id
    FailureReasonEnum errorType = new FailureReasonEnum(); // FailureReasonEnum | filter by errorType (failureReason)
    String jobID = "jobID_example"; // String | Filter by job id
    String engineID = "engineID_example"; // String | Filter by engine id
    String mediaSourceID = "mediaSourceID_example"; // String | Filter by media source id
    Long recordingID = 56L; // Long | Filter tasks by the recording id
    UUID engineCategoryID = new UUID(); // UUID | Filtering by engineCategoryID
    try {
      GetTasksEnginesStatsResponse result = apiInstance.getTasksStatsEngines(xCorrelationId, startTime, endTime, status, organizationID, taskID, errorType, jobID, engineID, mediaSourceID, recordingID, engineCategoryID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTasksStatsEngines");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **organizationID** | **String**| Filter by  organization id | [optional]
 **taskID** | **String**| Filter by task id | [optional]
 **errorType** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] [enum: internal_error, unknown, connection, rate_limited, unauthorized, api, resources, not_found, core_api, bad_data, scheduling, none]
 **jobID** | **String**| Filter by job id | [optional]
 **engineID** | **String**| Filter by engine id | [optional]
 **mediaSourceID** | **String**| Filter by media source id | [optional]
 **recordingID** | **Long**| Filter tasks by the recording id | [optional]
 **engineCategoryID** | [**UUID**](.md)| Filtering by engineCategoryID | [optional]

### Return type

[**GetTasksEnginesStatsResponse**](GetTasksEnginesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTasksStatsOrganizations"></a>
# **getTasksStatsOrganizations**
> GetTasksStatsOrganizationsResponse getTasksStatsOrganizations(xCorrelationId, startTime, endTime, status, organizationIDs, engineID)

This gets processing stats of the tasks grouped by engine, filter by organizations

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    TaskStatusEnum status = new TaskStatusEnum(); // TaskStatusEnum | Filtering by task Status
    UUID organizationIDs = new UUID(); // UUID | Filter by organization IDs
    UUID engineID = new UUID(); // UUID | Filter by engine ID
    try {
      GetTasksStatsOrganizationsResponse result = apiInstance.getTasksStatsOrganizations(xCorrelationId, startTime, endTime, status, organizationIDs, engineID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTasksStatsOrganizations");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **organizationIDs** | [**UUID**](.md)| Filter by organization IDs | [optional]
 **engineID** | [**UUID**](.md)| Filter by engine ID | [optional]

### Return type

[**GetTasksStatsOrganizationsResponse**](GetTasksStatsOrganizationsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTasksStatsTimeRanges"></a>
# **getTasksStatsTimeRanges**
> GetTasksTimeRangesStatsResponse getTasksStatsTimeRanges(xCorrelationId, startTime, endTime, status, interval, engineCategoryID, organizationIDs)

This gets processing stats of the tasks grouped by time ranges and sorted by a range start time

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    TaskStatusEnum status = new TaskStatusEnum(); // TaskStatusEnum | Filtering by task Status
    Long interval = 56L; // Long | Interval in seconds for output time ranges
    UUID engineCategoryID = new UUID(); // UUID | Filtering by engineCategoryID
    String organizationIDs = "organizationIDs_example"; // String | 
    try {
      GetTasksTimeRangesStatsResponse result = apiInstance.getTasksStatsTimeRanges(xCorrelationId, startTime, endTime, status, interval, engineCategoryID, organizationIDs);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTasksStatsTimeRanges");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional]
 **engineCategoryID** | [**UUID**](.md)| Filtering by engineCategoryID | [optional]
 **organizationIDs** | **String**|  | [optional]

### Return type

[**GetTasksTimeRangesStatsResponse**](GetTasksTimeRangesStatsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getTotalPendingScheduledJobs"></a>
# **getTotalPendingScheduledJobs**
> GetTotalPendingScheduledJobsResponse getTotalPendingScheduledJobs(xCorrelationId, startTime, endTime, interval)

This gets the total pending scheduled jobs by time ranges

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    Long interval = 56L; // Long | Interval in seconds for output time ranges
    try {
      GetTotalPendingScheduledJobsResponse result = apiInstance.getTotalPendingScheduledJobs(xCorrelationId, startTime, endTime, interval);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getTotalPendingScheduledJobs");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **interval** | **Long**| Interval in seconds for output time ranges | [optional]

### Return type

[**GetTotalPendingScheduledJobsResponse**](GetTotalPendingScheduledJobsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getWorkRequest"></a>
# **getWorkRequest**
> GetTaskWorkRequestResponse getWorkRequest(workRequestID, xCorrelationId)

This provides detail of workrequest

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID workRequestID = new UUID(); // UUID | ID of Work request
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetTaskWorkRequestResponse result = apiInstance.getWorkRequest(workRequestID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#getWorkRequest");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workRequestID** | [**UUID**](.md)| ID of Work request |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetTaskWorkRequestResponse**](GetTaskWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="launchJobTemplate"></a>
# **launchJobTemplate**
> LaunchJobTemplateResponse launchJobTemplate(templateID, launchJobTemplateRequest, xCorrelationId)

This launch a job based on the given job template

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String templateID = "templateID_example"; // String | ID of Job
    LaunchJobTemplateRequest launchJobTemplateRequest = new LaunchJobTemplateRequest(); // LaunchJobTemplateRequest | Launch Job Template API
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      LaunchJobTemplateResponse result = apiInstance.launchJobTemplate(templateID, launchJobTemplateRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#launchJobTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
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

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="pushContentToEndpoint"></a>
# **pushContentToEndpoint**
> CreateJobResponse pushContentToEndpoint(endpoint, body, xCorrelationId)

Whatever is posted to this endpoint will be added to the child input folder(s) for the task_routes that have this endpoint.  If more than one task_routes have this endpoint, it will be added to all child input folders.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID endpoint = new UUID(); // UUID | Endpoint UUID to push this chunk towards
    String body = "body_example"; // String | How to push content into a child input folder(s).
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      CreateJobResponse result = apiInstance.pushContentToEndpoint(endpoint, body, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#pushContentToEndpoint");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **endpoint** | [**UUID**](.md)| Endpoint UUID to push this chunk towards |
 **body** | **String**| How to push content into a child input folder(s). |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**CreateJobResponse**](CreateJobResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json, application/octet-stream, audio/_*, image/_*, text/html, text/plain, text/xml, video/_*
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="recheckJobStatus"></a>
# **recheckJobStatus**
> RecheckJobStatusResponse recheckJobStatus(jobID, xCorrelationId)

Recheck Job Status

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    UUID jobID = new UUID(); // UUID | ID of Job
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      RecheckJobStatusResponse result = apiInstance.recheckJobStatus(jobID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#recheckJobStatus");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobID** | [**UUID**](.md)| ID of Job |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**RecheckJobStatusResponse**](RecheckJobStatusResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="tasksStatusExport"></a>
# **tasksStatusExport**
> File tasksStatusExport(xCorrelationId, startTime, endTime, offset, limit, orderBy, direction, status, organizationID, taskID, coreTaskID, errorType, jobID, coreJobID, engineID, mediaSourceID, recordingID, engineCategoryID, modifiedBefore, modifiedAfter, createdBefore, createdAfter, backlog, alloc)

Export a task status report as a excel file

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    Long offset = 56L; // Long | the number of data to skip before getting the result set
    Long limit = 10lL; // Long | the number of items to return.
    String orderBy = "\"createdDateTime\""; // String | the field to sort
    String direction = "\"DESC\""; // String | the sort order.  ASC or DESC.
    TaskStatusEnum status = new TaskStatusEnum(); // TaskStatusEnum | Filtering by task Status
    String organizationID = "organizationID_example"; // String | Filter by organization id
    String taskID = "taskID_example"; // String | Filter by task id
    String coreTaskID = "coreTaskID_example"; // String | Filter by coreTaskID
    FailureReasonEnum errorType = new FailureReasonEnum(); // FailureReasonEnum | filter by errorType (failureReason)
    String jobID = "jobID_example"; // String | Filter by job id
    String coreJobID = "coreJobID_example"; // String | Filter by coreJobID
    String engineID = "engineID_example"; // String | Filter by engine id
    String mediaSourceID = "mediaSourceID_example"; // String | Filter by media source id
    Long recordingID = 56L; // Long | Filter tasks by the recording id
    UUID engineCategoryID = new UUID(); // UUID | Filtering by engineCategoryID
    Long modifiedBefore = 56L; // Long | Filter by items modified before expressed as timestamp
    Long modifiedAfter = 56L; // Long | Filter by items modified after expressed as timestamp
    Long createdBefore = 56L; // Long | Filter items where created date is before this date
    Long createdAfter = 56L; // Long | Filter items where created date is after this date
    Boolean backlog = true; // Boolean | Filtering all tasks in backlog
    Boolean alloc = true; // Boolean | Filtering all tasks have alloc = true or not
    try {
      File result = apiInstance.tasksStatusExport(xCorrelationId, startTime, endTime, offset, limit, orderBy, direction, status, organizationID, taskID, coreTaskID, errorType, jobID, coreJobID, engineID, mediaSourceID, recordingID, engineCategoryID, modifiedBefore, modifiedAfter, createdBefore, createdAfter, backlog, alloc);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#tasksStatusExport");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **offset** | **Long**| the number of data to skip before getting the result set | [optional]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10l]
 **orderBy** | **String**| the field to sort | [optional] [default to &quot;createdDateTime&quot;]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &quot;DESC&quot;]
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] [enum: pending, queued, aborted, failed, complete, running, scheduled, rejected, reprocessing]
 **organizationID** | **String**| Filter by organization id | [optional]
 **taskID** | **String**| Filter by task id | [optional]
 **coreTaskID** | **String**| Filter by coreTaskID | [optional]
 **errorType** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] [enum: internal_error, unknown, connection, rate_limited, unauthorized, api, resources, not_found, core_api, bad_data, scheduling, none]
 **jobID** | **String**| Filter by job id | [optional]
 **coreJobID** | **String**| Filter by coreJobID | [optional]
 **engineID** | **String**| Filter by engine id | [optional]
 **mediaSourceID** | **String**| Filter by media source id | [optional]
 **recordingID** | **Long**| Filter tasks by the recording id | [optional]
 **engineCategoryID** | [**UUID**](.md)| Filtering by engineCategoryID | [optional]
 **modifiedBefore** | **Long**| Filter by items modified before expressed as timestamp | [optional]
 **modifiedAfter** | **Long**| Filter by items modified after expressed as timestamp | [optional]
 **createdBefore** | **Long**| Filter items where created date is before this date | [optional]
 **createdAfter** | **Long**| Filter items where created date is after this date | [optional]
 **backlog** | **Boolean**| Filtering all tasks in backlog | [optional]
 **alloc** | **Boolean**| Filtering all tasks have alloc &#x3D; true or not | [optional]

### Return type

[**File**](File.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="updateTaskStatus"></a>
# **updateTaskStatus**
> TasksStatusUpdateResponse updateTaskStatus(tasksStatusUpdateRequest, xCorrelationId)

This updates the status for a bulk of tasks by taskID

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ProcessApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    ProcessApi apiInstance = new ProcessApi(defaultClient);
    TasksStatusUpdateRequest tasksStatusUpdateRequest = new TasksStatusUpdateRequest(); // TasksStatusUpdateRequest | The input for updateTaskStatus
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      TasksStatusUpdateResponse result = apiInstance.updateTaskStatus(tasksStatusUpdateRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProcessApi#updateTaskStatus");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
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

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

