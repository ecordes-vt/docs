# client.HostApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**drain_host**](HostApi.md#drain_host) | **POST** /host/{HostID}/drain | Put this host into drain mode.  A host in drain mode will not have work assigned to engines on the host.
[**get_host_cpu_usage**](HostApi.md#get_host_cpu_usage) | **GET** /hosts/cpu_usage | Get host cpu usage
[**get_host_detail**](HostApi.md#get_host_detail) | **GET** /host/{HostID}/detail | Get the latest info of the host
[**get_host_memory_usage**](HostApi.md#get_host_memory_usage) | **GET** /engine/memory_usage | Get host memory usage
[**get_host_status**](HostApi.md#get_host_status) | **GET** /host/{HostID}/status | Get the latest status of the host
[**get_hosts**](HostApi.md#get_hosts) | **GET** /hosts | This provides a list of hosts in the system
[**get_hosts_counts**](HostApi.md#get_hosts_counts) | **GET** /hosts/counts | Get the server counts in a time-range
[**get_hosts_counts_by_type**](HostApi.md#get_hosts_counts_by_type) | **GET** /hosts/counts_by_type | Get the server counts in a time-range
[**get_hosts_launch**](HostApi.md#get_hosts_launch) | **GET** /host/{HostID}/launch | This provides a list of host launches in the system
[**host_alert**](HostApi.md#host_alert) | **POST** /host/alert | Notifies the controller about a system alert.
[**launch_host**](HostApi.md#launch_host) | **POST** /host/launch | Launch a new host with a particular server type
[**pause_host**](HostApi.md#pause_host) | **POST** /host/{HostID}/pause | Pause all engines on this host.
[**register_engine_instance**](HostApi.md#register_engine_instance) | **POST** /host/{HostID}/engine/register | Register a new engine instance
[**register_host**](HostApi.md#register_host) | **POST** /host/register | Update the Host Status
[**resume_host**](HostApi.md#resume_host) | **POST** /host/{HostID}/resume | Resume all engines on this host.
[**terminate_host**](HostApi.md#terminate_host) | **POST** /host/{HostID}/terminate | Delete the host/agent record.  Any work still running on this host will be restarted on other hosts.
[**update_host_status**](HostApi.md#update_host_status) | **POST** /host/{HostID}/updatestatus | Update the Host Status


# **drain_host**
> AdminOperationResponse drain_host(host_id, drain_host_request, x_correlation_id=x_correlation_id)

Put this host into drain mode.  A host in drain mode will not have work assigned to engines on the host.

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
    api_instance = client.HostApi(api_client)
    host_id = 'host_id_example' # str | ID of Host
drain_host_request = client.DrainHostRequest() # DrainHostRequest | The Request to Drain a Host
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Put this host into drain mode.  A host in drain mode will not have work assigned to engines on the host.
        api_response = api_instance.drain_host(host_id, drain_host_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->drain_host: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_id** | [**str**](.md)| ID of Host | 
 **drain_host_request** | [**DrainHostRequest**](DrainHostRequest.md)| The Request to Drain a Host | 
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
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_host_cpu_usage**
> GetHostCPUUsageResponse get_host_cpu_usage(interval=interval, start_time=start_time, end_time=end_time, type=type, host_id=host_id)

Get host cpu usage

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
    api_instance = client.HostApi(api_client)
    interval = 56 # int | Interval in seconds for output time ranges. (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
type = client.RunModeEnum() # RunModeEnum | Filter for hosts by type (optional)
host_id = 'host_id_example' # str | Filter data by hostID (optional)

    try:
        # Get host cpu usage
        api_response = api_instance.get_host_cpu_usage(interval=interval, start_time=start_time, end_time=end_time, type=type, host_id=host_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->get_host_cpu_usage: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **int**| Interval in seconds for output time ranges. | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **type** | [**RunModeEnum**](.md)| Filter for hosts by type | [optional] 
 **host_id** | [**str**](.md)| Filter data by hostID | [optional] 

### Return type

[**GetHostCPUUsageResponse**](GetHostCPUUsageResponse.md)

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

# **get_host_detail**
> HostDetail get_host_detail(host_id, x_correlation_id=x_correlation_id)

Get the latest info of the host

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
    api_instance = client.HostApi(api_client)
    host_id = 'host_id_example' # str | ID of Host
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get the latest info of the host
        api_response = api_instance.get_host_detail(host_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->get_host_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_id** | [**str**](.md)| ID of Host | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**HostDetail**](HostDetail.md)

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

# **get_host_memory_usage**
> GetHostMemoryUsageResponse get_host_memory_usage(interval=interval, start_time=start_time, end_time=end_time, type=type, host_id=host_id)

Get host memory usage

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
    api_instance = client.HostApi(api_client)
    interval = 56 # int | Interval in seconds for output time ranges. (optional)
start_time = 56 # int | The unix timestamp, describing the start time for the stats (optional)
end_time = 56 # int | The unix timestamp, describing the end time for the stats (optional)
type = client.RunModeEnum() # RunModeEnum | Filter for hosts by type (optional)
host_id = 'host_id_example' # str | Filter data by hostID (optional)

    try:
        # Get host memory usage
        api_response = api_instance.get_host_memory_usage(interval=interval, start_time=start_time, end_time=end_time, type=type, host_id=host_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->get_host_memory_usage: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **int**| Interval in seconds for output time ranges. | [optional] 
 **start_time** | **int**| The unix timestamp, describing the start time for the stats | [optional] 
 **end_time** | **int**| The unix timestamp, describing the end time for the stats | [optional] 
 **type** | [**RunModeEnum**](.md)| Filter for hosts by type | [optional] 
 **host_id** | [**str**](.md)| Filter data by hostID | [optional] 

### Return type

[**GetHostMemoryUsageResponse**](GetHostMemoryUsageResponse.md)

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

# **get_host_status**
> HostStatus get_host_status(host_id, x_correlation_id=x_correlation_id)

Get the latest status of the host

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
    api_instance = client.HostApi(api_client)
    host_id = 'host_id_example' # str | ID of Host
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get the latest status of the host
        api_response = api_instance.get_host_status(host_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->get_host_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_id** | [**str**](.md)| ID of Host | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**HostStatus**](HostStatus.md)

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

# **get_hosts**
> AdminHostsGetResponse get_hosts(x_correlation_id=x_correlation_id, offset=offset, limit=limit, direction=direction, isactive=isactive, type=type, server_type=server_type, start_created_time=start_created_time, end_created_time=end_created_time, start_last_update_time=start_last_update_time, end_last_update_time=end_last_update_time, start_terminated_time=start_terminated_time, end_terminated_time=end_terminated_time, start_expire_time=start_expire_time, end_expire_time=end_expire_time, order_by=order_by, drain=drain, server_type_id=server_type_id, ip=ip)

This provides a list of hosts in the system

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
    api_instance = client.HostApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
direction = 'DESC' # str | the sort order.  ASC or DESC. (optional) (default to 'DESC')
isactive = True # bool | Filter for active or inactive hosts (optional)
type = client.RunModeEnum() # RunModeEnum | Filter for hosts by type (optional)
server_type = 'server_type_example' # str | Filter for server type. Currently it should be in [physical, virtual]. It can expand in the future (optional)
start_created_time = 56 # int | The unix timestamp (optional)
end_created_time = 56 # int | The unix timestamp (optional)
start_last_update_time = 56 # int | The unix timestamp (optional)
end_last_update_time = 56 # int | The unix timestamp (optional)
start_terminated_time = 56 # int | The unix timestamp (optional)
end_terminated_time = 56 # int | The unix timestamp (optional)
start_expire_time = 56 # int | The unix timestamp (optional)
end_expire_time = 56 # int | The unix timestamp (optional)
order_by = 'order_by_example' # str | It should be in [createdTime, terminatedTime, expireTime] (optional)
drain = True # bool | Filter by drain (optional)
server_type_id = 'server_type_id_example' # str | Filter by serverTypeID (optional)
ip = 'ip_example' # str | Filter by IP (optional)

    try:
        # This provides a list of hosts in the system
        api_response = api_instance.get_hosts(x_correlation_id=x_correlation_id, offset=offset, limit=limit, direction=direction, isactive=isactive, type=type, server_type=server_type, start_created_time=start_created_time, end_created_time=end_created_time, start_last_update_time=start_last_update_time, end_last_update_time=end_last_update_time, start_terminated_time=start_terminated_time, end_terminated_time=end_terminated_time, start_expire_time=start_expire_time, end_expire_time=end_expire_time, order_by=order_by, drain=drain, server_type_id=server_type_id, ip=ip)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->get_hosts: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **direction** | **str**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **isactive** | **bool**| Filter for active or inactive hosts | [optional] 
 **type** | [**RunModeEnum**](.md)| Filter for hosts by type | [optional] 
 **server_type** | **str**| Filter for server type. Currently it should be in [physical, virtual]. It can expand in the future | [optional] 
 **start_created_time** | **int**| The unix timestamp | [optional] 
 **end_created_time** | **int**| The unix timestamp | [optional] 
 **start_last_update_time** | **int**| The unix timestamp | [optional] 
 **end_last_update_time** | **int**| The unix timestamp | [optional] 
 **start_terminated_time** | **int**| The unix timestamp | [optional] 
 **end_terminated_time** | **int**| The unix timestamp | [optional] 
 **start_expire_time** | **int**| The unix timestamp | [optional] 
 **end_expire_time** | **int**| The unix timestamp | [optional] 
 **order_by** | **str**| It should be in [createdTime, terminatedTime, expireTime] | [optional] 
 **drain** | **bool**| Filter by drain | [optional] 
 **server_type_id** | [**str**](.md)| Filter by serverTypeID | [optional] 
 **ip** | **str**| Filter by IP | [optional] 

### Return type

[**AdminHostsGetResponse**](AdminHostsGetResponse.md)

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

# **get_hosts_counts**
> HostsCountsResponse get_hosts_counts(x_correlation_id=x_correlation_id, start_last_update_time=start_last_update_time, end_last_update_time=end_last_update_time)

Get the server counts in a time-range

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
    api_instance = client.HostApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_last_update_time = 56 # int | The unix timestamp (optional)
end_last_update_time = 56 # int | The unix timestamp (optional)

    try:
        # Get the server counts in a time-range
        api_response = api_instance.get_hosts_counts(x_correlation_id=x_correlation_id, start_last_update_time=start_last_update_time, end_last_update_time=end_last_update_time)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->get_hosts_counts: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_last_update_time** | **int**| The unix timestamp | [optional] 
 **end_last_update_time** | **int**| The unix timestamp | [optional] 

### Return type

[**HostsCountsResponse**](HostsCountsResponse.md)

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

# **get_hosts_counts_by_type**
> HostsCountsByTypeResponse get_hosts_counts_by_type(x_correlation_id=x_correlation_id, start_last_update_time=start_last_update_time, end_last_update_time=end_last_update_time, chart_type=chart_type, type=type)

Get the server counts in a time-range

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
    api_instance = client.HostApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
start_last_update_time = 56 # int | The unix timestamp (optional)
end_last_update_time = 56 # int | The unix timestamp (optional)
chart_type = client.ChartTypeEnum() # ChartTypeEnum | It will help API to kmow the response should return (optional)
type = client.RunModeEnum() # RunModeEnum | Filter for hosts by type (optional)

    try:
        # Get the server counts in a time-range
        api_response = api_instance.get_hosts_counts_by_type(x_correlation_id=x_correlation_id, start_last_update_time=start_last_update_time, end_last_update_time=end_last_update_time, chart_type=chart_type, type=type)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->get_hosts_counts_by_type: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **start_last_update_time** | **int**| The unix timestamp | [optional] 
 **end_last_update_time** | **int**| The unix timestamp | [optional] 
 **chart_type** | [**ChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] 
 **type** | [**RunModeEnum**](.md)| Filter for hosts by type | [optional] 

### Return type

[**HostsCountsByTypeResponse**](HostsCountsByTypeResponse.md)

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

# **get_hosts_launch**
> GetHostLaunchResponse get_hosts_launch(host_id, x_correlation_id=x_correlation_id)

This provides a list of host launches in the system

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
    api_instance = client.HostApi(api_client)
    host_id = 'host_id_example' # str | ID of Host
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides a list of host launches in the system
        api_response = api_instance.get_hosts_launch(host_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->get_hosts_launch: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_id** | [**str**](.md)| ID of Host | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetHostLaunchResponse**](GetHostLaunchResponse.md)

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

# **host_alert**
> AdminOperationResponse host_alert(host_alert_request, x_correlation_id=x_correlation_id)

Notifies the controller about a system alert.

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
    api_instance = client.HostApi(api_client)
    host_alert_request = client.HostAlertRequest() # HostAlertRequest | 
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Notifies the controller about a system alert.
        api_response = api_instance.host_alert(host_alert_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->host_alert: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_alert_request** | [**HostAlertRequest**](HostAlertRequest.md)|  | 
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
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **launch_host**
> AdminOperationResponse launch_host(launch_host_request)

Launch a new host with a particular server type

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
    api_instance = client.HostApi(api_client)
    launch_host_request = client.LaunchHostRequest() # LaunchHostRequest | The Request to Launch a Host

    try:
        # Launch a new host with a particular server type
        api_response = api_instance.launch_host(launch_host_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->launch_host: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **launch_host_request** | [**LaunchHostRequest**](LaunchHostRequest.md)| The Request to Launch a Host | 

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
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pause_host**
> AdminOperationResponse pause_host(host_id, x_correlation_id=x_correlation_id)

Pause all engines on this host.

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
    api_instance = client.HostApi(api_client)
    host_id = 'host_id_example' # str | ID of Host
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Pause all engines on this host.
        api_response = api_instance.pause_host(host_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->pause_host: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_id** | [**str**](.md)| ID of Host | 
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

# **register_engine_instance**
> EngineInstanceRegistrationInfo register_engine_instance(host_id, engine_instance_info, x_correlation_id=x_correlation_id)

Register a new engine instance

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
    api_instance = client.HostApi(api_client)
    host_id = 'host_id_example' # str | ID of Host
engine_instance_info = client.EngineInstanceInfo() # EngineInstanceInfo | Engine Instance Info
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Register a new engine instance
        api_response = api_instance.register_engine_instance(host_id, engine_instance_info, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->register_engine_instance: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_id** | [**str**](.md)| ID of Host | 
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

# **register_host**
> HostRegisterResponse register_host(host_register_request, x_correlation_id=x_correlation_id)

Update the Host Status

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
    api_instance = client.HostApi(api_client)
    host_register_request = client.HostRegisterRequest() # HostRegisterRequest | Engine Instance Info
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Update the Host Status
        api_response = api_instance.register_host(host_register_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->register_host: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_register_request** | [**HostRegisterRequest**](HostRegisterRequest.md)| Engine Instance Info | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**HostRegisterResponse**](HostRegisterResponse.md)

### Authorization

No authorization required

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

# **resume_host**
> AdminOperationResponse resume_host(host_id, x_correlation_id=x_correlation_id)

Resume all engines on this host.

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
    api_instance = client.HostApi(api_client)
    host_id = 'host_id_example' # str | ID of Host
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Resume all engines on this host.
        api_response = api_instance.resume_host(host_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->resume_host: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_id** | [**str**](.md)| ID of Host | 
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

# **terminate_host**
> AdminOperationResponse terminate_host(host_id, terminate_host_request, x_correlation_id=x_correlation_id)

Delete the host/agent record.  Any work still running on this host will be restarted on other hosts.

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
    api_instance = client.HostApi(api_client)
    host_id = 'host_id_example' # str | ID of Host
terminate_host_request = client.TerminateHostRequest() # TerminateHostRequest | The request to terminate the host
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Delete the host/agent record.  Any work still running on this host will be restarted on other hosts.
        api_response = api_instance.terminate_host(host_id, terminate_host_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->terminate_host: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_id** | [**str**](.md)| ID of Host | 
 **terminate_host_request** | [**TerminateHostRequest**](TerminateHostRequest.md)| The request to terminate the host | 
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
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_host_status**
> HostAction update_host_status(host_id, host_status, x_correlation_id=x_correlation_id)

Update the Host Status

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
    api_instance = client.HostApi(api_client)
    host_id = 'host_id_example' # str | ID of Host
host_status = client.HostStatus() # HostStatus | Host Status
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Update the Host Status
        api_response = api_instance.update_host_status(host_id, host_status, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling HostApi->update_host_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_id** | [**str**](.md)| ID of Host | 
 **host_status** | [**HostStatus**](HostStatus.md)| Host Status | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**HostAction**](HostAction.md)

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

