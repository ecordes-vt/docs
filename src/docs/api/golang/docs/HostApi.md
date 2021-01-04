# \HostApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DrainHost**](HostApi.md#DrainHost) | **Post** /host/{HostID}/drain | Put this host into drain mode.  A host in drain mode will not have work assigned to engines on the host.
[**GetHostCpuUsage**](HostApi.md#GetHostCpuUsage) | **Get** /hosts/cpu_usage | Get host cpu usage
[**GetHostDetail**](HostApi.md#GetHostDetail) | **Get** /host/{HostID}/detail | Get the latest info of the host
[**GetHostMemoryUsage**](HostApi.md#GetHostMemoryUsage) | **Get** /engine/memory_usage | Get host memory usage
[**GetHostStatus**](HostApi.md#GetHostStatus) | **Get** /host/{HostID}/status | Get the latest status of the host
[**GetHosts**](HostApi.md#GetHosts) | **Get** /hosts | This provides a list of hosts in the system
[**GetHostsCounts**](HostApi.md#GetHostsCounts) | **Get** /hosts/counts | Get the server counts in a time-range
[**GetHostsCountsByType**](HostApi.md#GetHostsCountsByType) | **Get** /hosts/counts_by_type | Get the server counts in a time-range
[**GetHostsLaunch**](HostApi.md#GetHostsLaunch) | **Get** /host/{HostID}/launch | This provides a list of host launches in the system
[**HostAlert**](HostApi.md#HostAlert) | **Post** /host/alert | Notifies the controller about a system alert.
[**LaunchHost**](HostApi.md#LaunchHost) | **Post** /host/launch | Launch a new host with a particular server type
[**PauseHost**](HostApi.md#PauseHost) | **Post** /host/{HostID}/pause | Pause all engines on this host.
[**RegisterEngineInstance**](HostApi.md#RegisterEngineInstance) | **Post** /host/{HostID}/engine/register | Register a new engine instance
[**RegisterHost**](HostApi.md#RegisterHost) | **Post** /host/register | Update the Host Status
[**ResumeHost**](HostApi.md#ResumeHost) | **Post** /host/{HostID}/resume | Resume all engines on this host.
[**TerminateHost**](HostApi.md#TerminateHost) | **Post** /host/{HostID}/terminate | Delete the host/agent record.  Any work still running on this host will be restarted on other hosts.
[**UpdateHostStatus**](HostApi.md#UpdateHostStatus) | **Post** /host/{HostID}/updatestatus | Update the Host Status



## DrainHost

> AdminOperationResponse DrainHost(ctx, hostID, drainHostRequest, optional)

Put this host into drain mode.  A host in drain mode will not have work assigned to engines on the host.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostID** | [**string**](.md)| ID of Host | 
**drainHostRequest** | [**DrainHostRequest**](DrainHostRequest.md)| The Request to Drain a Host | 
 **optional** | ***DrainHostOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DrainHostOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

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


## GetHostCpuUsage

> GetHostCpuUsageResponse GetHostCpuUsage(ctx, optional)

Get host cpu usage

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetHostCpuUsageOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetHostCpuUsageOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **optional.Int64**| Interval in seconds for output time ranges. | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **type_** | [**optional.Interface of RunModeEnum**](.md)| Filter for hosts by type | 
 **hostID** | [**optional.Interface of string**](.md)| Filter data by hostID | 

### Return type

[**GetHostCpuUsageResponse**](GetHostCPUUsageResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetHostDetail

> HostDetail GetHostDetail(ctx, hostID, optional)

Get the latest info of the host

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostID** | [**string**](.md)| ID of Host | 
 **optional** | ***GetHostDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetHostDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**HostDetail**](HostDetail.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetHostMemoryUsage

> GetHostMemoryUsageResponse GetHostMemoryUsage(ctx, optional)

Get host memory usage

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetHostMemoryUsageOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetHostMemoryUsageOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **optional.Int64**| Interval in seconds for output time ranges. | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **type_** | [**optional.Interface of RunModeEnum**](.md)| Filter for hosts by type | 
 **hostID** | [**optional.Interface of string**](.md)| Filter data by hostID | 

### Return type

[**GetHostMemoryUsageResponse**](GetHostMemoryUsageResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetHostStatus

> HostStatus GetHostStatus(ctx, hostID, optional)

Get the latest status of the host

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostID** | [**string**](.md)| ID of Host | 
 **optional** | ***GetHostStatusOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetHostStatusOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**HostStatus**](HostStatus.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetHosts

> AdminHostsGetResponse GetHosts(ctx, optional)

This provides a list of hosts in the system

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetHostsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetHostsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **direction** | **optional.String**| the sort order.  ASC or DESC. | [default to DESC]
 **isactive** | **optional.Bool**| Filter for active or inactive hosts | 
 **type_** | [**optional.Interface of RunModeEnum**](.md)| Filter for hosts by type | 
 **serverType** | **optional.String**| Filter for server type. Currently it should be in [physical, virtual]. It can expand in the future | 
 **startCreatedTime** | **optional.Int64**| The unix timestamp | 
 **endCreatedTime** | **optional.Int64**| The unix timestamp | 
 **startLastUpdateTime** | **optional.Int64**| The unix timestamp | 
 **endLastUpdateTime** | **optional.Int64**| The unix timestamp | 
 **startTerminatedTime** | **optional.Int64**| The unix timestamp | 
 **endTerminatedTime** | **optional.Int64**| The unix timestamp | 
 **startExpireTime** | **optional.Int64**| The unix timestamp | 
 **endExpireTime** | **optional.Int64**| The unix timestamp | 
 **orderBy** | **optional.String**| It should be in [createdTime, terminatedTime, expireTime] | 
 **drain** | **optional.Bool**| Filter by drain | 
 **serverTypeID** | [**optional.Interface of string**](.md)| Filter by serverTypeID | 
 **ip** | **optional.String**| Filter by IP | 

### Return type

[**AdminHostsGetResponse**](AdminHostsGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetHostsCounts

> HostsCountsResponse GetHostsCounts(ctx, optional)

Get the server counts in a time-range

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetHostsCountsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetHostsCountsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startLastUpdateTime** | **optional.Int64**| The unix timestamp | 
 **endLastUpdateTime** | **optional.Int64**| The unix timestamp | 

### Return type

[**HostsCountsResponse**](HostsCountsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetHostsCountsByType

> HostsCountsByTypeResponse GetHostsCountsByType(ctx, optional)

Get the server counts in a time-range

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetHostsCountsByTypeOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetHostsCountsByTypeOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **startLastUpdateTime** | **optional.Int64**| The unix timestamp | 
 **endLastUpdateTime** | **optional.Int64**| The unix timestamp | 
 **chartType** | [**optional.Interface of ChartTypeEnum**](.md)| It will help API to kmow the response should return | 
 **type_** | [**optional.Interface of RunModeEnum**](.md)| Filter for hosts by type | 

### Return type

[**HostsCountsByTypeResponse**](HostsCountsByTypeResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetHostsLaunch

> GetHostLaunchResponse GetHostsLaunch(ctx, hostID, optional)

This provides a list of host launches in the system

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostID** | [**string**](.md)| ID of Host | 
 **optional** | ***GetHostsLaunchOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetHostsLaunchOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetHostLaunchResponse**](GetHostLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## HostAlert

> AdminOperationResponse HostAlert(ctx, hostAlertRequest, optional)

Notifies the controller about a system alert.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostAlertRequest** | [**HostAlertRequest**](HostAlertRequest.md)|  | 
 **optional** | ***HostAlertOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a HostAlertOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

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


## LaunchHost

> AdminOperationResponse LaunchHost(ctx, launchHostRequest)

Launch a new host with a particular server type

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**launchHostRequest** | [**LaunchHostRequest**](LaunchHostRequest.md)| The Request to Launch a Host | 

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


## PauseHost

> AdminOperationResponse PauseHost(ctx, hostID, optional)

Pause all engines on this host.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostID** | [**string**](.md)| ID of Host | 
 **optional** | ***PauseHostOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a PauseHostOpts struct


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


## RegisterEngineInstance

> EngineInstanceRegistrationInfo RegisterEngineInstance(ctx, hostID, engineInstanceInfo, optional)

Register a new engine instance

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostID** | [**string**](.md)| ID of Host | 
**engineInstanceInfo** | [**EngineInstanceInfo**](EngineInstanceInfo.md)| Engine Instance Info | 
 **optional** | ***RegisterEngineInstanceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a RegisterEngineInstanceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**EngineInstanceRegistrationInfo**](EngineInstanceRegistrationInfo.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RegisterHost

> HostRegisterResponse RegisterHost(ctx, hostRegisterRequest, optional)

Update the Host Status

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostRegisterRequest** | [**HostRegisterRequest**](HostRegisterRequest.md)| Engine Instance Info | 
 **optional** | ***RegisterHostOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a RegisterHostOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**HostRegisterResponse**](HostRegisterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ResumeHost

> AdminOperationResponse ResumeHost(ctx, hostID, optional)

Resume all engines on this host.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostID** | [**string**](.md)| ID of Host | 
 **optional** | ***ResumeHostOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a ResumeHostOpts struct


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


## TerminateHost

> AdminOperationResponse TerminateHost(ctx, hostID, terminateHostRequest, optional)

Delete the host/agent record.  Any work still running on this host will be restarted on other hosts.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostID** | [**string**](.md)| ID of Host | 
**terminateHostRequest** | [**TerminateHostRequest**](TerminateHostRequest.md)| The request to terminate the host | 
 **optional** | ***TerminateHostOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a TerminateHostOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

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


## UpdateHostStatus

> HostAction UpdateHostStatus(ctx, hostID, hostStatus, optional)

Update the Host Status

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostID** | [**string**](.md)| ID of Host | 
**hostStatus** | [**HostStatus**](HostStatus.md)| Host Status | 
 **optional** | ***UpdateHostStatusOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateHostStatusOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**HostAction**](HostAction.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

