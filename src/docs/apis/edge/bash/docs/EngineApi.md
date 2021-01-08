# EngineApi

All URIs are relative to */edge/v1*

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

This API creates a new engine build

### Example

```bash
aiware createBuild X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createBuildRequest** | [**CreateBuildRequest**](CreateBuildRequest.md) | The fields for an engine build |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**CreateBuildResponse**](CreateBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## createEngine

This API creates a new engine

### Example

```bash
aiware createEngine X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createEngineRequest** | [**CreateEngineRequest**](CreateEngineRequest.md) | The fields for an engine |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**CreateEngineResponse**](CreateEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## createEngineCategory

This API creates a new engine category

### Example

```bash
aiware createEngineCategory X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createEngineCategoryDetail** | [**CreateEngineCategoryDetail**](CreateEngineCategoryDetail.md) | The fields for an engine category |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**CreateEngineCategoryResponse**](CreateEngineCategoryResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deleteBuildPost

This API provides the engine detail result

### Example

```bash
aiware deleteBuildPost EngineID=value BuildID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**string**](.md) | ID of Engine | [default to null]
 **buildID** | [**string**](.md) | ID of Build | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deleteEnginePost

This API delets an engine

### Example

```bash
aiware deleteEnginePost EngineID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**string**](.md) | ID of Engine | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineBuild

This gets a particular build

### Example

```bash
aiware getEngineBuild BuildID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buildID** | [**string**](.md) | ID of Build | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetEngineBuildResponse**](GetEngineBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineBuilds

Get the list of builds deployed and available on aiWARE for a particular engine

### Example

```bash
aiware getEngineBuilds EngineID=value X-Correlation-Id:value  BuildState=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**string**](.md) | ID of Engine | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **buildState** | **string** | Filter builds by the build state | [optional] [default to null]

### Return type

[**GetEngineBuildsResponse**](GetEngineBuildsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineBuildsByState

The api returns engine build records by build state

### Example

```bash
aiware getEngineBuildsByState X-Correlation-Id:value  state=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **state** | **string** | Filter data by build state | [optional] [default to null]

### Return type

[**GetEngineBuildByStateResponse**](GetEngineBuildByStateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineCategories

This provides a list of engine categories

### Example

```bash
aiware getEngineCategories X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetEngineCategoriesResponse**](GetEngineCategoriesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineCategoryDetail

This provides detail for an engine category

### Example

```bash
aiware getEngineCategoryDetail EngineCategoryID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineCategoryID** | [**string**](.md) | ID of Engine Category | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetEngineCategoryDetailResponse**](GetEngineCategoryDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineContainerCount

Get engine container count

### Example

```bash
aiware getEngineContainerCount  interval=value  startTime=value  endTime=value  groupBy=value  engineID=value  hostID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **integer** | Interval in seconds for output time ranges. | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **groupBy** | [**EngineContainerGroupByEnum**](.md) | Group data by engineID or instance | [optional] [default to null]
 **engineID** | [**string**](.md) | Filter data by engineID | [optional] [default to null]
 **hostID** | [**string**](.md) | Filter data by hostID | [optional] [default to null]

### Return type

[**GetEngineContainerCountResponse**](GetEngineContainerCountResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineDetail

This API provides the engine detail result

### Example

```bash
aiware getEngineDetail EngineID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**string**](.md) | ID of Engine | [default to null]

### Return type

[**GetEngineDetailResponse**](GetEngineDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineInstanceDetail

Get information about an engine Instance

### Example

```bash
aiware getEngineInstanceDetail EngineInstanceID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**string**](.md) | ID of Engine Instance | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**EngineInstanceInfo**](EngineInstanceInfo.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineInstanceList

Get engines instances with filtering

### Example

```bash
aiware getEngineInstanceList X-Correlation-Id:value  engineInstanceIDs=value  engineIDs=value  hostIDs=value  workRequestIDs=value  status=value  drain=value  launchStartTime=value  launchEndTime=value  modifiedBefore=value  modifiedAfter=value  CreatedBefore=value  CreatedAfter=value  offset=value  limit=value  direction=value  orderBy=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **engineInstanceIDs** | **string** | Field to provide the input to get engine instances by ID list. Separated by commas | [optional] [default to null]
 **engineIDs** | **string** | Field to provide the input to get engines by Engine ID list. Separated by commas | [optional] [default to null]
 **hostIDs** | [**string**](.md) | Filtering engine instances by host IDs. Separated by commas | [optional] [default to null]
 **workRequestIDs** | [**string**](.md) | Filters engine instances by workrequest IDs. Separated by commas | [optional] [default to null]
 **status** | [**EngineStatusEnum**](.md) | Field to match the current status | [optional] [default to null]
 **drain** | **boolean** | Filter by drain | [optional] [default to null]
 **launchStartTime** | **integer** | The unix timestamp, describing a lower limit for the time an engine instance was launched. | [optional] [default to null]
 **launchEndTime** | **integer** | The unix timestamp, describing an upper limit for the time an engine instance was launched. | [optional] [default to null]
 **modifiedBefore** | **integer** | Filter by items modified before expressed as timestamp | [optional] [default to null]
 **modifiedAfter** | **integer** | Filter by items modified after expressed as timestamp | [optional] [default to null]
 **createdBefore** | **integer** | Filter items where created date is before this date | [optional] [default to null]
 **createdAfter** | **integer** | Filter items where created date is after this date | [optional] [default to null]
 **offset** | **integer** | the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **integer** | the number of items to return. | [optional] [default to 10]
 **direction** | **string** | the sort order.  ASC or DESC. | [optional] [default to DESC]
 **orderBy** | **string** | It should be in [engineID, hostID, status, createdTime, modifiedTime, lastUpdateTime, launchTime] | [optional] [default to null]

### Return type

[**GetEngineInstanceListResponse**](GetEngineInstanceListResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineInstanceLogs

Get engine instance logs as a zip file

### Example

```bash
aiware getEngineInstanceLogs EngineInstanceID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**string**](.md) | ID of Engine Instance | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

**binary**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/zip, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineInstanceStatus

Get the latest status of the engine instance

### Example

```bash
aiware getEngineInstanceStatus EngineInstanceID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**string**](.md) | ID of Engine Instance | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**EngineInstanceStatus**](EngineInstanceStatus.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineInstanceWork

Get a work request

### Example

```bash
aiware getEngineInstanceWork EngineInstanceID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**string**](.md) | ID of Engine Instance | [default to null]
 **engineInstanceWorkRequest** | [**EngineInstanceWorkRequest**](EngineInstanceWorkRequest.md) | Engine Instance Info |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**EngineInstanceWorkRequestResponse**](EngineInstanceWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineInstanceWorkDetail

Get detail of the work being done by the engine instance

### Example

```bash
aiware getEngineInstanceWorkDetail EngineInstanceID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**string**](.md) | ID of Engine Instance | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**EngineInstanceWorkDetailsResponse**](EngineInstanceWorkDetailsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineInstances

Get information about the instances of an engine

### Example

```bash
aiware getEngineInstances EngineID=value X-Correlation-Id:value  launchStartTime=value  launchEndTime=value  modifiedBefore=value  modifiedAfter=value  CreatedBefore=value  CreatedAfter=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | **string** | EngineID of node-red container request | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **launchStartTime** | **integer** | The unix timestamp, describing a lower limit for the time an engine instance was launched. | [optional] [default to null]
 **launchEndTime** | **integer** | The unix timestamp, describing an upper limit for the time an engine instance was launched. | [optional] [default to null]
 **modifiedBefore** | **integer** | Filter by items modified before expressed as timestamp | [optional] [default to null]
 **modifiedAfter** | **integer** | Filter by items modified after expressed as timestamp | [optional] [default to null]
 **createdBefore** | **integer** | Filter items where created date is before this date | [optional] [default to null]
 **createdAfter** | **integer** | Filter items where created date is after this date | [optional] [default to null]

### Return type

[**GetEngineInstancesResponse**](GetEngineInstancesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineLaunchDetail

This API returns the list of launches for this engine

### Example

```bash
aiware getEngineLaunchDetail EngineID=value LaunchID=value  CreatedBefore=value  CreatedAfter=value  offset=value  limit=value  orderBy=value  direction=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**string**](.md) | ID of Engine | [default to null]
 **launchID** | [**string**](.md) | ID of Launch | [default to null]
 **createdBefore** | **integer** | Filter items where created date is before this date | [optional] [default to null]
 **createdAfter** | **integer** | Filter items where created date is after this date | [optional] [default to null]
 **offset** | **integer** | the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **integer** | the number of items to return. | [optional] [default to 10]
 **orderBy** | **string** | the field to sort | [optional] [default to createdDateTime]
 **direction** | **string** | the sort order.  ASC or DESC. | [optional] [default to DESC]

