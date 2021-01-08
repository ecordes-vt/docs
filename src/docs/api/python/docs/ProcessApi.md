# client.ProcessApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_task**](ProcessApi.md#add_task) | **POST** /proc/job/{JobID}/addtask | Adds a Task to a current job
[**add_task_route**](ProcessApi.md#add_task_route) | **POST** /proc/job/{JobID}/addtaskroute | Adds a Task Route to a current job
[**create_job**](ProcessApi.md#create_job) | **POST** /proc/job/create | This creates a new Job
[**delete_job**](ProcessApi.md#delete_job) | **POST** /proc/job/{JobID}/delete | This API deletes the specified job
[**delete_task**](ProcessApi.md#delete_task) | **POST** /proc/task/{TaskID}/delete | This API deletes the specified task
[**get_engine_error_time_ranges**](ProcessApi.md#get_engine_error_time_ranges) | **GET** /proc/tasks/error/engine_error_time_ranges | This gets engine error count by error tasks grouped by time ranges and sorted by a range start time
[**get_job_detail**](ProcessApi.md#get_job_detail) | **GET** /proc/job/{JobID}/detail | Gets Job Detail
[**get_job_download**](ProcessApi.md#get_job_download) | **GET** /proc/job/{JobID}/download/{JobOutputName} | Returns the contents of the job&#39;s output
[**get_job_output**](ProcessApi.md#get_job_output) | **GET** /proc/job/{JobID}/output/{JobOutputName} | Returns the contents of the job&#39;s output
[**get_job_outputs**](ProcessApi.md#get_job_outputs) | **GET** /proc/job/{JobID}/outputs | Returns a list of output information about this job
[**get_job_performance**](ProcessApi.md#get_job_performance) | **GET** /proc/job/{JobID}/performance | This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time
[**get_job_status**](ProcessApi.md#get_job_status) | **GET** /proc/job/{JobID}/status | Gets Job Status
[**get_job_work_requests**](ProcessApi.md#get_job_work_requests) | **GET** /proc/job/{JobID}/workrequests | This provides a list of workrequests of a job
[**get_jobs**](ProcessApi.md#get_jobs) | **GET** /proc/jobs | This gets a list of jobs
[**get_jobs_organization_stats**](ProcessApi.md#get_jobs_organization_stats) | **GET** /proc/jobs/stats/organization | This gets processing stats of the jobs by organization
[**get_jobs_performance**](ProcessApi.md#get_jobs_performance) | **GET** /proc/jobs/performance | This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time
[**get_jobs_stats**](ProcessApi.md#get_jobs_stats) | **GET** /proc/jobs/stats | This gets processing stats of the jobs
[**get_jobs_time_ranges_stats**](ProcessApi.md#get_jobs_time_ranges_stats) | **GET** /proc/jobs/stats/time_ranges | This gets processing stats of the jobs grouped by time ranges and sorted by a range start time
[**get_rate_pending_scheduled_jobs**](ProcessApi.md#get_rate_pending_scheduled_jobs) | **GET** /proc/scheduled_jobs/rate_pending_time_ranges | This gets the rate of pending scheduled jobs by time ranges
[**get_scheduled_job_detail**](ProcessApi.md#get_scheduled_job_detail) | **GET** /proc/scheduled_job/{ScheduledJobID}/detail | This gets scheduled job detail
[**get_scheduled_jobs**](ProcessApi.md#get_scheduled_jobs) | **GET** /proc/scheduled_jobs | This gets a list of scheduled jobs
[**get_server_error_counts**](ProcessApi.md#get_server_error_counts) | **GET** /proc/tasks/error/server_error_counts | Get server error counts in a time-range
[**get_task_detail**](ProcessApi.md#get_task_detail) | **GET** /proc/task/{TaskID}/detail | Gets Task Detail
[**get_task_download**](ProcessApi.md#get_task_download) | **GET** /proc/task/{TaskID}/download/{TaskOutputName} | Returns the contents of the task&#39;s output
[**get_task_logs**](ProcessApi.md#get_task_logs) | **GET** /proc/task/{TaskID}/logs | Gets logs associated with a task
[**get_task_output**](ProcessApi.md#get_task_output) | **GET** /proc/task/{TaskID}/output/{TaskOutputName} | Returns the contents of the task&#39;s output
[**get_task_outputs**](ProcessApi.md#get_task_outputs) | **GET** /proc/task/{TaskID}/outputs | Gets Task Output
[**get_task_sync_backlog**](ProcessApi.md#get_task_sync_backlog) | **GET** /proc/tasks/sync_backlog | Gets task sync backlog in a time-range
[**get_tasks**](ProcessApi.md#get_tasks) | **GET** /proc/tasks | This gets a list of tasks based on the provided criteria
[**get_tasks_error_type_count_by_engine**](ProcessApi.md#get_tasks_error_type_count_by_engine) | **GET** /proc/tasks/error/count_type_by_engine | This gets error type count by engines
[**get_tasks_errors**](ProcessApi.md#get_tasks_errors) | **GET** /proc/tasks/errors | This provides a error list in a time range
[**get_tasks_instances**](ProcessApi.md#get_tasks_instances) | **GET** /proc/tasks/instances/by_category_host | This gets processing stats of the tasks
[**get_tasks_stats**](ProcessApi.md#get_tasks_stats) | **GET** /proc/tasks/stats | This gets processing stats of the tasks
[**get_tasks_stats_categories**](ProcessApi.md#get_tasks_stats_categories) | **GET** /proc/tasks/stats/categories | This gets processing stats of the tasks grouped by engine categories
[**get_tasks_stats_engines**](ProcessApi.md#get_tasks_stats_engines) | **GET** /proc/tasks/stats/engines | This gets processing stats of the tasks grouped by engine
[**get_tasks_stats_organizations**](ProcessApi.md#get_tasks_stats_organizations) | **GET** /proc/tasks/stats/organizations | This gets processing stats of the tasks grouped by engine, filter by organizations
[**get_tasks_stats_time_ranges**](ProcessApi.md#get_tasks_stats_time_ranges) | **GET** /proc/tasks/stats/time_ranges | This gets processing stats of the tasks grouped by time ranges and sorted by a range start time
[**get_total_pending_scheduled_jobs**](ProcessApi.md#get_total_pending_scheduled_jobs) | **GET** /proc/scheduled_jobs/total_pending_time_ranges | This gets the total pending scheduled jobs by time ranges
[**get_work_request**](ProcessApi.md#get_work_request) | **GET** /proc/workrequest/{WorkRequestID}/detail | This provides detail of workrequest
[**launch_job_template**](ProcessApi.md#launch_job_template) | **POST** /proc/template/{TemplateID}/launch | This launch a job based on the given job template
[**push_content_to_endpoint**](ProcessApi.md#push_content_to_endpoint) | **POST** /proc/endpoint/{Endpoint} | Whatever is posted to this endpoint will be added to the child input folder(s) for the task_routes that have this endpoint.  If more than one task_routes have this endpoint, it will be added to all child input folders.
[**recheck_job_status**](ProcessApi.md#recheck_job_status) | **GET** /proc/job/{JobID}/recheck_status | Recheck Job Status
[**tasks_status_export**](ProcessApi.md#tasks_status_export) | **GET** /proc/tasks/stats/export | Export a task status report as a excel file
[**update_task_status**](ProcessApi.md#update_task_status) | **POST** /proc/tasks/update_status | This updates the status for a bulk of tasks by taskID


# **add_task**
> AddTaskResponse add_task(job_id, add_task_request, x_correlation_id=x_correlation_id)

Adds a Task to a current job

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    job_id = 'job_id_example' # str | ID of Job
add_task_request = client.AddTaskRequest() # AddTaskRequest | Create Job API
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Adds a Task to a current job
        api_response = api_instance.add_task(job_id, add_task_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->add_task: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | [**str**](.md)| ID of Job | 
 **add_task_request** | [**AddTaskRequest**](AddTaskRequest.md)| Create Job API | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_task_route**
> AddTaskRouteResponse add_task_route(job_id, add_task_route_request, x_correlation_id=x_correlation_id)

Adds a Task Route to a current job

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    job_id = 'job_id_example' # str | ID of Job
add_task_route_request = client.AddTaskRouteRequest() # AddTaskRouteRequest | Adds a Task Route
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Adds a Task Route to a current job
        api_response = api_instance.add_task_route(job_id, add_task_route_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->add_task_route: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | [**str**](.md)| ID of Job | 
 **add_task_route_request** | [**AddTaskRouteRequest**](AddTaskRouteRequest.md)| Adds a Task Route | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_job**
> CreateJobResponse create_job(create_job_request, x_correlation_id=x_correlation_id)

This creates a new Job

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    create_job_request = client.CreateJobRequest() # CreateJobRequest | Create Job API
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This creates a new Job
        api_response = api_instance.create_job(create_job_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->create_job: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_job_request** | [**CreateJobRequest**](CreateJobRequest.md)| Create Job API | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_job**
> AdminOperationResponse delete_job(job_id, x_correlation_id=x_correlation_id, delete_job_request=delete_job_request)

This API deletes the specified job

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    job_id = 'job_id_example' # str | ID of Job
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
delete_job_request = client.DeleteJobRequest() # DeleteJobRequest | Request information to delete the specified job (optional)

    try:
        # This API deletes the specified job
        api_response = api_instance.delete_job(job_id, x_correlation_id=x_correlation_id, delete_job_request=delete_job_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->delete_job: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | [**str**](.md)| ID of Job | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **delete_job_request** | [**DeleteJobRequest**](DeleteJobRequest.md)| Request information to delete the specified job | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_task**
> AdminOperationResponse delete_task(task_id, x_correlation_id=x_correlation_id)

This API deletes the specified task

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    task_id = 'task_id_example' # str | ID of Task
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API deletes the specified task
        api_response = api_instance.delete_task(task_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->delete_task: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **task_id** | [**str**](.md)| ID of Task | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_engine_error_time_ranges**
> GetEngineErrorTimeRangesResponse get_engine_error_time_ranges(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, chart_type=chart_type, interval=interval, engine_id=engine_id)

This gets engine error count by error tasks grouped by time ranges and sorted by a range start time

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
chart_type = client.EngineErrorChartTypeEnum() # EngineErrorChartTypeEnum | It will help API to kmow the response should return (optional)
interval = 56 # int | Interval in seconds for output time ranges (optional)
engine_id = 'engine_id_example' # str | Filtering by engineID (optional)

    try:
        # This gets engine error count by error tasks grouped by time ranges and sorted by a range start time
        api_response = api_instance.get_engine_error_time_ranges(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, chart_type=chart_type, interval=interval, engine_id=engine_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_engine_error_time_ranges: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **chart_type** | [**EngineErrorChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] 
 **interval** | **int**| Interval in seconds for output time ranges | [optional] 
 **engine_id** | [**str**](.md)| Filtering by engineID | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_job_detail**
> GetJobDetailResponse get_job_detail(job_id, x_correlation_id=x_correlation_id)

Gets Job Detail

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    job_id = 'job_id_example' # str | ID of Job
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Gets Job Detail
        api_response = api_instance.get_job_detail(job_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_job_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | [**str**](.md)| ID of Job | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_job_download**
> list[str] get_job_download(job_id, job_output_name, x_correlation_id=x_correlation_id)

Returns the contents of the job's output

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    job_id = 'job_id_example' # str | ID of Job
job_output_name = 'job_output_name_example' # str | Name of the job output, e.g. vtn-standard.json
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Returns the contents of the job's output
        api_response = api_instance.get_job_download(job_id, job_output_name, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_job_download: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | [**str**](.md)| ID of Job | 
 **job_output_name** | **str**| Name of the job output, e.g. vtn-standard.json | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

**list[str]**

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_job_output**
> GetJobOutputResponse get_job_output(job_id, job_output_name, x_correlation_id=x_correlation_id)

Returns the contents of the job's output

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    job_id = 'job_id_example' # str | ID of Job
job_output_name = 'job_output_name_example' # str | Name of the job output, e.g. vtn-standard.json
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Returns the contents of the job's output
        api_response = api_instance.get_job_output(job_id, job_output_name, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_job_output: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | [**str**](.md)| ID of Job | 
 **job_output_name** | **str**| Name of the job output, e.g. vtn-standard.json | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_job_outputs**
> GetJobOutputsResponse get_job_outputs(job_id, x_correlation_id=x_correlation_id)

Returns a list of output information about this job

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    job_id = 'job_id_example' # str | ID of Job
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Returns a list of output information about this job
        api_response = api_instance.get_job_outputs(job_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_job_outputs: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | [**str**](.md)| ID of Job | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_job_performance**
> GetJobPerformanceResponse get_job_performance(job_id, x_correlation_id=x_correlation_id, interval=interval, task_id=task_id, work_request_id=work_request_id)

This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    job_id = 'job_id_example' # str | ID of Job
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
interval = 56 # int | Interval in seconds for output time ranges (optional)
task_id = 'task_id_example' # str | Filter data by taskID (optional)
work_request_id = 'work_request_id_example' # str | Filter data by workRequestID (optional)

    try:
        # This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time
        api_response = api_instance.get_job_performance(job_id, x_correlation_id=x_correlation_id, interval=interval, task_id=task_id, work_request_id=work_request_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_job_performance: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | [**str**](.md)| ID of Job | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **interval** | **int**| Interval in seconds for output time ranges | [optional] 
 **task_id** | [**str**](.md)| Filter data by taskID | [optional] 
 **work_request_id** | [**str**](.md)| Filter data by workRequestID | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_job_status**
> GetJobStatusResponse get_job_status(job_id, x_correlation_id=x_correlation_id)

Gets Job Status

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    job_id = 'job_id_example' # str | ID of Job
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Gets Job Status
        api_response = api_instance.get_job_status(job_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_job_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | [**str**](.md)| ID of Job | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_job_work_requests**
> GetJobWorkRequestResponse get_job_work_requests(job_id, x_correlation_id=x_correlation_id, offset=offset, limit=limit, order_by=order_by, direction=direction, status=status, task_id=task_id)

This provides a list of workrequests of a job

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    job_id = 'job_id_example' # str | ID of Job
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
offset = 56 # int | the number of records to skip before getting the result set (optional)
limit = 100 # int | the number of records to return. (optional) (default to 100)
order_by = 'createdDateTime' # str | the field to sort. It should be in [createdDateTime, modifiedDateTime] (optional) (default to 'createdDateTime')
direction = 'DESC' # str | the sort order (optional) (default to 'DESC')
status = 'status_example' # str | the value should be in [active, trial, inactive, deleted] (optional)
task_id = 'task_id_example' # str | This is an internal task ID to get work request (optional)

    try:
        # This provides a list of workrequests of a job
        api_response = api_instance.get_job_work_requests(job_id, x_correlation_id=x_correlation_id, offset=offset, limit=limit, order_by=order_by, direction=direction, status=status, task_id=task_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_job_work_requests: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | [**str**](.md)| ID of Job | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **offset** | **int**| the number of records to skip before getting the result set | [optional] 
 **limit** | **int**| the number of records to return. | [optional] [default to 100]
 **order_by** | **str**| the field to sort. It should be in [createdDateTime, modifiedDateTime] | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **str**| the sort order | [optional] [default to &#39;DESC&#39;]
 **status** | **str**| the value should be in [active, trial, inactive, deleted] | [optional] 
 **task_id** | **str**| This is an internal task ID to get work request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_jobs**
> GetJobListResponse get_jobs(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, offset=offset, limit=limit, order_by=order_by, direction=direction, core_id=core_id, organization_id=organization_id, recording_id=recording_id, job_id=job_id, core_job_id=core_job_id, modified_before=modified_before, modified_after=modified_after, created_before=created_before, created_after=created_after)

This gets a list of jobs

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
status = client.JobStatusEnum() # JobStatusEnum | If specified, this limits the jobs or tasks to follow status (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
order_by = 'createdDateTime' # str | the field to sort (optional) (default to 'createdDateTime')
direction = 'DESC' # str | the sort order.  ASC or DESC. (optional) (default to 'DESC')
core_id = 'core_id_example' # str | Filter by coreID (optional)
organization_id = 'organization_id_example' # str | Filter by organizationID (optional)
recording_id = 'recording_id_example' # str | Filter by recordingID (optional)
job_id = 'job_id_example' # str | Filter by jobID (optional)
core_job_id = 'core_job_id_example' # str | Filter by coreJobID (optional)
modified_before = 56 # int | Filter by items modified before expressed as timestamp (optional)
modified_after = 56 # int | Filter by items modified after expressed as timestamp (optional)
created_before = 56 # int | Filter items where created date is before this date (optional)
created_after = 56 # int | Filter items where created date is after this date (optional)

    try:
        # This gets a list of jobs
        api_response = api_instance.get_jobs(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, offset=offset, limit=limit, order_by=order_by, direction=direction, core_id=core_id, organization_id=organization_id, recording_id=recording_id, job_id=job_id, core_job_id=core_job_id, modified_before=modified_before, modified_after=modified_after, created_before=created_before, created_after=created_after)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_jobs: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**JobStatusEnum**](.md)| If specified, this limits the jobs or tasks to follow status | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **order_by** | **str**| the field to sort | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **str**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **core_id** | [**str**](.md)| Filter by coreID | [optional] 
 **organization_id** | [**str**](.md)| Filter by organizationID | [optional] 
 **recording_id** | [**str**](.md)| Filter by recordingID | [optional] 
 **job_id** | [**str**](.md)| Filter by jobID | [optional] 
 **core_job_id** | **str**| Filter by coreJobID | [optional] 
 **modified_before** | **int**| Filter by items modified before expressed as timestamp | [optional] 
 **modified_after** | **int**| Filter by items modified after expressed as timestamp | [optional] 
 **created_before** | **int**| Filter items where created date is before this date | [optional] 
 **created_after** | **int**| Filter items where created date is after this date | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_jobs_organization_stats**
> GetJobsOrganizationStatsResponse get_jobs_organization_stats(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, organization_i_ds=organization_i_ds)

This gets processing stats of the jobs by organization

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
organization_i_ds = 'organization_i_ds_example' # str |  (optional)

    try:
        # This gets processing stats of the jobs by organization
        api_response = api_instance.get_jobs_organization_stats(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, organization_i_ds=organization_i_ds)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_jobs_organization_stats: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **organization_i_ds** | **str**|  | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_jobs_performance**
> GetJobsPerformanceResponse get_jobs_performance(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, interval=interval)

This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
interval = 56 # int | Interval in seconds for output time ranges (optional)

    try:
        # This gets cpu/gpu, memory state of the hosts grouped by time ranges and sorted by a range start time
        api_response = api_instance.get_jobs_performance(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, interval=interval)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_jobs_performance: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **interval** | **int**| Interval in seconds for output time ranges | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_jobs_stats**
> GetJobsStatsResponse get_jobs_stats(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, chart_type=chart_type, status=status, organization_i_ds=organization_i_ds)

This gets processing stats of the jobs

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
chart_type = client.JobTaskStatusChartTypeEnum() # JobTaskStatusChartTypeEnum | It will help API to kmow the response should return (optional)
status = client.JobStatusEnum() # JobStatusEnum | If specified, this limits the jobs or tasks to follow status (optional)
organization_i_ds = 'organization_i_ds_example' # str |  (optional)

    try:
        # This gets processing stats of the jobs
        api_response = api_instance.get_jobs_stats(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, chart_type=chart_type, status=status, organization_i_ds=organization_i_ds)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_jobs_stats: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **chart_type** | [**JobTaskStatusChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] 
 **status** | [**JobStatusEnum**](.md)| If specified, this limits the jobs or tasks to follow status | [optional] 
 **organization_i_ds** | **str**|  | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_jobs_time_ranges_stats**
> GetJobsTimeRangesStatsResponse get_jobs_time_ranges_stats(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, interval=interval, organization_i_ds=organization_i_ds, engine_category_id=engine_category_id)

This gets processing stats of the jobs grouped by time ranges and sorted by a range start time

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
status = client.JobStatusEnum() # JobStatusEnum | If specified, this limits the jobs or tasks to follow status (optional)
interval = 56 # int | Interval in seconds for output time ranges (optional)
organization_i_ds = 'organization_i_ds_example' # str |  (optional)
engine_category_id = 'engine_category_id_example' # str |  (optional)

    try:
        # This gets processing stats of the jobs grouped by time ranges and sorted by a range start time
        api_response = api_instance.get_jobs_time_ranges_stats(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, interval=interval, organization_i_ds=organization_i_ds, engine_category_id=engine_category_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_jobs_time_ranges_stats: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**JobStatusEnum**](.md)| If specified, this limits the jobs or tasks to follow status | [optional] 
 **interval** | **int**| Interval in seconds for output time ranges | [optional] 
 **organization_i_ds** | **str**|  | [optional] 
 **engine_category_id** | [**str**](.md)|  | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_rate_pending_scheduled_jobs**
> GetRatePendingScheduledJobsResponse get_rate_pending_scheduled_jobs(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, interval=interval)

This gets the rate of pending scheduled jobs by time ranges

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
interval = 56 # int | Interval in seconds for output time ranges (optional)

    try:
        # This gets the rate of pending scheduled jobs by time ranges
        api_response = api_instance.get_rate_pending_scheduled_jobs(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, interval=interval)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_rate_pending_scheduled_jobs: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **interval** | **int**| Interval in seconds for output time ranges | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_scheduled_job_detail**
> GetScheduledJobDetailResponse get_scheduled_job_detail(scheduled_job_id, x_correlation_id=x_correlation_id)

This gets scheduled job detail

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    scheduled_job_id = 'scheduled_job_id_example' # str | ID of Scheduled Job. It can be an internal ID or core ID
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This gets scheduled job detail
        api_response = api_instance.get_scheduled_job_detail(scheduled_job_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_scheduled_job_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scheduled_job_id** | [**str**](.md)| ID of Scheduled Job. It can be an internal ID or core ID | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_scheduled_jobs**
> GetScheduledJobsResponse get_scheduled_jobs(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, offset=offset, limit=limit, direction=direction, scheduled_job_id=scheduled_job_id, internal_organization_id=internal_organization_id, core_id=core_id, start_start_time=start_start_time, end_start_time=end_start_time, start_stop_time=start_stop_time, end_stop_time=end_stop_time, is_active=is_active, run_mode=run_mode, source_id=source_id, source_type=source_type, order_by=order_by, scheduled_job_name=scheduled_job_name)

This gets a list of scheduled jobs

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
direction = 'DESC' # str | the sort order.  ASC or DESC. (optional) (default to 'DESC')
scheduled_job_id = 'scheduled_job_id_example' # str | Filter by internal scheduled Job ID(uuid) or core scheduled Job ID (integer) (optional)
internal_organization_id = 'internal_organization_id_example' # str | Filter by internal organization id (optional)
core_id = 'core_id_example' # str | Filter by coreID (optional)
start_start_time = 56 # int |  (optional)
end_start_time = 56 # int |  (optional)
start_stop_time = 56 # int |  (optional)
end_stop_time = 56 # int |  (optional)
is_active = True # bool |  (optional)
run_mode = client.ScheduleRunModeEnum() # ScheduleRunModeEnum | Filter by runMode (optional)
source_id = 56 # int |  (optional)
source_type = 'source_type_example' # str |  (optional)
order_by = 'order_by_example' # str | The value should be in [organizationID, runMode, createdTime, startTime, stopTime] (optional)
scheduled_job_name = 'scheduled_job_name_example' # str |  (optional)

    try:
        # This gets a list of scheduled jobs
        api_response = api_instance.get_scheduled_jobs(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, offset=offset, limit=limit, direction=direction, scheduled_job_id=scheduled_job_id, internal_organization_id=internal_organization_id, core_id=core_id, start_start_time=start_start_time, end_start_time=end_start_time, start_stop_time=start_stop_time, end_stop_time=end_stop_time, is_active=is_active, run_mode=run_mode, source_id=source_id, source_type=source_type, order_by=order_by, scheduled_job_name=scheduled_job_name)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_scheduled_jobs: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **direction** | **str**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **scheduled_job_id** | **str**| Filter by internal scheduled Job ID(uuid) or core scheduled Job ID (integer) | [optional] 
 **internal_organization_id** | [**str**](.md)| Filter by internal organization id | [optional] 
 **core_id** | [**str**](.md)| Filter by coreID | [optional] 
 **start_start_time** | **int**|  | [optional] 
 **end_start_time** | **int**|  | [optional] 
 **start_stop_time** | **int**|  | [optional] 
 **end_stop_time** | **int**|  | [optional] 
 **is_active** | **bool**|  | [optional] 
 **run_mode** | [**ScheduleRunModeEnum**](.md)| Filter by runMode | [optional] 
 **source_id** | **int**|  | [optional] 
 **source_type** | **str**|  | [optional] 
 **order_by** | **str**| The value should be in [organizationID, runMode, createdTime, startTime, stopTime] | [optional] 
 **scheduled_job_name** | **str**|  | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_error_counts**
> GetServerErrorCountsResponse get_server_error_counts(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, chart_type=chart_type, service=service, interval=interval)

Get server error counts in a time-range

### Example

```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)


# Enter a context with an instance of the API client
with client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
chart_type = client.ServerErrorChartTypeEnum() # ServerErrorChartTypeEnum | It will help API to kmow the response should return (optional)
service = 'service_example' # str | Filter data by service name. (optional)
interval = 56 # int | Interval in seconds for output time ranges (optional)

    try:
        # Get server error counts in a time-range
        api_response = api_instance.get_server_error_counts(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, chart_type=chart_type, service=service, interval=interval)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_server_error_counts: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **chart_type** | [**ServerErrorChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] 
 **service** | **str**| Filter data by service name. | [optional] 
 **interval** | **int**| Interval in seconds for output time ranges | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_task_detail**
> GetTaskDetailResponse get_task_detail(task_id, x_correlation_id=x_correlation_id)

Gets Task Detail

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    task_id = 'task_id_example' # str | ID of Task
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Gets Task Detail
        api_response = api_instance.get_task_detail(task_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_task_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **task_id** | [**str**](.md)| ID of Task | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_task_download**
> list[Byte] get_task_download(task_id, task_output_name, x_correlation_id=x_correlation_id)

Returns the contents of the task's output

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    task_id = 'task_id_example' # str | ID of Task
task_output_name = 'task_output_name_example' # str | Name of the task output, e.g. vtn-standard.json
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Returns the contents of the task's output
        api_response = api_instance.get_task_download(task_id, task_output_name, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_task_download: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **task_id** | [**str**](.md)| ID of Task | 
 **task_output_name** | **str**| Name of the task output, e.g. vtn-standard.json | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**list[Byte]**](Byte.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_task_logs**
> file get_task_logs(task_id, x_correlation_id=x_correlation_id)

Gets logs associated with a task

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    task_id = 'task_id_example' # str | ID of Task
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Gets logs associated with a task
        api_response = api_instance.get_task_logs(task_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_task_logs: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **task_id** | [**str**](.md)| ID of Task | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

**file**

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_task_output**
> GetTaskOutputResponse get_task_output(task_id, task_output_name, x_correlation_id=x_correlation_id)

Returns the contents of the task's output

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    task_id = 'task_id_example' # str | ID of Task
task_output_name = 'task_output_name_example' # str | Name of the task output, e.g. vtn-standard.json
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Returns the contents of the task's output
        api_response = api_instance.get_task_output(task_id, task_output_name, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_task_output: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **task_id** | [**str**](.md)| ID of Task | 
 **task_output_name** | **str**| Name of the task output, e.g. vtn-standard.json | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_task_outputs**
> GetTaskOutputsResponse get_task_outputs(task_id, x_correlation_id=x_correlation_id)

Gets Task Output

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    task_id = 'task_id_example' # str | ID of Task
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Gets Task Output
        api_response = api_instance.get_task_outputs(task_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_task_outputs: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **task_id** | [**str**](.md)| ID of Task | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_task_sync_backlog**
> GetTaskSyncBacklogResponse get_task_sync_backlog(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, interval=interval)

Gets task sync backlog in a time-range

### Example

```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)


# Enter a context with an instance of the API client
with client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
interval = 56 # int | Interval in seconds for output time ranges (optional)

    try:
        # Gets task sync backlog in a time-range
        api_response = api_instance.get_task_sync_backlog(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, interval=interval)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_task_sync_backlog: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **interval** | **int**| Interval in seconds for output time ranges | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_tasks**
> GetTasksResponse get_tasks(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, offset=offset, limit=limit, order_by=order_by, direction=direction, status=status, organization_id=organization_id, task_id=task_id, core_task_id=core_task_id, error_type=error_type, job_id=job_id, core_job_id=core_job_id, engine_id=engine_id, media_source_id=media_source_id, recording_id=recording_id, engine_category_id=engine_category_id, modified_before=modified_before, modified_after=modified_after, created_before=created_before, created_after=created_after, backlog=backlog, alloc=alloc)

This gets a list of tasks based on the provided criteria

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
order_by = 'createdDateTime' # str | the field to sort (optional) (default to 'createdDateTime')
direction = 'DESC' # str | the sort order.  ASC or DESC. (optional) (default to 'DESC')
status = client.TaskStatusEnum() # TaskStatusEnum | Filtering by task Status (optional)
organization_id = 'organization_id_example' # str | Filter by organization id (optional)
task_id = 'task_id_example' # str | Filter by task id (optional)
core_task_id = 'core_task_id_example' # str | Filter by coreTaskID (optional)
error_type = client.FailureReasonEnum() # FailureReasonEnum | filter by errorType (failureReason) (optional)
job_id = 'job_id_example' # str | Filter by job id (optional)
core_job_id = 'core_job_id_example' # str | Filter by coreJobID (optional)
engine_id = 'engine_id_example' # str | Filter by engine id (optional)
media_source_id = 'media_source_id_example' # str | Filter by media source id (optional)
recording_id = 56 # int | Filter tasks by the recording id (optional)
engine_category_id = 'engine_category_id_example' # str | Filtering by engineCategoryID (optional)
modified_before = 56 # int | Filter by items modified before expressed as timestamp (optional)
modified_after = 56 # int | Filter by items modified after expressed as timestamp (optional)
created_before = 56 # int | Filter items where created date is before this date (optional)
created_after = 56 # int | Filter items where created date is after this date (optional)
backlog = True # bool | Filtering all tasks in backlog (optional)
alloc = True # bool | Filtering all tasks have alloc = true or not (optional)

    try:
        # This gets a list of tasks based on the provided criteria
        api_response = api_instance.get_tasks(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, offset=offset, limit=limit, order_by=order_by, direction=direction, status=status, organization_id=organization_id, task_id=task_id, core_task_id=core_task_id, error_type=error_type, job_id=job_id, core_job_id=core_job_id, engine_id=engine_id, media_source_id=media_source_id, recording_id=recording_id, engine_category_id=engine_category_id, modified_before=modified_before, modified_after=modified_after, created_before=created_before, created_after=created_after, backlog=backlog, alloc=alloc)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_tasks: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **order_by** | **str**| the field to sort | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **str**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **organization_id** | **str**| Filter by organization id | [optional] 
 **task_id** | **str**| Filter by task id | [optional] 
 **core_task_id** | **str**| Filter by coreTaskID | [optional] 
 **error_type** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] 
 **job_id** | **str**| Filter by job id | [optional] 
 **core_job_id** | **str**| Filter by coreJobID | [optional] 
 **engine_id** | **str**| Filter by engine id | [optional] 
 **media_source_id** | **str**| Filter by media source id | [optional] 
 **recording_id** | **int**| Filter tasks by the recording id | [optional] 
 **engine_category_id** | [**str**](.md)| Filtering by engineCategoryID | [optional] 
 **modified_before** | **int**| Filter by items modified before expressed as timestamp | [optional] 
 **modified_after** | **int**| Filter by items modified after expressed as timestamp | [optional] 
 **created_before** | **int**| Filter items where created date is before this date | [optional] 
 **created_after** | **int**| Filter items where created date is after this date | [optional] 
 **backlog** | **bool**| Filtering all tasks in backlog | [optional] 
 **alloc** | **bool**| Filtering all tasks have alloc &#x3D; true or not | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_tasks_error_type_count_by_engine**
> GetTasksErrorTypeCountByEngineResponse get_tasks_error_type_count_by_engine(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, engine_id=engine_id, status=status, error_type=error_type)

This gets error type count by engines

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
engine_id = 'engine_id_example' # str | Filter by engine id (optional)
status = client.TaskStatusEnum() # TaskStatusEnum | Filtering by task Status (optional)
error_type = client.FailureReasonEnum() # FailureReasonEnum | filter by errorType (failureReason) (optional)

    try:
        # This gets error type count by engines
        api_response = api_instance.get_tasks_error_type_count_by_engine(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, engine_id=engine_id, status=status, error_type=error_type)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_tasks_error_type_count_by_engine: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **engine_id** | **str**| Filter by engine id | [optional] 
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **error_type** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_tasks_errors**
> GetTaskErrorsResponse get_tasks_errors(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, task_id=task_id, job_id=job_id, error_type=error_type, offset=offset, limit=limit, order_by=order_by, direction=direction)

This provides a error list in a time range

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
task_id = 'task_id_example' # str | filter by taskID (optional)
job_id = 'job_id_example' # str | filter by jobID (optional)
error_type = client.FailureReasonEnum() # FailureReasonEnum | filter by errorType (failureReason) (optional)
offset = 56 # int | the number of records to skip before getting the result set (optional)
limit = 100 # int | the number of records to return. (optional) (default to 100)
order_by = 'createdDateTime' # str | the field to sort. It should be in [createdDateTime, modifiedDateTime] (optional) (default to 'createdDateTime')
direction = 'DESC' # str | the sort order (optional) (default to 'DESC')

    try:
        # This provides a error list in a time range
        api_response = api_instance.get_tasks_errors(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, task_id=task_id, job_id=job_id, error_type=error_type, offset=offset, limit=limit, order_by=order_by, direction=direction)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_tasks_errors: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **task_id** | [**str**](.md)| filter by taskID | [optional] 
 **job_id** | [**str**](.md)| filter by jobID | [optional] 
 **error_type** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] 
 **offset** | **int**| the number of records to skip before getting the result set | [optional] 
 **limit** | **int**| the number of records to return. | [optional] [default to 100]
 **order_by** | **str**| the field to sort. It should be in [createdDateTime, modifiedDateTime] | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **str**| the sort order | [optional] [default to &#39;DESC&#39;]

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_tasks_instances**
> GetTasksInstancesResponse get_tasks_instances(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, engine_category_id=engine_category_id)

This gets processing stats of the tasks

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
status = client.EngineStatusEnum() # EngineStatusEnum | If specified, this limits the engine instances to follow status (optional)
engine_category_id = 'engine_category_id_example' # str |  (optional)

    try:
        # This gets processing stats of the tasks
        api_response = api_instance.get_tasks_instances(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, engine_category_id=engine_category_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_tasks_instances: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**EngineStatusEnum**](.md)| If specified, this limits the engine instances to follow status | [optional] 
 **engine_category_id** | [**str**](.md)|  | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_tasks_stats**
> GetTasksStatsResponse get_tasks_stats(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, chart_type=chart_type, status=status, organization_i_ds=organization_i_ds, engine_i_ds=engine_i_ds)

This gets processing stats of the tasks

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
chart_type = client.JobTaskStatusChartTypeEnum() # JobTaskStatusChartTypeEnum | It will help API to kmow the response should return (optional)
status = client.TaskStatusEnum() # TaskStatusEnum | Filtering by task Status (optional)
organization_i_ds = 'organization_i_ds_example' # str |  (optional)
engine_i_ds = 'engine_i_ds_example' # str |  (optional)

    try:
        # This gets processing stats of the tasks
        api_response = api_instance.get_tasks_stats(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, chart_type=chart_type, status=status, organization_i_ds=organization_i_ds, engine_i_ds=engine_i_ds)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_tasks_stats: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **chart_type** | [**JobTaskStatusChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] 
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **organization_i_ds** | [**str**](.md)|  | [optional] 
 **engine_i_ds** | [**str**](.md)|  | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_tasks_stats_categories**
> GetTasksCategoriesStatsResponse get_tasks_stats_categories(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, organization_i_ds=organization_i_ds, engine_category_id=engine_category_id)

This gets processing stats of the tasks grouped by engine categories

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
status = client.TaskStatusEnum() # TaskStatusEnum | Filtering by task Status (optional)
organization_i_ds = 'organization_i_ds_example' # str |  (optional)
engine_category_id = 'engine_category_id_example' # str |  (optional)

    try:
        # This gets processing stats of the tasks grouped by engine categories
        api_response = api_instance.get_tasks_stats_categories(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, organization_i_ds=organization_i_ds, engine_category_id=engine_category_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_tasks_stats_categories: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **organization_i_ds** | [**str**](.md)|  | [optional] 
 **engine_category_id** | [**str**](.md)|  | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_tasks_stats_engines**
> GetTasksEnginesStatsResponse get_tasks_stats_engines(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, organization_id=organization_id, task_id=task_id, error_type=error_type, job_id=job_id, engine_id=engine_id, media_source_id=media_source_id, recording_id=recording_id, engine_category_id=engine_category_id)

This gets processing stats of the tasks grouped by engine

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
status = client.TaskStatusEnum() # TaskStatusEnum | Filtering by task Status (optional)
organization_id = 'organization_id_example' # str | Filter by  organization id (optional)
task_id = 'task_id_example' # str | Filter by task id (optional)
error_type = client.FailureReasonEnum() # FailureReasonEnum | filter by errorType (failureReason) (optional)
job_id = 'job_id_example' # str | Filter by job id (optional)
engine_id = 'engine_id_example' # str | Filter by engine id (optional)
media_source_id = 'media_source_id_example' # str | Filter by media source id (optional)
recording_id = 56 # int | Filter tasks by the recording id (optional)
engine_category_id = 'engine_category_id_example' # str | Filtering by engineCategoryID (optional)

    try:
        # This gets processing stats of the tasks grouped by engine
        api_response = api_instance.get_tasks_stats_engines(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, organization_id=organization_id, task_id=task_id, error_type=error_type, job_id=job_id, engine_id=engine_id, media_source_id=media_source_id, recording_id=recording_id, engine_category_id=engine_category_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_tasks_stats_engines: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **organization_id** | **str**| Filter by  organization id | [optional] 
 **task_id** | **str**| Filter by task id | [optional] 
 **error_type** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] 
 **job_id** | **str**| Filter by job id | [optional] 
 **engine_id** | **str**| Filter by engine id | [optional] 
 **media_source_id** | **str**| Filter by media source id | [optional] 
 **recording_id** | **int**| Filter tasks by the recording id | [optional] 
 **engine_category_id** | [**str**](.md)| Filtering by engineCategoryID | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_tasks_stats_organizations**
> GetTasksStatsOrganizationsResponse get_tasks_stats_organizations(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, organization_i_ds=organization_i_ds, engine_id=engine_id)

This gets processing stats of the tasks grouped by engine, filter by organizations

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
status = client.TaskStatusEnum() # TaskStatusEnum | Filtering by task Status (optional)
organization_i_ds = 'organization_i_ds_example' # str | Filter by organization IDs (optional)
engine_id = 'engine_id_example' # str | Filter by engine ID (optional)

    try:
        # This gets processing stats of the tasks grouped by engine, filter by organizations
        api_response = api_instance.get_tasks_stats_organizations(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, organization_i_ds=organization_i_ds, engine_id=engine_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_tasks_stats_organizations: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **organization_i_ds** | [**str**](.md)| Filter by organization IDs | [optional] 
 **engine_id** | [**str**](.md)| Filter by engine ID | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_tasks_stats_time_ranges**
> GetTasksTimeRangesStatsResponse get_tasks_stats_time_ranges(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, interval=interval, engine_category_id=engine_category_id, organization_i_ds=organization_i_ds)

This gets processing stats of the tasks grouped by time ranges and sorted by a range start time

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
status = client.TaskStatusEnum() # TaskStatusEnum | Filtering by task Status (optional)
interval = 56 # int | Interval in seconds for output time ranges (optional)
engine_category_id = 'engine_category_id_example' # str | Filtering by engineCategoryID (optional)
organization_i_ds = 'organization_i_ds_example' # str |  (optional)

    try:
        # This gets processing stats of the tasks grouped by time ranges and sorted by a range start time
        api_response = api_instance.get_tasks_stats_time_ranges(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, status=status, interval=interval, engine_category_id=engine_category_id, organization_i_ds=organization_i_ds)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_tasks_stats_time_ranges: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **interval** | **int**| Interval in seconds for output time ranges | [optional] 
 **engine_category_id** | [**str**](.md)| Filtering by engineCategoryID | [optional] 
 **organization_i_ds** | **str**|  | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_total_pending_scheduled_jobs**
> GetTotalPendingScheduledJobsResponse get_total_pending_scheduled_jobs(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, interval=interval)

This gets the total pending scheduled jobs by time ranges

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
interval = 56 # int | Interval in seconds for output time ranges (optional)

    try:
        # This gets the total pending scheduled jobs by time ranges
        api_response = api_instance.get_total_pending_scheduled_jobs(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, interval=interval)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_total_pending_scheduled_jobs: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **interval** | **int**| Interval in seconds for output time ranges | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_work_request**
> GetTaskWorkRequestResponse get_work_request(work_request_id, x_correlation_id=x_correlation_id)

This provides detail of workrequest

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    work_request_id = 'work_request_id_example' # str | ID of Work request
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides detail of workrequest
        api_response = api_instance.get_work_request(work_request_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->get_work_request: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **work_request_id** | [**str**](.md)| ID of Work request | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **launch_job_template**
> LaunchJobTemplateResponse launch_job_template(template_id, launch_job_template_request, x_correlation_id=x_correlation_id)

This launch a job based on the given job template

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    template_id = 'template_id_example' # str | ID of Job
launch_job_template_request = client.LaunchJobTemplateRequest() # LaunchJobTemplateRequest | Launch Job Template API
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This launch a job based on the given job template
        api_response = api_instance.launch_job_template(template_id, launch_job_template_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->launch_job_template: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **template_id** | **str**| ID of Job | 
 **launch_job_template_request** | [**LaunchJobTemplateRequest**](LaunchJobTemplateRequest.md)| Launch Job Template API | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **push_content_to_endpoint**
> CreateJobResponse push_content_to_endpoint(endpoint, body, x_correlation_id=x_correlation_id)

Whatever is posted to this endpoint will be added to the child input folder(s) for the task_routes that have this endpoint.  If more than one task_routes have this endpoint, it will be added to all child input folders.

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    endpoint = 'endpoint_example' # str | Endpoint UUID to push this chunk towards
body = 'body_example' # str | How to push content into a child input folder(s).
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Whatever is posted to this endpoint will be added to the child input folder(s) for the task_routes that have this endpoint.  If more than one task_routes have this endpoint, it will be added to all child input folders.
        api_response = api_instance.push_content_to_endpoint(endpoint, body, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->push_content_to_endpoint: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **endpoint** | [**str**](.md)| Endpoint UUID to push this chunk towards | 
 **body** | **str**| How to push content into a child input folder(s). | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateJobResponse**](CreateJobResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json, application/octet-stream, audio/*, image/*, text/html, text/plain, text/xml, video/*
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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **recheck_job_status**
> RecheckJobStatusResponse recheck_job_status(job_id, x_correlation_id=x_correlation_id)

Recheck Job Status

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    job_id = 'job_id_example' # str | ID of Job
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Recheck Job Status
        api_response = api_instance.recheck_job_status(job_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->recheck_job_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | [**str**](.md)| ID of Job | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tasks_status_export**
> file tasks_status_export(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, offset=offset, limit=limit, order_by=order_by, direction=direction, status=status, organization_id=organization_id, task_id=task_id, core_task_id=core_task_id, error_type=error_type, job_id=job_id, core_job_id=core_job_id, engine_id=engine_id, media_source_id=media_source_id, recording_id=recording_id, engine_category_id=engine_category_id, modified_before=modified_before, modified_after=modified_after, created_before=created_before, created_after=created_after, backlog=backlog, alloc=alloc)

Export a task status report as a excel file

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
order_by = 'createdDateTime' # str | the field to sort (optional) (default to 'createdDateTime')
direction = 'DESC' # str | the sort order.  ASC or DESC. (optional) (default to 'DESC')
status = client.TaskStatusEnum() # TaskStatusEnum | Filtering by task Status (optional)
organization_id = 'organization_id_example' # str | Filter by organization id (optional)
task_id = 'task_id_example' # str | Filter by task id (optional)
core_task_id = 'core_task_id_example' # str | Filter by coreTaskID (optional)
error_type = client.FailureReasonEnum() # FailureReasonEnum | filter by errorType (failureReason) (optional)
job_id = 'job_id_example' # str | Filter by job id (optional)
core_job_id = 'core_job_id_example' # str | Filter by coreJobID (optional)
engine_id = 'engine_id_example' # str | Filter by engine id (optional)
media_source_id = 'media_source_id_example' # str | Filter by media source id (optional)
recording_id = 56 # int | Filter tasks by the recording id (optional)
engine_category_id = 'engine_category_id_example' # str | Filtering by engineCategoryID (optional)
modified_before = 56 # int | Filter by items modified before expressed as timestamp (optional)
modified_after = 56 # int | Filter by items modified after expressed as timestamp (optional)
created_before = 56 # int | Filter items where created date is before this date (optional)
created_after = 56 # int | Filter items where created date is after this date (optional)
backlog = True # bool | Filtering all tasks in backlog (optional)
alloc = True # bool | Filtering all tasks have alloc = true or not (optional)

    try:
        # Export a task status report as a excel file
        api_response = api_instance.tasks_status_export(x_correlation_id=x_correlation_id, start_time=start_time, end_time=end_time, offset=offset, limit=limit, order_by=order_by, direction=direction, status=status, organization_id=organization_id, task_id=task_id, core_task_id=core_task_id, error_type=error_type, job_id=job_id, core_job_id=core_job_id, engine_id=engine_id, media_source_id=media_source_id, recording_id=recording_id, engine_category_id=engine_category_id, modified_before=modified_before, modified_after=modified_after, created_before=created_before, created_after=created_after, backlog=backlog, alloc=alloc)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->tasks_status_export: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **order_by** | **str**| the field to sort | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **str**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **status** | [**TaskStatusEnum**](.md)| Filtering by task Status | [optional] 
 **organization_id** | **str**| Filter by organization id | [optional] 
 **task_id** | **str**| Filter by task id | [optional] 
 **core_task_id** | **str**| Filter by coreTaskID | [optional] 
 **error_type** | [**FailureReasonEnum**](.md)| filter by errorType (failureReason) | [optional] 
 **job_id** | **str**| Filter by job id | [optional] 
 **core_job_id** | **str**| Filter by coreJobID | [optional] 
 **engine_id** | **str**| Filter by engine id | [optional] 
 **media_source_id** | **str**| Filter by media source id | [optional] 
 **recording_id** | **int**| Filter tasks by the recording id | [optional] 
 **engine_category_id** | [**str**](.md)| Filtering by engineCategoryID | [optional] 
 **modified_before** | **int**| Filter by items modified before expressed as timestamp | [optional] 
 **modified_after** | **int**| Filter by items modified after expressed as timestamp | [optional] 
 **created_before** | **int**| Filter items where created date is before this date | [optional] 
 **created_after** | **int**| Filter items where created date is after this date | [optional] 
 **backlog** | **bool**| Filtering all tasks in backlog | [optional] 
 **alloc** | **bool**| Filtering all tasks have alloc &#x3D; true or not | [optional] 

### Return type

**file**

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_task_status**
> TasksStatusUpdateResponse update_task_status(tasks_status_update_request, x_correlation_id=x_correlation_id)

This updates the status for a bulk of tasks by taskID

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.ProcessApi(api_client)
    tasks_status_update_request = client.TasksStatusUpdateRequest() # TasksStatusUpdateRequest | The input for updateTaskStatus
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This updates the status for a bulk of tasks by taskID
        api_response = api_instance.update_task_status(tasks_status_update_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ProcessApi->update_task_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tasks_status_update_request** | [**TasksStatusUpdateRequest**](TasksStatusUpdateRequest.md)| The input for updateTaskStatus | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

