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

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.FlowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    FlowApi apiInstance = new FlowApi(defaultClient);
    try {
      AdminOperationResponse result = apiInstance.cleanAutomateRequests();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FlowApi#cleanAutomateRequests");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
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

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="createNodeRedContainerInfo"></a>
# **createNodeRedContainerInfo**
> AdminOperationResponse createNodeRedContainerInfo(createNodRedContainerDetail, xCorrelationId)

Create node-red container infomation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.FlowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");

    FlowApi apiInstance = new FlowApi(defaultClient);
    CreateNodRedContainerDetail createNodRedContainerDetail = new CreateNodRedContainerDetail(); // CreateNodRedContainerDetail | Node-RED container info
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AdminOperationResponse result = apiInstance.createNodeRedContainerInfo(createNodRedContainerDetail, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FlowApi#createNodeRedContainerInfo");
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
 **createNodRedContainerDetail** | [**CreateNodRedContainerDetail**](CreateNodRedContainerDetail.md)| Node-RED container info |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="deleteAutomateContainer"></a>
# **deleteAutomateContainer**
> AdminOperationResponse deleteAutomateContainer(containerID)

Delete automate container.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.FlowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    FlowApi apiInstance = new FlowApi(defaultClient);
    String containerID = "containerID_example"; // String | ContainerID of node-red container
    try {
      AdminOperationResponse result = apiInstance.deleteAutomateContainer(containerID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FlowApi#deleteAutomateContainer");
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
 **containerID** | **String**| ContainerID of node-red container |

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
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="updateAutomateRequestStatus"></a>
# **updateAutomateRequestStatus**
> AdminOperationResponse updateAutomateRequestStatus(updateNodeRedRequestDetail, xCorrelationId)

Put this automate request into update status mode. This automate request will be updated to new status.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.FlowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    FlowApi apiInstance = new FlowApi(defaultClient);
    UpdateNodeRedRequestDetail updateNodeRedRequestDetail = new UpdateNodeRedRequestDetail(); // UpdateNodeRedRequestDetail | Node-RED container info
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AdminOperationResponse result = apiInstance.updateAutomateRequestStatus(updateNodeRedRequestDetail, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FlowApi#updateAutomateRequestStatus");
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
 **updateNodeRedRequestDetail** | [**UpdateNodeRedRequestDetail**](UpdateNodeRedRequestDetail.md)| Node-RED container info |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

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
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="updateAutomateStatus"></a>
# **updateAutomateStatus**
> HostAction updateAutomateStatus(hostID)

Get updated information to launch node-red container, terminate node-red container.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.FlowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    FlowApi apiInstance = new FlowApi(defaultClient);
    UUID hostID = new UUID(); // UUID | ID of Host
    try {
      HostAction result = apiInstance.updateAutomateStatus(hostID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FlowApi#updateAutomateStatus");
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
 **hostID** | [**UUID**](.md)| ID of Host |

### Return type

[**HostAction**](HostAction.md)

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