### Return type

[**GetEngineLaunchResponse**](GetEngineLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngineLaunches

This API returns the list of launches for this engine

### Example

```bash
aiware getEngineLaunches EngineID=value  LaunchStatus=value  LaunchAction=value  CreatedBefore=value  CreatedAfter=value  offset=value  limit=value  orderBy=value  direction=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**string**](.md) | ID of Engine | [default to null]
 **launchStatus** | [**LaunchStatusEnum**](.md) | Field to match the current launch status | [optional] [default to null]
 **launchAction** | [**LaunchActionEnum**](.md) | Field to match the current launch action | [optional] [default to null]
 **createdBefore** | **integer** | Filter items where created date is before this date | [optional] [default to null]
 **createdAfter** | **integer** | Filter items where created date is after this date | [optional] [default to null]
 **offset** | **integer** | the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **integer** | the number of items to return. | [optional] [default to 10]
 **orderBy** | **string** | the field to sort | [optional] [default to createdDateTime]
 **direction** | **string** | the sort order.  ASC or DESC. | [optional] [default to DESC]

### Return type

[**GetEngineLaunchResponse**](GetEngineLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getEngines

Get the list of engines deployed and available on aiWARE

### Example

```bash
aiware getEngines X-Correlation-Id:value  internalOrganizationID=value  engineName=value  engineState=value  engineType=value  engineOutputType=value  engineCategoryID=value  engineIDs=value  offset=value  limit=value  direction=value  startTime=value  endTime=value  preload=value  orderBy=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **internalOrganizationID** | [**string**](.md) | ID of Organization.  UUID.  This ID is unique to this aiWARE installation. | [optional] [default to null]
 **engineName** | **string** | Field to string match against the engine names | [optional] [default to null]
 **engineState** | [**EngineStateEnum**](.md) | Field to match the current state | [optional] [default to null]
 **engineType** | [**EngineTypeEnum**](.md) | Field to match the current type | [optional] [default to null]
 **engineOutputType** | [**EngineTypeEnum**](.md) | Field to match the current type | [optional] [default to null]
 **engineCategoryID** | **string** | Filter to the particular engine category ID | [optional] [default to null]
 **engineIDs** | **string** | Field to provide the input to get engines by Engine ID list. Separated by commas | [optional] [default to null]
 **offset** | **integer** | the number of data to skip before getting the result set | [optional] [default to null]
 **limit** | **integer** | the number of items to return. | [optional] [default to 10]
 **direction** | **string** | the sort order.  ASC or DESC. | [optional] [default to DESC]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **preload** | **boolean** | Filter engines by preload | [optional] [default to null]
 **orderBy** | **string** | The value should be in [name, state, type, organizationID, createdTime] | [optional] [default to null]

### Return type

[**GetEnginesResponse**](GetEnginesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getJobsBacklogCountByEngine

Get backlog count by engine

### Example

```bash
aiware getJobsBacklogCountByEngine  interval=value  startTime=value  endTime=value  organizationIDs=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **integer** | Interval in seconds for output time ranges. | [optional] [default to null]
 **startTime** | **integer** | The unix timestamp, describing the start time for the stats | [optional] [default to null]
 **endTime** | **integer** | The unix timestamp, describing the end time for the stats | [optional] [default to null]
 **organizationIDs** | **string** |  | [optional] [default to null]

### Return type

[**GetJobsBacklogCountResponse**](GetJobsBacklogCountResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getResourcesForEngineInstance

Get resources for engine instance

### Example

```bash
aiware getResourcesForEngineInstance EngineInstanceID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**string**](.md) | ID of Engine Instance | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**GetResourcesForEngineInstanceResponse**](GetResourcesForEngineInstanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pauseBuild

This API pauses a build so that tasks based on this engine build will not run.

### Example

```bash
aiware pauseBuild BuildID=value X-Correlation-Id:value  BuildState=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buildID** | [**string**](.md) | ID of Build | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **buildState** | **string** | Filter builds by the build state | [optional] [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pauseEngine

This API pauses an engine so that tasks based on this engine will not run.

### Example

```bash
aiware pauseEngine EngineID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**string**](.md) | ID of Engine | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **pauseEngineRequest** | [**PauseEngineRequest**](PauseEngineRequest.md) | Engine Instance Info | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## registerEngineInstanceNoAuth

