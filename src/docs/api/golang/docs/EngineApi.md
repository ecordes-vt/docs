# \EngineApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateBuild**](EngineApi.md#CreateBuild) | **Post** /admin/build/create | This API creates a new engine build
[**CreateEngine**](EngineApi.md#CreateEngine) | **Post** /admin/engine/create | This API creates a new engine
[**CreateEngineCategory**](EngineApi.md#CreateEngineCategory) | **Post** /admin/engine/category/create | This API creates a new engine category
[**DeleteBuildPost**](EngineApi.md#DeleteBuildPost) | **Post** /engine/{EngineID}/build/{BuildID}/delete | This API provides the engine detail result
[**DeleteEnginePost**](EngineApi.md#DeleteEnginePost) | **Post** /admin/engine/{EngineID}/delete | This API delets an engine
[**GetEngineBuild**](EngineApi.md#GetEngineBuild) | **Get** /admin/build/{BuildID}/detail | This gets a particular build
[**GetEngineBuilds**](EngineApi.md#GetEngineBuilds) | **Get** /admin/engine/{EngineID}/builds | Get the list of builds deployed and available on aiWARE for a particular engine
[**GetEngineBuildsByState**](EngineApi.md#GetEngineBuildsByState) | **Get** /engine/builds | The api returns engine build records by build state
[**GetEngineCategories**](EngineApi.md#GetEngineCategories) | **Get** /admin/engine/categories | This provides a list of engine categories
[**GetEngineCategoryDetail**](EngineApi.md#GetEngineCategoryDetail) | **Get** /admin/engine/category/{EngineCategoryID}/detail | This provides detail for an engine category
[**GetEngineContainerCount**](EngineApi.md#GetEngineContainerCount) | **Get** /engine/container_count | Get engine container count
[**GetEngineDetail**](EngineApi.md#GetEngineDetail) | **Get** /admin/engine/{EngineID}/detail | This API provides the engine detail result
[**GetEngineInstanceDetail**](EngineApi.md#GetEngineInstanceDetail) | **Get** /engine/instance/{EngineInstanceID}/detail | Get information about an engine Instance
[**GetEngineInstanceList**](EngineApi.md#GetEngineInstanceList) | **Get** /engine/instances | Get engines instances with filtering
[**GetEngineInstanceLogs**](EngineApi.md#GetEngineInstanceLogs) | **Get** /engine/instance/{EngineInstanceID}/logs | Get engine instance logs as a zip file
[**GetEngineInstanceStatus**](EngineApi.md#GetEngineInstanceStatus) | **Get** /engine/instance/{EngineInstanceID}/status | Get the latest status of the engine instance
[**GetEngineInstanceWork**](EngineApi.md#GetEngineInstanceWork) | **Post** /engine/instance/{EngineInstanceID}/getwork | Get a work request
[**GetEngineInstanceWorkDetail**](EngineApi.md#GetEngineInstanceWorkDetail) | **Get** /engine/instance/{EngineInstanceID}/workdetail | Get detail of the work being done by the engine instance
[**GetEngineInstances**](EngineApi.md#GetEngineInstances) | **Get** /engine/{EngineID}/instances | Get information about the instances of an engine
[**GetEngineLaunchDetail**](EngineApi.md#GetEngineLaunchDetail) | **Get** /engine/{EngineID}/launch/{LaunchID}/detail | This API returns the list of launches for this engine
[**GetEngineLaunches**](EngineApi.md#GetEngineLaunches) | **Get** /engine/{EngineID}/launches | This API returns the list of launches for this engine
[**GetEngines**](EngineApi.md#GetEngines) | **Get** /admin/engines | Get the list of engines deployed and available on aiWARE
[**GetJobsBacklogCountByEngine**](EngineApi.md#GetJobsBacklogCountByEngine) | **Post** /proc/jobs/backlog_count_by_engine | Get backlog count by engine
[**GetResourcesForEngineInstance**](EngineApi.md#GetResourcesForEngineInstance) | **Get** /engine/instance/{EngineInstanceID}/resources | Get resources for engine instance
[**PauseBuild**](EngineApi.md#PauseBuild) | **Post** /admin/build/{BuildID}/pause | This API pauses a build so that tasks based on this engine build will not run.
[**PauseEngine**](EngineApi.md#PauseEngine) | **Post** /admin/engine/{EngineID}/pause | This API pauses an engine so that tasks based on this engine will not run.
[**RegisterEngineInstanceNoAuth**](EngineApi.md#RegisterEngineInstanceNoAuth) | **Post** /engine/instance/register | Register a new engine instance without authorization
[**ReplaceEngine**](EngineApi.md#ReplaceEngine) | **Post** /admin/engine/{EngineID}/replace | This API replaced an engine so that tasks based on this engine will not run.
[**ResumeBuild**](EngineApi.md#ResumeBuild) | **Post** /admin/build/{BuildID}/resume | This API resumes a build so that tasks based on this engine build will start running.
[**ResumeEngine**](EngineApi.md#ResumeEngine) | **Post** /admin/engine/{EngineID}/resume | This API resumes a build so that tasks based on this engine build will start running.
[**TerminateEngineInstance**](EngineApi.md#TerminateEngineInstance) | **Post** /engine/instance/{EngineInstanceID}/terminate | Delete the engine instance record
[**UpdateEngine**](EngineApi.md#UpdateEngine) | **Post** /admin/engine/{EngineID}/update | This API updates the specified engine
[**UpdateEngineBuild**](EngineApi.md#UpdateEngineBuild) | **Post** /admin/build/{BuildID}/update | This API updates the specified engine
[**UpdateEngineBuildState**](EngineApi.md#UpdateEngineBuildState) | **Post** /engine/build/{BuildID}/state | Update the Engine Build State
[**UpdateEngineCategory**](EngineApi.md#UpdateEngineCategory) | **Post** /admin/engine/category/{EngineCategoryID}/update | This updates the specified engine category
[**UpdateEngineInstanceStatus**](EngineApi.md#UpdateEngineInstanceStatus) | **Post** /engine/instance/{EngineInstanceID}/updatestatus | Update the Engine Instance Status.  Heartbeat to communicate back to controller both aggregated work and delta work from last heartbeat



## CreateBuild

> CreateBuildResponse CreateBuild(ctx, createBuildRequest, optional)

This API creates a new engine build

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**createBuildRequest** | [**CreateBuildRequest**](CreateBuildRequest.md)| The fields for an engine build | 
 **optional** | ***CreateBuildOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateBuildOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**CreateBuildResponse**](CreateBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateEngine

> CreateEngineResponse CreateEngine(ctx, createEngineRequest, optional)

This API creates a new engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**createEngineRequest** | [**CreateEngineRequest**](CreateEngineRequest.md)| The fields for an engine | 
 **optional** | ***CreateEngineOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateEngineOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**CreateEngineResponse**](CreateEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateEngineCategory

> CreateEngineCategoryResponse CreateEngineCategory(ctx, createEngineCategoryDetail, optional)

This API creates a new engine category

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**createEngineCategoryDetail** | [**CreateEngineCategoryDetail**](CreateEngineCategoryDetail.md)| The fields for an engine category | 
 **optional** | ***CreateEngineCategoryOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateEngineCategoryOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**CreateEngineCategoryResponse**](CreateEngineCategoryResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteBuildPost

> AdminOperationResponse DeleteBuildPost(ctx, engineID, buildID, optional)

This API provides the engine detail result

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | [**string**](.md)| ID of Engine | 
**buildID** | [**string**](.md)| ID of Build | 
 **optional** | ***DeleteBuildPostOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteBuildPostOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteEnginePost

> AdminOperationResponse DeleteEnginePost(ctx, engineID, optional)

This API delets an engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | [**string**](.md)| ID of Engine | 
 **optional** | ***DeleteEnginePostOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteEnginePostOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineBuild

> GetEngineBuildResponse GetEngineBuild(ctx, buildID, optional)

This gets a particular build

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**buildID** | [**string**](.md)| ID of Build | 
 **optional** | ***GetEngineBuildOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineBuildOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetEngineBuildResponse**](GetEngineBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineBuilds

> GetEngineBuildsResponse GetEngineBuilds(ctx, engineID, optional)

Get the list of builds deployed and available on aiWARE for a particular engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | [**string**](.md)| ID of Engine | 
 **optional** | ***GetEngineBuildsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineBuildsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **buildState** | **optional.String**| Filter builds by the build state | 

### Return type

[**GetEngineBuildsResponse**](GetEngineBuildsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineBuildsByState

> GetEngineBuildByStateResponse GetEngineBuildsByState(ctx, optional)

The api returns engine build records by build state

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetEngineBuildsByStateOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineBuildsByStateOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **state** | **optional.String**| Filter data by build state | 

### Return type

[**GetEngineBuildByStateResponse**](GetEngineBuildByStateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineCategories

> GetEngineCategoriesResponse GetEngineCategories(ctx, optional)

This provides a list of engine categories

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetEngineCategoriesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineCategoriesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetEngineCategoriesResponse**](GetEngineCategoriesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineCategoryDetail

> GetEngineCategoryDetailResponse GetEngineCategoryDetail(ctx, engineCategoryID, optional)

This provides detail for an engine category

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineCategoryID** | [**string**](.md)| ID of Engine Category | 
 **optional** | ***GetEngineCategoryDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineCategoryDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetEngineCategoryDetailResponse**](GetEngineCategoryDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineContainerCount

> GetEngineContainerCountResponse GetEngineContainerCount(ctx, optional)

Get engine container count

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetEngineContainerCountOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineContainerCountOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **optional.Int64**| Interval in seconds for output time ranges. | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **groupBy** | [**optional.Interface of EngineContainerGroupByEnum**](.md)| Group data by engineID or instance | 
 **engineID** | [**optional.Interface of string**](.md)| Filter data by engineID | 
 **hostID** | [**optional.Interface of string**](.md)| Filter data by hostID | 

### Return type

[**GetEngineContainerCountResponse**](GetEngineContainerCountResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineDetail

> GetEngineDetailResponse GetEngineDetail(ctx, engineID)

This API provides the engine detail result

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | [**string**](.md)| ID of Engine | 

### Return type

[**GetEngineDetailResponse**](GetEngineDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineInstanceDetail

> EngineInstanceInfo GetEngineInstanceDetail(ctx, engineInstanceID, optional)

Get information about an engine Instance

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineInstanceID** | [**string**](.md)| ID of Engine Instance | 
 **optional** | ***GetEngineInstanceDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineInstanceDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**EngineInstanceInfo**](EngineInstanceInfo.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineInstanceList

> GetEngineInstanceListResponse GetEngineInstanceList(ctx, optional)

Get engines instances with filtering

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetEngineInstanceListOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineInstanceListOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **engineInstanceIDs** | **optional.String**| Field to provide the input to get engine instances by ID list. Separated by commas | 
 **engineIDs** | **optional.String**| Field to provide the input to get engines by Engine ID list. Separated by commas | 
 **hostIDs** | [**optional.Interface of string**](.md)| Filtering engine instances by host IDs. Separated by commas | 
 **workRequestIDs** | [**optional.Interface of string**](.md)| Filters engine instances by workrequest IDs. Separated by commas | 
 **status** | [**optional.Interface of EngineStatusEnum**](.md)| Field to match the current status | 
 **drain** | **optional.Bool**| Filter by drain | 
 **launchStartTime** | **optional.Int64**| The unix timestamp, describing a lower limit for the time an engine instance was launched. | 
 **launchEndTime** | **optional.Int64**| The unix timestamp, describing an upper limit for the time an engine instance was launched. | 
 **modifiedBefore** | **optional.Int64**| Filter by items modified before expressed as timestamp | 
 **modifiedAfter** | **optional.Int64**| Filter by items modified after expressed as timestamp | 
 **createdBefore** | **optional.Int64**| Filter items where created date is before this date | 
 **createdAfter** | **optional.Int64**| Filter items where created date is after this date | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **direction** | **optional.String**| the sort order.  ASC or DESC. | [default to DESC]
 **orderBy** | **optional.String**| It should be in [engineID, hostID, status, createdTime, modifiedTime, lastUpdateTime, launchTime] | 

### Return type

[**GetEngineInstanceListResponse**](GetEngineInstanceListResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineInstanceLogs

> *os.File GetEngineInstanceLogs(ctx, engineInstanceID, optional)

Get engine instance logs as a zip file

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineInstanceID** | [**string**](.md)| ID of Engine Instance | 
 **optional** | ***GetEngineInstanceLogsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineInstanceLogsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[***os.File**](*os.File.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/zip, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineInstanceStatus

> EngineInstanceStatus GetEngineInstanceStatus(ctx, engineInstanceID, optional)

Get the latest status of the engine instance

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineInstanceID** | [**string**](.md)| ID of Engine Instance | 
 **optional** | ***GetEngineInstanceStatusOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineInstanceStatusOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**EngineInstanceStatus**](EngineInstanceStatus.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineInstanceWork

> EngineInstanceWorkRequestResponse GetEngineInstanceWork(ctx, engineInstanceID, engineInstanceWorkRequest, optional)

Get a work request

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineInstanceID** | [**string**](.md)| ID of Engine Instance | 
**engineInstanceWorkRequest** | [**EngineInstanceWorkRequest**](EngineInstanceWorkRequest.md)| Engine Instance Info | 
 **optional** | ***GetEngineInstanceWorkOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineInstanceWorkOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**EngineInstanceWorkRequestResponse**](EngineInstanceWorkRequestResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineInstanceWorkDetail

> EngineInstanceWorkDetailsResponse GetEngineInstanceWorkDetail(ctx, engineInstanceID, optional)

Get detail of the work being done by the engine instance

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineInstanceID** | [**string**](.md)| ID of Engine Instance | 
 **optional** | ***GetEngineInstanceWorkDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineInstanceWorkDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**EngineInstanceWorkDetailsResponse**](EngineInstanceWorkDetailsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineInstances

> GetEngineInstancesResponse GetEngineInstances(ctx, engineID, optional)

Get information about the instances of an engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | **string**| EngineID of node-red container request | 
 **optional** | ***GetEngineInstancesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineInstancesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **launchStartTime** | **optional.Int64**| The unix timestamp, describing a lower limit for the time an engine instance was launched. | 
 **launchEndTime** | **optional.Int64**| The unix timestamp, describing an upper limit for the time an engine instance was launched. | 
 **modifiedBefore** | **optional.Int64**| Filter by items modified before expressed as timestamp | 
 **modifiedAfter** | **optional.Int64**| Filter by items modified after expressed as timestamp | 
 **createdBefore** | **optional.Int64**| Filter items where created date is before this date | 
 **createdAfter** | **optional.Int64**| Filter items where created date is after this date | 

### Return type

[**GetEngineInstancesResponse**](GetEngineInstancesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineLaunchDetail

> GetEngineLaunchResponse GetEngineLaunchDetail(ctx, engineID, launchID, optional)

This API returns the list of launches for this engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | [**string**](.md)| ID of Engine | 
**launchID** | [**string**](.md)| ID of Launch | 
 **optional** | ***GetEngineLaunchDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineLaunchDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **createdBefore** | **optional.Int64**| Filter items where created date is before this date | 
 **createdAfter** | **optional.Int64**| Filter items where created date is after this date | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **orderBy** | **optional.String**| the field to sort | [default to createdDateTime]
 **direction** | **optional.String**| the sort order.  ASC or DESC. | [default to DESC]

### Return type

[**GetEngineLaunchResponse**](GetEngineLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngineLaunches

> GetEngineLaunchResponse GetEngineLaunches(ctx, engineID, optional)

This API returns the list of launches for this engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | [**string**](.md)| ID of Engine | 
 **optional** | ***GetEngineLaunchesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEngineLaunchesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **launchStatus** | [**optional.Interface of LaunchStatusEnum**](.md)| Field to match the current launch status | 
 **launchAction** | [**optional.Interface of LaunchActionEnum**](.md)| Field to match the current launch action | 
 **createdBefore** | **optional.Int64**| Filter items where created date is before this date | 
 **createdAfter** | **optional.Int64**| Filter items where created date is after this date | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **orderBy** | **optional.String**| the field to sort | [default to createdDateTime]
 **direction** | **optional.String**| the sort order.  ASC or DESC. | [default to DESC]

### Return type

[**GetEngineLaunchResponse**](GetEngineLaunchResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEngines

> GetEnginesResponse GetEngines(ctx, optional)

Get the list of engines deployed and available on aiWARE

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetEnginesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEnginesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **internalOrganizationID** | [**optional.Interface of string**](.md)| ID of Organization.  UUID.  This ID is unique to this aiWARE installation. | 
 **engineName** | **optional.String**| Field to string match against the engine names | 
 **engineState** | [**optional.Interface of EngineStateEnum**](.md)| Field to match the current state | 
 **engineType** | [**optional.Interface of EngineTypeEnum**](.md)| Field to match the current type | 
 **engineOutputType** | [**optional.Interface of EngineTypeEnum**](.md)| Field to match the current type | 
 **engineCategoryID** | **optional.String**| Filter to the particular engine category ID | 
 **engineIDs** | **optional.String**| Field to provide the input to get engines by Engine ID list. Separated by commas | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **direction** | **optional.String**| the sort order.  ASC or DESC. | [default to DESC]
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **preload** | **optional.Bool**| Filter engines by preload | 
 **orderBy** | **optional.String**| The value should be in [name, state, type, organizationID, createdTime] | 

### Return type

[**GetEnginesResponse**](GetEnginesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetJobsBacklogCountByEngine

> GetJobsBacklogCountResponse GetJobsBacklogCountByEngine(ctx, optional)

Get backlog count by engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetJobsBacklogCountByEngineOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetJobsBacklogCountByEngineOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **interval** | **optional.Int64**| Interval in seconds for output time ranges. | 
 **startTime** | **optional.Int64**| The unix timestamp, describing the start time for the stats | 
 **endTime** | **optional.Int64**| The unix timestamp, describing the end time for the stats | 
 **organizationIDs** | **optional.String**|  | 

### Return type

[**GetJobsBacklogCountResponse**](GetJobsBacklogCountResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetResourcesForEngineInstance

> GetResourcesForEngineInstanceResponse GetResourcesForEngineInstance(ctx, engineInstanceID, optional)

Get resources for engine instance

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineInstanceID** | [**string**](.md)| ID of Engine Instance | 
 **optional** | ***GetResourcesForEngineInstanceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetResourcesForEngineInstanceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetResourcesForEngineInstanceResponse**](GetResourcesForEngineInstanceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PauseBuild

> AdminOperationResponse PauseBuild(ctx, buildID, optional)

This API pauses a build so that tasks based on this engine build will not run.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**buildID** | [**string**](.md)| ID of Build | 
 **optional** | ***PauseBuildOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a PauseBuildOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **buildState** | **optional.String**| Filter builds by the build state | 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PauseEngine

> AdminOperationResponse PauseEngine(ctx, engineID, optional)

This API pauses an engine so that tasks based on this engine will not run.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | [**string**](.md)| ID of Engine | 
 **optional** | ***PauseEngineOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a PauseEngineOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **pauseEngineRequest** | [**optional.Interface of PauseEngineRequest**](PauseEngineRequest.md)| Engine Instance Info | 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RegisterEngineInstanceNoAuth

> EngineInstanceRegistrationInfo RegisterEngineInstanceNoAuth(ctx, engineInstanceInfo, optional)

Register a new engine instance without authorization

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineInstanceInfo** | [**EngineInstanceInfo**](EngineInstanceInfo.md)| Engine Instance Info | 
 **optional** | ***RegisterEngineInstanceNoAuthOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a RegisterEngineInstanceNoAuthOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**EngineInstanceRegistrationInfo**](EngineInstanceRegistrationInfo.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ReplaceEngine

> AdminOperationResponse ReplaceEngine(ctx, engineID, optional)

This API replaced an engine so that tasks based on this engine will not run.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | [**string**](.md)| ID of Engine | 
 **optional** | ***ReplaceEngineOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a ReplaceEngineOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **replaceEngineRequest** | [**optional.Interface of ReplaceEngineRequest**](ReplaceEngineRequest.md)| Engine Instance Info | 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ResumeBuild

> AdminOperationResponse ResumeBuild(ctx, buildID, optional)

This API resumes a build so that tasks based on this engine build will start running.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**buildID** | [**string**](.md)| ID of Build | 
 **optional** | ***ResumeBuildOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a ResumeBuildOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ResumeEngine

> AdminOperationResponse ResumeEngine(ctx, engineID, optional)

This API resumes a build so that tasks based on this engine build will start running.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | [**string**](.md)| ID of Engine | 
 **optional** | ***ResumeEngineOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a ResumeEngineOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **resumeEngineRequest** | [**optional.Interface of ResumeEngineRequest**](ResumeEngineRequest.md)| Engine Instance Info | 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## TerminateEngineInstance

> TerminateEngineInstance(ctx, engineInstanceID, optional)

Delete the engine instance record

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineInstanceID** | [**string**](.md)| ID of Engine Instance | 
 **optional** | ***TerminateEngineInstanceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a TerminateEngineInstanceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

 (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateEngine

> UpdateEngineResponse UpdateEngine(ctx, engineID, updateEngineRequest, optional)

This API updates the specified engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | [**string**](.md)| ID of Engine | 
**updateEngineRequest** | [**UpdateEngineRequest**](UpdateEngineRequest.md)| Update Engine | 
 **optional** | ***UpdateEngineOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateEngineOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**UpdateEngineResponse**](UpdateEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateEngineBuild

> UpdateBuildResponse UpdateEngineBuild(ctx, engineID, buildID, buildDetail, optional)

This API updates the specified engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | [**string**](.md)| ID of Engine | 
**buildID** | [**string**](.md)| ID of Build | 
**buildDetail** | [**BuildDetail**](BuildDetail.md)| Update Engine BUild | 
 **optional** | ***UpdateEngineBuildOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateEngineBuildOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**UpdateBuildResponse**](UpdateBuildResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateEngineBuildState

> UpdateEngineBuildState(ctx, buildID, updateEngineBuildStateRequest, optional)

Update the Engine Build State

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**buildID** | **string**| BuildID of node-red container request | 
**updateEngineBuildStateRequest** | [**UpdateEngineBuildStateRequest**](UpdateEngineBuildStateRequest.md)| Engine Build State | 
 **optional** | ***UpdateEngineBuildStateOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateEngineBuildStateOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

 (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateEngineCategory

> UpdateEngineCategoryResponse UpdateEngineCategory(ctx, engineCategoryID, optional)

This updates the specified engine category

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineCategoryID** | [**string**](.md)| ID of Engine Category | 
 **optional** | ***UpdateEngineCategoryOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateEngineCategoryOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**UpdateEngineCategoryResponse**](UpdateEngineCategoryResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateEngineInstanceStatus

> UpdateEngineInstanceStatus(ctx, engineInstanceID, engineInstanceStatus, optional)

Update the Engine Instance Status.  Heartbeat to communicate back to controller both aggregated work and delta work from last heartbeat

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineInstanceID** | [**string**](.md)| ID of Engine Instance | 
**engineInstanceStatus** | [**EngineInstanceStatus**](EngineInstanceStatus.md)| Engine Instance Status | 
 **optional** | ***UpdateEngineInstanceStatusOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateEngineInstanceStatusOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

 (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

