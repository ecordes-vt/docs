# AiwareJsClient.HostApi

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



## drainHost

> AdminOperationResponse drainHost(hostID, drainHostRequest, opts)

Put this host into drain mode.  A host in drain mode will not have work assigned to engines on the host.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.HostApi();
let hostID = null; // String | ID of Host
let drainHostRequest = new AiwareJsClient.DrainHostRequest(); // DrainHostRequest | The Request to Drain a Host
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.drainHost(hostID, drainHostRequest, opts, (error, data, response) => {
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
 **drainHostRequest** | [**DrainHostRequest**](DrainHostRequest.md)| The Request to Drain a Host | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## getHostCpuUsage

> GetHostCPUUsageResponse getHostCpuUsage(opts)

Get host cpu usage

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.HostApi();
let opts = {
  'interval': 789, // Number | Interval in seconds for output time ranges.
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'type': new AiwareJsClient.RunModeEnum(), // RunModeEnum | Filter for hosts by type
  'hostID': null // String | Filter data by hostID
};
apiInstance.getHostCpuUsage(opts, (error, data, response) => {
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
 **interval** | **Number**| Interval in seconds for output time ranges. | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **type** | [**RunModeEnum**](.md)| Filter for hosts by type | [optional] 
 **hostID** | [**String**](.md)| Filter data by hostID | [optional] 

### Return type

[**GetHostCPUUsageResponse**](GetHostCPUUsageResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getHostDetail

> HostDetail getHostDetail(hostID, opts)

Get the latest info of the host

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.HostApi();
let hostID = null; // String | ID of Host
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getHostDetail(hostID, opts, (error, data, response) => {
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
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**HostDetail**](HostDetail.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getHostMemoryUsage

> GetHostMemoryUsageResponse getHostMemoryUsage(opts)

Get host memory usage

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.HostApi();
let opts = {
  'interval': 789, // Number | Interval in seconds for output time ranges.
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'type': new AiwareJsClient.RunModeEnum(), // RunModeEnum | Filter for hosts by type
  'hostID': null // String | Filter data by hostID
};
apiInstance.getHostMemoryUsage(opts, (error, data, response) => {
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
 **interval** | **Number**| Interval in seconds for output time ranges. | [optional] 
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **type** | [**RunModeEnum**](.md)| Filter for hosts by type | [optional] 
 **hostID** | [**String**](.md)| Filter data by hostID | [optional] 

### Return type

[**GetHostMemoryUsageResponse**](GetHostMemoryUsageResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getHostStatus

> HostStatus getHostStatus(hostID, opts)

Get the latest status of the host

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';

let apiInstance = new AiwareJsClient.HostApi();
let hostID = null; // String | ID of Host
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getHostStatus(hostID, opts, (error, data, response) => {
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
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**HostStatus**](HostStatus.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getHosts

> AdminHostsGetResponse getHosts(opts)

This provides a list of hosts in the system

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.HostApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'direction': "'DESC'", // String | the sort order.  ASC or DESC.
  'isactive': true, // Boolean | Filter for active or inactive hosts
  'type': new AiwareJsClient.RunModeEnum(), // RunModeEnum | Filter for hosts by type
  'serverType': "serverType_example", // String | Filter for server type. Currently it should be in [physical, virtual]. It can expand in the future
  'startCreatedTime': 789, // Number | The unix timestamp
  'endCreatedTime': 789, // Number | The unix timestamp
  'startLastUpdateTime': 789, // Number | The unix timestamp
  'endLastUpdateTime': 789, // Number | The unix timestamp
  'startTerminatedTime': 789, // Number | The unix timestamp
  'endTerminatedTime': 789, // Number | The unix timestamp
  'startExpireTime': 789, // Number | The unix timestamp
  'endExpireTime': 789, // Number | The unix timestamp
  'orderBy': "orderBy_example", // String | It should be in [createdTime, terminatedTime, expireTime]
  'drain': true, // Boolean | Filter by drain
  'serverTypeID': null, // String | Filter by serverTypeID
  'ip': "ip_example" // String | Filter by IP
};
apiInstance.getHosts(opts, (error, data, response) => {
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
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **offset** | **Number**| the number of data to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of items to return. | [optional] [default to 10]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **isactive** | **Boolean**| Filter for active or inactive hosts | [optional] 
 **type** | [**RunModeEnum**](.md)| Filter for hosts by type | [optional] 
 **serverType** | **String**| Filter for server type. Currently it should be in [physical, virtual]. It can expand in the future | [optional] 
 **startCreatedTime** | **Number**| The unix timestamp | [optional] 
 **endCreatedTime** | **Number**| The unix timestamp | [optional] 
 **startLastUpdateTime** | **Number**| The unix timestamp | [optional] 
 **endLastUpdateTime** | **Number**| The unix timestamp | [optional] 
 **startTerminatedTime** | **Number**| The unix timestamp | [optional] 
 **endTerminatedTime** | **Number**| The unix timestamp | [optional] 
 **startExpireTime** | **Number**| The unix timestamp | [optional] 
 **endExpireTime** | **Number**| The unix timestamp | [optional] 
 **orderBy** | **String**| It should be in [createdTime, terminatedTime, expireTime] | [optional] 
 **drain** | **Boolean**| Filter by drain | [optional] 
 **serverTypeID** | [**String**](.md)| Filter by serverTypeID | [optional] 
 **ip** | **String**| Filter by IP | [optional] 

### Return type

[**AdminHostsGetResponse**](AdminHostsGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getHostsCounts

> HostsCountsResponse getHostsCounts(opts)

Get the server counts in a time-range

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';

let apiInstance = new AiwareJsClient.HostApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startLastUpdateTime': 789, // Number | The unix timestamp
  'endLastUpdateTime': 789 // Number | The unix timestamp
};
apiInstance.getHostsCounts(opts, (error, data, response) => {
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
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startLastUpdateTime** | **Number**| The unix timestamp | [optional] 
 **endLastUpdateTime** | **Number**| The unix timestamp | [optional] 

### Return type

[**HostsCountsResponse**](HostsCountsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getHostsCountsByType

> HostsCountsByTypeResponse getHostsCountsByType(opts)

Get the server counts in a time-range

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';

let apiInstance = new AiwareJsClient.HostApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'startLastUpdateTime': 789, // Number | The unix timestamp
  'endLastUpdateTime': 789, // Number | The unix timestamp
  'chartType': new AiwareJsClient.ChartTypeEnum(), // ChartTypeEnum | It will help API to kmow the response should return
  'type': new AiwareJsClient.RunModeEnum() // RunModeEnum | Filter for hosts by type
};
apiInstance.getHostsCountsByType(opts, (error, data, response) => {
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
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **startLastUpdateTime** | **Number**| The unix timestamp | [optional] 
 **endLastUpdateTime** | **Number**| The unix timestamp | [optional] 
 **chartType** | [**ChartTypeEnum**](.md)| It will help API to kmow the response should return | [optional] 
 **type** | [**RunModeEnum**](.md)| Filter for hosts by type | [optional] 

### Return type

[**HostsCountsByTypeResponse**](HostsCountsByTypeResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getHostsLaunch

> GetHostLaunchResponse getHostsLaunch(hostID, opts)

This provides a list of host launches in the system

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.HostApi();
let hostID = null; // String | ID of Host
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getHostsLaunch(hostID, opts, (error, data, response) => {
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
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetHostLaunchResponse**](GetHostLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## hostAlert

> AdminOperationResponse hostAlert(hostAlertRequest, opts)

Notifies the controller about a system alert.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.HostApi();
let hostAlertRequest = new AiwareJsClient.HostAlertRequest(); // HostAlertRequest | 
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.hostAlert(hostAlertRequest, opts, (error, data, response) => {
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
 **hostAlertRequest** | [**HostAlertRequest**](HostAlertRequest.md)|  | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## launchHost

> AdminOperationResponse launchHost(launchHostRequest)

Launch a new host with a particular server type

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.HostApi();
let launchHostRequest = new AiwareJsClient.LaunchHostRequest(); // LaunchHostRequest | The Request to Launch a Host
apiInstance.launchHost(launchHostRequest, (error, data, response) => {
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
 **launchHostRequest** | [**LaunchHostRequest**](LaunchHostRequest.md)| The Request to Launch a Host | 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## pauseHost

> AdminOperationResponse pauseHost(hostID, opts)

Pause all engines on this host.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.HostApi();
let hostID = null; // String | ID of Host
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.pauseHost(hostID, opts, (error, data, response) => {
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
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## registerEngineInstance

> EngineInstanceRegistrationInfo registerEngineInstance(hostID, engineInstanceInfo, opts)

Register a new engine instance

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';

let apiInstance = new AiwareJsClient.HostApi();
let hostID = null; // String | ID of Host
let engineInstanceInfo = new AiwareJsClient.EngineInstanceInfo(); // EngineInstanceInfo | Engine Instance Info
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.registerEngineInstance(hostID, engineInstanceInfo, opts, (error, data, response) => {
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
 **engineInstanceInfo** | [**EngineInstanceInfo**](EngineInstanceInfo.md)| Engine Instance Info | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceRegistrationInfo**](EngineInstanceRegistrationInfo.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## registerHost

> HostRegisterResponse registerHost(hostRegisterRequest, opts)

Update the Host Status

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';

let apiInstance = new AiwareJsClient.HostApi();
let hostRegisterRequest = new AiwareJsClient.HostRegisterRequest(); // HostRegisterRequest | Engine Instance Info
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.registerHost(hostRegisterRequest, opts, (error, data, response) => {
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
 **hostRegisterRequest** | [**HostRegisterRequest**](HostRegisterRequest.md)| Engine Instance Info | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**HostRegisterResponse**](HostRegisterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## resumeHost

> AdminOperationResponse resumeHost(hostID, opts)

Resume all engines on this host.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.HostApi();
let hostID = null; // String | ID of Host
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.resumeHost(hostID, opts, (error, data, response) => {
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
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## terminateHost

> AdminOperationResponse terminateHost(hostID, terminateHostRequest, opts)

Delete the host/agent record.  Any work still running on this host will be restarted on other hosts.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.HostApi();
let hostID = null; // String | ID of Host
let terminateHostRequest = new AiwareJsClient.TerminateHostRequest(); // TerminateHostRequest | The request to terminate the host
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.terminateHost(hostID, terminateHostRequest, opts, (error, data, response) => {
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
 **terminateHostRequest** | [**TerminateHostRequest**](TerminateHostRequest.md)| The request to terminate the host | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateHostStatus

> HostAction updateHostStatus(hostID, hostStatus, opts)

Update the Host Status

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.HostApi();
let hostID = null; // String | ID of Host
let hostStatus = new AiwareJsClient.HostStatus(); // HostStatus | Host Status
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateHostStatus(hostID, hostStatus, opts, (error, data, response) => {
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
 **hostStatus** | [**HostStatus**](HostStatus.md)| Host Status | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**HostAction**](HostAction.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

