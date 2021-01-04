# FlowApi

All URIs are relative to */edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cleanAutomateRequests**](FlowApi.md#cleanAutomateRequests) | **GET** /flowaction/requests/clean | Clean old automate requests.
[**createNodeRedContainerInfo**](FlowApi.md#createNodeRedContainerInfo) | **POST** /flow/nrcontainer/create | Create node-red container infomation
[**deleteAutomateContainer**](FlowApi.md#deleteAutomateContainer) | **POST** /flow/delete/{ContainerID} | Delete automate container.
[**updateAutomateRequestStatus**](FlowApi.md#updateAutomateRequestStatus) | **POST** /flow/request/update | Put this automate request into update status mode. This automate request will be updated to new status.
[**updateAutomateStatus**](FlowApi.md#updateAutomateStatus) | **POST** /flow/{HostID}/updatestatus | Get updated information to launch node-red container, terminate node-red container.



## cleanAutomateRequests

Clean old automate requests.

### Example

```bash
aiware cleanAutomateRequests
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## createNodeRedContainerInfo

Create node-red container infomation

### Example

```bash
aiware createNodeRedContainerInfo X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createNodRedContainerDetail** | [**CreateNodRedContainerDetail**](CreateNodRedContainerDetail.md) | Node-RED container info |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deleteAutomateContainer

Delete automate container.

### Example

```bash
aiware deleteAutomateContainer ContainerID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **containerID** | **string** | ContainerID of node-red container | [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateAutomateRequestStatus

Put this automate request into update status mode. This automate request will be updated to new status.

### Example

```bash
aiware updateAutomateRequestStatus X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **updateNodeRedRequestDetail** | [**UpdateNodeRedRequestDetail**](UpdateNodeRedRequestDetail.md) | Node-RED container info |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateAutomateStatus

Get updated information to launch node-red container, terminate node-red container.

### Example

```bash
aiware updateAutomateStatus HostID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostID** | [**string**](.md) | ID of Host | [default to null]

### Return type

[**HostAction**](HostAction.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

