# ServiceApi

All URIs are relative to */edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createServiceInstance**](ServiceApi.md#createServiceInstance) | **POST** /service/instance/create | This creates a new service instance
[**deleteServiceInstance**](ServiceApi.md#deleteServiceInstance) | **POST** /service/instance/{ServiceInstanceID}/delete | This deletes a service instance
[**getResourcesForServiceInstance**](ServiceApi.md#getResourcesForServiceInstance) | **GET** /service/instance/{ServiceInstanceID}/resources | Get resources for service instance



## createServiceInstance

This creates a new service instance

### Example

```bash
aiware createServiceInstance X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **serviceInstanceCreateRequest** | [**ServiceInstanceCreateRequest**](ServiceInstanceCreateRequest.md) | The input for createServiceInstance |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**ServiceInstanceCreateResponse**](ServiceInstanceCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deleteServiceInstance

This deletes a service instance

### Example

```bash
aiware deleteServiceInstance ServiceInstanceID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **serviceInstanceID** | [**string**](.md) | ID of Service Instance | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**ServiceInstanceDeleteResponse**](ServiceInstanceDeleteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getResourcesForServiceInstance

Get resources for service instance

### Example

```bash
aiware getResourcesForServiceInstance ServiceInstanceID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **serviceInstanceID** | [**string**](.md) | ID of Service Instance | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetResourcesForServiceInstanceResponse**](GetResourcesForServiceInstanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

