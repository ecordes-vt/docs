# HostApi

All URIs are relative to */edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**drainHost**](HostApi.md#drainHost) | **POST** /host/{HostID}/drain | Put this host into drain mode.  A host in drain mode will not have work assigned to engines on the host.
[**getHostCpuUsage**](HostApi.md#getHostCpuUsage) | **GET** /hosts/cpu_usage | Get host cpu usage
[**getHostDetail**](HostApi.md#getHostDetail) | **GET** /host/{HostID}/detail | Get the latest info of the host
[**getHostMemoryUsage**](HostApi.md#getHostMemoryUsage) | **GET** /engine/memory_usage | Get host memory usage
[**getHostStatus**](HostApi.md#getHostStatus) | **GET** /host/{HostID}/status | Get the latest status of the host
[**getHosts**](HostApi.md#getHosts) | **GET** /hosts | This provides a list of hosts in the system
[**getHostsCounts**](HostApi.md#getHostsCounts) | **GET** /hosts/counts | Get the server counts in a time-range
[**getHostsCountsByType**](HostApi.md#getHostsCountsByType) | **GET** /hosts/counts_by_type | Get the server counts in a time-range
[**getHostsLaunch**](HostApi.md#getHostsLaunch) | **GET** /host/{HostID}/launch | This provides a list of host launches in the system
[**hostAlert**](HostApi.md#hostAlert) | **POST** /host/alert | Notifies the controller about a system alert.
[**launchHost**](HostApi.md#launchHost) | **POST** /host/launch | Launch a new host with a particular server type
[**pauseHost**](HostApi.md#pauseHost) | **POST** /host/{HostID}/pause | Pause all engines on this host.
[**registerEngineInstance**](HostApi.md#registerEngineInstance) | **POST** /host/{HostID}/engine/register | Register a new engine instance
[**registerHost**](HostApi.md#registerHost) | **POST** /host/register | Update the Host Status
[**resumeHost**](HostApi.md#resumeHost) | **POST** /host/{HostID}/resume | Resume all engines on this host.
[**terminateHost**](HostApi.md#terminateHost) | **POST** /host/{HostID}/terminate | Delete the host/agent record.  Any work still running on this host will be restarted on other hosts.
[**updateHostStatus**](HostApi.md#updateHostStatus) | **POST** /host/{HostID}/updatestatus | Update the Host Status



## drainHost

Put this host into drain mode.  A host in drain mode will not have work assigned to engines on the host.

### Example

```bash
aiware drainHost HostID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostID** | [**string**](.md) | ID of Host | [default to null]
 **drainHostRequest** | [**DrainHostRequest**](DrainHostRequest.md) | The Request to Drain a Host |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getHostCpuUsage

Get host cpu usage

### Example

```bash
aiware getHostCpuUsage  interval=value  startTime=value  endTime=value  type=value  hostID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **integer** | Interval in seconds for output time ranges. | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **type** | [**RunModeEnum**](.md) | Filter for hosts by type | [optional] [default to null]
 **hostID** | [**string**](.md) | Filter data by hostID | [optional] [default to null]

### Return type

[**GetHostCPUUsageResponse**](GetHostCPUUsageResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getHostDetail

Get the latest info of the host

### Example

```bash
aiware getHostDetail HostID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostID** | [**string**](.md) | ID of Host | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**HostDetail**](HostDetail.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getHostMemoryUsage

Get host memory usage

### Example

```bash
aiware getHostMemoryUsage  interval=value  startTime=value  endTime=value  type=value  hostID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **integer** | Interval in seconds for output time ranges. | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **type** | [**RunModeEnum**](.md) | Filter for hosts by type | [optional] [default to null]
 **hostID** | [**string**](.md) | Filter data by hostID | [optional] [default to null]

### Return type

[**GetHostMemoryUsageResponse**](GetHostMemoryUsageResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getHostStatus

Get the latest status of the host

### Example

```bash
aiware getHostStatus HostID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostID** | [**string**](.md) | ID of Host | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**HostStatus**](HostStatus.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getHosts

This provides a list of hosts in the system

### Example

```bash
aiware getHosts X-Correlation-Id:value  offset=value  limit=value  direction=value  isactive=value  type=value  serverType=value  startCreatedTime=value  endCreatedTime=value  startLastUpdateTime=value  endLastUpdateTime=value  startTerminatedTime=value  endTerminatedTime=value  startExpireTime=value  endExpireTime=value  orderBy=value  drain=value  serverTypeID=value  ip=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **offset** | **integer** | the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **integer** | the number of items to return. | [optional] [default to 10]
 **direction** | **string** | the sort order.  ASC or DESC. | [optional] [default to DESC]
 **isactive** | **boolean** | Filter for active or inactive hosts | [optional] [default to null]
 **type** | [**RunModeEnum**](.md) | Filter for hosts by type | [optional] [default to null]
 **serverType** | **string** | Filter for server type. Currently it should be in [physical, virtual]. It can expand in the future | [optional] [default to null]
 **startCreatedTime** | **integer** | The unix timestamp | [optional] [default to null]
 **endCreatedTime** | **integer** | The unix timestamp | [optional] [default to null]
 **startLastUpdateTime** | **integer** | The unix timestamp | [optional] [default to null]
 **endLastUpdateTime** | **integer** | The unix timestamp | [optional] [default to null]
 **startTerminatedTime** | **integer** | The unix timestamp | [optional] [default to null]
 **endTerminatedTime** | **integer** | The unix timestamp | [optional] [default to null]
 **startExpireTime** | **integer** | The unix timestamp | [optional] [default to null]
 **endExpireTime** | **integer** | The unix timestamp | [optional] [default to null]
 **orderBy** | **string** | It should be in [createdTime, terminatedTime, expireTime] | [optional] [default to null]
 **drain** | **boolean** | Filter by drain | [optional] [default to null]
 **serverTypeID** | [**string**](.md) | Filter by serverTypeID | [optional] [default to null]
 **ip** | **string** | Filter by IP | [optional] [default to null]

### Return type

[**AdminHostsGetResponse**](AdminHostsGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getHostsCounts

Get the server counts in a time-range

### Example

```bash
aiware getHostsCounts X-Correlation-Id:value  startLastUpdateTime=value  endLastUpdateTime=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startLastUpdateTime** | **integer** | The unix timestamp | [optional] [default to null]
 **endLastUpdateTime** | **integer** | The unix timestamp | [optional] [default to null]

### Return type

[**HostsCountsResponse**](HostsCountsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getHostsCountsByType

Get the server counts in a time-range

### Example

```bash
aiware getHostsCountsByType X-Correlation-Id:value  startLastUpdateTime=value  endLastUpdateTime=value  chartType=value  type=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **startLastUpdateTime** | **integer** | The unix timestamp | [optional] [default to null]
 **endLastUpdateTime** | **integer** | The unix timestamp | [optional] [default to null]
 **chartType** | [**ChartTypeEnum**](.md) | It will help API to kmow the response should return | [optional] [default to null]
 **type** | [**RunModeEnum**](.md) | Filter for hosts by type | [optional] [default to null]

### Return type

[**HostsCountsByTypeResponse**](HostsCountsByTypeResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getHostsLaunch

This provides a list of host launches in the system

### Example

```bash
aiware getHostsLaunch HostID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostID** | [**string**](.md) | ID of Host | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetHostLaunchResponse**](GetHostLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## hostAlert

Notifies the controller about a system alert.

### Example

```bash
aiware hostAlert X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostAlertRequest** | [**HostAlertRequest**](HostAlertRequest.md) |  |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## launchHost

Launch a new host with a particular server type

### Example

```bash
aiware launchHost
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **launchHostRequest** | [**LaunchHostRequest**](LaunchHostRequest.md) | The Request to Launch a Host |

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pauseHost

Pause all engines on this host.

### Example

```bash
aiware pauseHost HostID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostID** | [**string**](.md) | ID of Host | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## registerEngineInstance

Register a new engine instance

### Example

```bash
aiware registerEngineInstance HostID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostID** | [**string**](.md) | ID of Host | [default to null]
 **engineInstanceInfo** | [**EngineInstanceInfo**](EngineInstanceInfo.md) | Engine Instance Info |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**EngineInstanceRegistrationInfo**](EngineInstanceRegistrationInfo.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## registerHost

Update the Host Status

### Example

```bash
aiware registerHost X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostRegisterRequest** | [**HostRegisterRequest**](HostRegisterRequest.md) | Engine Instance Info |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**HostRegisterResponse**](HostRegisterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## resumeHost

Resume all engines on this host.

### Example

```bash
aiware resumeHost HostID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostID** | [**string**](.md) | ID of Host | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## terminateHost

Delete the host/agent record.  Any work still running on this host will be restarted on other hosts.

### Example

```bash
aiware terminateHost HostID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostID** | [**string**](.md) | ID of Host | [default to null]
 **terminateHostRequest** | [**TerminateHostRequest**](TerminateHostRequest.md) | The request to terminate the host |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateHostStatus

Update the Host Status

### Example

```bash
aiware updateHostStatus HostID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostID** | [**string**](.md) | ID of Host | [default to null]
 **hostStatus** | [**HostStatus**](HostStatus.md) | Host Status |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**HostAction**](HostAction.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

