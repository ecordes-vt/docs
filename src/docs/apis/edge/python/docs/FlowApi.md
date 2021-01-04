# client.FlowApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clean_automate_requests**](FlowApi.md#clean_automate_requests) | **GET** /flowaction/requests/clean | Clean old automate requests.
[**create_node_red_container_info**](FlowApi.md#create_node_red_container_info) | **POST** /flow/nrcontainer/create | Create node-red container infomation
[**delete_automate_container**](FlowApi.md#delete_automate_container) | **POST** /flow/delete/{ContainerID} | Delete automate container.
[**update_automate_request_status**](FlowApi.md#update_automate_request_status) | **POST** /flow/request/update | Put this automate request into update status mode. This automate request will be updated to new status.
[**update_automate_status**](FlowApi.md#update_automate_status) | **POST** /flow/{HostID}/updatestatus | Get updated information to launch node-red container, terminate node-red container.


# **clean_automate_requests**
> AdminOperationResponse clean_automate_requests()

Clean old automate requests.

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
    api_instance = client.FlowApi(api_client)
    
    try:
        # Clean old automate requests.
        api_response = api_instance.clean_automate_requests()
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling FlowApi->clean_automate_requests: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

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
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_node_red_container_info**
> AdminOperationResponse create_node_red_container_info(create_nod_red_container_detail, x_correlation_id=x_correlation_id)

Create node-red container infomation

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
    api_instance = client.FlowApi(api_client)
    create_nod_red_container_detail = client.CreateNodRedContainerDetail() # CreateNodRedContainerDetail | Node-RED container info
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Create node-red container infomation
        api_response = api_instance.create_node_red_container_info(create_nod_red_container_detail, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling FlowApi->create_node_red_container_info: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_nod_red_container_detail** | [**CreateNodRedContainerDetail**](CreateNodRedContainerDetail.md)| Node-RED container info | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_automate_container**
> AdminOperationResponse delete_automate_container(container_id)

Delete automate container.

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
    api_instance = client.FlowApi(api_client)
    container_id = 'container_id_example' # str | ContainerID of node-red container

    try:
        # Delete automate container.
        api_response = api_instance.delete_automate_container(container_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling FlowApi->delete_automate_container: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **container_id** | **str**| ContainerID of node-red container | 

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
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_automate_request_status**
> AdminOperationResponse update_automate_request_status(update_node_red_request_detail, x_correlation_id=x_correlation_id)

Put this automate request into update status mode. This automate request will be updated to new status.

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
    api_instance = client.FlowApi(api_client)
    update_node_red_request_detail = client.UpdateNodeRedRequestDetail() # UpdateNodeRedRequestDetail | Node-RED container info
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Put this automate request into update status mode. This automate request will be updated to new status.
        api_response = api_instance.update_automate_request_status(update_node_red_request_detail, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling FlowApi->update_automate_request_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **update_node_red_request_detail** | [**UpdateNodeRedRequestDetail**](UpdateNodeRedRequestDetail.md)| Node-RED container info | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_automate_status**
> HostAction update_automate_status(host_id)

Get updated information to launch node-red container, terminate node-red container.

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
    api_instance = client.FlowApi(api_client)
    host_id = 'host_id_example' # str | ID of Host

    try:
        # Get updated information to launch node-red container, terminate node-red container.
        api_response = api_instance.update_automate_status(host_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling FlowApi->update_automate_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_id** | [**str**](.md)| ID of Host | 

### Return type

[**HostAction**](HostAction.md)

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

