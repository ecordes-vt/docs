# AiwareJsClient.FlowApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cleanAutomateRequests**](FlowApi.md#cleanAutomateRequests) | **GET** /flowaction/requests/clean | Clean old automate requests.
[**createNodeRedContainerInfo**](FlowApi.md#createNodeRedContainerInfo) | **POST** /flow/nrcontainer/create | Create node-red container infomation
[**deleteAutomateContainer**](FlowApi.md#deleteAutomateContainer) | **POST** /flow/delete/{ContainerID} | Delete automate container.
[**updateAutomateRequestStatus**](FlowApi.md#updateAutomateRequestStatus) | **POST** /flow/request/update | Put this automate request into update status mode. This automate request will be updated to new status.
[**updateAutomateStatus**](FlowApi.md#updateAutomateStatus) | **POST** /flow/{HostID}/updatestatus | Get updated information to launch node-red container, terminate node-red container.



## cleanAutomateRequests

> AdminOperationResponse cleanAutomateRequests()

Clean old automate requests.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.FlowApi();
apiInstance.cleanAutomateRequests((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
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


## createNodeRedContainerInfo

> AdminOperationResponse createNodeRedContainerInfo(createNodRedContainerDetail, opts)

Create node-red container infomation

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';

let apiInstance = new AiwareJsClient.FlowApi();
let createNodRedContainerDetail = new AiwareJsClient.CreateNodRedContainerDetail(); // CreateNodRedContainerDetail | Node-RED container info
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createNodeRedContainerInfo(createNodRedContainerDetail, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createNodRedContainerDetail** | [**CreateNodRedContainerDetail**](CreateNodRedContainerDetail.md)| Node-RED container info | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## deleteAutomateContainer

> AdminOperationResponse deleteAutomateContainer(containerID)

Delete automate container.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.FlowApi();
let containerID = "containerID_example"; // String | ContainerID of node-red container
apiInstance.deleteAutomateContainer(containerID, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **containerID** | **String**| ContainerID of node-red container | 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## updateAutomateRequestStatus

> AdminOperationResponse updateAutomateRequestStatus(updateNodeRedRequestDetail, opts)

Put this automate request into update status mode. This automate request will be updated to new status.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.FlowApi();
let updateNodeRedRequestDetail = new AiwareJsClient.UpdateNodeRedRequestDetail(); // UpdateNodeRedRequestDetail | Node-RED container info
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateAutomateRequestStatus(updateNodeRedRequestDetail, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **updateNodeRedRequestDetail** | [**UpdateNodeRedRequestDetail**](UpdateNodeRedRequestDetail.md)| Node-RED container info | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateAutomateStatus

> HostAction updateAutomateStatus(hostID)

Get updated information to launch node-red container, terminate node-red container.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.FlowApi();
let hostID = null; // String | ID of Host
apiInstance.updateAutomateStatus(hostID, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hostID** | [**String**](.md)| ID of Host | 

### Return type

[**HostAction**](HostAction.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

