# \ServiceApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateServiceInstance**](ServiceApi.md#CreateServiceInstance) | **Post** /service/instance/create | This creates a new service instance
[**DeleteServiceInstance**](ServiceApi.md#DeleteServiceInstance) | **Post** /service/instance/{ServiceInstanceID}/delete | This deletes a service instance
[**GetResourcesForServiceInstance**](ServiceApi.md#GetResourcesForServiceInstance) | **Get** /service/instance/{ServiceInstanceID}/resources | Get resources for service instance



## CreateServiceInstance

> ServiceInstanceCreateResponse CreateServiceInstance(ctx, serviceInstanceCreateRequest, optional)

This creates a new service instance

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serviceInstanceCreateRequest** | [**ServiceInstanceCreateRequest**](ServiceInstanceCreateRequest.md)| The input for createServiceInstance | 
 **optional** | ***CreateServiceInstanceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateServiceInstanceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**ServiceInstanceCreateResponse**](ServiceInstanceCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteServiceInstance

> ServiceInstanceDeleteResponse DeleteServiceInstance(ctx, serviceInstanceID, optional)

This deletes a service instance

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serviceInstanceID** | [**string**](.md)| ID of Service Instance | 
 **optional** | ***DeleteServiceInstanceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteServiceInstanceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**ServiceInstanceDeleteResponse**](ServiceInstanceDeleteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetResourcesForServiceInstance

> GetResourcesForServiceInstanceResponse GetResourcesForServiceInstance(ctx, serviceInstanceID, optional)

Get resources for service instance

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serviceInstanceID** | [**string**](.md)| ID of Service Instance | 
 **optional** | ***GetResourcesForServiceInstanceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetResourcesForServiceInstanceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetResourcesForServiceInstanceResponse**](GetResourcesForServiceInstanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

