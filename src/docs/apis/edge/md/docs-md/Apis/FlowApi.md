# FlowApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cleanAutomateRequests**](FlowApi.md#cleanAutomateRequests) | **GET** /flowaction/requests/clean | Clean old automate requests.
[**createNodeRedContainerInfo**](FlowApi.md#createNodeRedContainerInfo) | **POST** /flow/nrcontainer/create | Create node-red container infomation
[**deleteAutomateContainer**](FlowApi.md#deleteAutomateContainer) | **POST** /flow/delete/{ContainerID} | Delete automate container.
[**updateAutomateRequestStatus**](FlowApi.md#updateAutomateRequestStatus) | **POST** /flow/request/update | Put this automate request into update status mode. This automate request will be updated to new status.
[**updateAutomateStatus**](FlowApi.md#updateAutomateStatus) | **POST** /flow/{HostID}/updatestatus | Get updated information to launch node-red container, terminate node-red container.


<a name="cleanAutomateRequests"></a>
# **cleanAutomateRequests**
> AdminOperationResponse cleanAutomateRequests()

Clean old automate requests.

### Parameters
This endpoint does not need any parameter.

### Return type

[**AdminOperationResponse**](../Models/AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="createNodeRedContainerInfo"></a>
# **createNodeRedContainerInfo**
> AdminOperationResponse createNodeRedContainerInfo(CreateNodRedContainerDetail, X-Correlation-Id)

Create node-red container infomation

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateNodRedContainerDetail** | [**CreateNodRedContainerDetail**](../Models/CreateNodRedContainerDetail.md)| Node-RED container info |
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](../Models/AdminOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deleteAutomateContainer"></a>
# **deleteAutomateContainer**
> AdminOperationResponse deleteAutomateContainer(ContainerID)

Delete automate container.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ContainerID** | **String**| ContainerID of node-red container | [default to null]

### Return type

[**AdminOperationResponse**](../Models/AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="updateAutomateRequestStatus"></a>
# **updateAutomateRequestStatus**
> AdminOperationResponse updateAutomateRequestStatus(UpdateNodeRedRequestDetail, X-Correlation-Id)

Put this automate request into update status mode. This automate request will be updated to new status.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **UpdateNodeRedRequestDetail** | [**UpdateNodeRedRequestDetail**](../Models/UpdateNodeRedRequestDetail.md)| Node-RED container info |
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](../Models/AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="updateAutomateStatus"></a>
# **updateAutomateStatus**
> HostAction updateAutomateStatus(HostID)

Get updated information to launch node-red container, terminate node-red container.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **HostID** | [**UUID**](../Models/.md)| ID of Host | [default to null]

### Return type

[**HostAction**](../Models/HostAction.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

