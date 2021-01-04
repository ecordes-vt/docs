# AiwareJsClient.EngineApi

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



## createBuild

> CreateBuildResponse createBuild(createBuildRequest, opts)

This API creates a new engine build

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let createBuildRequest = new AiwareJsClient.CreateBuildRequest(); // CreateBuildRequest | The fields for an engine build
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createBuild(createBuildRequest, opts, (error, data, response) => {
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
 **createBuildRequest** | [**CreateBuildRequest**](CreateBuildRequest.md)| The fields for an engine build | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateBuildResponse**](CreateBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createEngine

> CreateEngineResponse createEngine(createEngineRequest, opts)

This API creates a new engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let createEngineRequest = new AiwareJsClient.CreateEngineRequest(); // CreateEngineRequest | The fields for an engine
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createEngine(createEngineRequest, opts, (error, data, response) => {
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
 **createEngineRequest** | [**CreateEngineRequest**](CreateEngineRequest.md)| The fields for an engine | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateEngineResponse**](CreateEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createEngineCategory

> CreateEngineCategoryResponse createEngineCategory(createEngineCategoryDetail, opts)

This API creates a new engine category

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let createEngineCategoryDetail = new AiwareJsClient.CreateEngineCategoryDetail(); // CreateEngineCategoryDetail | The fields for an engine category
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createEngineCategory(createEngineCategoryDetail, opts, (error, data, response) => {
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
 **createEngineCategoryDetail** | [**CreateEngineCategoryDetail**](CreateEngineCategoryDetail.md)| The fields for an engine category | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateEngineCategoryResponse**](CreateEngineCategoryResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## deleteBuildPost

> AdminOperationResponse deleteBuildPost(engineID, buildID, opts)

This API provides the engine detail result

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineID = null; // String | ID of Engine
let buildID = null; // String | ID of Build
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.deleteBuildPost(engineID, buildID, opts, (error, data, response) => {
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
 **engineID** | [**String**](.md)| ID of Engine | 
 **buildID** | [**String**](.md)| ID of Build | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## deleteEnginePost

> AdminOperationResponse deleteEnginePost(engineID, opts)

This API delets an engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineID = null; // String | ID of Engine
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.deleteEnginePost(engineID, opts, (error, data, response) => {
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
 **engineID** | [**String**](.md)| ID of Engine | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineBuild

> GetEngineBuildResponse getEngineBuild(buildID, opts)

This gets a particular build

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let buildID = null; // String | ID of Build
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getEngineBuild(buildID, opts, (error, data, response) => {
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
 **buildID** | [**String**](.md)| ID of Build | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetEngineBuildResponse**](GetEngineBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineBuilds

> GetEngineBuildsResponse getEngineBuilds(engineID, opts)

Get the list of builds deployed and available on aiWARE for a particular engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineID = null; // String | ID of Engine
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'buildState': "buildState_example" // String | Filter builds by the build state
};
apiInstance.getEngineBuilds(engineID, opts, (error, data, response) => {
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
 **engineID** | [**String**](.md)| ID of Engine | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **buildState** | **String**| Filter builds by the build state | [optional] 

### Return type

[**GetEngineBuildsResponse**](GetEngineBuildsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineBuildsByState

> GetEngineBuildByStateResponse getEngineBuildsByState(opts)

The api returns engine build records by build state

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'state': "state_example" // String | Filter data by build state
};
apiInstance.getEngineBuildsByState(opts, (error, data, response) => {
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
 **state** | **String**| Filter data by build state | [optional] 

### Return type

[**GetEngineBuildByStateResponse**](GetEngineBuildByStateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineCategories

> GetEngineCategoriesResponse getEngineCategories(opts)

This provides a list of engine categories

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getEngineCategories(opts, (error, data, response) => {
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

### Return type

[**GetEngineCategoriesResponse**](GetEngineCategoriesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineCategoryDetail

> GetEngineCategoryDetailResponse getEngineCategoryDetail(engineCategoryID, opts)

This provides detail for an engine category

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineCategoryID = null; // String | ID of Engine Category
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getEngineCategoryDetail(engineCategoryID, opts, (error, data, response) => {
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
 **engineCategoryID** | [**String**](.md)| ID of Engine Category | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetEngineCategoryDetailResponse**](GetEngineCategoryDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineContainerCount

> GetEngineContainerCountResponse getEngineContainerCount(opts)

Get engine container count

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let opts = {
  'interval': 789, // Number | Interval in seconds for output time ranges.
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'groupBy': new AiwareJsClient.EngineContainerGroupByEnum(), // EngineContainerGroupByEnum | Group data by engineID or instance
  'engineID': null, // String | Filter data by engineID
  'hostID': null // String | Filter data by hostID
};
apiInstance.getEngineContainerCount(opts, (error, data, response) => {
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
 **groupBy** | [**EngineContainerGroupByEnum**](.md)| Group data by engineID or instance | [optional] 
 **engineID** | [**String**](.md)| Filter data by engineID | [optional] 
 **hostID** | [**String**](.md)| Filter data by hostID | [optional] 

### Return type

[**GetEngineContainerCountResponse**](GetEngineContainerCountResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineDetail

> GetEngineDetailResponse getEngineDetail(engineID)

This API provides the engine detail result

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineID = null; // String | ID of Engine
apiInstance.getEngineDetail(engineID, (error, data, response) => {
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
 **engineID** | [**String**](.md)| ID of Engine | 

### Return type

[**GetEngineDetailResponse**](GetEngineDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineInstanceDetail

> EngineInstanceInfo getEngineInstanceDetail(engineInstanceID, opts)

Get information about an engine Instance

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineInstanceID = null; // String | ID of Engine Instance
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getEngineInstanceDetail(engineInstanceID, opts, (error, data, response) => {
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
 **engineInstanceID** | [**String**](.md)| ID of Engine Instance | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceInfo**](EngineInstanceInfo.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineInstanceList

> GetEngineInstanceListResponse getEngineInstanceList(opts)

Get engines instances with filtering

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'engineInstanceIDs': "engineInstanceIDs_example", // String | Field to provide the input to get engine instances by ID list. Separated by commas
  'engineIDs': "engineIDs_example", // String | Field to provide the input to get engines by Engine ID list. Separated by commas
  'hostIDs': null, // String | Filtering engine instances by host IDs. Separated by commas
  'workRequestIDs': null, // String | Filters engine instances by workrequest IDs. Separated by commas
  'status': new AiwareJsClient.EngineStatusEnum(), // EngineStatusEnum | Field to match the current status
  'drain': true, // Boolean | Filter by drain
  'launchStartTime': 789, // Number | The unix timestamp, describing a lower limit for the time an engine instance was launched.
  'launchEndTime': 789, // Number | The unix timestamp, describing an upper limit for the time an engine instance was launched.
  'modifiedBefore': 789, // Number | Filter by items modified before expressed as timestamp
  'modifiedAfter': 789, // Number | Filter by items modified after expressed as timestamp
  'createdBefore': 789, // Number | Filter items where created date is before this date
  'createdAfter': 789, // Number | Filter items where created date is after this date
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'direction': "'DESC'", // String | the sort order.  ASC or DESC.
  'orderBy': "orderBy_example" // String | It should be in [engineID, hostID, status, createdTime, modifiedTime, lastUpdateTime, launchTime]
};
apiInstance.getEngineInstanceList(opts, (error, data, response) => {
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
 **engineInstanceIDs** | **String**| Field to provide the input to get engine instances by ID list. Separated by commas | [optional] 
 **engineIDs** | **String**| Field to provide the input to get engines by Engine ID list. Separated by commas | [optional] 
 **hostIDs** | [**String**](.md)| Filtering engine instances by host IDs. Separated by commas | [optional] 
 **workRequestIDs** | [**String**](.md)| Filters engine instances by workrequest IDs. Separated by commas | [optional] 
 **status** | [**EngineStatusEnum**](.md)| Field to match the current status | [optional] 
 **drain** | **Boolean**| Filter by drain | [optional] 
 **launchStartTime** | **Number**| The unix timestamp, describing a lower limit for the time an engine instance was launched. | [optional] 
 **launchEndTime** | **Number**| The unix timestamp, describing an upper limit for the time an engine instance was launched. | [optional] 
 **modifiedBefore** | **Number**| Filter by items modified before expressed as timestamp | [optional] 
 **modifiedAfter** | **Number**| Filter by items modified after expressed as timestamp | [optional] 
 **createdBefore** | **Number**| Filter items where created date is before this date | [optional] 
 **createdAfter** | **Number**| Filter items where created date is after this date | [optional] 
 **offset** | **Number**| the number of data to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of items to return. | [optional] [default to 10]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **orderBy** | **String**| It should be in [engineID, hostID, status, createdTime, modifiedTime, lastUpdateTime, launchTime] | [optional] 

### Return type

[**GetEngineInstanceListResponse**](GetEngineInstanceListResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineInstanceLogs

> File getEngineInstanceLogs(engineInstanceID, opts)

Get engine instance logs as a zip file

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineInstanceID = null; // String | ID of Engine Instance
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getEngineInstanceLogs(engineInstanceID, opts, (error, data, response) => {
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
 **engineInstanceID** | [**String**](.md)| ID of Engine Instance | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

**File**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/zip, application/json


## getEngineInstanceStatus

> EngineInstanceStatus getEngineInstanceStatus(engineInstanceID, opts)

Get the latest status of the engine instance

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineInstanceID = null; // String | ID of Engine Instance
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getEngineInstanceStatus(engineInstanceID, opts, (error, data, response) => {
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
 **engineInstanceID** | [**String**](.md)| ID of Engine Instance | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceStatus**](EngineInstanceStatus.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineInstanceWork

> EngineInstanceWorkRequestResponse getEngineInstanceWork(engineInstanceID, engineInstanceWorkRequest, opts)

Get a work request

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineInstanceID = null; // String | ID of Engine Instance
let engineInstanceWorkRequest = new AiwareJsClient.EngineInstanceWorkRequest(); // EngineInstanceWorkRequest | Engine Instance Info
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getEngineInstanceWork(engineInstanceID, engineInstanceWorkRequest, opts, (error, data, response) => {
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
 **engineInstanceID** | [**String**](.md)| ID of Engine Instance | 
 **engineInstanceWorkRequest** | [**EngineInstanceWorkRequest**](EngineInstanceWorkRequest.md)| Engine Instance Info | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceWorkRequestResponse**](EngineInstanceWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## getEngineInstanceWorkDetail

> EngineInstanceWorkDetailsResponse getEngineInstanceWorkDetail(engineInstanceID, opts)

Get detail of the work being done by the engine instance

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineInstanceID = null; // String | ID of Engine Instance
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getEngineInstanceWorkDetail(engineInstanceID, opts, (error, data, response) => {
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
 **engineInstanceID** | [**String**](.md)| ID of Engine Instance | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceWorkDetailsResponse**](EngineInstanceWorkDetailsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineInstances

> GetEngineInstancesResponse getEngineInstances(engineID, opts)

Get information about the instances of an engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineID = "engineID_example"; // String | EngineID of node-red container request
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'launchStartTime': 789, // Number | The unix timestamp, describing a lower limit for the time an engine instance was launched.
  'launchEndTime': 789, // Number | The unix timestamp, describing an upper limit for the time an engine instance was launched.
  'modifiedBefore': 789, // Number | Filter by items modified before expressed as timestamp
  'modifiedAfter': 789, // Number | Filter by items modified after expressed as timestamp
  'createdBefore': 789, // Number | Filter items where created date is before this date
  'createdAfter': 789 // Number | Filter items where created date is after this date
};
apiInstance.getEngineInstances(engineID, opts, (error, data, response) => {
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
 **engineID** | **String**| EngineID of node-red container request | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **launchStartTime** | **Number**| The unix timestamp, describing a lower limit for the time an engine instance was launched. | [optional] 
 **launchEndTime** | **Number**| The unix timestamp, describing an upper limit for the time an engine instance was launched. | [optional] 
 **modifiedBefore** | **Number**| Filter by items modified before expressed as timestamp | [optional] 
 **modifiedAfter** | **Number**| Filter by items modified after expressed as timestamp | [optional] 
 **createdBefore** | **Number**| Filter items where created date is before this date | [optional] 
 **createdAfter** | **Number**| Filter items where created date is after this date | [optional] 

### Return type

[**GetEngineInstancesResponse**](GetEngineInstancesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineLaunchDetail

> GetEngineLaunchResponse getEngineLaunchDetail(engineID, launchID, opts)

This API returns the list of launches for this engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineID = null; // String | ID of Engine
let launchID = null; // String | ID of Launch
let opts = {
  'createdBefore': 789, // Number | Filter items where created date is before this date
  'createdAfter': 789, // Number | Filter items where created date is after this date
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'orderBy': "'createdDateTime'", // String | the field to sort
  'direction': "'DESC'" // String | the sort order.  ASC or DESC.
};
apiInstance.getEngineLaunchDetail(engineID, launchID, opts, (error, data, response) => {
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
 **engineID** | [**String**](.md)| ID of Engine | 
 **launchID** | [**String**](.md)| ID of Launch | 
 **createdBefore** | **Number**| Filter items where created date is before this date | [optional] 
 **createdAfter** | **Number**| Filter items where created date is after this date | [optional] 
 **offset** | **Number**| the number of data to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of items to return. | [optional] [default to 10]
 **orderBy** | **String**| the field to sort | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]

### Return type

[**GetEngineLaunchResponse**](GetEngineLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngineLaunches

> GetEngineLaunchResponse getEngineLaunches(engineID, opts)

This API returns the list of launches for this engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineID = null; // String | ID of Engine
let opts = {
  'launchStatus': new AiwareJsClient.LaunchStatusEnum(), // LaunchStatusEnum | Field to match the current launch status
  'launchAction': new AiwareJsClient.LaunchActionEnum(), // LaunchActionEnum | Field to match the current launch action
  'createdBefore': 789, // Number | Filter items where created date is before this date
  'createdAfter': 789, // Number | Filter items where created date is after this date
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'orderBy': "'createdDateTime'", // String | the field to sort
  'direction': "'DESC'" // String | the sort order.  ASC or DESC.
};
apiInstance.getEngineLaunches(engineID, opts, (error, data, response) => {
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
 **engineID** | [**String**](.md)| ID of Engine | 
 **launchStatus** | [**LaunchStatusEnum**](.md)| Field to match the current launch status | [optional] 
 **launchAction** | [**LaunchActionEnum**](.md)| Field to match the current launch action | [optional] 
 **createdBefore** | **Number**| Filter items where created date is before this date | [optional] 
 **createdAfter** | **Number**| Filter items where created date is after this date | [optional] 
 **offset** | **Number**| the number of data to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of items to return. | [optional] [default to 10]
 **orderBy** | **String**| the field to sort | [optional] [default to &#39;createdDateTime&#39;]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]

### Return type

[**GetEngineLaunchResponse**](GetEngineLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEngines

> GetEnginesResponse getEngines(opts)

Get the list of engines deployed and available on aiWARE

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'internalOrganizationID': null, // String | ID of Organization.  UUID.  This ID is unique to this aiWARE installation.
  'engineName': "engineName_example", // String | Field to string match against the engine names
  'engineState': new AiwareJsClient.EngineStateEnum(), // EngineStateEnum | Field to match the current state
  'engineType': new AiwareJsClient.EngineTypeEnum(), // EngineTypeEnum | Field to match the current type
  'engineOutputType': new AiwareJsClient.EngineTypeEnum(), // EngineTypeEnum | Field to match the current type
  'engineCategoryID': "engineCategoryID_example", // String | Filter to the particular engine category ID
  'engineIDs': "engineIDs_example", // String | Field to provide the input to get engines by Engine ID list. Separated by commas
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'direction': "'DESC'", // String | the sort order.  ASC or DESC.
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'preload': true, // Boolean | Filter engines by preload
  'orderBy': "orderBy_example" // String | The value should be in [name, state, type, organizationID, createdTime]
};
apiInstance.getEngines(opts, (error, data, response) => {
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
 **internalOrganizationID** | [**String**](.md)| ID of Organization.  UUID.  This ID is unique to this aiWARE installation. | [optional] 
 **engineName** | **String**| Field to string match against the engine names | [optional] 
 **engineState** | [**EngineStateEnum**](.md)| Field to match the current state | [optional] 
 **engineType** | [**EngineTypeEnum**](.md)| Field to match the current type | [optional] 
 **engineOutputType** | [**EngineTypeEnum**](.md)| Field to match the current type | [optional] 
 **engineCategoryID** | **String**| Filter to the particular engine category ID | [optional] 
 **engineIDs** | **String**| Field to provide the input to get engines by Engine ID list. Separated by commas | [optional] 
 **offset** | **Number**| the number of data to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of items to return. | [optional] [default to 10]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **startTime** | **Number**| The unix timestamp, describing the start time for the stats | [optional] 
 **endTime** | **Number**| The unix timestamp, describing the end time for the stats | [optional] 
 **preload** | **Boolean**| Filter engines by preload | [optional] 
 **orderBy** | **String**| The value should be in [name, state, type, organizationID, createdTime] | [optional] 

### Return type

[**GetEnginesResponse**](GetEnginesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getJobsBacklogCountByEngine

> GetJobsBacklogCountResponse getJobsBacklogCountByEngine(opts)

Get backlog count by engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let opts = {
  'interval': 789, // Number | Interval in seconds for output time ranges.
  'startTime': 789, // Number | The unix timestamp, describing the start time for the stats
  'endTime': 789, // Number | The unix timestamp, describing the end time for the stats
  'organizationIDs': "organizationIDs_example" // String | 
};
apiInstance.getJobsBacklogCountByEngine(opts, (error, data, response) => {
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
 **organizationIDs** | **String**|  | [optional] 

### Return type

[**GetJobsBacklogCountResponse**](GetJobsBacklogCountResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getResourcesForEngineInstance

> GetResourcesForEngineInstanceResponse getResourcesForEngineInstance(engineInstanceID, opts)

Get resources for engine instance

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineInstanceID = null; // String | ID of Engine Instance
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getResourcesForEngineInstance(engineInstanceID, opts, (error, data, response) => {
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
 **engineInstanceID** | [**String**](.md)| ID of Engine Instance | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetResourcesForEngineInstanceResponse**](GetResourcesForEngineInstanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pauseBuild

> AdminOperationResponse pauseBuild(buildID, opts)

This API pauses a build so that tasks based on this engine build will not run.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let buildID = null; // String | ID of Build
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'buildState': "buildState_example" // String | Filter builds by the build state
};
apiInstance.pauseBuild(buildID, opts, (error, data, response) => {
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
 **buildID** | [**String**](.md)| ID of Build | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **buildState** | **String**| Filter builds by the build state | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pauseEngine

> AdminOperationResponse pauseEngine(engineID, opts)

This API pauses an engine so that tasks based on this engine will not run.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineID = null; // String | ID of Engine
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'pauseEngineRequest': new AiwareJsClient.PauseEngineRequest() // PauseEngineRequest | Engine Instance Info
};
apiInstance.pauseEngine(engineID, opts, (error, data, response) => {
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
 **engineID** | [**String**](.md)| ID of Engine | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **pauseEngineRequest** | [**PauseEngineRequest**](PauseEngineRequest.md)| Engine Instance Info | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## registerEngineInstanceNoAuth

> EngineInstanceRegistrationInfo registerEngineInstanceNoAuth(engineInstanceInfo, opts)

Register a new engine instance without authorization

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';

let apiInstance = new AiwareJsClient.EngineApi();
let engineInstanceInfo = new AiwareJsClient.EngineInstanceInfo(); // EngineInstanceInfo | Engine Instance Info
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.registerEngineInstanceNoAuth(engineInstanceInfo, opts, (error, data, response) => {
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
 **engineInstanceInfo** | [**EngineInstanceInfo**](EngineInstanceInfo.md)| Engine Instance Info | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceRegistrationInfo**](EngineInstanceRegistrationInfo.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## replaceEngine

> AdminOperationResponse replaceEngine(engineID, opts)

This API replaced an engine so that tasks based on this engine will not run.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineID = null; // String | ID of Engine
let opts = {
  'replaceEngineRequest': new AiwareJsClient.ReplaceEngineRequest() // ReplaceEngineRequest | Engine Instance Info
};
apiInstance.replaceEngine(engineID, opts, (error, data, response) => {
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
 **engineID** | [**String**](.md)| ID of Engine | 
 **replaceEngineRequest** | [**ReplaceEngineRequest**](ReplaceEngineRequest.md)| Engine Instance Info | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## resumeBuild

> AdminOperationResponse resumeBuild(buildID, opts)

This API resumes a build so that tasks based on this engine build will start running.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let buildID = null; // String | ID of Build
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.resumeBuild(buildID, opts, (error, data, response) => {
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
 **buildID** | [**String**](.md)| ID of Build | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## resumeEngine

> AdminOperationResponse resumeEngine(engineID, opts)

This API resumes a build so that tasks based on this engine build will start running.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineID = null; // String | ID of Engine
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'resumeEngineRequest': new AiwareJsClient.ResumeEngineRequest() // ResumeEngineRequest | Engine Instance Info
};
apiInstance.resumeEngine(engineID, opts, (error, data, response) => {
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
 **engineID** | [**String**](.md)| ID of Engine | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **resumeEngineRequest** | [**ResumeEngineRequest**](ResumeEngineRequest.md)| Engine Instance Info | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## terminateEngineInstance

> terminateEngineInstance(engineInstanceID, opts)

Delete the engine instance record

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineInstanceID = null; // String | ID of Engine Instance
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.terminateEngineInstance(engineInstanceID, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**String**](.md)| ID of Engine Instance | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

null (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## updateEngine

> UpdateEngineResponse updateEngine(engineID, updateEngineRequest, opts)

This API updates the specified engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineID = null; // String | ID of Engine
let updateEngineRequest = new AiwareJsClient.UpdateEngineRequest(); // UpdateEngineRequest | Update Engine
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateEngine(engineID, updateEngineRequest, opts, (error, data, response) => {
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
 **engineID** | [**String**](.md)| ID of Engine | 
 **updateEngineRequest** | [**UpdateEngineRequest**](UpdateEngineRequest.md)| Update Engine | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**UpdateEngineResponse**](UpdateEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateEngineBuild

> UpdateBuildResponse updateEngineBuild(engineID, buildID, buildDetail, opts)

This API updates the specified engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineID = null; // String | ID of Engine
let buildID = null; // String | ID of Build
let buildDetail = new AiwareJsClient.BuildDetail(); // BuildDetail | Update Engine BUild
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateEngineBuild(engineID, buildID, buildDetail, opts, (error, data, response) => {
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
 **engineID** | [**String**](.md)| ID of Engine | 
 **buildID** | [**String**](.md)| ID of Build | 
 **buildDetail** | [**BuildDetail**](BuildDetail.md)| Update Engine BUild | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**UpdateBuildResponse**](UpdateBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateEngineBuildState

> updateEngineBuildState(buildID, updateEngineBuildStateRequest, opts)

Update the Engine Build State

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let buildID = "buildID_example"; // String | BuildID of node-red container request
let updateEngineBuildStateRequest = new AiwareJsClient.UpdateEngineBuildStateRequest(); // UpdateEngineBuildStateRequest | Engine Build State
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateEngineBuildState(buildID, updateEngineBuildStateRequest, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
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


## updateEngineCategory

> UpdateEngineCategoryResponse updateEngineCategory(engineCategoryID, opts)

This updates the specified engine category

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineCategoryID = null; // String | ID of Engine Category
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateEngineCategory(engineCategoryID, opts, (error, data, response) => {
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
 **engineCategoryID** | [**String**](.md)| ID of Engine Category | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**UpdateEngineCategoryResponse**](UpdateEngineCategoryResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## updateEngineInstanceStatus

> updateEngineInstanceStatus(engineInstanceID, engineInstanceStatus, opts)

Update the Engine Instance Status.  Heartbeat to communicate back to controller both aggregated work and delta work from last heartbeat

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.EngineApi();
let engineInstanceID = null; // String | ID of Engine Instance
let engineInstanceStatus = new AiwareJsClient.EngineInstanceStatus(); // EngineInstanceStatus | Engine Instance Status
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateEngineInstanceStatus(engineInstanceID, engineInstanceStatus, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**String**](.md)| ID of Engine Instance | 
 **engineInstanceStatus** | [**EngineInstanceStatus**](EngineInstanceStatus.md)| Engine Instance Status | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

null (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

