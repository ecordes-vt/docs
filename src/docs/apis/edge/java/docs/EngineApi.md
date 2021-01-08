# EngineApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createBuild**](EngineApi.md#createBuild) | **POST** /admin/build/create | This API creates a new engine build
[**createEngine**](EngineApi.md#createEngine) | **POST** /admin/engine/create | This API creates a new engine
[**createEngineCategory**](EngineApi.md#createEngineCategory) | **POST** /admin/engine/category/create | This API creates a new engine category
[**deleteBuildPost**](EngineApi.md#deleteBuildPost) | **POST** /engine/{EngineID}/build/{BuildID}/delete | This API provides the engine detail result
[**deleteEnginePost**](EngineApi.md#deleteEnginePost) | **POST** /admin/engine/{EngineID}/delete | This API delets an engine
[**getEngineBuild**](EngineApi.md#getEngineBuild) | **GET** /admin/build/{BuildID}/detail | This gets a particular build
[**getEngineBuilds**](EngineApi.md#getEngineBuilds) | **GET** /admin/engine/{EngineID}/builds | Get the list of builds deployed and available on aiWARE for a particular engine
[**getEngineBuildsByState**](EngineApi.md#getEngineBuildsByState) | **GET** /engine/builds | The api returns engine build records by build state
[**getEngineCategories**](EngineApi.md#getEngineCategories) | **GET** /admin/engine/categories | This provides a list of engine categories
[**getEngineCategoryDetail**](EngineApi.md#getEngineCategoryDetail) | **GET** /admin/engine/category/{EngineCategoryID}/detail | This provides detail for an engine category
[**getEngineContainerCount**](EngineApi.md#getEngineContainerCount) | **GET** /engine/container_count | Get engine container count
[**getEngineDetail**](EngineApi.md#getEngineDetail) | **GET** /admin/engine/{EngineID}/detail | This API provides the engine detail result
[**getEngineInstanceDetail**](EngineApi.md#getEngineInstanceDetail) | **GET** /engine/instance/{EngineInstanceID}/detail | Get information about an engine Instance
[**getEngineInstanceList**](EngineApi.md#getEngineInstanceList) | **GET** /engine/instances | Get engines instances with filtering
[**getEngineInstanceLogs**](EngineApi.md#getEngineInstanceLogs) | **GET** /engine/instance/{EngineInstanceID}/logs | Get engine instance logs as a zip file
[**getEngineInstanceStatus**](EngineApi.md#getEngineInstanceStatus) | **GET** /engine/instance/{EngineInstanceID}/status | Get the latest status of the engine instance
[**getEngineInstanceWork**](EngineApi.md#getEngineInstanceWork) | **POST** /engine/instance/{EngineInstanceID}/getwork | Get a work request
[**getEngineInstanceWorkDetail**](EngineApi.md#getEngineInstanceWorkDetail) | **GET** /engine/instance/{EngineInstanceID}/workdetail | Get detail of the work being done by the engine instance
[**getEngineInstances**](EngineApi.md#getEngineInstances) | **GET** /engine/{EngineID}/instances | Get information about the instances of an engine
[**getEngineLaunchDetail**](EngineApi.md#getEngineLaunchDetail) | **GET** /engine/{EngineID}/launch/{LaunchID}/detail | This API returns the list of launches for this engine
[**getEngineLaunches**](EngineApi.md#getEngineLaunches) | **GET** /engine/{EngineID}/launches | This API returns the list of launches for this engine
[**getEngines**](EngineApi.md#getEngines) | **GET** /admin/engines | Get the list of engines deployed and available on aiWARE
[**getJobsBacklogCountByEngine**](EngineApi.md#getJobsBacklogCountByEngine) | **POST** /proc/jobs/backlog_count_by_engine | Get backlog count by engine
[**getResourcesForEngineInstance**](EngineApi.md#getResourcesForEngineInstance) | **GET** /engine/instance/{EngineInstanceID}/resources | Get resources for engine instance
[**pauseBuild**](EngineApi.md#pauseBuild) | **POST** /admin/build/{BuildID}/pause | This API pauses a build so that tasks based on this engine build will not run.
[**pauseEngine**](EngineApi.md#pauseEngine) | **POST** /admin/engine/{EngineID}/pause | This API pauses an engine so that tasks based on this engine will not run.
[**registerEngineInstanceNoAuth**](EngineApi.md#registerEngineInstanceNoAuth) | **POST** /engine/instance/register | Register a new engine instance without authorization
[**replaceEngine**](EngineApi.md#replaceEngine) | **POST** /admin/engine/{EngineID}/replace | This API replaced an engine so that tasks based on this engine will not run.
[**resumeBuild**](EngineApi.md#resumeBuild) | **POST** /admin/build/{BuildID}/resume | This API resumes a build so that tasks based on this engine build will start running.
[**resumeEngine**](EngineApi.md#resumeEngine) | **POST** /admin/engine/{EngineID}/resume | This API resumes a build so that tasks based on this engine build will start running.
[**terminateEngineInstance**](EngineApi.md#terminateEngineInstance) | **POST** /engine/instance/{EngineInstanceID}/terminate | Delete the engine instance record
[**updateEngine**](EngineApi.md#updateEngine) | **POST** /admin/engine/{EngineID}/update | This API updates the specified engine
[**updateEngineBuild**](EngineApi.md#updateEngineBuild) | **POST** /admin/build/{BuildID}/update | This API updates the specified engine
[**updateEngineBuildState**](EngineApi.md#updateEngineBuildState) | **POST** /engine/build/{BuildID}/state | Update the Engine Build State
[**updateEngineCategory**](EngineApi.md#updateEngineCategory) | **POST** /admin/engine/category/{EngineCategoryID}/update | This updates the specified engine category
[**updateEngineInstanceStatus**](EngineApi.md#updateEngineInstanceStatus) | **POST** /engine/instance/{EngineInstanceID}/updatestatus | Update the Engine Instance Status.  Heartbeat to communicate back to controller both aggregated work and delta work from last heartbeat


<a name="createBuild"></a>
# **createBuild**
> CreateBuildResponse createBuild(createBuildRequest, xCorrelationId)

This API creates a new engine build

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    CreateBuildRequest createBuildRequest = new CreateBuildRequest(); // CreateBuildRequest | The fields for an engine build
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      CreateBuildResponse result = apiInstance.createBuild(createBuildRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#createBuild");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createBuildRequest** | [**CreateBuildRequest**](CreateBuildRequest.md)| The fields for an engine build |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**CreateBuildResponse**](CreateBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of the Create Engine Build API |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="createEngine"></a>
# **createEngine**
> CreateEngineResponse createEngine(createEngineRequest, xCorrelationId)

This API creates a new engine

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    CreateEngineRequest createEngineRequest = new CreateEngineRequest(); // CreateEngineRequest | The fields for an engine
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      CreateEngineResponse result = apiInstance.createEngine(createEngineRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#createEngine");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createEngineRequest** | [**CreateEngineRequest**](CreateEngineRequest.md)| The fields for an engine |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**CreateEngineResponse**](CreateEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of the Create Engine API |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="createEngineCategory"></a>
# **createEngineCategory**
> CreateEngineCategoryResponse createEngineCategory(createEngineCategoryDetail, xCorrelationId)

This API creates a new engine category

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    CreateEngineCategoryDetail createEngineCategoryDetail = new CreateEngineCategoryDetail(); // CreateEngineCategoryDetail | The fields for an engine category
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      CreateEngineCategoryResponse result = apiInstance.createEngineCategory(createEngineCategoryDetail, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#createEngineCategory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createEngineCategoryDetail** | [**CreateEngineCategoryDetail**](CreateEngineCategoryDetail.md)| The fields for an engine category |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**CreateEngineCategoryResponse**](CreateEngineCategoryResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of the Create Engine Category API |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="deleteBuildPost"></a>
# **deleteBuildPost**
> AdminOperationResponse deleteBuildPost(engineID, buildID, xCorrelationId)

This API provides the engine detail result

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineID = new UUID(); // UUID | ID of Engine
    UUID buildID = new UUID(); // UUID | ID of Build
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AdminOperationResponse result = apiInstance.deleteBuildPost(engineID, buildID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#deleteBuildPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**UUID**](.md)| ID of Engine |
 **buildID** | [**UUID**](.md)| ID of Build |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Delete a particular engine |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="deleteEnginePost"></a>
# **deleteEnginePost**
> AdminOperationResponse deleteEnginePost(engineID, xCorrelationId)

This API delets an engine

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineID = new UUID(); // UUID | ID of Engine
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AdminOperationResponse result = apiInstance.deleteEnginePost(engineID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#deleteEnginePost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**UUID**](.md)| ID of Engine |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Delete a particular engine |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineBuild"></a>
# **getEngineBuild**
> GetEngineBuildResponse getEngineBuild(buildID, xCorrelationId)

This gets a particular build

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID buildID = new UUID(); // UUID | ID of Build
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetEngineBuildResponse result = apiInstance.getEngineBuild(buildID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineBuild");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buildID** | [**UUID**](.md)| ID of Build |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetEngineBuildResponse**](GetEngineBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Specific build |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineBuilds"></a>
# **getEngineBuilds**
> GetEngineBuildsResponse getEngineBuilds(engineID, xCorrelationId, buildState)

Get the list of builds deployed and available on aiWARE for a particular engine

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineID = new UUID(); // UUID | ID of Engine
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    String buildState = "buildState_example"; // String | Filter builds by the build state
    try {
      GetEngineBuildsResponse result = apiInstance.getEngineBuilds(engineID, xCorrelationId, buildState);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineBuilds");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**UUID**](.md)| ID of Engine |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **buildState** | **String**| Filter builds by the build state | [optional]

### Return type

[**GetEngineBuildsResponse**](GetEngineBuildsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of engines |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineBuildsByState"></a>
# **getEngineBuildsByState**
> GetEngineBuildByStateResponse getEngineBuildsByState(xCorrelationId, state)

The api returns engine build records by build state

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    String state = "state_example"; // String | Filter data by build state
    try {
      GetEngineBuildByStateResponse result = apiInstance.getEngineBuildsByState(xCorrelationId, state);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineBuildsByState");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **state** | **String**| Filter data by build state | [optional]

### Return type

[**GetEngineBuildByStateResponse**](GetEngineBuildByStateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid status request |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineCategories"></a>
# **getEngineCategories**
> GetEngineCategoriesResponse getEngineCategories(xCorrelationId)

This provides a list of engine categories

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetEngineCategoriesResponse result = apiInstance.getEngineCategories(xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineCategories");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetEngineCategoriesResponse**](GetEngineCategoriesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of get_engine_categories |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineCategoryDetail"></a>
# **getEngineCategoryDetail**
> GetEngineCategoryDetailResponse getEngineCategoryDetail(engineCategoryID, xCorrelationId)

This provides detail for an engine category

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineCategoryID = new UUID(); // UUID | ID of Engine Category
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetEngineCategoryDetailResponse result = apiInstance.getEngineCategoryDetail(engineCategoryID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineCategoryDetail");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineCategoryID** | [**UUID**](.md)| ID of Engine Category |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetEngineCategoryDetailResponse**](GetEngineCategoryDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of get_engine_category_detail |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineContainerCount"></a>
# **getEngineContainerCount**
> GetEngineContainerCountResponse getEngineContainerCount(interval, startTime, endTime, groupBy, engineID, hostID)

Get engine container count

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    Long interval = 56L; // Long | Interval in seconds for output time ranges.
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    EngineContainerGroupByEnum groupBy = new EngineContainerGroupByEnum(); // EngineContainerGroupByEnum | Group data by engineID or instance
    UUID engineID = new UUID(); // UUID | Filter data by engineID
    UUID hostID = new UUID(); // UUID | Filter data by hostID
    try {
      GetEngineContainerCountResponse result = apiInstance.getEngineContainerCount(interval, startTime, endTime, groupBy, engineID, hostID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineContainerCount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **Long**| Interval in seconds for output time ranges. | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **groupBy** | [**EngineContainerGroupByEnum**](.md)| Group data by engineID or instance | [optional] [enum: engineID, engineInstanceID]
 **engineID** | [**UUID**](.md)| Filter data by engineID | [optional]
 **hostID** | [**UUID**](.md)| Filter data by hostID | [optional]

### Return type

[**GetEngineContainerCountResponse**](GetEngineContainerCountResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineDetail"></a>
# **getEngineDetail**
> GetEngineDetailResponse getEngineDetail(engineID)

This API provides the engine detail result

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineID = new UUID(); // UUID | ID of Engine
    try {
      GetEngineDetailResponse result = apiInstance.getEngineDetail(engineID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineDetail");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**UUID**](.md)| ID of Engine |

### Return type

[**GetEngineDetailResponse**](GetEngineDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of engines |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineInstanceDetail"></a>
# **getEngineInstanceDetail**
> EngineInstanceInfo getEngineInstanceDetail(engineInstanceID, xCorrelationId)

Get information about an engine Instance

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineInstanceID = new UUID(); // UUID | ID of Engine Instance
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      EngineInstanceInfo result = apiInstance.getEngineInstanceDetail(engineInstanceID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineInstanceDetail");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**UUID**](.md)| ID of Engine Instance |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**EngineInstanceInfo**](EngineInstanceInfo.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineInstanceList"></a>
# **getEngineInstanceList**
> GetEngineInstanceListResponse getEngineInstanceList(xCorrelationId, engineInstanceIDs, engineIDs, hostIDs, workRequestIDs, status, drain, launchStartTime, launchEndTime, modifiedBefore, modifiedAfter, createdBefore, createdAfter, offset, limit, direction, orderBy)

Get engines instances with filtering

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    String engineInstanceIDs = "engineInstanceIDs_example"; // String | Field to provide the input to get engine instances by ID list. Separated by commas
    String engineIDs = "engineIDs_example"; // String | Field to provide the input to get engines by Engine ID list. Separated by commas
    UUID hostIDs = new UUID(); // UUID | Filtering engine instances by host IDs. Separated by commas
    UUID workRequestIDs = new UUID(); // UUID | Filters engine instances by workrequest IDs. Separated by commas
    EngineStatusEnum status = new EngineStatusEnum(); // EngineStatusEnum | Field to match the current status
    Boolean drain = true; // Boolean | Filter by drain
    Long launchStartTime = 56L; // Long | The unix timestamp, describing a lower limit for the time an engine instance was launched.
    Long launchEndTime = 56L; // Long | The unix timestamp, describing an upper limit for the time an engine instance was launched.
    Long modifiedBefore = 56L; // Long | Filter by items modified before expressed as timestamp
    Long modifiedAfter = 56L; // Long | Filter by items modified after expressed as timestamp
    Long createdBefore = 56L; // Long | Filter items where created date is before this date
    Long createdAfter = 56L; // Long | Filter items where created date is after this date
    Long offset = 56L; // Long | the number of data to skip before getting the result set
    Long limit = 10lL; // Long | the number of items to return.
    String direction = "\"DESC\""; // String | the sort order.  ASC or DESC.
    String orderBy = "orderBy_example"; // String | It should be in [engineID, hostID, status, createdTime, modifiedTime, lastUpdateTime, launchTime]
    try {
      GetEngineInstanceListResponse result = apiInstance.getEngineInstanceList(xCorrelationId, engineInstanceIDs, engineIDs, hostIDs, workRequestIDs, status, drain, launchStartTime, launchEndTime, modifiedBefore, modifiedAfter, createdBefore, createdAfter, offset, limit, direction, orderBy);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineInstanceList");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **engineInstanceIDs** | **String**| Field to provide the input to get engine instances by ID list. Separated by commas | [optional]
 **engineIDs** | **String**| Field to provide the input to get engines by Engine ID list. Separated by commas | [optional]
 **hostIDs** | [**UUID**](.md)| Filtering engine instances by host IDs. Separated by commas | [optional]
 **workRequestIDs** | [**UUID**](.md)| Filters engine instances by workrequest IDs. Separated by commas | [optional]
 **status** | [**EngineStatusEnum**](.md)| Field to match the current status | [optional] [enum: active, terminated]
 **drain** | **Boolean**| Filter by drain | [optional]
 **launchStartTime** | **Long**| The unix timestamp, describing a lower limit for the time an engine instance was launched. | [optional]
 **launchEndTime** | **Long**| The unix timestamp, describing an upper limit for the time an engine instance was launched. | [optional]
 **modifiedBefore** | **Long**| Filter by items modified before expressed as timestamp | [optional]
 **modifiedAfter** | **Long**| Filter by items modified after expressed as timestamp | [optional]
 **createdBefore** | **Long**| Filter items where created date is before this date | [optional]
 **createdAfter** | **Long**| Filter items where created date is after this date | [optional]
 **offset** | **Long**| the number of data to skip before getting the result set | [optional]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10l]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &quot;DESC&quot;]
 **orderBy** | **String**| It should be in [engineID, hostID, status, createdTime, modifiedTime, lastUpdateTime, launchTime] | [optional]

### Return type

[**GetEngineInstanceListResponse**](GetEngineInstanceListResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineInstanceLogs"></a>
# **getEngineInstanceLogs**
> File getEngineInstanceLogs(engineInstanceID, xCorrelationId)

Get engine instance logs as a zip file

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineInstanceID = new UUID(); // UUID | ID of Engine Instance
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      File result = apiInstance.getEngineInstanceLogs(engineInstanceID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineInstanceLogs");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**UUID**](.md)| ID of Engine Instance |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**File**](File.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineInstanceStatus"></a>
# **getEngineInstanceStatus**
> EngineInstanceStatus getEngineInstanceStatus(engineInstanceID, xCorrelationId)

Get the latest status of the engine instance

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineInstanceID = new UUID(); // UUID | ID of Engine Instance
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      EngineInstanceStatus result = apiInstance.getEngineInstanceStatus(engineInstanceID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineInstanceStatus");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**UUID**](.md)| ID of Engine Instance |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**EngineInstanceStatus**](EngineInstanceStatus.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineInstanceWork"></a>
# **getEngineInstanceWork**
> EngineInstanceWorkRequestResponse getEngineInstanceWork(engineInstanceID, engineInstanceWorkRequest, xCorrelationId)

Get a work request

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineInstanceID = new UUID(); // UUID | ID of Engine Instance
    EngineInstanceWorkRequest engineInstanceWorkRequest = new EngineInstanceWorkRequest(); // EngineInstanceWorkRequest | Engine Instance Info
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      EngineInstanceWorkRequestResponse result = apiInstance.getEngineInstanceWork(engineInstanceID, engineInstanceWorkRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineInstanceWork");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**UUID**](.md)| ID of Engine Instance |
 **engineInstanceWorkRequest** | [**EngineInstanceWorkRequest**](EngineInstanceWorkRequest.md)| Engine Instance Info |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**EngineInstanceWorkRequestResponse**](EngineInstanceWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid work response |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineInstanceWorkDetail"></a>
# **getEngineInstanceWorkDetail**
> EngineInstanceWorkDetailsResponse getEngineInstanceWorkDetail(engineInstanceID, xCorrelationId)

Get detail of the work being done by the engine instance

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineInstanceID = new UUID(); // UUID | ID of Engine Instance
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      EngineInstanceWorkDetailsResponse result = apiInstance.getEngineInstanceWorkDetail(engineInstanceID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineInstanceWorkDetail");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**UUID**](.md)| ID of Engine Instance |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**EngineInstanceWorkDetailsResponse**](EngineInstanceWorkDetailsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineInstances"></a>
# **getEngineInstances**
> GetEngineInstancesResponse getEngineInstances(engineID, xCorrelationId, launchStartTime, launchEndTime, modifiedBefore, modifiedAfter, createdBefore, createdAfter)

Get information about the instances of an engine

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    String engineID = "engineID_example"; // String | EngineID of node-red container request
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long launchStartTime = 56L; // Long | The unix timestamp, describing a lower limit for the time an engine instance was launched.
    Long launchEndTime = 56L; // Long | The unix timestamp, describing an upper limit for the time an engine instance was launched.
    Long modifiedBefore = 56L; // Long | Filter by items modified before expressed as timestamp
    Long modifiedAfter = 56L; // Long | Filter by items modified after expressed as timestamp
    Long createdBefore = 56L; // Long | Filter items where created date is before this date
    Long createdAfter = 56L; // Long | Filter items where created date is after this date
    try {
      GetEngineInstancesResponse result = apiInstance.getEngineInstances(engineID, xCorrelationId, launchStartTime, launchEndTime, modifiedBefore, modifiedAfter, createdBefore, createdAfter);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineInstances");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | **String**| EngineID of node-red container request |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **launchStartTime** | **Long**| The unix timestamp, describing a lower limit for the time an engine instance was launched. | [optional]
 **launchEndTime** | **Long**| The unix timestamp, describing an upper limit for the time an engine instance was launched. | [optional]
 **modifiedBefore** | **Long**| Filter by items modified before expressed as timestamp | [optional]
 **modifiedAfter** | **Long**| Filter by items modified after expressed as timestamp | [optional]
 **createdBefore** | **Long**| Filter items where created date is before this date | [optional]
 **createdAfter** | **Long**| Filter items where created date is after this date | [optional]

### Return type

[**GetEngineInstancesResponse**](GetEngineInstancesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineLaunchDetail"></a>
# **getEngineLaunchDetail**
> GetEngineLaunchResponse getEngineLaunchDetail(engineID, launchID, createdBefore, createdAfter, offset, limit, orderBy, direction)

This API returns the list of launches for this engine

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineID = new UUID(); // UUID | ID of Engine
    UUID launchID = new UUID(); // UUID | ID of Launch
    Long createdBefore = 56L; // Long | Filter items where created date is before this date
    Long createdAfter = 56L; // Long | Filter items where created date is after this date
    Long offset = 56L; // Long | the number of data to skip before getting the result set
    Long limit = 10lL; // Long | the number of items to return.
    String orderBy = "\"createdDateTime\""; // String | the field to sort
    String direction = "\"DESC\""; // String | the sort order.  ASC or DESC.
    try {
      GetEngineLaunchResponse result = apiInstance.getEngineLaunchDetail(engineID, launchID, createdBefore, createdAfter, offset, limit, orderBy, direction);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineLaunchDetail");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**UUID**](.md)| ID of Engine |
 **launchID** | [**UUID**](.md)| ID of Launch |
 **createdBefore** | **Long**| Filter items where created date is before this date | [optional]
 **createdAfter** | **Long**| Filter items where created date is after this date | [optional]
 **offset** | **Long**| the number of data to skip before getting the result set | [optional]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10l]
 **orderBy** | **String**| the field to sort | [optional] [default to &quot;createdDateTime&quot;]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &quot;DESC&quot;]

### Return type

[**GetEngineLaunchResponse**](GetEngineLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Returns detail on a specific launch |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngineLaunches"></a>
# **getEngineLaunches**
> GetEngineLaunchResponse getEngineLaunches(engineID, launchStatus, launchAction, createdBefore, createdAfter, offset, limit, orderBy, direction)

This API returns the list of launches for this engine

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineID = new UUID(); // UUID | ID of Engine
    LaunchStatusEnum launchStatus = new LaunchStatusEnum(); // LaunchStatusEnum | Field to match the current launch status
    LaunchActionEnum launchAction = new LaunchActionEnum(); // LaunchActionEnum | Field to match the current launch action
    Long createdBefore = 56L; // Long | Filter items where created date is before this date
    Long createdAfter = 56L; // Long | Filter items where created date is after this date
    Long offset = 56L; // Long | the number of data to skip before getting the result set
    Long limit = 10lL; // Long | the number of items to return.
    String orderBy = "\"createdDateTime\""; // String | the field to sort
    String direction = "\"DESC\""; // String | the sort order.  ASC or DESC.
    try {
      GetEngineLaunchResponse result = apiInstance.getEngineLaunches(engineID, launchStatus, launchAction, createdBefore, createdAfter, offset, limit, orderBy, direction);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngineLaunches");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**UUID**](.md)| ID of Engine |
 **launchStatus** | [**LaunchStatusEnum**](.md)| Field to match the current launch status | [optional] [enum: pending, running, complete, pending_terminate]
 **launchAction** | [**LaunchActionEnum**](.md)| Field to match the current launch action | [optional] [enum: launch, terminate]
 **createdBefore** | **Long**| Filter items where created date is before this date | [optional]
 **createdAfter** | **Long**| Filter items where created date is after this date | [optional]
 **offset** | **Long**| the number of data to skip before getting the result set | [optional]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10l]
 **orderBy** | **String**| the field to sort | [optional] [default to &quot;createdDateTime&quot;]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &quot;DESC&quot;]

### Return type

[**GetEngineLaunchResponse**](GetEngineLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of launches for specified engine |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getEngines"></a>
# **getEngines**
> GetEnginesResponse getEngines(xCorrelationId, internalOrganizationID, engineName, engineState, engineType, engineOutputType, engineCategoryID, engineIDs, offset, limit, direction, startTime, endTime, preload, orderBy)

Get the list of engines deployed and available on aiWARE

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    UUID internalOrganizationID = new UUID(); // UUID | ID of Organization.  UUID.  This ID is unique to this aiWARE installation.
    String engineName = "engineName_example"; // String | Field to string match against the engine names
    EngineStateEnum engineState = new EngineStateEnum(); // EngineStateEnum | Field to match the current state
    EngineTypeEnum engineType = new EngineTypeEnum(); // EngineTypeEnum | Field to match the current type
    EngineTypeEnum engineOutputType = new EngineTypeEnum(); // EngineTypeEnum | Field to match the current type
    String engineCategoryID = "engineCategoryID_example"; // String | Filter to the particular engine category ID
    String engineIDs = "engineIDs_example"; // String | Field to provide the input to get engines by Engine ID list. Separated by commas
    Long offset = 56L; // Long | the number of data to skip before getting the result set
    Long limit = 10lL; // Long | the number of items to return.
    String direction = "\"DESC\""; // String | the sort order.  ASC or DESC.
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    Boolean preload = true; // Boolean | Filter engines by preload
    String orderBy = "orderBy_example"; // String | The value should be in [name, state, type, organizationID, createdTime]
    try {
      GetEnginesResponse result = apiInstance.getEngines(xCorrelationId, internalOrganizationID, engineName, engineState, engineType, engineOutputType, engineCategoryID, engineIDs, offset, limit, direction, startTime, endTime, preload, orderBy);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getEngines");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **internalOrganizationID** | [**UUID**](.md)| ID of Organization.  UUID.  This ID is unique to this aiWARE installation. | [optional]
 **engineName** | **String**| Field to string match against the engine names | [optional]
 **engineState** | [**EngineStateEnum**](.md)| Field to match the current state | [optional] [enum: active, paused, replace]
 **engineType** | [**EngineTypeEnum**](.md)| Field to match the current type | [optional] [enum: chunk, stream, batch, any]
 **engineOutputType** | [**EngineTypeEnum**](.md)| Field to match the current type | [optional] [enum: chunk, stream, batch, any]
 **engineCategoryID** | **String**| Filter to the particular engine category ID | [optional]
 **engineIDs** | **String**| Field to provide the input to get engines by Engine ID list. Separated by commas | [optional]
 **offset** | **Long**| the number of data to skip before getting the result set | [optional]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10l]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &quot;DESC&quot;]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **preload** | **Boolean**| Filter engines by preload | [optional]
 **orderBy** | **String**| The value should be in [name, state, type, organizationID, createdTime] | [optional]

### Return type

[**GetEnginesResponse**](GetEnginesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of engines |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getJobsBacklogCountByEngine"></a>
# **getJobsBacklogCountByEngine**
> GetJobsBacklogCountResponse getJobsBacklogCountByEngine(interval, startTime, endTime, organizationIDs)

Get backlog count by engine

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    Long interval = 56L; // Long | Interval in seconds for output time ranges.
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    String organizationIDs = "organizationIDs_example"; // String | 
    try {
      GetJobsBacklogCountResponse result = apiInstance.getJobsBacklogCountByEngine(interval, startTime, endTime, organizationIDs);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getJobsBacklogCountByEngine");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **Long**| Interval in seconds for output time ranges. | [optional]
 **startTime** | **Long**| The unix timestamp, describing the start time for the stats | [optional]
 **endTime** | **Long**| The unix timestamp, describing the end time for the stats | [optional]
 **organizationIDs** | **String**|  | [optional]

### Return type

[**GetJobsBacklogCountResponse**](GetJobsBacklogCountResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getResourcesForEngineInstance"></a>
# **getResourcesForEngineInstance**
> GetResourcesForEngineInstanceResponse getResourcesForEngineInstance(engineInstanceID, xCorrelationId)

Get resources for engine instance

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineInstanceID = new UUID(); // UUID | ID of Engine Instance
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetResourcesForEngineInstanceResponse result = apiInstance.getResourcesForEngineInstance(engineInstanceID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#getResourcesForEngineInstance");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**UUID**](.md)| ID of Engine Instance |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetResourcesForEngineInstanceResponse**](GetResourcesForEngineInstanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Valid work response |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="pauseBuild"></a>
# **pauseBuild**
> AdminOperationResponse pauseBuild(buildID, xCorrelationId, buildState)

This API pauses a build so that tasks based on this engine build will not run.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID buildID = new UUID(); // UUID | ID of Build
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    String buildState = "buildState_example"; // String | Filter builds by the build state
    try {
      AdminOperationResponse result = apiInstance.pauseBuild(buildID, xCorrelationId, buildState);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#pauseBuild");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buildID** | [**UUID**](.md)| ID of Build |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **buildState** | **String**| Filter builds by the build state | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Pause a particular build |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="pauseEngine"></a>
# **pauseEngine**
> AdminOperationResponse pauseEngine(engineID, xCorrelationId, pauseEngineRequest)

This API pauses an engine so that tasks based on this engine will not run.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineID = new UUID(); // UUID | ID of Engine
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    PauseEngineRequest pauseEngineRequest = new PauseEngineRequest(); // PauseEngineRequest | Engine Instance Info
    try {
      AdminOperationResponse result = apiInstance.pauseEngine(engineID, xCorrelationId, pauseEngineRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#pauseEngine");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**UUID**](.md)| ID of Engine |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **pauseEngineRequest** | [**PauseEngineRequest**](PauseEngineRequest.md)| Engine Instance Info | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Pause a particular engine |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="registerEngineInstanceNoAuth"></a>
# **registerEngineInstanceNoAuth**
> EngineInstanceRegistrationInfo registerEngineInstanceNoAuth(engineInstanceInfo, xCorrelationId)

Register a new engine instance without authorization

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");

    EngineApi apiInstance = new EngineApi(defaultClient);
    EngineInstanceInfo engineInstanceInfo = new EngineInstanceInfo(); // EngineInstanceInfo | Engine Instance Info
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      EngineInstanceRegistrationInfo result = apiInstance.registerEngineInstanceNoAuth(engineInstanceInfo, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#registerEngineInstanceNoAuth");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceInfo** | [**EngineInstanceInfo**](EngineInstanceInfo.md)| Engine Instance Info |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**EngineInstanceRegistrationInfo**](EngineInstanceRegistrationInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful registration of Engine Instance |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="replaceEngine"></a>
# **replaceEngine**
> AdminOperationResponse replaceEngine(engineID, replaceEngineRequest)

This API replaced an engine so that tasks based on this engine will not run.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineID = new UUID(); // UUID | ID of Engine
    ReplaceEngineRequest replaceEngineRequest = new ReplaceEngineRequest(); // ReplaceEngineRequest | Engine Instance Info
    try {
      AdminOperationResponse result = apiInstance.replaceEngine(engineID, replaceEngineRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#replaceEngine");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**UUID**](.md)| ID of Engine |
 **replaceEngineRequest** | [**ReplaceEngineRequest**](ReplaceEngineRequest.md)| Engine Instance Info | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Pause a particular engine |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="resumeBuild"></a>
# **resumeBuild**
> AdminOperationResponse resumeBuild(buildID, xCorrelationId)

This API resumes a build so that tasks based on this engine build will start running.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID buildID = new UUID(); // UUID | ID of Build
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AdminOperationResponse result = apiInstance.resumeBuild(buildID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#resumeBuild");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buildID** | [**UUID**](.md)| ID of Build |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Resume a particular build |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="resumeEngine"></a>
# **resumeEngine**
> AdminOperationResponse resumeEngine(engineID, xCorrelationId, resumeEngineRequest)

This API resumes a build so that tasks based on this engine build will start running.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineID = new UUID(); // UUID | ID of Engine
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    ResumeEngineRequest resumeEngineRequest = new ResumeEngineRequest(); // ResumeEngineRequest | Engine Instance Info
    try {
      AdminOperationResponse result = apiInstance.resumeEngine(engineID, xCorrelationId, resumeEngineRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#resumeEngine");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**UUID**](.md)| ID of Engine |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]
 **resumeEngineRequest** | [**ResumeEngineRequest**](ResumeEngineRequest.md)| Engine Instance Info | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Resume a particular build |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="terminateEngineInstance"></a>
# **terminateEngineInstance**
> terminateEngineInstance(engineInstanceID, xCorrelationId)

Delete the engine instance record

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineInstanceID = new UUID(); // UUID | ID of Engine Instance
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      apiInstance.terminateEngineInstance(engineInstanceID, xCorrelationId);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#terminateEngineInstance");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**UUID**](.md)| ID of Engine Instance |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

null (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="updateEngine"></a>
# **updateEngine**
> UpdateEngineResponse updateEngine(engineID, updateEngineRequest, xCorrelationId)

This API updates the specified engine

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineID = new UUID(); // UUID | ID of Engine
    UpdateEngineRequest updateEngineRequest = new UpdateEngineRequest(); // UpdateEngineRequest | Update Engine
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      UpdateEngineResponse result = apiInstance.updateEngine(engineID, updateEngineRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#updateEngine");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**UUID**](.md)| ID of Engine |
 **updateEngineRequest** | [**UpdateEngineRequest**](UpdateEngineRequest.md)| Update Engine |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**UpdateEngineResponse**](UpdateEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of the Update Engine API |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="updateEngineBuild"></a>
# **updateEngineBuild**
> UpdateBuildResponse updateEngineBuild(engineID, buildID, buildDetail, xCorrelationId)

This API updates the specified engine

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineID = new UUID(); // UUID | ID of Engine
    UUID buildID = new UUID(); // UUID | ID of Build
    BuildDetail buildDetail = new BuildDetail(); // BuildDetail | Update Engine BUild
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      UpdateBuildResponse result = apiInstance.updateEngineBuild(engineID, buildID, buildDetail, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#updateEngineBuild");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**UUID**](.md)| ID of Engine |
 **buildID** | [**UUID**](.md)| ID of Build |
 **buildDetail** | [**BuildDetail**](BuildDetail.md)| Update Engine BUild |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**UpdateBuildResponse**](UpdateBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of engines |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="updateEngineBuildState"></a>
# **updateEngineBuildState**
> updateEngineBuildState(buildID, updateEngineBuildStateRequest, xCorrelationId)

Update the Engine Build State

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    String buildID = "buildID_example"; // String | BuildID of node-red container request
    UpdateEngineBuildStateRequest updateEngineBuildStateRequest = new UpdateEngineBuildStateRequest(); // UpdateEngineBuildStateRequest | Engine Build State
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      apiInstance.updateEngineBuildState(buildID, updateEngineBuildStateRequest, xCorrelationId);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#updateEngineBuildState");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buildID** | **String**| BuildID of node-red container request |
 **updateEngineBuildStateRequest** | [**UpdateEngineBuildStateRequest**](UpdateEngineBuildStateRequest.md)| Engine Build State |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

null (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Item created |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="updateEngineCategory"></a>
# **updateEngineCategory**
> UpdateEngineCategoryResponse updateEngineCategory(engineCategoryID, xCorrelationId)

This updates the specified engine category

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineCategoryID = new UUID(); // UUID | ID of Engine Category
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      UpdateEngineCategoryResponse result = apiInstance.updateEngineCategory(engineCategoryID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#updateEngineCategory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineCategoryID** | [**UUID**](.md)| ID of Engine Category |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**UpdateEngineCategoryResponse**](UpdateEngineCategoryResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | This updates the specified engine category |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="updateEngineInstanceStatus"></a>
# **updateEngineInstanceStatus**
> updateEngineInstanceStatus(engineInstanceID, engineInstanceStatus, xCorrelationId)

Update the Engine Instance Status.  Heartbeat to communicate back to controller both aggregated work and delta work from last heartbeat

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EngineApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    EngineApi apiInstance = new EngineApi(defaultClient);
    UUID engineInstanceID = new UUID(); // UUID | ID of Engine Instance
    EngineInstanceStatus engineInstanceStatus = new EngineInstanceStatus(); // EngineInstanceStatus | Engine Instance Status
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      apiInstance.updateEngineInstanceStatus(engineInstanceID, engineInstanceStatus, xCorrelationId);
    } catch (ApiException e) {
      System.err.println("Exception when calling EngineApi#updateEngineInstanceStatus");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**UUID**](.md)| ID of Engine Instance |
 **engineInstanceStatus** | [**EngineInstanceStatus**](EngineInstanceStatus.md)| Engine Instance Status |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

null (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Item created |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