Register a new engine instance without authorization

### Example

```bash
aiware registerEngineInstanceNoAuth X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceInfo** | [**EngineInstanceInfo**](EngineInstanceInfo.md) | Engine Instance Info |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**EngineInstanceRegistrationInfo**](EngineInstanceRegistrationInfo.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## replaceEngine

This API replaced an engine so that tasks based on this engine will not run.

### Example

```bash
aiware replaceEngine EngineID=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**string**](.md) | ID of Engine | [default to null]
 **replaceEngineRequest** | [**ReplaceEngineRequest**](ReplaceEngineRequest.md) | Engine Instance Info | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## resumeBuild

This API resumes a build so that tasks based on this engine build will start running.

### Example

```bash
aiware resumeBuild BuildID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buildID** | [**string**](.md) | ID of Build | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## resumeEngine

This API resumes a build so that tasks based on this engine build will start running.

### Example

```bash
aiware resumeEngine EngineID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**string**](.md) | ID of Engine | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]
 **resumeEngineRequest** | [**ResumeEngineRequest**](ResumeEngineRequest.md) | Engine Instance Info | [optional]

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## terminateEngineInstance

Delete the engine instance record

### Example

```bash
aiware terminateEngineInstance EngineInstanceID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**string**](.md) | ID of Engine Instance | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

(empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateEngine

This API updates the specified engine

### Example

```bash
aiware updateEngine EngineID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**string**](.md) | ID of Engine | [default to null]
 **updateEngineRequest** | [**UpdateEngineRequest**](UpdateEngineRequest.md) | Update Engine |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**UpdateEngineResponse**](UpdateEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateEngineBuild

This API updates the specified engine

### Example

```bash
aiware updateEngineBuild EngineID=value BuildID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineID** | [**string**](.md) | ID of Engine | [default to null]
 **buildID** | [**string**](.md) | ID of Build | [default to null]
 **buildDetail** | [**BuildDetail**](BuildDetail.md) | Update Engine BUild |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**UpdateBuildResponse**](UpdateBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateEngineBuildState

Update the Engine Build State

### Example

```bash
aiware updateEngineBuildState BuildID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buildID** | **string** | BuildID of node-red container request | [default to null]
 **updateEngineBuildStateRequest** | [**UpdateEngineBuildStateRequest**](UpdateEngineBuildStateRequest.md) | Engine Build State |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

(empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateEngineCategory

This updates the specified engine category

### Example

```bash
aiware updateEngineCategory EngineCategoryID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineCategoryID** | [**string**](.md) | ID of Engine Category | [default to null]
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

[**UpdateEngineCategoryResponse**](UpdateEngineCategoryResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateEngineInstanceStatus

Update the Engine Instance Status.  Heartbeat to communicate back to controller both aggregated work and delta work from last heartbeat

### Example

```bash
aiware updateEngineInstanceStatus EngineInstanceID=value X-Correlation-Id:value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engineInstanceID** | [**string**](.md) | ID of Engine Instance | [default to null]
 **engineInstanceStatus** | [**EngineInstanceStatus**](EngineInstanceStatus.md) | Engine Instance Status |
 **xCorrelationId** | **string** | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] [default to null]

### Return type

(empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

