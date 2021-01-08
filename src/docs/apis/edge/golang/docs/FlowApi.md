# \FlowApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CleanAutomateRequests**](FlowApi.md#CleanAutomateRequests) | **Get** /flowaction/requests/clean | Clean old automate requests.
[**CreateNodeRedContainerInfo**](FlowApi.md#CreateNodeRedContainerInfo) | **Post** /flow/nrcontainer/create | Create node-red container infomation
[**DeleteAutomateContainer**](FlowApi.md#DeleteAutomateContainer) | **Post** /flow/delete/{ContainerID} | Delete automate container.
[**UpdateAutomateRequestStatus**](FlowApi.md#UpdateAutomateRequestStatus) | **Post** /flow/request/update | Put this automate request into update status mode. This automate request will be updated to new status.
[**UpdateAutomateStatus**](FlowApi.md#UpdateAutomateStatus) | **Post** /flow/{HostID}/updatestatus | Get updated information to launch node-red container, terminate node-red container.



## CleanAutomateRequests

> AdminOperationResponse CleanAutomateRequests(ctx, )

Clean old automate requests.

### Required Parameters

This endpoint does not need any parameter.

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


## CreateNodeRedContainerInfo

> AdminOperationResponse CreateNodeRedContainerInfo(ctx, createNodRedContainerDetail, optional)

Create node-red container infomation

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**createNodRedContainerDetail** | [**CreateNodRedContainerDetail**](CreateNodRedContainerDetail.md)| Node-RED container info | 
 **optional** | ***CreateNodeRedContainerInfoOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateNodeRedContainerInfoOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteAutomateContainer

> AdminOperationResponse DeleteAutomateContainer(ctx, containerID)

Delete automate container.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**containerID** | **string**| ContainerID of node-red container | 

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


## UpdateAutomateRequestStatus

> AdminOperationResponse UpdateAutomateRequestStatus(ctx, updateNodeRedRequestDetail, optional)

Put this automate request into update status mode. This automate request will be updated to new status.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**updateNodeRedRequestDetail** | [**UpdateNodeRedRequestDetail**](UpdateNodeRedRequestDetail.md)| Node-RED container info | 
 **optional** | ***UpdateAutomateRequestStatusOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateAutomateRequestStatusOpts struct


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


## UpdateAutomateStatus

> HostAction UpdateAutomateStatus(ctx, hostID)

Get updated information to launch node-red container, terminate node-red container.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostID** | [**string**](.md)| ID of Host | 

### Return type

[**HostAction**](HostAction.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

