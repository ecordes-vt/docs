# HostApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**drainHost**](HostApi.md#drainHost) | **POST** /host/{HostID}/drain | Put this host into drain mode.  A host in drain mode will not have work assigned to engines on the host.
[**getHostCpuUsage**](HostApi.md#getHostCpuUsage) | **GET** /hosts/cpu_usage | Get host cpu usage
[**getHostDetail**](HostApi.md#getHostDetail) | **GET** /host/{HostID}/detail | Get the latest info of the host
[**getHostMemoryUsage**](HostApi.md#getHostMemoryUsage) | **GET** /engine/memory_usage | Get host memory usage
[**getHostStatus**](HostApi.md#getHostStatus) | **GET** /host/{HostID}/status | Get the latest status of the host
[**getHosts**](HostApi.md#getHosts) | **GET** /hosts | This provides a list of hosts in the system
[**getHostsCounts**](HostApi.md#getHostsCounts) | **GET** /hosts/counts | Get the server counts in a time-range
[**getHostsCountsByType**](HostApi.md#getHostsCountsByType) | **GET** /hosts/counts_by_type | Get the server counts in a time-range
[**getHostsLaunch**](HostApi.md#getHostsLaunch) | **GET** /host/{HostID}/launch | This provides a list of host launches in the system
[**hostAlert**](HostApi.md#hostAlert) | **POST** /host/alert | Notifies the controller about a system alert.
[**launchHost**](HostApi.md#launchHost) | **POST** /host/launch | Launch a new host with a particular server type
[**pauseHost**](HostApi.md#pauseHost) | **POST** /host/{HostID}/pause | Pause all engines on this host.
[**registerEngineInstance**](HostApi.md#registerEngineInstance) | **POST** /host/{HostID}/engine/register | Register a new engine instance
[**registerHost**](HostApi.md#registerHost) | **POST** /host/register | Update the Host Status
[**resumeHost**](HostApi.md#resumeHost) | **POST** /host/{HostID}/resume | Resume all engines on this host.
[**terminateHost**](HostApi.md#terminateHost) | **POST** /host/{HostID}/terminate | Delete the host/agent record.  Any work still running on this host will be restarted on other hosts.
[**updateHostStatus**](HostApi.md#updateHostStatus) | **POST** /host/{HostID}/updatestatus | Update the Host Status


<a name="drainHost"></a>
# **drainHost**
> AdminOperationResponse drainHost(hostID, drainHostRequest, xCorrelationId)

Put this host into drain mode.  A host in drain mode will not have work assigned to engines on the host.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    HostApi apiInstance = new HostApi(defaultClient);
    UUID hostID = new UUID(); // UUID | ID of Host
    DrainHostRequest drainHostRequest = new DrainHostRequest(); // DrainHostRequest | The Request to Drain a Host
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AdminOperationResponse result = apiInstance.drainHost(hostID, drainHostRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#drainHost");
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
 **drainHostRequest** | [**DrainHostRequest**](DrainHostRequest.md)| The Request to Drain a Host |
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
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="getHostCpuUsage"></a>
# **getHostCpuUsage**
> GetHostCPUUsageResponse getHostCpuUsage(interval, startTime, endTime, type, hostID)

Get host cpu usage

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    HostApi apiInstance = new HostApi(defaultClient);
    Long interval = 56L; // Long | Interval in seconds for output time ranges.
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    RunModeEnum type = new RunModeEnum(); // RunModeEnum | Filter for hosts by type
    UUID hostID = new UUID(); // UUID | Filter data by hostID
    try {
      GetHostCPUUsageResponse result = apiInstance.getHostCpuUsage(interval, startTime, endTime, type, hostID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#getHostCpuUsage");
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
 **type** | [**RunModeEnum**](.md)| Filter for hosts by type | [optional] [enum: engine, nfs, registry, controller, db, standby, all, single, prometheus, api, apps, eventing, automatestudio, lb, nsq, es, redis, ceph-fs]
 **hostID** | [**UUID**](.md)| Filter data by hostID | [optional]

### Return type

[**GetHostCPUUsageResponse**](GetHostCPUUsageResponse.md)

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

<a name="getHostDetail"></a>
# **getHostDetail**
> HostDetail getHostDetail(hostID, xCorrelationId)

Get the latest info of the host

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    HostApi apiInstance = new HostApi(defaultClient);
    UUID hostID = new UUID(); // UUID | ID of Host
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      HostDetail result = apiInstance.getHostDetail(hostID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#getHostDetail");
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
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**HostDetail**](HostDetail.md)

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

<a name="getHostMemoryUsage"></a>
# **getHostMemoryUsage**
> GetHostMemoryUsageResponse getHostMemoryUsage(interval, startTime, endTime, type, hostID)

Get host memory usage

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    HostApi apiInstance = new HostApi(defaultClient);
    Long interval = 56L; // Long | Interval in seconds for output time ranges.
    Long startTime = 56L; // Long | The unix timestamp, describing the start time for the stats
    Long endTime = 56L; // Long | The unix timestamp, describing the end time for the stats
    RunModeEnum type = new RunModeEnum(); // RunModeEnum | Filter for hosts by type
    UUID hostID = new UUID(); // UUID | Filter data by hostID
    try {
      GetHostMemoryUsageResponse result = apiInstance.getHostMemoryUsage(interval, startTime, endTime, type, hostID);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#getHostMemoryUsage");
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
 **type** | [**RunModeEnum**](.md)| Filter for hosts by type | [optional] [enum: engine, nfs, registry, controller, db, standby, all, single, prometheus, api, apps, eventing, automatestudio, lb, nsq, es, redis, ceph-fs]
 **hostID** | [**UUID**](.md)| Filter data by hostID | [optional]

### Return type

[**GetHostMemoryUsageResponse**](GetHostMemoryUsageResponse.md)

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

<a name="getHostStatus"></a>
# **getHostStatus**
> HostStatus getHostStatus(hostID, xCorrelationId)

Get the latest status of the host

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");

    HostApi apiInstance = new HostApi(defaultClient);
    UUID hostID = new UUID(); // UUID | ID of Host
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      HostStatus result = apiInstance.getHostStatus(hostID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#getHostStatus");
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
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**HostStatus**](HostStatus.md)

### Authorization

No authorization required

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

<a name="getHosts"></a>
# **getHosts**
> AdminHostsGetResponse getHosts(xCorrelationId, offset, limit, direction, isactive, type, serverType, startCreatedTime, endCreatedTime, startLastUpdateTime, endLastUpdateTime, startTerminatedTime, endTerminatedTime, startExpireTime, endExpireTime, orderBy, drain, serverTypeID, ip)

This provides a list of hosts in the system

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    HostApi apiInstance = new HostApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long offset = 56L; // Long | the number of data to skip before getting the result set
    Long limit = 10lL; // Long | the number of items to return.
    String direction = "\"DESC\""; // String | the sort order.  ASC or DESC.
    Boolean isactive = true; // Boolean | Filter for active or inactive hosts
    RunModeEnum type = new RunModeEnum(); // RunModeEnum | Filter for hosts by type
    String serverType = "serverType_example"; // String | Filter for server type. Currently it should be in [physical, virtual]. It can expand in the future
    Long startCreatedTime = 56L; // Long | The unix timestamp
    Long endCreatedTime = 56L; // Long | The unix timestamp
    Long startLastUpdateTime = 56L; // Long | The unix timestamp
    Long endLastUpdateTime = 56L; // Long | The unix timestamp
    Long startTerminatedTime = 56L; // Long | The unix timestamp
    Long endTerminatedTime = 56L; // Long | The unix timestamp
    Long startExpireTime = 56L; // Long | The unix timestamp
    Long endExpireTime = 56L; // Long | The unix timestamp
    String orderBy = "orderBy_example"; // String | It should be in [createdTime, terminatedTime, expireTime]
    Boolean drain = true; // Boolean | Filter by drain
    UUID serverTypeID = new UUID(); // UUID | Filter by serverTypeID
    String ip = "ip_example"; // String | Filter by IP
    try {
      AdminHostsGetResponse result = apiInstance.getHosts(xCorrelationId, offset, limit, direction, isactive, type, serverType, startCreatedTime, endCreatedTime, startLastUpdateTime, endLastUpdateTime, startTerminatedTime, endTerminatedTime, startExpireTime, endExpireTime, orderBy, drain, serverTypeID, ip);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#getHosts");
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
 **offset** | **Long**| the number of data to skip before getting the result set | [optional]
 **limit** | **Long**| the number of items to return. | [optional] [default to 10l]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &quot;DESC&quot;]
 **isactive** | **Boolean**| Filter for active or inactive hosts | [optional]
 **type** | [**RunModeEnum**](.md)| Filter for hosts by type | [optional] [enum: engine, nfs, registry, controller, db, standby, all, single, prometheus, api, apps, eventing, automatestudio, lb, nsq, es, redis, ceph-fs]
 **serverType** | **String**| Filter for server type. Currently it should be in [physical, virtual]. It can expand in the future | [optional]
 **startCreatedTime** | **Long**| The unix timestamp | [optional]
 **endCreatedTime** | **Long**| The unix timestamp | [optional]
 **startLastUpdateTime** | **Long**| The unix timestamp | [optional]
 **endLastUpdateTime** | **Long**| The unix timestamp | [optional]
 **startTerminatedTime** | **Long**| The unix timestamp | [optional]
 **endTerminatedTime** | **Long**| The unix timestamp | [optional]
 **startExpireTime** | **Long**| The unix timestamp | [optional]
 **endExpireTime** | **Long**| The unix timestamp | [optional]
 **orderBy** | **String**| It should be in [createdTime, terminatedTime, expireTime] | [optional]
 **drain** | **Boolean**| Filter by drain | [optional]
 **serverTypeID** | [**UUID**](.md)| Filter by serverTypeID | [optional]
 **ip** | **String**| Filter by IP | [optional]

### Return type

[**AdminHostsGetResponse**](AdminHostsGetResponse.md)

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

<a name="getHostsCounts"></a>
# **getHostsCounts**
> HostsCountsResponse getHostsCounts(xCorrelationId, startLastUpdateTime, endLastUpdateTime)

Get the server counts in a time-range

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");

    HostApi apiInstance = new HostApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startLastUpdateTime = 56L; // Long | The unix timestamp
    Long endLastUpdateTime = 56L; // Long | The unix timestamp
    try {
      HostsCountsResponse result = apiInstance.getHostsCounts(xCorrelationId, startLastUpdateTime, endLastUpdateTime);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#getHostsCounts");
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
 **startLastUpdateTime** | **Long**| The unix timestamp | [optional]
 **endLastUpdateTime** | **Long**| The unix timestamp | [optional]

### Return type

[**HostsCountsResponse**](HostsCountsResponse.md)

### Authorization

No authorization required

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

<a name="getHostsCountsByType"></a>
# **getHostsCountsByType**
> HostsCountsByTypeResponse getHostsCountsByType(xCorrelationId, startLastUpdateTime, endLastUpdateTime, chartType, type)

Get the server counts in a time-range

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");

    HostApi apiInstance = new HostApi(defaultClient);
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    Long startLastUpdateTime = 56L; // Long | The unix timestamp
    Long endLastUpdateTime = 56L; // Long | The unix timestamp
    ChartTypeEnum chartType = new ChartTypeEnum(); // ChartTypeEnum | It will help API to kmow the response should return
    RunModeEnum type = new RunModeEnum(); // RunModeEnum | Filter for hosts by type
    try {
      HostsCountsByTypeResponse result = apiInstance.getHostsCountsByType(xCorrelationId, startLastUpdateTime, endLastUpdateTime, chartType, type);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#getHostsCountsByType");
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
 **startLastUpdateTime** | **Long**| The unix timestamp | [optional]
 **endLastUpdateTime** | **Long**| The unix timestamp | [optional]
 **chartType** | [**ChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] [enum: pie, time_range]
 **type** | [**RunModeEnum**](.md)| Filter for hosts by type | [optional] [enum: engine, nfs, registry, controller, db, standby, all, single, prometheus, api, apps, eventing, automatestudio, lb, nsq, es, redis, ceph-fs]

### Return type

[**HostsCountsByTypeResponse**](HostsCountsByTypeResponse.md)

### Authorization

No authorization required

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

<a name="getHostsLaunch"></a>
# **getHostsLaunch**
> GetHostLaunchResponse getHostsLaunch(hostID, xCorrelationId)

This provides a list of host launches in the system

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    HostApi apiInstance = new HostApi(defaultClient);
    UUID hostID = new UUID(); // UUID | ID of Host
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      GetHostLaunchResponse result = apiInstance.getHostsLaunch(hostID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#getHostsLaunch");
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
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**GetHostLaunchResponse**](GetHostLaunchResponse.md)

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

<a name="hostAlert"></a>
# **hostAlert**
> AdminOperationResponse hostAlert(hostAlertRequest, xCorrelationId)

Notifies the controller about a system alert.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    HostApi apiInstance = new HostApi(defaultClient);
    HostAlertRequest hostAlertRequest = new HostAlertRequest(); // HostAlertRequest | 
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AdminOperationResponse result = apiInstance.hostAlert(hostAlertRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#hostAlert");
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
 **hostAlertRequest** | [**HostAlertRequest**](HostAlertRequest.md)|  |
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
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="launchHost"></a>
# **launchHost**
> AdminOperationResponse launchHost(launchHostRequest)

Launch a new host with a particular server type

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    HostApi apiInstance = new HostApi(defaultClient);
    LaunchHostRequest launchHostRequest = new LaunchHostRequest(); // LaunchHostRequest | The Request to Launch a Host
    try {
      AdminOperationResponse result = apiInstance.launchHost(launchHostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#launchHost");
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
 **launchHostRequest** | [**LaunchHostRequest**](LaunchHostRequest.md)| The Request to Launch a Host |

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
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="pauseHost"></a>
# **pauseHost**
> AdminOperationResponse pauseHost(hostID, xCorrelationId)

Pause all engines on this host.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    HostApi apiInstance = new HostApi(defaultClient);
    UUID hostID = new UUID(); // UUID | ID of Host
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AdminOperationResponse result = apiInstance.pauseHost(hostID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#pauseHost");
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
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="registerEngineInstance"></a>
# **registerEngineInstance**
> EngineInstanceRegistrationInfo registerEngineInstance(hostID, engineInstanceInfo, xCorrelationId)

Register a new engine instance

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");

    HostApi apiInstance = new HostApi(defaultClient);
    UUID hostID = new UUID(); // UUID | ID of Host
    EngineInstanceInfo engineInstanceInfo = new EngineInstanceInfo(); // EngineInstanceInfo | Engine Instance Info
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      EngineInstanceRegistrationInfo result = apiInstance.registerEngineInstance(hostID, engineInstanceInfo, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#registerEngineInstance");
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

<a name="registerHost"></a>
# **registerHost**
> HostRegisterResponse registerHost(hostRegisterRequest, xCorrelationId)

Update the Host Status

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");

    HostApi apiInstance = new HostApi(defaultClient);
    HostRegisterRequest hostRegisterRequest = new HostRegisterRequest(); // HostRegisterRequest | Engine Instance Info
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      HostRegisterResponse result = apiInstance.registerHost(hostRegisterRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#registerHost");
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
 **hostRegisterRequest** | [**HostRegisterRequest**](HostRegisterRequest.md)| Engine Instance Info |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**HostRegisterResponse**](HostRegisterResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
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

<a name="resumeHost"></a>
# **resumeHost**
> AdminOperationResponse resumeHost(hostID, xCorrelationId)

Resume all engines on this host.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    HostApi apiInstance = new HostApi(defaultClient);
    UUID hostID = new UUID(); // UUID | ID of Host
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AdminOperationResponse result = apiInstance.resumeHost(hostID, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#resumeHost");
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
**200** | Successful operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="terminateHost"></a>
# **terminateHost**
> AdminOperationResponse terminateHost(hostID, terminateHostRequest, xCorrelationId)

Delete the host/agent record.  Any work still running on this host will be restarted on other hosts.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    HostApi apiInstance = new HostApi(defaultClient);
    UUID hostID = new UUID(); // UUID | ID of Host
    TerminateHostRequest terminateHostRequest = new TerminateHostRequest(); // TerminateHostRequest | The request to terminate the host
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      AdminOperationResponse result = apiInstance.terminateHost(hostID, terminateHostRequest, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#terminateHost");
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
 **terminateHostRequest** | [**TerminateHostRequest**](TerminateHostRequest.md)| The request to terminate the host |
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
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

<a name="updateHostStatus"></a>
# **updateHostStatus**
> HostAction updateHostStatus(hostID, hostStatus, xCorrelationId)

Update the Host Status

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.HostApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.aiware.com/edge/v1");
    
    // Configure API key authorization: api_key
    ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
    api_key.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //api_key.setApiKeyPrefix("Token");

    HostApi apiInstance = new HostApi(defaultClient);
    UUID hostID = new UUID(); // UUID | ID of Host
    HostStatus hostStatus = new HostStatus(); // HostStatus | Host Status
    String xCorrelationId = "xCorrelationId_example"; // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
    try {
      HostAction result = apiInstance.updateHostStatus(hostID, hostStatus, xCorrelationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HostApi#updateHostStatus");
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
 **hostStatus** | [**HostStatus**](HostStatus.md)| Host Status |
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional]

### Return type

[**HostAction**](HostAction.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
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

