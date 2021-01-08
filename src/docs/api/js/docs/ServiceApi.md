# AiwareJsClient.ServiceApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createServiceInstance**](ServiceApi.md#createServiceInstance) | **POST** /service/instance/create | This creates a new service instance
[**deleteServiceInstance**](ServiceApi.md#deleteServiceInstance) | **POST** /service/instance/{ServiceInstanceID}/delete | This deletes a service instance
[**getResourcesForServiceInstance**](ServiceApi.md#getResourcesForServiceInstance) | **GET** /service/instance/{ServiceInstanceID}/resources | Get resources for service instance



## createServiceInstance

> ServiceInstanceCreateResponse createServiceInstance(serviceInstanceCreateRequest, opts)

This creates a new service instance

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ServiceApi();
let serviceInstanceCreateRequest = new AiwareJsClient.ServiceInstanceCreateRequest(); // ServiceInstanceCreateRequest | The input for createServiceInstance
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createServiceInstance(serviceInstanceCreateRequest, opts, (error, data, response) => {
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
 **serviceInstanceCreateRequest** | [**ServiceInstanceCreateRequest**](ServiceInstanceCreateRequest.md)| The input for createServiceInstance | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**ServiceInstanceCreateResponse**](ServiceInstanceCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## deleteServiceInstance

> ServiceInstanceDeleteResponse deleteServiceInstance(serviceInstanceID, opts)

This deletes a service instance

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ServiceApi();
let serviceInstanceID = null; // String | ID of Service Instance
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.deleteServiceInstance(serviceInstanceID, opts, (error, data, response) => {
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
 **serviceInstanceID** | [**String**](.md)| ID of Service Instance | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**ServiceInstanceDeleteResponse**](ServiceInstanceDeleteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getResourcesForServiceInstance

> GetResourcesForServiceInstanceResponse getResourcesForServiceInstance(serviceInstanceID, opts)

Get resources for service instance

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.ServiceApi();
let serviceInstanceID = null; // String | ID of Service Instance
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getResourcesForServiceInstance(serviceInstanceID, opts, (error, data, response) => {
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
 **serviceInstanceID** | [**String**](.md)| ID of Service Instance | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetResourcesForServiceInstanceResponse**](GetResourcesForServiceInstanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

