# client.EngineApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_build**](EngineApi.md#create_build) | **POST** /admin/build/create | This API creates a new engine build
[**create_engine**](EngineApi.md#create_engine) | **POST** /admin/engine/create | This API creates a new engine
[**create_engine_category**](EngineApi.md#create_engine_category) | **POST** /admin/engine/category/create | This API creates a new engine category
[**delete_build_post**](EngineApi.md#delete_build_post) | **POST** /engine/{EngineID}/build/{BuildID}/delete | This API provides the engine detail result
[**delete_engine_post**](EngineApi.md#delete_engine_post) | **POST** /admin/engine/{EngineID}/delete | This API delets an engine
[**get_engine_build**](EngineApi.md#get_engine_build) | **GET** /admin/build/{BuildID}/detail | This gets a particular build
[**get_engine_builds**](EngineApi.md#get_engine_builds) | **GET** /admin/engine/{EngineID}/builds | Get the list of builds deployed and available on aiWARE for a particular engine
[**get_engine_builds_by_state**](EngineApi.md#get_engine_builds_by_state) | **GET** /engine/builds | The api returns engine build records by build state
[**get_engine_categories**](EngineApi.md#get_engine_categories) | **GET** /admin/engine/categories | This provides a list of engine categories
[**get_engine_category_detail**](EngineApi.md#get_engine_category_detail) | **GET** /admin/engine/category/{EngineCategoryID}/detail | This provides detail for an engine category
[**get_engine_container_count**](EngineApi.md#get_engine_container_count) | **GET** /engine/container_count | Get engine container count
[**get_engine_detail**](EngineApi.md#get_engine_detail) | **GET** /admin/engine/{EngineID}/detail | This API provides the engine detail result
[**get_engine_instance_detail**](EngineApi.md#get_engine_instance_detail) | **GET** /engine/instance/{EngineInstanceID}/detail | Get information about an engine Instance
[**get_engine_instance_list**](EngineApi.md#get_engine_instance_list) | **GET** /engine/instances | Get engines instances with filtering
[**get_engine_instance_logs**](EngineApi.md#get_engine_instance_logs) | **GET** /engine/instance/{EngineInstanceID}/logs | Get engine instance logs as a zip file
[**get_engine_instance_status**](EngineApi.md#get_engine_instance_status) | **GET** /engine/instance/{EngineInstanceID}/status | Get the latest status of the engine instance
[**get_engine_instance_work**](EngineApi.md#get_engine_instance_work) | **POST** /engine/instance/{EngineInstanceID}/getwork | Get a work request
[**get_engine_instance_work_detail**](EngineApi.md#get_engine_instance_work_detail) | **GET** /engine/instance/{EngineInstanceID}/workdetail | Get detail of the work being done by the engine instance
[**get_engine_instances**](EngineApi.md#get_engine_instances) | **GET** /engine/{EngineID}/instances | Get information about the instances of an engine
[**get_engine_launch_detail**](EngineApi.md#get_engine_launch_detail) | **GET** /engine/{EngineID}/launch/{LaunchID}/detail | This API returns the list of launches for this engine
[**get_engine_launches**](EngineApi.md#get_engine_launches) | **GET** /engine/{EngineID}/launches | This API returns the list of launches for this engine
[**get_engines**](EngineApi.md#get_engines) | **GET** /admin/engines | Get the list of engines deployed and available on aiWARE
[**get_jobs_backlog_count_by_engine**](EngineApi.md#get_jobs_backlog_count_by_engine) | **POST** /proc/jobs/backlog_count_by_engine | Get backlog count by engine
[**get_resources_for_engine_instance**](EngineApi.md#get_resources_for_engine_instance) | **GET** /engine/instance/{EngineInstanceID}/resources | Get resources for engine instance
[**pause_build**](EngineApi.md#pause_build) | **POST** /admin/build/{BuildID}/pause | This API pauses a build so that tasks based on this engine build will not run.
[**pause_engine**](EngineApi.md#pause_engine) | **POST** /admin/engine/{EngineID}/pause | This API pauses an engine so that tasks based on this engine will not run.
[**register_engine_instance_no_auth**](EngineApi.md#register_engine_instance_no_auth) | **POST** /engine/instance/register | Register a new engine instance without authorization
[**replace_engine**](EngineApi.md#replace_engine) | **POST** /admin/engine/{EngineID}/replace | This API replaced an engine so that tasks based on this engine will not run.
[**resume_build**](EngineApi.md#resume_build) | **POST** /admin/build/{BuildID}/resume | This API resumes a build so that tasks based on this engine build will start running.
[**resume_engine**](EngineApi.md#resume_engine) | **POST** /admin/engine/{EngineID}/resume | This API resumes a build so that tasks based on this engine build will start running.
[**terminate_engine_instance**](EngineApi.md#terminate_engine_instance) | **POST** /engine/instance/{EngineInstanceID}/terminate | Delete the engine instance record
[**update_engine**](EngineApi.md#update_engine) | **POST** /admin/engine/{EngineID}/update | This API updates the specified engine
[**update_engine_build**](EngineApi.md#update_engine_build) | **POST** /admin/build/{BuildID}/update | This API updates the specified engine
[**update_engine_build_state**](EngineApi.md#update_engine_build_state) | **POST** /engine/build/{BuildID}/state | Update the Engine Build State
[**update_engine_category**](EngineApi.md#update_engine_category) | **POST** /admin/engine/category/{EngineCategoryID}/update | This updates the specified engine category
[**update_engine_instance_status**](EngineApi.md#update_engine_instance_status) | **POST** /engine/instance/{EngineInstanceID}/updatestatus | Update the Engine Instance Status.  Heartbeat to communicate back to controller both aggregated work and delta work from last heartbeat


# **create_build**
> CreateBuildResponse create_build(create_build_request, x_correlation_id=x_correlation_id)

This API creates a new engine build

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
    api_instance = client.EngineApi(api_client)
    create_build_request = client.CreateBuildRequest() # CreateBuildRequest | The fields for an engine build
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API creates a new engine build
        api_response = api_instance.create_build(create_build_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->create_build: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_build_request** | [**CreateBuildRequest**](CreateBuildRequest.md)| The fields for an engine build | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateBuildResponse**](CreateBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of the Create Engine Build API |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_engine**
> CreateEngineResponse create_engine(create_engine_request, x_correlation_id=x_correlation_id)

This API creates a new engine

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
    api_instance = client.EngineApi(api_client)
    create_engine_request = client.CreateEngineRequest() # CreateEngineRequest | The fields for an engine
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API creates a new engine
        api_response = api_instance.create_engine(create_engine_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->create_engine: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_engine_request** | [**CreateEngineRequest**](CreateEngineRequest.md)| The fields for an engine | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateEngineResponse**](CreateEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of the Create Engine API |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_engine_category**
> CreateEngineCategoryResponse create_engine_category(create_engine_category_detail, x_correlation_id=x_correlation_id)

This API creates a new engine category

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
    api_instance = client.EngineApi(api_client)
    create_engine_category_detail = client.CreateEngineCategoryDetail() # CreateEngineCategoryDetail | The fields for an engine category
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API creates a new engine category
        api_response = api_instance.create_engine_category(create_engine_category_detail, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->create_engine_category: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_engine_category_detail** | [**CreateEngineCategoryDetail**](CreateEngineCategoryDetail.md)| The fields for an engine category | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateEngineCategoryResponse**](CreateEngineCategoryResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of the Create Engine Category API |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_build_post**
> AdminOperationResponse delete_build_post(engine_id, build_id, x_correlation_id=x_correlation_id)

This API provides the engine detail result

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
    api_instance = client.EngineApi(api_client)
    engine_id = 'engine_id_example' # str | ID of Engine
build_id = 'build_id_example' # str | ID of Build
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API provides the engine detail result
        api_response = api_instance.delete_build_post(engine_id, build_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->delete_build_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | [**str**](.md)| ID of Engine | 
 **build_id** | [**str**](.md)| ID of Build | 
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
**204** | Delete a particular engine |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_engine_post**
> AdminOperationResponse delete_engine_post(engine_id, x_correlation_id=x_correlation_id)

This API delets an engine

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
    api_instance = client.EngineApi(api_client)
    engine_id = 'engine_id_example' # str | ID of Engine
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API delets an engine
        api_response = api_instance.delete_engine_post(engine_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->delete_engine_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | [**str**](.md)| ID of Engine | 
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
**204** | Delete a particular engine |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_engine_build**
> GetEngineBuildResponse get_engine_build(build_id, x_correlation_id=x_correlation_id)

This gets a particular build

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
    api_instance = client.EngineApi(api_client)
    build_id = 'build_id_example' # str | ID of Build
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This gets a particular build
        api_response = api_instance.get_engine_build(build_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_build: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **build_id** | [**str**](.md)| ID of Build | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetEngineBuildResponse**](GetEngineBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Specific build |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_engine_builds**
> GetEngineBuildsResponse get_engine_builds(engine_id, x_correlation_id=x_correlation_id, build_state=build_state)

Get the list of builds deployed and available on aiWARE for a particular engine

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
    api_instance = client.EngineApi(api_client)
    engine_id = 'engine_id_example' # str | ID of Engine
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
build_state = 'build_state_example' # str | Filter builds by the build state (optional)

    try:
        # Get the list of builds deployed and available on aiWARE for a particular engine
        api_response = api_instance.get_engine_builds(engine_id, x_correlation_id=x_correlation_id, build_state=build_state)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_builds: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | [**str**](.md)| ID of Engine | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **build_state** | **str**| Filter builds by the build state | [optional] 

### Return type

[**GetEngineBuildsResponse**](GetEngineBuildsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of engines |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_engine_builds_by_state**
> GetEngineBuildByStateResponse get_engine_builds_by_state(x_correlation_id=x_correlation_id, state=state)

The api returns engine build records by build state

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
    api_instance = client.EngineApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
state = 'state_example' # str | Filter data by build state (optional)

    try:
        # The api returns engine build records by build state
        api_response = api_instance.get_engine_builds_by_state(x_correlation_id=x_correlation_id, state=state)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_builds_by_state: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **state** | **str**| Filter data by build state | [optional] 

### Return type

[**GetEngineBuildByStateResponse**](GetEngineBuildByStateResponse.md)

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

# **get_engine_categories**
> GetEngineCategoriesResponse get_engine_categories(x_correlation_id=x_correlation_id)

This provides a list of engine categories

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
    api_instance = client.EngineApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides a list of engine categories
        api_response = api_instance.get_engine_categories(x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_categories: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetEngineCategoriesResponse**](GetEngineCategoriesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of get_engine_categories |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_engine_category_detail**
> GetEngineCategoryDetailResponse get_engine_category_detail(engine_category_id, x_correlation_id=x_correlation_id)

This provides detail for an engine category

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
    api_instance = client.EngineApi(api_client)
    engine_category_id = 'engine_category_id_example' # str | ID of Engine Category
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides detail for an engine category
        api_response = api_instance.get_engine_category_detail(engine_category_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_category_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_category_id** | [**str**](.md)| ID of Engine Category | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetEngineCategoryDetailResponse**](GetEngineCategoryDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of get_engine_category_detail |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_engine_container_count**
> GetEngineContainerCountResponse get_engine_container_count(interval=interval, start_time=start_time, end_time=end_time, group_by=group_by, engine_id=engine_id, host_id=host_id)

Get engine container count

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
    api_instance = client.EngineApi(api_client)
    interval = 56 # int | Interval in seconds for output time ranges. (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
group_by = client.EngineContainerGroupByEnum() # EngineContainerGroupByEnum | Group data by engineID or instance (optional)
engine_id = 'engine_id_example' # str | Filter data by engineID (optional)
host_id = 'host_id_example' # str | Filter data by hostID (optional)

    try:
        # Get engine container count
        api_response = api_instance.get_engine_container_count(interval=interval, start_time=start_time, end_time=end_time, group_by=group_by, engine_id=engine_id, host_id=host_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_container_count: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **int**| Interval in seconds for output time ranges. | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **group_by** | [**EngineContainerGroupByEnum**](.md)| Group data by engineID or instance | [optional] 
 **engine_id** | [**str**](.md)| Filter data by engineID | [optional] 
 **host_id** | [**str**](.md)| Filter data by hostID | [optional] 

### Return type

[**GetEngineContainerCountResponse**](GetEngineContainerCountResponse.md)

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

# **get_engine_detail**
> GetEngineDetailResponse get_engine_detail(engine_id)

This API provides the engine detail result

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
    api_instance = client.EngineApi(api_client)
    engine_id = 'engine_id_example' # str | ID of Engine

    try:
        # This API provides the engine detail result
        api_response = api_instance.get_engine_detail(engine_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | [**str**](.md)| ID of Engine | 

### Return type

[**GetEngineDetailResponse**](GetEngineDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of engines |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_engine_instance_detail**
> EngineInstanceInfo get_engine_instance_detail(engine_instance_id, x_correlation_id=x_correlation_id)

Get information about an engine Instance

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
    api_instance = client.EngineApi(api_client)
    engine_instance_id = 'engine_instance_id_example' # str | ID of Engine Instance
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get information about an engine Instance
        api_response = api_instance.get_engine_instance_detail(engine_instance_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_instance_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_instance_id** | [**str**](.md)| ID of Engine Instance | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceInfo**](EngineInstanceInfo.md)

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

# **get_engine_instance_list**
> GetEngineInstanceListResponse get_engine_instance_list(x_correlation_id=x_correlation_id, engine_instance_i_ds=engine_instance_i_ds, engine_i_ds=engine_i_ds, host_i_ds=host_i_ds, work_request_i_ds=work_request_i_ds, status=status, drain=drain, launch_start_time=launch_start_time, launch_end_time=launch_end_time, modified_before=modified_before, modified_after=modified_after, created_before=created_before, created_after=created_after, offset=offset, limit=limit, direction=direction, order_by=order_by)

Get engines instances with filtering

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
    api_instance = client.EngineApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
engine_instance_i_ds = 'engine_instance_i_ds_example' # str | Field to provide the input to get engine instances by ID list. Separated by commas (optional)
engine_i_ds = 'engine_i_ds_example' # str | Field to provide the input to get engines by Engine ID list. Separated by commas (optional)
host_i_ds = 'host_i_ds_example' # str | Filtering engine instances by host IDs. Separated by commas (optional)
work_request_i_ds = 'work_request_i_ds_example' # str | Filters engine instances by workrequest IDs. Separated by commas (optional)
status = client.EngineStatusEnum() # EngineStatusEnum | Field to match the current status (optional)
drain = True # bool | Filter by drain (optional)
launch_start_time = 56 # int | The unix timestamp, describing a lower limit for the time an engine instance was launched. (optional)
launch_end_time = 56 # int | The unix timestamp, describing an upper limit for the time an engine instance was launched. (optional)
modified_before = 56 # int | Filter by items modified before expressed as timestamp (optional)
modified_after = 56 # int | Filter by items modified after expressed as timestamp (optional)
created_before = 56 # int | Filter items where created date is before this date (optional)
created_after = 56 # int | Filter items where created date is after this date (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
direction = 'DESC' # str | the sort order.  ASC or DESC. (optional) (default to 'DESC')
order_by = 'order_by_example' # str | It should be in [engineID, hostID, status, createdTime, modifiedTime, lastUpdateTime, launchTime] (optional)

    try:
        # Get engines instances with filtering
        api_response = api_instance.get_engine_instance_list(x_correlation_id=x_correlation_id, engine_instance_i_ds=engine_instance_i_ds, engine_i_ds=engine_i_ds, host_i_ds=host_i_ds, work_request_i_ds=work_request_i_ds, status=status, drain=drain, launch_start_time=launch_start_time, launch_end_time=launch_end_time, modified_before=modified_before, modified_after=modified_after, created_before=created_before, created_after=created_after, offset=offset, limit=limit, direction=direction, order_by=order_by)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_instance_list: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **engine_instance_i_ds** | **str**| Field to provide the input to get engine instances by ID list. Separated by commas | [optional] 
 **engine_i_ds** | **str**| Field to provide the input to get engines by Engine ID list. Separated by commas | [optional] 
 **host_i_ds** | [**str**](.md)| Filtering engine instances by host IDs. Separated by commas | [optional] 
 **work_request_i_ds** | [**str**](.md)| Filters engine instances by workrequest IDs. Separated by commas | [optional] 
 **status** | [**EngineStatusEnum**](.md)| Field to match the current status | [optional] 
 **drain** | **bool**| Filter by drain | [optional] 
 **launch_start_time** | **int**| The unix timestamp, describing a lower limit for the time an engine instance was launched. | [optional] 
 **launch_end_time** | **int**| The unix timestamp, describing an upper limit for the time an engine instance was launched. | [optional] 
 **modified_before** | **int**| Filter by items modified before expressed as timestamp | [optional] 
 **modified_after** | **int**| Filter by items modified after expressed as timestamp | [optional] 
 **created_before** | **int**| Filter items where created date is before this date | [optional] 
 **created_after** | **int**| Filter items where created date is after this date | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **direction** | **str**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **order_by** | **str**| It should be in [engineID, hostID, status, createdTime, modifiedTime, lastUpdateTime, launchTime] | [optional] 

### Return type

[**GetEngineInstanceListResponse**](GetEngineInstanceListResponse.md)

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

# **get_engine_instance_logs**
> file get_engine_instance_logs(engine_instance_id, x_correlation_id=x_correlation_id)

Get engine instance logs as a zip file

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
    api_instance = client.EngineApi(api_client)
    engine_instance_id = 'engine_instance_id_example' # str | ID of Engine Instance
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get engine instance logs as a zip file
        api_response = api_instance.get_engine_instance_logs(engine_instance_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_instance_logs: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_instance_id** | [**str**](.md)| ID of Engine Instance | 
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

# **get_engine_instance_status**
> EngineInstanceStatus get_engine_instance_status(engine_instance_id, x_correlation_id=x_correlation_id)

Get the latest status of the engine instance

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
    api_instance = client.EngineApi(api_client)
    engine_instance_id = 'engine_instance_id_example' # str | ID of Engine Instance
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get the latest status of the engine instance
        api_response = api_instance.get_engine_instance_status(engine_instance_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_instance_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_instance_id** | [**str**](.md)| ID of Engine Instance | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceStatus**](EngineInstanceStatus.md)

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

# **get_engine_instance_work**
> EngineInstanceWorkRequestResponse get_engine_instance_work(engine_instance_id, engine_instance_work_request, x_correlation_id=x_correlation_id)

Get a work request

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
    api_instance = client.EngineApi(api_client)
    engine_instance_id = 'engine_instance_id_example' # str | ID of Engine Instance
engine_instance_work_request = client.EngineInstanceWorkRequest() # EngineInstanceWorkRequest | Engine Instance Info
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get a work request
        api_response = api_instance.get_engine_instance_work(engine_instance_id, engine_instance_work_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_instance_work: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_instance_id** | [**str**](.md)| ID of Engine Instance | 
 **engine_instance_work_request** | [**EngineInstanceWorkRequest**](EngineInstanceWorkRequest.md)| Engine Instance Info | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceWorkRequestResponse**](EngineInstanceWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid work response |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_engine_instance_work_detail**
> EngineInstanceWorkDetailsResponse get_engine_instance_work_detail(engine_instance_id, x_correlation_id=x_correlation_id)

Get detail of the work being done by the engine instance

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
    api_instance = client.EngineApi(api_client)
    engine_instance_id = 'engine_instance_id_example' # str | ID of Engine Instance
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get detail of the work being done by the engine instance
        api_response = api_instance.get_engine_instance_work_detail(engine_instance_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_instance_work_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_instance_id** | [**str**](.md)| ID of Engine Instance | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceWorkDetailsResponse**](EngineInstanceWorkDetailsResponse.md)

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

# **get_engine_instances**
> GetEngineInstancesResponse get_engine_instances(engine_id, x_correlation_id=x_correlation_id, launch_start_time=launch_start_time, launch_end_time=launch_end_time, modified_before=modified_before, modified_after=modified_after, created_before=created_before, created_after=created_after)

Get information about the instances of an engine

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
    api_instance = client.EngineApi(api_client)
    engine_id = 'engine_id_example' # str | EngineID of node-red container request
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
launch_start_time = 56 # int | The unix timestamp, describing a lower limit for the time an engine instance was launched. (optional)
launch_end_time = 56 # int | The unix timestamp, describing an upper limit for the time an engine instance was launched. (optional)
modified_before = 56 # int | Filter by items modified before expressed as timestamp (optional)
modified_after = 56 # int | Filter by items modified after expressed as timestamp (optional)
created_before = 56 # int | Filter items where created date is before this date (optional)
created_after = 56 # int | Filter items where created date is after this date (optional)

    try:
        # Get information about the instances of an engine
        api_response = api_instance.get_engine_instances(engine_id, x_correlation_id=x_correlation_id, launch_start_time=launch_start_time, launch_end_time=launch_end_time, modified_before=modified_before, modified_after=modified_after, created_before=created_before, created_after=created_after)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_instances: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | **str**| EngineID of node-red container request | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **launch_start_time** | **int**| The unix timestamp, describing a lower limit for the time an engine instance was launched. | [optional] 
 **launch_end_time** | **int**| The unix timestamp, describing an upper limit for the time an engine instance was launched. | [optional] 
 **modified_before** | **int**| Filter by items modified before expressed as timestamp | [optional] 
 **modified_after** | **int**| Filter by items modified after expressed as timestamp | [optional] 
 **created_before** | **int**| Filter items where created date is before this date | [optional] 
 **created_after** | **int**| Filter items where created date is after this date | [optional] 

### Return type

[**GetEngineInstancesResponse**](GetEngineInstancesResponse.md)

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

# **get_engine_launch_detail**
> GetEngineLaunchResponse get_engine_launch_detail(engine_id, launch_id, created_before=created_before, created_after=created_after, offset=offset, limit=limit, order_by=order_by, direction=direction)

This API returns the list of launches for this engine

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
    api_instance = client.EngineApi(api_client)
    engine_id = 'engine_id_example' # str | ID of Engine
launch_id = 'launch_id_example' # str | ID of Launch
created_before = 56 # int | Filter items where created date is before this date (optional)
created_after = 56 # int | Filter items where created date is after this date (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
order_by = 'createdDateTime' # str | the field to sort (optional) (default to 'createdDateTime')
direction = 'DESC' # str | the sort order.  ASC or DESC. (optional) (default to 'DESC')

    try:
        # This API returns the list of launches for this engine
        api_response = api_instance.get_engine_launch_detail(engine_id, launch_id, created_before=created_before, created_after=created_after, offset=offset, limit=limit, order_by=order_by, direction=direction)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_launch_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | [**str**](.md)| ID of Engine | 
 **launch_id** | [**str**](.md)| ID of Launch | 
 **created_before** | **int**| Filter items where created date is before this date | [optional] 
 **created_after** | **int**| Filter items where created date is after this date | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **order_by** | **str**| the field to sort | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **str**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]

### Return type

[**GetEngineLaunchResponse**](GetEngineLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Returns detail on a specific launch |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_engine_launches**
> GetEngineLaunchResponse get_engine_launches(engine_id, launch_status=launch_status, launch_action=launch_action, created_before=created_before, created_after=created_after, offset=offset, limit=limit, order_by=order_by, direction=direction)

This API returns the list of launches for this engine

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
    api_instance = client.EngineApi(api_client)
    engine_id = 'engine_id_example' # str | ID of Engine
launch_status = client.LaunchStatusEnum() # LaunchStatusEnum | Field to match the current launch status (optional)
launch_action = client.LaunchActionEnum() # LaunchActionEnum | Field to match the current launch action (optional)
created_before = 56 # int | Filter items where created date is before this date (optional)
created_after = 56 # int | Filter items where created date is after this date (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
order_by = 'createdDateTime' # str | the field to sort (optional) (default to 'createdDateTime')
direction = 'DESC' # str | the sort order.  ASC or DESC. (optional) (default to 'DESC')

    try:
        # This API returns the list of launches for this engine
        api_response = api_instance.get_engine_launches(engine_id, launch_status=launch_status, launch_action=launch_action, created_before=created_before, created_after=created_after, offset=offset, limit=limit, order_by=order_by, direction=direction)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engine_launches: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | [**str**](.md)| ID of Engine | 
 **launch_status** | [**LaunchStatusEnum**](.md)| Field to match the current launch status | [optional] 
 **launch_action** | [**LaunchActionEnum**](.md)| Field to match the current launch action | [optional] 
 **created_before** | **int**| Filter items where created date is before this date | [optional] 
 **created_after** | **int**| Filter items where created date is after this date | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **order_by** | **str**| the field to sort | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **str**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]

### Return type

[**GetEngineLaunchResponse**](GetEngineLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of launches for specified engine |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_engines**
> GetEnginesResponse get_engines(x_correlation_id=x_correlation_id, internal_organization_id=internal_organization_id, engine_name=engine_name, engine_state=engine_state, engine_type=engine_type, engine_output_type=engine_output_type, engine_category_id=engine_category_id, engine_i_ds=engine_i_ds, offset=offset, limit=limit, direction=direction, start_time=start_time, end_time=end_time, preload=preload, order_by=order_by)

Get the list of engines deployed and available on aiWARE

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
    api_instance = client.EngineApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
internal_organization_id = 'internal_organization_id_example' # str | ID of Organization.  UUID.  This ID is unique to this aiWARE installation. (optional)
engine_name = 'engine_name_example' # str | Field to string match against the engine names (optional)
engine_state = client.EngineStateEnum() # EngineStateEnum | Field to match the current state (optional)
engine_type = client.EngineTypeEnum() # EngineTypeEnum | Field to match the current type (optional)
engine_output_type = client.EngineTypeEnum() # EngineTypeEnum | Field to match the current type (optional)
engine_category_id = 'engine_category_id_example' # str | Filter to the particular engine category ID (optional)
engine_i_ds = 'engine_i_ds_example' # str | Field to provide the input to get engines by Engine ID list. Separated by commas (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
direction = 'DESC' # str | the sort order.  ASC or DESC. (optional) (default to 'DESC')
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
preload = True # bool | Filter engines by preload (optional)
order_by = 'order_by_example' # str | The value should be in [name, state, type, organizationID, createdTime] (optional)

    try:
        # Get the list of engines deployed and available on aiWARE
        api_response = api_instance.get_engines(x_correlation_id=x_correlation_id, internal_organization_id=internal_organization_id, engine_name=engine_name, engine_state=engine_state, engine_type=engine_type, engine_output_type=engine_output_type, engine_category_id=engine_category_id, engine_i_ds=engine_i_ds, offset=offset, limit=limit, direction=direction, start_time=start_time, end_time=end_time, preload=preload, order_by=order_by)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_engines: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **internal_organization_id** | [**str**](.md)| ID of Organization.  UUID.  This ID is unique to this aiWARE installation. | [optional] 
 **engine_name** | **str**| Field to string match against the engine names | [optional] 
 **engine_state** | [**EngineStateEnum**](.md)| Field to match the current state | [optional] 
 **engine_type** | [**EngineTypeEnum**](.md)| Field to match the current type | [optional] 
 **engine_output_type** | [**EngineTypeEnum**](.md)| Field to match the current type | [optional] 
 **engine_category_id** | **str**| Filter to the particular engine category ID | [optional] 
 **engine_i_ds** | **str**| Field to provide the input to get engines by Engine ID list. Separated by commas | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **direction** | **str**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **preload** | **bool**| Filter engines by preload | [optional] 
 **order_by** | **str**| The value should be in [name, state, type, organizationID, createdTime] | [optional] 

### Return type

[**GetEnginesResponse**](GetEnginesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of engines |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_jobs_backlog_count_by_engine**
> GetJobsBacklogCountResponse get_jobs_backlog_count_by_engine(interval=interval, start_time=start_time, end_time=end_time, organization_i_ds=organization_i_ds)

Get backlog count by engine

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
    api_instance = client.EngineApi(api_client)
    interval = 56 # int | Interval in seconds for output time ranges. (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
organization_i_ds = 'organization_i_ds_example' # str |  (optional)

    try:
        # Get backlog count by engine
        api_response = api_instance.get_jobs_backlog_count_by_engine(interval=interval, start_time=start_time, end_time=end_time, organization_i_ds=organization_i_ds)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_jobs_backlog_count_by_engine: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **int**| Interval in seconds for output time ranges. | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **organization_i_ds** | **str**|  | [optional] 

### Return type

[**GetJobsBacklogCountResponse**](GetJobsBacklogCountResponse.md)

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

# **get_resources_for_engine_instance**
> GetResourcesForEngineInstanceResponse get_resources_for_engine_instance(engine_instance_id, x_correlation_id=x_correlation_id)

Get resources for engine instance

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
    api_instance = client.EngineApi(api_client)
    engine_instance_id = 'engine_instance_id_example' # str | ID of Engine Instance
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get resources for engine instance
        api_response = api_instance.get_resources_for_engine_instance(engine_instance_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->get_resources_for_engine_instance: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_instance_id** | [**str**](.md)| ID of Engine Instance | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetResourcesForEngineInstanceResponse**](GetResourcesForEngineInstanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid work response |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pause_build**
> AdminOperationResponse pause_build(build_id, x_correlation_id=x_correlation_id, build_state=build_state)

This API pauses a build so that tasks based on this engine build will not run.

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
    api_instance = client.EngineApi(api_client)
    build_id = 'build_id_example' # str | ID of Build
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
build_state = 'build_state_example' # str | Filter builds by the build state (optional)

    try:
        # This API pauses a build so that tasks based on this engine build will not run.
        api_response = api_instance.pause_build(build_id, x_correlation_id=x_correlation_id, build_state=build_state)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->pause_build: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **build_id** | [**str**](.md)| ID of Build | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **build_state** | **str**| Filter builds by the build state | [optional] 

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
**204** | Pause a particular build |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pause_engine**
> AdminOperationResponse pause_engine(engine_id, x_correlation_id=x_correlation_id, pause_engine_request=pause_engine_request)

This API pauses an engine so that tasks based on this engine will not run.

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
    api_instance = client.EngineApi(api_client)
    engine_id = 'engine_id_example' # str | ID of Engine
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
pause_engine_request = client.PauseEngineRequest() # PauseEngineRequest | Engine Instance Info (optional)

    try:
        # This API pauses an engine so that tasks based on this engine will not run.
        api_response = api_instance.pause_engine(engine_id, x_correlation_id=x_correlation_id, pause_engine_request=pause_engine_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->pause_engine: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | [**str**](.md)| ID of Engine | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **pause_engine_request** | [**PauseEngineRequest**](PauseEngineRequest.md)| Engine Instance Info | [optional] 

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
**204** | Pause a particular engine |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register_engine_instance_no_auth**
> EngineInstanceRegistrationInfo register_engine_instance_no_auth(engine_instance_info, x_correlation_id=x_correlation_id)

Register a new engine instance without authorization

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
    api_instance = client.EngineApi(api_client)
    engine_instance_info = client.EngineInstanceInfo() # EngineInstanceInfo | Engine Instance Info
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Register a new engine instance without authorization
        api_response = api_instance.register_engine_instance_no_auth(engine_instance_info, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->register_engine_instance_no_auth: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_instance_info** | [**EngineInstanceInfo**](EngineInstanceInfo.md)| Engine Instance Info | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceRegistrationInfo**](EngineInstanceRegistrationInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful registration of Engine Instance |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **replace_engine**
> AdminOperationResponse replace_engine(engine_id, replace_engine_request=replace_engine_request)

This API replaced an engine so that tasks based on this engine will not run.

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
    api_instance = client.EngineApi(api_client)
    engine_id = 'engine_id_example' # str | ID of Engine
replace_engine_request = client.ReplaceEngineRequest() # ReplaceEngineRequest | Engine Instance Info (optional)

    try:
        # This API replaced an engine so that tasks based on this engine will not run.
        api_response = api_instance.replace_engine(engine_id, replace_engine_request=replace_engine_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->replace_engine: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | [**str**](.md)| ID of Engine | 
 **replace_engine_request** | [**ReplaceEngineRequest**](ReplaceEngineRequest.md)| Engine Instance Info | [optional] 

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
**204** | Pause a particular engine |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **resume_build**
> AdminOperationResponse resume_build(build_id, x_correlation_id=x_correlation_id)

This API resumes a build so that tasks based on this engine build will start running.

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
    api_instance = client.EngineApi(api_client)
    build_id = 'build_id_example' # str | ID of Build
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API resumes a build so that tasks based on this engine build will start running.
        api_response = api_instance.resume_build(build_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->resume_build: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **build_id** | [**str**](.md)| ID of Build | 
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
**204** | Resume a particular build |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **resume_engine**
> AdminOperationResponse resume_engine(engine_id, x_correlation_id=x_correlation_id, resume_engine_request=resume_engine_request)

This API resumes a build so that tasks based on this engine build will start running.

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
    api_instance = client.EngineApi(api_client)
    engine_id = 'engine_id_example' # str | ID of Engine
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
resume_engine_request = client.ResumeEngineRequest() # ResumeEngineRequest | Engine Instance Info (optional)

    try:
        # This API resumes a build so that tasks based on this engine build will start running.
        api_response = api_instance.resume_engine(engine_id, x_correlation_id=x_correlation_id, resume_engine_request=resume_engine_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->resume_engine: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | [**str**](.md)| ID of Engine | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **resume_engine_request** | [**ResumeEngineRequest**](ResumeEngineRequest.md)| Engine Instance Info | [optional] 

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
**204** | Resume a particular build |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **terminate_engine_instance**
> terminate_engine_instance(engine_instance_id, x_correlation_id=x_correlation_id)

Delete the engine instance record

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
    api_instance = client.EngineApi(api_client)
    engine_instance_id = 'engine_instance_id_example' # str | ID of Engine Instance
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Delete the engine instance record
        api_instance.terminate_engine_instance(engine_instance_id, x_correlation_id=x_correlation_id)
    except ApiException as e:
        print("Exception when calling EngineApi->terminate_engine_instance: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_instance_id** | [**str**](.md)| ID of Engine Instance | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

void (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_engine**
> UpdateEngineResponse update_engine(engine_id, update_engine_request, x_correlation_id=x_correlation_id)

This API updates the specified engine

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
    api_instance = client.EngineApi(api_client)
    engine_id = 'engine_id_example' # str | ID of Engine
update_engine_request = client.UpdateEngineRequest() # UpdateEngineRequest | Update Engine
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API updates the specified engine
        api_response = api_instance.update_engine(engine_id, update_engine_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->update_engine: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | [**str**](.md)| ID of Engine | 
 **update_engine_request** | [**UpdateEngineRequest**](UpdateEngineRequest.md)| Update Engine | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**UpdateEngineResponse**](UpdateEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of the Update Engine API |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_engine_build**
> UpdateBuildResponse update_engine_build(engine_id, build_id, build_detail, x_correlation_id=x_correlation_id)

This API updates the specified engine

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
    api_instance = client.EngineApi(api_client)
    engine_id = 'engine_id_example' # str | ID of Engine
build_id = 'build_id_example' # str | ID of Build
build_detail = client.BuildDetail() # BuildDetail | Update Engine BUild
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API updates the specified engine
        api_response = api_instance.update_engine_build(engine_id, build_id, build_detail, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->update_engine_build: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | [**str**](.md)| ID of Engine | 
 **build_id** | [**str**](.md)| ID of Build | 
 **build_detail** | [**BuildDetail**](BuildDetail.md)| Update Engine BUild | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**UpdateBuildResponse**](UpdateBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of engines |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_engine_build_state**
> update_engine_build_state(build_id, update_engine_build_state_request, x_correlation_id=x_correlation_id)

Update the Engine Build State

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
    api_instance = client.EngineApi(api_client)
    build_id = 'build_id_example' # str | BuildID of node-red container request
update_engine_build_state_request = client.UpdateEngineBuildStateRequest() # UpdateEngineBuildStateRequest | Engine Build State
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Update the Engine Build State
        api_instance.update_engine_build_state(build_id, update_engine_build_state_request, x_correlation_id=x_correlation_id)
    except ApiException as e:
        print("Exception when calling EngineApi->update_engine_build_state: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **build_id** | **str**| BuildID of node-red container request | 
 **update_engine_build_state_request** | [**UpdateEngineBuildStateRequest**](UpdateEngineBuildStateRequest.md)| Engine Build State | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

void (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Item created |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_engine_category**
> UpdateEngineCategoryResponse update_engine_category(engine_category_id, x_correlation_id=x_correlation_id)

This updates the specified engine category

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
    api_instance = client.EngineApi(api_client)
    engine_category_id = 'engine_category_id_example' # str | ID of Engine Category
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This updates the specified engine category
        api_response = api_instance.update_engine_category(engine_category_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling EngineApi->update_engine_category: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_category_id** | [**str**](.md)| ID of Engine Category | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**UpdateEngineCategoryResponse**](UpdateEngineCategoryResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | This updates the specified engine category |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_engine_instance_status**
> update_engine_instance_status(engine_instance_id, engine_instance_status, x_correlation_id=x_correlation_id)

Update the Engine Instance Status.  Heartbeat to communicate back to controller both aggregated work and delta work from last heartbeat

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
    api_instance = client.EngineApi(api_client)
    engine_instance_id = 'engine_instance_id_example' # str | ID of Engine Instance
engine_instance_status = client.EngineInstanceStatus() # EngineInstanceStatus | Engine Instance Status
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Update the Engine Instance Status.  Heartbeat to communicate back to controller both aggregated work and delta work from last heartbeat
        api_instance.update_engine_instance_status(engine_instance_id, engine_instance_status, x_correlation_id=x_correlation_id)
    except ApiException as e:
        print("Exception when calling EngineApi->update_engine_instance_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_instance_id** | [**str**](.md)| ID of Engine Instance | 
 **engine_instance_status** | [**EngineInstanceStatus**](EngineInstanceStatus.md)| Engine Instance Status | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

void (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Item created |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

