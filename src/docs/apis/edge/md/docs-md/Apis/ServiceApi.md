# ServiceApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createServiceInstance**](ServiceApi.md#createServiceInstance) | **POST** /service/instance/create | This creates a new service instance
[**deleteServiceInstance**](ServiceApi.md#deleteServiceInstance) | **POST** /service/instance/{ServiceInstanceID}/delete | This deletes a service instance
[**getResourcesForServiceInstance**](ServiceApi.md#getResourcesForServiceInstance) | **GET** /service/instance/{ServiceInstanceID}/resources | Get resources for service instance


<a name="createServiceInstance"></a>
# **createServiceInstance**
> ServiceInstanceCreateResponse createServiceInstance(ServiceInstanceCreateRequest, X-Correlation-Id)

This creates a new service instance

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ServiceInstanceCreateRequest** | [**ServiceInstanceCreateRequest**](../Models/ServiceInstanceCreateRequest.md)| The input for createServiceInstance |
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**ServiceInstanceCreateResponse**](../Models/ServiceInstanceCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deleteServiceInstance"></a>
# **deleteServiceInstance**
> ServiceInstanceDeleteResponse deleteServiceInstance(ServiceInstanceID, X-Correlation-Id)

This deletes a service instance

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ServiceInstanceID** | [**UUID**](../Models/.md)| ID of Service Instance | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**ServiceInstanceDeleteResponse**](../Models/ServiceInstanceDeleteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getResourcesForServiceInstance"></a>
# **getResourcesForServiceInstance**
> GetResourcesForServiceInstanceResponse getResourcesForServiceInstance(ServiceInstanceID, X-Correlation-Id)

Get resources for service instance

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ServiceInstanceID** | [**UUID**](../Models/.md)| ID of Service Instance | [default to null]
 **X-Correlation-Id** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetResourcesForServiceInstanceResponse**](../Models/GetResourcesForServiceInstanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

