# \AdminApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddEngineToResource**](AdminApi.md#AddEngineToResource) | **Post** /admin/resource/{ResourceID}/engine | This API adds the engine to the resource
[**AddServiceToResource**](AdminApi.md#AddServiceToResource) | **Post** /admin/resource/{ResourceID}/service | This API adds the service to the resource
[**AddserversServerType**](AdminApi.md#AddserversServerType) | **Post** /admin/server_type/{ServerTypeID}/add | This API add servers to the specified server type
[**AdminTerminateCluster**](AdminApi.md#AdminTerminateCluster) | **Post** /admin/terminate | This terminates the cluster
[**ApplyLicense**](AdminApi.md#ApplyLicense) | **Post** /admin/licenses/apply | This applies a license to aiWARE
[**CheckAuth**](AdminApi.md#CheckAuth) | **Post** /admin/auth | This check auth for a token
[**ClearBacklog**](AdminApi.md#ClearBacklog) | **Post** /admin/backlog/clear | This clears some or all of the currently queued tasks
[**CreateAdminApplication**](AdminApi.md#CreateAdminApplication) | **Post** /admin/applications/create | This creates a new application
[**CreateAdminCore**](AdminApi.md#CreateAdminCore) | **Post** /admin/cores/create | This creates a new core
[**CreateAdminOrganization**](AdminApi.md#CreateAdminOrganization) | **Post** /admin/organizations/create | This updates the config for the cluster for a given key
[**CreatePermission**](AdminApi.md#CreatePermission) | **Post** /admin/users/permission/create | This creates a new permission
[**CreateResource**](AdminApi.md#CreateResource) | **Post** /admin/resource/create | This API creates a new resource definition such as a database, nsq or redis DB.
[**CreateRole**](AdminApi.md#CreateRole) | **Post** /admin/users/role/create | This creates a new role
[**CreateServerType**](AdminApi.md#CreateServerType) | **Post** /admin/server_types/create | This creates a new server type
[**CreateServerTypeEngineRunning**](AdminApi.md#CreateServerTypeEngineRunning) | **Post** /admin/server_types/running_engine/create | This creates a new server_type_engine_running
[**CreateService**](AdminApi.md#CreateService) | **Post** /admin/service/create | This API creates a new service definition.
[**CreateToken**](AdminApi.md#CreateToken) | **Post** /admin/tokens/create | This creates a new token
[**CreateUser**](AdminApi.md#CreateUser) | **Post** /admin/users/create | This creates a new user
[**DeleteApplication**](AdminApi.md#DeleteApplication) | **Post** /admin/applications/{ApplicationID}/delete | This deletes an application
[**DeleteLicense**](AdminApi.md#DeleteLicense) | **Delete** /admin/licenses/{LicenseID}/delete | This deletes a license from aiWARE
[**DeleteResource**](AdminApi.md#DeleteResource) | **Post** /admin/resource/{ResourceID}/delete | This deletes the specified resource
[**DeleteRole**](AdminApi.md#DeleteRole) | **Post** /admin/users/role/{RoleID}/delete | This deletes a role
[**DeleteServerType**](AdminApi.md#DeleteServerType) | **Delete** /admin/server_type/{ServerTypeID}/delete | This API deletes the specified server type
[**DeleteServerTypePost**](AdminApi.md#DeleteServerTypePost) | **Post** /admin/server_type/{ServerTypeID}/delete | This API deletes the specified server type
[**DeleteServerTypeRunningEngine**](AdminApi.md#DeleteServerTypeRunningEngine) | **Delete** /admin/server_type/{ServerTypeID}/engine/{EngineID}/delete | This API deletes the running engine for a server type
[**DeleteToken**](AdminApi.md#DeleteToken) | **Post** /admin/token/{TokenID}/delete | This deletes a token
[**DeleteUser**](AdminApi.md#DeleteUser) | **Post** /admin/user/{UserID}/delete | This deletes a user
[**DesiredserversServerType**](AdminApi.md#DesiredserversServerType) | **Post** /admin/server_type/{ServerTypeID}/desired | This API add servers to the specified server type
[**GetAdminApplicationDetail**](AdminApi.md#GetAdminApplicationDetail) | **Get** /admin/applications/{ApplicationID}/detail | This provides information on the given application.
[**GetAdminCoreDetail**](AdminApi.md#GetAdminCoreDetail) | **Get** /admin/core/{CoreID}/detail | This provides information on the given core.
[**GetAdminCores**](AdminApi.md#GetAdminCores) | **Get** /admin/cores | This provides a list of core systems
[**GetAdminEngineConfigSectionKey**](AdminApi.md#GetAdminEngineConfigSectionKey) | **Get** /admin/engine/{EngineID}/config/{ConfigSection}/{ConfigKey} | This provides a config section key for the engine
[**GetAdminOrganizationDetail**](AdminApi.md#GetAdminOrganizationDetail) | **Get** /admin/organization/{OrganizationID}/detail | This gets organization detail by ID
[**GetAdminOrganizationTokens**](AdminApi.md#GetAdminOrganizationTokens) | **Get** /admin/organization/{OrganizationID}/tokens | This provides information on the given organization tokens.
[**GetAdminOrganizations**](AdminApi.md#GetAdminOrganizations) | **Get** /admin/organizations | This provides a list of organizations
[**GetAdminPermissionDetail**](AdminApi.md#GetAdminPermissionDetail) | **Get** /admin/users/permission/{PermissionID}/detail | This gets permission detail by ID
[**GetAdminRoleDetail**](AdminApi.md#GetAdminRoleDetail) | **Get** /admin/users/role/{RoleID}/detail | This gets role detail by ID
[**GetAdminServiceConfig**](AdminApi.md#GetAdminServiceConfig) | **Get** /admin/service/{ServiceID}/config | This provides all the config for the service
[**GetAdminServiceConfigSection**](AdminApi.md#GetAdminServiceConfigSection) | **Get** /admin/service/{ServiceID}/config/{ConfigSection} | This provides all the config for the service
[**GetAdminServiceConfigSectionKey**](AdminApi.md#GetAdminServiceConfigSectionKey) | **Get** /admin/service/{ServiceID}/config/{ConfigSection}/{ConfigKey} | This provides a config section key for the service
[**GetAdminServiceInstances**](AdminApi.md#GetAdminServiceInstances) | **Get** /admin/service/instances | This lists the service instances available for a system
[**GetAdminStatus**](AdminApi.md#GetAdminStatus) | **Get** /admin/status | This provides information on the status of the aiWARE edge
[**GetAdminTokenDetail**](AdminApi.md#GetAdminTokenDetail) | **Get** /admin/token/{TokenID}/detail | Get the token info by ID
[**GetAdminTokenPermissions**](AdminApi.md#GetAdminTokenPermissions) | **Get** /admin/token/{TokenID}/permissions | This provides a list of all token permissions for a token by TokenID
[**GetAdminTokens**](AdminApi.md#GetAdminTokens) | **Get** /admin/tokens | This provides information about all tokens.
[**GetAdminUserDetail**](AdminApi.md#GetAdminUserDetail) | **Get** /admin/user/{UserID}/detail | This provides information on the given user.
[**GetAdminUserPermissions**](AdminApi.md#GetAdminUserPermissions) | **Get** /admin/user/{UserID}/permissions | This provides a list of all user permissions for an user by UserID
[**GetAdminUserTokens**](AdminApi.md#GetAdminUserTokens) | **Get** /admin/user/{UserID}/tokens | This provides information on the given user.
[**GetAdminUsers**](AdminApi.md#GetAdminUsers) | **Get** /admin/users | This provides a list of users in the system
[**GetAdminUsersPermission**](AdminApi.md#GetAdminUsersPermission) | **Get** /admin/users/permissions | This provides a list of all user permissions in the system
[**GetAdminUsersRoles**](AdminApi.md#GetAdminUsersRoles) | **Get** /admin/users/roles | This provides a list of user role in the system
[**GetApplications**](AdminApi.md#GetApplications) | **Get** /admin/applications | Get the list of applications deployed and available on aiWARE
[**GetBacklogSummary**](AdminApi.md#GetBacklogSummary) | **Get** /admin/backlog/summary | This provides summary information on the current backlog
[**GetConfig**](AdminApi.md#GetConfig) | **Get** /admin/config | This provides all the config for the cluster
[**GetConfigSection**](AdminApi.md#GetConfigSection) | **Get** /admin/config/{ConfigSection} | This provides all the config for the cluster
[**GetConfigSectionKey**](AdminApi.md#GetConfigSectionKey) | **Get** /admin/config/{ConfigSection}/{ConfigKey} | This provides a config section key for the cluster
[**GetEnginesForResource**](AdminApi.md#GetEnginesForResource) | **Get** /admin/resource/{ResourceID}/engines | Get list of engines for resource
[**GetLicenseDetail**](AdminApi.md#GetLicenseDetail) | **Get** /admin/licenses/{LicenseID}/detail | This gets detail on a license key
[**GetLicenses**](AdminApi.md#GetLicenses) | **Get** /admin/licenses | This provides a licenses on the system
[**GetResource**](AdminApi.md#GetResource) | **Get** /admin/resource/{ResourceID} | Get a resource definition
[**GetResources**](AdminApi.md#GetResources) | **Get** /admin/resources | Get the list of resources
[**GetResourcesForEngine**](AdminApi.md#GetResourcesForEngine) | **Get** /admin/engine/{EngineID}/resources | Get list of resources for engine
[**GetResourcesForHost**](AdminApi.md#GetResourcesForHost) | **Get** /admin/host/{HostID}/resources | Get list of resources for host
[**GetResourcesForService**](AdminApi.md#GetResourcesForService) | **Get** /admin/service/{ServiceID}/resources | Get list of resources for service
[**GetServerType**](AdminApi.md#GetServerType) | **Get** /admin/server_type/{ServerTypeID}/detail | This provides detail on the server type
[**GetServerTypeEngineRunning**](AdminApi.md#GetServerTypeEngineRunning) | **Get** /admin/server_types/running_engines | This lists the running engine with server types
[**GetServerTypeEngineRunningDetail**](AdminApi.md#GetServerTypeEngineRunningDetail) | **Get** /admin/server_type/{ServerTypeID}/engine/{EngineID}/detail | This gets the detail of server type - running engine
[**GetServerTypes**](AdminApi.md#GetServerTypes) | **Get** /admin/server_types | This lists the server types available on the system
[**GetServices**](AdminApi.md#GetServices) | **Get** /admin/services | This lists the services available on the system
[**LoginUser**](AdminApi.md#LoginUser) | **Post** /admin/users/login | This logs a user in if successful
[**OauthLoginUser**](AdminApi.md#OauthLoginUser) | **Post** /admin/users/oauth2_login | This logs a user in if successful with OAuth2
[**RegisterUser**](AdminApi.md#RegisterUser) | **Post** /admin/users/register | This registers a new user
[**RemoveEngineForResource**](AdminApi.md#RemoveEngineForResource) | **Post** /admin/resource/{ResourceID}/engine/{EngineID}/delete | This API removes the engine to the resource
[**RemoveserversServerType**](AdminApi.md#RemoveserversServerType) | **Post** /admin/server_type/{ServerTypeID}/remove | This API removes servers from the specified server type
[**ResetAllocTable**](AdminApi.md#ResetAllocTable) | **Post** /admin/backlog/reset-alloc | This resets the alloc table
[**UpdateApplication**](AdminApi.md#UpdateApplication) | **Post** /admin/applications/{ApplicationID}/update | This updates an application
[**UpdateConfigAll**](AdminApi.md#UpdateConfigAll) | **Post** /admin/config | This gets the config for the cluster
[**UpdateConfigSection**](AdminApi.md#UpdateConfigSection) | **Post** /admin/config/{ConfigSection} | This gets the config for the cluster
[**UpdateConfigSectionKey**](AdminApi.md#UpdateConfigSectionKey) | **Post** /admin/config/{ConfigSection}/{ConfigKey} | This updates the config for the cluster for a given key
[**UpdateEnginesForResource**](AdminApi.md#UpdateEnginesForResource) | **Post** /admin/resource/{ResourceID}/engine/update | This API updates the specified server type-running engine
[**UpdateOrganization**](AdminApi.md#UpdateOrganization) | **Post** /admin/organization/{OrganizationID}/update | This updates a organization
[**UpdatePermission**](AdminApi.md#UpdatePermission) | **Post** /admin/users/permission/{PermissionID}/update | This updates a permission
[**UpdateResource**](AdminApi.md#UpdateResource) | **Post** /admin/resource/{ResourceID}/update | This API updates the specified resource
[**UpdateResourceState**](AdminApi.md#UpdateResourceState) | **Post** /admin/resource/{ResourceID}/updatestate | This API updates the state of the specified resource
[**UpdateRole**](AdminApi.md#UpdateRole) | **Post** /admin/users/role/{RoleID}/update | This updates a role
[**UpdateServerType**](AdminApi.md#UpdateServerType) | **Post** /admin/server_type/{ServerTypeID}/update | This API updates the specified server type
[**UpdateServerTypeEngineRunning**](AdminApi.md#UpdateServerTypeEngineRunning) | **Post** /admin/server_type/{ServerTypeID}/engine/{EngineID}/update | This API updates the specified server type-running engine
[**UpdateToken**](AdminApi.md#UpdateToken) | **Post** /admin/token/{TokenID}/update | This updates a token
[**UpdateUser**](AdminApi.md#UpdateUser) | **Post** /admin/user/{UserID}/update | This updates a user
[**UserPasswordForgot**](AdminApi.md#UserPasswordForgot) | **Post** /admin/users/password/forgot | This api will help users to reset their password when they forgot
[**UserPasswordReset**](AdminApi.md#UserPasswordReset) | **Post** /admin/users/password/reset | Helps users to reset their password
[**UserPasswordUpdate**](AdminApi.md#UserPasswordUpdate) | **Post** /admin/users/password/update | This api will help users to update their password



## AddEngineToResource

> AddEngineForResourceResponse AddEngineToResource(ctx, resourceID, optional)

This API adds the engine to the resource

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**resourceID** | [**string**](.md)| ID of Resource | 
 **optional** | ***AddEngineToResourceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a AddEngineToResourceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **addEngineForResourceRequest** | [**optional.Interface of AddEngineForResourceRequest**](AddEngineForResourceRequest.md)| Add Engine Mapping for Resource | 

### Return type

[**AddEngineForResourceResponse**](AddEngineForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## AddServiceToResource

> AddServiceForResourceResponse AddServiceToResource(ctx, resourceID, optional)

This API adds the service to the resource

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**resourceID** | [**string**](.md)| ID of Resource | 
 **optional** | ***AddServiceToResourceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a AddServiceToResourceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **addServiceForResourceRequest** | [**optional.Interface of AddServiceForResourceRequest**](AddServiceForResourceRequest.md)| Add Service Mapping for Resource | 

### Return type

[**AddServiceForResourceResponse**](AddServiceForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## AddserversServerType

> AdminOperationResponse AddserversServerType(ctx, serverTypeID, optional)

This API add servers to the specified server type

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serverTypeID** | [**string**](.md)| ID of Server Type | 
 **optional** | ***AddserversServerTypeOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a AddserversServerTypeOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **addServersToServerTypeRequest** | [**optional.Interface of AddServersToServerTypeRequest**](AddServersToServerTypeRequest.md)| Add Servers Server Type | 

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


## AdminTerminateCluster

> AdminTerminateCluster(ctx, optional)

This terminates the cluster

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***AdminTerminateClusterOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a AdminTerminateClusterOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **adminOperationRequest** | [**optional.Interface of AdminOperationRequest**](AdminOperationRequest.md)| ClusterID | 

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


## ApplyLicense

> LicenseDetail ApplyLicense(ctx, optional)

This applies a license to aiWARE

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***ApplyLicenseOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a ApplyLicenseOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **createLicenseDetail** | [**optional.Interface of CreateLicenseDetail**](CreateLicenseDetail.md)|  | 

### Return type

[**LicenseDetail**](LicenseDetail.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CheckAuth

> AdminAuthResponse CheckAuth(ctx, adminAuthRequest, optional)

This check auth for a token

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**adminAuthRequest** | [**AdminAuthRequest**](AdminAuthRequest.md)| The input for check auth | 
 **optional** | ***CheckAuthOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CheckAuthOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminAuthResponse**](AdminAuthResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ClearBacklog

> AdminCoreCreateResponse ClearBacklog(ctx, optional)

This clears some or all of the currently queued tasks

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***ClearBacklogOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a ClearBacklogOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **status** | [**optional.Interface of EngineStatusEnum**](.md)| Field to match the current status | 
 **engineID** | **optional.String**| Filter by engine id | 
 **modifiedBefore** | **optional.Int64**| Filter by items modified before expressed as timestamp | 
 **modifiedAfter** | **optional.Int64**| Filter by items modified after expressed as timestamp | 
 **createdBefore** | **optional.Int64**| Filter items where created date is before this date | 
 **createdAfter** | **optional.Int64**| Filter items where created date is after this date | 

### Return type

[**AdminCoreCreateResponse**](AdminCoreCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateAdminApplication

> AdminApplicationCreateResponse CreateAdminApplication(ctx, adminApplicationCreateRequest, optional)

This creates a new application

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**adminApplicationCreateRequest** | [**AdminApplicationCreateRequest**](AdminApplicationCreateRequest.md)| The input for createApplication | 
 **optional** | ***CreateAdminApplicationOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateAdminApplicationOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminApplicationCreateResponse**](AdminApplicationCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateAdminCore

> AdminCoreCreateResponse CreateAdminCore(ctx, adminCoreCreateRequest, optional)

This creates a new core

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**adminCoreCreateRequest** | [**AdminCoreCreateRequest**](AdminCoreCreateRequest.md)| The input for createCor | 
 **optional** | ***CreateAdminCoreOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateAdminCoreOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminCoreCreateResponse**](AdminCoreCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateAdminOrganization

> AdminOrganizationCreateResponse CreateAdminOrganization(ctx, adminOrganizationCreateRequest, optional)

This updates the config for the cluster for a given key

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**adminOrganizationCreateRequest** | [**AdminOrganizationCreateRequest**](AdminOrganizationCreateRequest.md)| The input for createOrganization | 
 **optional** | ***CreateAdminOrganizationOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateAdminOrganizationOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminOrganizationCreateResponse**](AdminOrganizationCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreatePermission

> AdminPermissionCreateResponse CreatePermission(ctx, adminPermissionCreateRequest, optional)

This creates a new permission

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**adminPermissionCreateRequest** | [**AdminPermissionCreateRequest**](AdminPermissionCreateRequest.md)| The input for createPermission | 
 **optional** | ***CreatePermissionOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreatePermissionOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminPermissionCreateResponse**](AdminPermissionCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateResource

> CreateResourceResponse CreateResource(ctx, createResourceRequest, optional)

This API creates a new resource definition such as a database, nsq or redis DB.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**createResourceRequest** | [**CreateResourceRequest**](CreateResourceRequest.md)| The fields for a resource definition | 
 **optional** | ***CreateResourceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateResourceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**CreateResourceResponse**](CreateResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateRole

> AdminRoleCreateResponse CreateRole(ctx, adminRoleCreateRequest, optional)

This creates a new role

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**adminRoleCreateRequest** | [**AdminRoleCreateRequest**](AdminRoleCreateRequest.md)| The input for createRole | 
 **optional** | ***CreateRoleOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateRoleOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminRoleCreateResponse**](AdminRoleCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateServerType

> CreateServerTypeResponse CreateServerType(ctx, createServerTypeRequest, optional)

This creates a new server type

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**createServerTypeRequest** | [**CreateServerTypeRequest**](CreateServerTypeRequest.md)| The input for createServerType | 
 **optional** | ***CreateServerTypeOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateServerTypeOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**CreateServerTypeResponse**](CreateServerTypeResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateServerTypeEngineRunning

> CreateServerTypeEngineRunningResponse CreateServerTypeEngineRunning(ctx, createServerTypeEngineRunningRequest, optional)

This creates a new server_type_engine_running

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**createServerTypeEngineRunningRequest** | [**CreateServerTypeEngineRunningRequest**](CreateServerTypeEngineRunningRequest.md)| The input for createServerTypeEngineRunning | 
 **optional** | ***CreateServerTypeEngineRunningOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateServerTypeEngineRunningOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**CreateServerTypeEngineRunningResponse**](CreateServerTypeEngineRunningResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateService

> CreateServiceResponse CreateService(ctx, createServiceRequest, optional)

This API creates a new service definition.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**createServiceRequest** | [**CreateServiceRequest**](CreateServiceRequest.md)| The fields for a service definition | 
 **optional** | ***CreateServiceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateServiceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**CreateServiceResponse**](CreateServiceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateToken

> AdminTokenCreateResponse CreateToken(ctx, adminTokenCreateRequest, optional)

This creates a new token

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**adminTokenCreateRequest** | [**AdminTokenCreateRequest**](AdminTokenCreateRequest.md)| The input for createToken | 
 **optional** | ***CreateTokenOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateTokenOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminTokenCreateResponse**](AdminTokenCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateUser

> AdminUserCreateResponse CreateUser(ctx, adminUserCreateRequest, optional)

This creates a new user

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**adminUserCreateRequest** | [**AdminUserCreateRequest**](AdminUserCreateRequest.md)| The input for createUser | 
 **optional** | ***CreateUserOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateUserOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminUserCreateResponse**](AdminUserCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteApplication

> AdminApplicationDeleteResponse DeleteApplication(ctx, applicationID, optional)

This deletes an application

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**applicationID** | [**string**](.md)| ID of Application | 
 **optional** | ***DeleteApplicationOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteApplicationOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminApplicationDeleteResponse**](AdminApplicationDeleteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteLicense

> AdminOperationResponse DeleteLicense(ctx, licenseID, optional)

This deletes a license from aiWARE

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**licenseID** | **string**| License ID | 
 **optional** | ***DeleteLicenseOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteLicenseOpts struct


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


## DeleteResource

> AdminOperationResponse DeleteResource(ctx, resourceID, optional)

This deletes the specified resource

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**resourceID** | [**string**](.md)| ID of Resource | 
 **optional** | ***DeleteResourceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteResourceOpts struct


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


## DeleteRole

> AdminRoleDeleteResponse DeleteRole(ctx, roleID, optional)

This deletes a role

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**roleID** | [**string**](.md)| ID of Role | 
 **optional** | ***DeleteRoleOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteRoleOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminRoleDeleteResponse**](AdminRoleDeleteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteServerType

> AdminOperationResponse DeleteServerType(ctx, serverTypeID, optional)

This API deletes the specified server type

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serverTypeID** | [**string**](.md)| ID of Server Type | 
 **optional** | ***DeleteServerTypeOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteServerTypeOpts struct


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


## DeleteServerTypePost

> AdminOperationResponse DeleteServerTypePost(ctx, serverTypeID, optional)

This API deletes the specified server type

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serverTypeID** | [**string**](.md)| ID of Server Type | 
 **optional** | ***DeleteServerTypePostOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteServerTypePostOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **deleteServerTypeRequest** | [**optional.Interface of DeleteServerTypeRequest**](DeleteServerTypeRequest.md)| Engine Instance Info | 

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


## DeleteServerTypeRunningEngine

> AdminOperationResponse DeleteServerTypeRunningEngine(ctx, serverTypeID, engineID, optional)

This API deletes the running engine for a server type

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serverTypeID** | [**string**](.md)| ID of Server Type | 
**engineID** | [**string**](.md)| ID of Engine | 
 **optional** | ***DeleteServerTypeRunningEngineOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteServerTypeRunningEngineOpts struct


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


## DeleteToken

> AdminTokenDeleteResponse DeleteToken(ctx, tokenID, optional)

This deletes a token

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**tokenID** | [**string**](.md)| ID of Token | 
 **optional** | ***DeleteTokenOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteTokenOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminTokenDeleteResponse**](AdminTokenDeleteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteUser

> AdminUserDeleteResponse DeleteUser(ctx, userID, optional)

This deletes a user

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userID** | [**string**](.md)| ID of User | 
 **optional** | ***DeleteUserOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DeleteUserOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminUserDeleteResponse**](AdminUserDeleteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DesiredserversServerType

> AdminOperationResponse DesiredserversServerType(ctx, serverTypeID, optional)

This API add servers to the specified server type

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serverTypeID** | [**string**](.md)| ID of Server Type | 
 **optional** | ***DesiredserversServerTypeOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a DesiredserversServerTypeOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **desiredServersToServerTypeRequest** | [**optional.Interface of DesiredServersToServerTypeRequest**](DesiredServersToServerTypeRequest.md)| Set Servers for Server Type | 

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


## GetAdminApplicationDetail

> AdminApplicationGetDetailResponse GetAdminApplicationDetail(ctx, applicationID, optional)

This provides information on the given application.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**applicationID** | [**string**](.md)| ID of Application | 
 **optional** | ***GetAdminApplicationDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminApplicationDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminApplicationGetDetailResponse**](AdminApplicationGetDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminCoreDetail

> AdminCoreGetDetailResponse GetAdminCoreDetail(ctx, coreID, optional)

This provides information on the given core.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**coreID** | [**string**](.md)| ID of Core | 
 **optional** | ***GetAdminCoreDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminCoreDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminCoreGetDetailResponse**](AdminCoreGetDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminCores

> GetCoresResponse GetAdminCores(ctx, optional)

This provides a list of core systems

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetAdminCoresOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminCoresOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetCoresResponse**](GetCoresResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminEngineConfigSectionKey

> AdminEngineConfigSectionKeyResponse GetAdminEngineConfigSectionKey(ctx, engineID, configSection, configKey, optional)

This provides a config section key for the engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | **string**| EngineID of node-red container request | 
**configSection** | **string**| Config Section Entry | 
**configKey** | **string**| Config Key | 
 **optional** | ***GetAdminEngineConfigSectionKeyOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminEngineConfigSectionKeyOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminEngineConfigSectionKeyResponse**](AdminEngineConfigSectionKeyResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/csv, text/html, text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminOrganizationDetail

> AdminOrganizationGetDetailResponse GetAdminOrganizationDetail(ctx, organizationID, optional)

This gets organization detail by ID

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**organizationID** | [**string**](.md)| ID of Organization | 
 **optional** | ***GetAdminOrganizationDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminOrganizationDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminOrganizationGetDetailResponse**](AdminOrganizationGetDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminOrganizationTokens

> AdminOrganizationGetTokensResponse GetAdminOrganizationTokens(ctx, organizationID, optional)

This provides information on the given organization tokens.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**organizationID** | [**string**](.md)| ID of Organization | 
 **optional** | ***GetAdminOrganizationTokensOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminOrganizationTokensOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminOrganizationGetTokensResponse**](AdminOrganizationGetTokensResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminOrganizations

> AdminOrganizationsGetResponse GetAdminOrganizations(ctx, optional)

This provides a list of organizations

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetAdminOrganizationsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminOrganizationsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **organizationID** | [**optional.Interface of string**](.md)| Filter by organizationID | 
 **organizationName** | **optional.String**| Filter by organizationName | 
 **orderBy** | **optional.String**| The value should be in [organizationName, organizationID, createdTime, basePriority] | 

### Return type

[**AdminOrganizationsGetResponse**](AdminOrganizationsGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminPermissionDetail

> AdminPermissionDetailResponse GetAdminPermissionDetail(ctx, permissionID, optional)

This gets permission detail by ID

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**permissionID** | [**string**](.md)| ID of Permission | 
 **optional** | ***GetAdminPermissionDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminPermissionDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminPermissionDetailResponse**](AdminPermissionDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminRoleDetail

> AdminRoleDetailResponse GetAdminRoleDetail(ctx, roleID, optional)

This gets role detail by ID

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**roleID** | [**string**](.md)| ID of Role | 
 **optional** | ***GetAdminRoleDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminRoleDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminRoleDetailResponse**](AdminRoleDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminServiceConfig

> AdminServiceConfigResponse GetAdminServiceConfig(ctx, serviceID, optional)

This provides all the config for the service

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serviceID** | [**string**](.md)| ID of the service | 
 **optional** | ***GetAdminServiceConfigOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminServiceConfigOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **configKey** | **optional.String**| Config Key | 

### Return type

[**AdminServiceConfigResponse**](AdminServiceConfigResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminServiceConfigSection

> AdminServiceConfigSectionResponse GetAdminServiceConfigSection(ctx, serviceID, configSection, optional)

This provides all the config for the service

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serviceID** | [**string**](.md)| ID of the service | 
**configSection** | **string**| Config Section Entry | 
 **optional** | ***GetAdminServiceConfigSectionOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminServiceConfigSectionOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminServiceConfigSectionResponse**](AdminServiceConfigSectionResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminServiceConfigSectionKey

> AdminServiceConfigSectionKeyResponse GetAdminServiceConfigSectionKey(ctx, serviceID, configSection, configKey, optional)

This provides a config section key for the service

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serviceID** | [**string**](.md)| ID of the service | 
**configSection** | **string**| Config Section Entry | 
**configKey** | **string**| Config Key | 
 **optional** | ***GetAdminServiceConfigSectionKeyOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminServiceConfigSectionKeyOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminServiceConfigSectionKeyResponse**](AdminServiceConfigSectionKeyResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/csv, text/html, text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminServiceInstances

> GetAdminServiceInstancesResponse GetAdminServiceInstances(ctx, optional)

This lists the service instances available for a system

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetAdminServiceInstancesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminServiceInstancesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetAdminServiceInstancesResponse**](GetAdminServiceInstancesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminStatus

> EngineInstanceInfo GetAdminStatus(ctx, optional)

This provides information on the status of the aiWARE edge

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetAdminStatusOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminStatusOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **format** | [**optional.Interface of StatusFormatEnum**](.md)| If specified, this limits the jobs or tasks to follow status | 
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**EngineInstanceInfo**](EngineInstanceInfo.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/csv, text/html, text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminTokenDetail

> TokenDetail GetAdminTokenDetail(ctx, tokenID, optional)

Get the token info by ID

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**tokenID** | [**string**](.md)| ID of Token | 
 **optional** | ***GetAdminTokenDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminTokenDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**TokenDetail**](TokenDetail.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminTokenPermissions

> AdminTokenPermissionsGetResponse GetAdminTokenPermissions(ctx, tokenID, optional)

This provides a list of all token permissions for a token by TokenID

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**tokenID** | [**string**](.md)| ID of Token | 
 **optional** | ***GetAdminTokenPermissionsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminTokenPermissionsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminTokenPermissionsGetResponse**](AdminTokenPermissionsGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminTokens

> AdminGetTokensResponse GetAdminTokens(ctx, optional)

This provides information about all tokens.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetAdminTokensOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminTokensOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **direction** | **optional.String**| the sort order.  ASC or DESC. | [default to DESC]
 **startCreatedTime** | **optional.Int64**| The unix timestamp | 
 **endCreatedTime** | **optional.Int64**| The unix timestamp | 
 **startExpireTime** | **optional.Int64**| The unix timestamp | 
 **endExpireTime** | **optional.Int64**| The unix timestamp | 
 **tokenID** | [**optional.Interface of string**](.md)| Filter by token IDs | 
 **organizationIDs** | [**optional.Interface of string**](.md)| Filter by organization IDs | 
 **hostID** | [**optional.Interface of string**](.md)| Filter by host IDs | 
 **userID** | [**optional.Interface of string**](.md)| Filter by user IDs | 
 **engineInstanceID** | [**optional.Interface of string**](.md)| Filter by engine instance IDs | 
 **type_** | [**optional.Interface of TokenTypeEnum**](.md)| Filter by token type | 
 **orderBy** | **optional.String**| It should be in [createdTime, expirationTime, tokenType] | 
 **roleIDs** | [**optional.Interface of string**](.md)| Filters by role | 
 **accessAllOrganization** | **optional.Bool**|  | 

### Return type

[**AdminGetTokensResponse**](AdminGetTokensResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminUserDetail

> AdminUserGetDetailResponse GetAdminUserDetail(ctx, userID, optional)

This provides information on the given user.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userID** | [**string**](.md)| ID of User | 
 **optional** | ***GetAdminUserDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminUserDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminUserGetDetailResponse**](AdminUserGetDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminUserPermissions

> AdminUserPermissionsGetResponse GetAdminUserPermissions(ctx, userID, optional)

This provides a list of all user permissions for an user by UserID

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userID** | [**string**](.md)| ID of User | 
 **optional** | ***GetAdminUserPermissionsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminUserPermissionsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminUserPermissionsGetResponse**](AdminUserPermissionsGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminUserTokens

> AdminUserGetTokensResponse GetAdminUserTokens(ctx, userID, optional)

This provides information on the given user.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userID** | [**string**](.md)| ID of User | 
 **optional** | ***GetAdminUserTokensOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminUserTokensOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminUserGetTokensResponse**](AdminUserGetTokensResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminUsers

> AdminUsersGetResponse GetAdminUsers(ctx, optional)

This provides a list of users in the system

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetAdminUsersOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminUsersOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **offset** | **optional.Int32**| the number of users to skip before getting the result set | 
 **limit** | **optional.Int32**| the number of users to return. | [default to 100]
 **orderBy** | **optional.String**| the field to sort | [default to created_date_time]
 **direction** | **optional.String**| the sort order | [default to DESC]
 **status** | **optional.String**| the value should be in [active, trial, inactive, deleted] | 
 **name** | **optional.String**| Name of user | 
 **userName** | **optional.String**| userName of user | 
 **email** | **optional.String**| email of user | 
 **roleIDs** | [**optional.Interface of string**](.md)| Filters by role | 
 **organizationIDs** | [**optional.Interface of string**](.md)| Filters by internal organization ID | 
 **accessAllOrganization** | **optional.Bool**| A user can access to all organization or not. | 
 **isSuperAdmin** | **optional.Bool**|  | 

### Return type

[**AdminUsersGetResponse**](AdminUsersGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminUsersPermission

> AdminUsersPermissionsGetResponse GetAdminUsersPermission(ctx, optional)

This provides a list of all user permissions in the system

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetAdminUsersPermissionOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminUsersPermissionOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminUsersPermissionsGetResponse**](AdminUsersPermissionsGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminUsersRoles

> AdminUsersRolesGetResponse GetAdminUsersRoles(ctx, optional)

This provides a list of user role in the system

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetAdminUsersRolesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetAdminUsersRolesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **roleID** | [**optional.Interface of string**](.md)| Filter by role ID | 
 **roleName** | **optional.String**| Filter by roleName | 
 **orderBy** | **optional.String**| The value should be in [roleName, createdTime] | 

### Return type

[**AdminUsersRolesGetResponse**](AdminUsersRolesGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetApplications

> GetApplicationsResponse GetApplications(ctx, optional)

Get the list of applications deployed and available on aiWARE

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetApplicationsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetApplicationsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **applicationStatusQueryOptional** | [**optional.Interface of ApplicationStatusEnum**](.md)| status | 
 **applicationTypeQueryOptional** | [**optional.Interface of ApplicationTypeEnum**](.md)| type | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **orderBy** | **optional.String**| The value should be in [applicationName, createdTime] | 

### Return type

[**GetApplicationsResponse**](GetApplicationsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetBacklogSummary

> GetBacklogSummaryResponse GetBacklogSummary(ctx, optional)

This provides summary information on the current backlog

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetBacklogSummaryOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetBacklogSummaryOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetBacklogSummaryResponse**](GetBacklogSummaryResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetConfig

> AdminConfigResponse GetConfig(ctx, optional)

This provides all the config for the cluster

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetConfigOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetConfigOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **configSection** | [**optional.Interface of ConfigSectionEnum**](.md)| Config Section Entry | 
 **configKey** | **optional.String**| Config Key | 
 **deprecated** | **optional.Bool**|  | 
 **secure** | **optional.Bool**|  | 
 **isOverridden** | **optional.Bool**|  | 

### Return type

[**AdminConfigResponse**](AdminConfigResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetConfigSection

> AdminConfigSectionResponse GetConfigSection(ctx, configSection, optional)

This provides all the config for the cluster

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**configSection** | **string**| Config Section Entry | 
 **optional** | ***GetConfigSectionOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetConfigSectionOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminConfigSectionResponse**](AdminConfigSectionResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetConfigSectionKey

> AdminConfigSectionKeyResponse GetConfigSectionKey(ctx, configSection, configKey, optional)

This provides a config section key for the cluster

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**configSection** | **string**| Config Section Entry | 
**configKey** | **string**| Config Key | 
 **optional** | ***GetConfigSectionKeyOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetConfigSectionKeyOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminConfigSectionKeyResponse**](AdminConfigSectionKeyResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/csv, text/html, text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetEnginesForResource

> GetEnginesForResourceResponse GetEnginesForResource(ctx, resourceID, optional)

Get list of engines for resource

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**resourceID** | [**string**](.md)| ID of Resource | 
 **optional** | ***GetEnginesForResourceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetEnginesForResourceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetEnginesForResourceResponse**](GetEnginesForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetLicenseDetail

> LicenseDetail GetLicenseDetail(ctx, licenseID, optional)

This gets detail on a license key

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**licenseID** | **string**| License ID | 
 **optional** | ***GetLicenseDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetLicenseDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**LicenseDetail**](LicenseDetail.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetLicenses

> GetLicensesResponse GetLicenses(ctx, optional)

This provides a licenses on the system

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetLicensesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetLicensesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetLicensesResponse**](GetLicensesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetResource

> GetResourceResponse GetResource(ctx, resourceID, optional)

Get a resource definition

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**resourceID** | [**string**](.md)| ID of Resource | 
 **optional** | ***GetResourceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetResourceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetResourceResponse**](GetResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetResources

> GetResourcesResponse GetResources(ctx, optional)

Get the list of resources

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetResourcesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetResourcesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **engineIDs** | **optional.String**| Field to provide the input to get engines by Engine ID list. Separated by commas | 
 **resourceType** | **optional.String**| Filter by resourceType | 
 **offset** | **optional.Int64**| the number of data to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of items to return. | [default to 10]
 **direction** | **optional.String**| the sort order.  ASC or DESC. | [default to DESC]
 **orderBy** | **optional.String**| The sort column to use | 

### Return type

[**GetResourcesResponse**](GetResourcesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetResourcesForEngine

> GetResourcesForEngineResponse GetResourcesForEngine(ctx, engineID, optional)

Get list of resources for engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**engineID** | [**string**](.md)| ID of Engine | 
 **optional** | ***GetResourcesForEngineOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetResourcesForEngineOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetResourcesForEngineResponse**](GetResourcesForEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetResourcesForHost

> GetResourcesForHostResponse GetResourcesForHost(ctx, hostID, optional)

Get list of resources for host

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**hostID** | [**string**](.md)| ID of Host | 
 **optional** | ***GetResourcesForHostOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetResourcesForHostOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetResourcesForHostResponse**](GetResourcesForHostResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetResourcesForService

> GetResourcesForServiceResponse GetResourcesForService(ctx, serviceID, optional)

Get list of resources for service

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serviceID** | [**string**](.md)| ID of the service | 
 **optional** | ***GetResourcesForServiceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetResourcesForServiceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetResourcesForServiceResponse**](GetResourcesForServiceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetServerType

> GetServerTypeResponse GetServerType(ctx, serverTypeID, optional)

This provides detail on the server type

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serverTypeID** | [**string**](.md)| ID of Server Type | 
 **optional** | ***GetServerTypeOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetServerTypeOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetServerTypeResponse**](GetServerTypeResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetServerTypeEngineRunning

> GetServerTypeRunningEnginesResponse GetServerTypeEngineRunning(ctx, optional)

This lists the running engine with server types

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetServerTypeEngineRunningOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetServerTypeEngineRunningOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **serverTypeID** | **optional.String**| Filter by serverTypeID | 
 **engineID** | **optional.String**| Filter by engine id | 
 **offset** | **optional.Int64**| the number of records to skip before getting the result set | 
 **limit** | **optional.Int64**| the number of records to return. | [default to 100]

### Return type

[**GetServerTypeRunningEnginesResponse**](GetServerTypeRunningEnginesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetServerTypeEngineRunningDetail

> GetServerTypeRunningEngineDetailResponse GetServerTypeEngineRunningDetail(ctx, serverTypeID, engineID, optional)

This gets the detail of server type - running engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serverTypeID** | [**string**](.md)| ID of Server Type | 
**engineID** | [**string**](.md)| ID of Engine | 
 **optional** | ***GetServerTypeEngineRunningDetailOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetServerTypeEngineRunningDetailOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetServerTypeRunningEngineDetailResponse**](GetServerTypeRunningEngineDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetServerTypes

> GetServerTypesResponse GetServerTypes(ctx, runMode, optional)

This lists the server types available on the system

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**runMode** | **string**| Filer by run mode | 
 **optional** | ***GetServerTypesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetServerTypesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**GetServerTypesResponse**](GetServerTypesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetServices

> GetAdminServicesResponse GetServices(ctx, optional)

This lists the services available on the system

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetServicesOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a GetServicesOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **tags** | **optional.String**| Filter by tags | 

### Return type

[**GetAdminServicesResponse**](GetAdminServicesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## LoginUser

> AdminUserLoginResponse LoginUser(ctx, optional)

This logs a user in if successful

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***LoginUserOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a LoginUserOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **adminUserLoginRequest** | [**optional.Interface of AdminUserLoginRequest**](AdminUserLoginRequest.md)| This logs in the user | 

### Return type

[**AdminUserLoginResponse**](AdminUserLoginResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## OauthLoginUser

> AdminUserLoginResponse OauthLoginUser(ctx, optional)

This logs a user in if successful with OAuth2

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***OauthLoginUserOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a OauthLoginUserOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **adminUserOAuth2LoginRequest** | [**optional.Interface of AdminUserOAuth2LoginRequest**](AdminUserOAuth2LoginRequest.md)| This logs in the user with the OAuth2 response | 

### Return type

[**AdminUserLoginResponse**](AdminUserLoginResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RegisterUser

> AdminUserRegisterResponse RegisterUser(ctx, adminUserRegisterRequest, optional)

This registers a new user

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**adminUserRegisterRequest** | [**AdminUserRegisterRequest**](AdminUserRegisterRequest.md)| The input for registerUser | 
 **optional** | ***RegisterUserOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a RegisterUserOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminUserRegisterResponse**](AdminUserRegisterResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemoveEngineForResource

> RemoveEngineForResourceResponse RemoveEngineForResource(ctx, resourceID, engineID, optional)

This API removes the engine to the resource

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**resourceID** | [**string**](.md)| ID of Resource | 
**engineID** | [**string**](.md)| ID of Engine | 
 **optional** | ***RemoveEngineForResourceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a RemoveEngineForResourceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **removeEngineForResourceRequest** | [**optional.Interface of RemoveEngineForResourceRequest**](RemoveEngineForResourceRequest.md)| Remove Engine Mapping for Resource | 

### Return type

[**RemoveEngineForResourceResponse**](RemoveEngineForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RemoveserversServerType

> AdminOperationResponse RemoveserversServerType(ctx, serverTypeID, optional)

This API removes servers from the specified server type

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serverTypeID** | [**string**](.md)| ID of Server Type | 
 **optional** | ***RemoveserversServerTypeOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a RemoveserversServerTypeOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **removeServersToServerTypeRequest** | [**optional.Interface of RemoveServersToServerTypeRequest**](RemoveServersToServerTypeRequest.md)| Update Server Type | 

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


## ResetAllocTable

> AdminOperationResponse ResetAllocTable(ctx, optional)

This resets the alloc table

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***ResetAllocTableOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a ResetAllocTableOpts struct


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


## UpdateApplication

> AdminApplicationUpdateResponse UpdateApplication(ctx, applicationID, adminApplicationUpdateRequest, optional)

This updates an application

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**applicationID** | [**string**](.md)| ID of Application | 
**adminApplicationUpdateRequest** | [**AdminApplicationUpdateRequest**](AdminApplicationUpdateRequest.md)| The input for updateApplication | 
 **optional** | ***UpdateApplicationOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateApplicationOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminApplicationUpdateResponse**](AdminApplicationUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateConfigAll

> AdminConfigUpdateResponse UpdateConfigAll(ctx, adminConfigUpdateRequest, optional)

This gets the config for the cluster

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**adminConfigUpdateRequest** | [**AdminConfigUpdateRequest**](AdminConfigUpdateRequest.md)| Config Update for core | 
 **optional** | ***UpdateConfigAllOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateConfigAllOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **configSection** | [**optional.Interface of ConfigSectionEnum**](.md)| Config Section Entry | 
 **configKey** | **optional.String**| Config Key | 
 **deprecated** | **optional.Bool**|  | 
 **secure** | **optional.Bool**|  | 
 **isOverridden** | **optional.Bool**|  | 

### Return type

[**AdminConfigUpdateResponse**](AdminConfigUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateConfigSection

> AdminConfigUpdateSectionResponse UpdateConfigSection(ctx, configSection, adminConfigUpdateSectionRequest, optional)

This gets the config for the cluster

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**configSection** | **string**| Config Section Entry | 
**adminConfigUpdateSectionRequest** | [**AdminConfigUpdateSectionRequest**](AdminConfigUpdateSectionRequest.md)| The input for createConfigSection | 
 **optional** | ***UpdateConfigSectionOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateConfigSectionOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminConfigUpdateSectionResponse**](AdminConfigUpdateSectionResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/csv, text/html, text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateConfigSectionKey

> AdminConfigUpdateSectionKeyResponse UpdateConfigSectionKey(ctx, configSection, configKey, adminConfigUpdateSectionKeyRequest, optional)

This updates the config for the cluster for a given key

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**configSection** | **string**| Config Section Entry | 
**configKey** | **string**| Config Key | 
**adminConfigUpdateSectionKeyRequest** | [**AdminConfigUpdateSectionKeyRequest**](AdminConfigUpdateSectionKeyRequest.md)| The input for createSectionKey | 
 **optional** | ***UpdateConfigSectionKeyOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateConfigSectionKeyOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminConfigUpdateSectionKeyResponse**](AdminConfigUpdateSectionKeyResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/csv, text/html, text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateEnginesForResource

> UpdateEnginesForResourceResponse UpdateEnginesForResource(ctx, resourceID, optional)

This API updates the specified server type-running engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**resourceID** | [**string**](.md)| ID of Resource | 
 **optional** | ***UpdateEnginesForResourceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateEnginesForResourceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **updateEnginesForResourceRequest** | [**optional.Interface of UpdateEnginesForResourceRequest**](UpdateEnginesForResourceRequest.md)| Update Engine Mapping for Resource | 

### Return type

[**UpdateEnginesForResourceResponse**](UpdateEnginesForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateOrganization

> AdminOrganizationUpdateResponse UpdateOrganization(ctx, organizationID, adminOrganizationUpdateRequest, optional)

This updates a organization

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**organizationID** | [**string**](.md)| ID of Organization | 
**adminOrganizationUpdateRequest** | [**AdminOrganizationUpdateRequest**](AdminOrganizationUpdateRequest.md)| The input for updateOrganization | 
 **optional** | ***UpdateOrganizationOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateOrganizationOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminOrganizationUpdateResponse**](AdminOrganizationUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdatePermission

> AdminPermissionUpdateResponse UpdatePermission(ctx, permissionID, adminPermissionUpdateRequest, optional)

This updates a permission

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**permissionID** | [**string**](.md)| ID of Permission | 
**adminPermissionUpdateRequest** | [**AdminPermissionUpdateRequest**](AdminPermissionUpdateRequest.md)| The input for updatePermission | 
 **optional** | ***UpdatePermissionOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdatePermissionOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminPermissionUpdateResponse**](AdminPermissionUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateResource

> UpdateResourceResponse UpdateResource(ctx, resourceID, updateResourceRequest, optional)

This API updates the specified resource

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**resourceID** | [**string**](.md)| ID of Resource | 
**updateResourceRequest** | [**UpdateResourceRequest**](UpdateResourceRequest.md)| Update Resource | 
 **optional** | ***UpdateResourceOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateResourceOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**UpdateResourceResponse**](UpdateResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateResourceState

> UpdateResourceState(ctx, resourceID, updateResourceStateRequest, optional)

This API updates the state of the specified resource

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**resourceID** | [**string**](.md)| ID of Resource | 
**updateResourceStateRequest** | [**UpdateResourceStateRequest**](UpdateResourceStateRequest.md)| Update Resource State | 
 **optional** | ***UpdateResourceStateOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateResourceStateOpts struct


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


## UpdateRole

> AdminRoleUpdateResponse UpdateRole(ctx, roleID, adminRoleUpdateRequest, optional)

This updates a role

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**roleID** | [**string**](.md)| ID of Role | 
**adminRoleUpdateRequest** | [**AdminRoleUpdateRequest**](AdminRoleUpdateRequest.md)| The input for updateRole | 
 **optional** | ***UpdateRoleOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateRoleOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminRoleUpdateResponse**](AdminRoleUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateServerType

> UpdateServerTypeResponse UpdateServerType(ctx, serverTypeID, optional)

This API updates the specified server type

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serverTypeID** | [**string**](.md)| ID of Server Type | 
 **optional** | ***UpdateServerTypeOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateServerTypeOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **serverTypeDetail** | [**optional.Interface of ServerTypeDetail**](ServerTypeDetail.md)| Update Server Type | 

### Return type

[**UpdateServerTypeResponse**](UpdateServerTypeResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateServerTypeEngineRunning

> UpdateServerTypeEngineRunningResponse UpdateServerTypeEngineRunning(ctx, serverTypeID, engineID, optional)

This API updates the specified server type-running engine

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**serverTypeID** | [**string**](.md)| ID of Server Type | 
**engineID** | [**string**](.md)| ID of Engine | 
 **optional** | ***UpdateServerTypeEngineRunningOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateServerTypeEngineRunningOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **updateServerTypeEngineRunningRequest** | [**optional.Interface of UpdateServerTypeEngineRunningRequest**](UpdateServerTypeEngineRunningRequest.md)| Update Server Type - Running Engine | 

### Return type

[**UpdateServerTypeEngineRunningResponse**](UpdateServerTypeEngineRunningResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateToken

> AdminTokenUpdateResponse UpdateToken(ctx, tokenID, adminTokenUpdateRequest, optional)

This updates a token

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**tokenID** | [**string**](.md)| ID of Token | 
**adminTokenUpdateRequest** | [**AdminTokenUpdateRequest**](AdminTokenUpdateRequest.md)| The input for updateToken | 
 **optional** | ***UpdateTokenOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateTokenOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminTokenUpdateResponse**](AdminTokenUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateUser

> AdminUserUpdateResponse UpdateUser(ctx, userID, adminUserUpdateRequest, optional)

This updates a user

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userID** | [**string**](.md)| ID of User | 
**adminUserUpdateRequest** | [**AdminUserUpdateRequest**](AdminUserUpdateRequest.md)| The input for updateUser | 
 **optional** | ***UpdateUserOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UpdateUserOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 

### Return type

[**AdminUserUpdateResponse**](AdminUserUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UserPasswordForgot

> AdminUserPasswordForgotResponse UserPasswordForgot(ctx, optional)

This api will help users to reset their password when they forgot

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***UserPasswordForgotOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UserPasswordForgotOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **adminUserPasswordForgotRequest** | [**optional.Interface of AdminUserPasswordForgotRequest**](AdminUserPasswordForgotRequest.md)| Needs to provide the info to reset user&#39;s password when they forgot | 

### Return type

[**AdminUserPasswordForgotResponse**](AdminUserPasswordForgotResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UserPasswordReset

> AdminUserPasswordResetResponse UserPasswordReset(ctx, optional)

Helps users to reset their password

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***UserPasswordResetOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UserPasswordResetOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **adminUserPasswordResetRequest** | [**optional.Interface of AdminUserPasswordResetRequest**](AdminUserPasswordResetRequest.md)| Needs to provide the info to reset password | 

### Return type

[**AdminUserPasswordResetResponse**](AdminUserPasswordResetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UserPasswordUpdate

> AdminUserPasswordUpdateResponse UserPasswordUpdate(ctx, optional)

This api will help users to update their password

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***UserPasswordUpdateOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a UserPasswordUpdateOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xCorrelationId** | **optional.String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | 
 **adminUserPasswordUpdateRequest** | [**optional.Interface of AdminUserPasswordUpdateRequest**](AdminUserPasswordUpdateRequest.md)| Users provide the password info to change | 

### Return type

[**AdminUserPasswordUpdateResponse**](AdminUserPasswordUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

