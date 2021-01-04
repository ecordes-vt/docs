# AiwareJsClient.AdminApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addEngineToResource**](AdminApi.md#addEngineToResource) | **POST** /admin/resource/{ResourceID}/engine | This API adds the engine to the resource
[**addServiceToResource**](AdminApi.md#addServiceToResource) | **POST** /admin/resource/{ResourceID}/service | This API adds the service to the resource
[**addserversServerType**](AdminApi.md#addserversServerType) | **POST** /admin/server_type/{ServerTypeID}/add | This API add servers to the specified server type
[**adminTerminateCluster**](AdminApi.md#adminTerminateCluster) | **POST** /admin/terminate | This terminates the cluster
[**applyLicense**](AdminApi.md#applyLicense) | **POST** /admin/licenses/apply | This applies a license to aiWARE
[**checkAuth**](AdminApi.md#checkAuth) | **POST** /admin/auth | This check auth for a token
[**clearBacklog**](AdminApi.md#clearBacklog) | **POST** /admin/backlog/clear | This clears some or all of the currently queued tasks
[**createAdminApplication**](AdminApi.md#createAdminApplication) | **POST** /admin/applications/create | This creates a new application
[**createAdminCore**](AdminApi.md#createAdminCore) | **POST** /admin/cores/create | This creates a new core
[**createAdminOrganization**](AdminApi.md#createAdminOrganization) | **POST** /admin/organizations/create | This updates the config for the cluster for a given key
[**createPermission**](AdminApi.md#createPermission) | **POST** /admin/users/permission/create | This creates a new permission
[**createResource**](AdminApi.md#createResource) | **POST** /admin/resource/create | This API creates a new resource definition such as a database, nsq or redis DB.
[**createRole**](AdminApi.md#createRole) | **POST** /admin/users/role/create | This creates a new role
[**createServerType**](AdminApi.md#createServerType) | **POST** /admin/server_types/create | This creates a new server type
[**createServerTypeEngineRunning**](AdminApi.md#createServerTypeEngineRunning) | **POST** /admin/server_types/running_engine/create | This creates a new server_type_engine_running
[**createToken**](AdminApi.md#createToken) | **POST** /admin/tokens/create | This creates a new token
[**createUser**](AdminApi.md#createUser) | **POST** /admin/users/create | This creates a new user
[**deleteApplication**](AdminApi.md#deleteApplication) | **POST** /admin/applications/{ApplicationID}/delete | This deletes an application
[**deleteLicense**](AdminApi.md#deleteLicense) | **DELETE** /admin/licenses/{LicenseID}/delete | This deletes a license from aiWARE
[**deleteResource**](AdminApi.md#deleteResource) | **POST** /admin/resource/{ResourceID}/delete | This deletes the specified resource
[**deleteRole**](AdminApi.md#deleteRole) | **POST** /admin/users/role/{RoleID}/delete | This deletes a role
[**deleteServerType**](AdminApi.md#deleteServerType) | **DELETE** /admin/server_type/{ServerTypeID}/delete | This API deletes the specified server type
[**deleteServerTypePost**](AdminApi.md#deleteServerTypePost) | **POST** /admin/server_type/{ServerTypeID}/delete | This API deletes the specified server type
[**deleteServerTypeRunningEngine**](AdminApi.md#deleteServerTypeRunningEngine) | **DELETE** /admin/server_type/{ServerTypeID}/engine/{EngineID}/delete | This API deletes the running engine for a server type
[**deleteToken**](AdminApi.md#deleteToken) | **POST** /admin/token/{TokenID}/delete | This deletes a token
[**deleteUser**](AdminApi.md#deleteUser) | **POST** /admin/user/{UserID}/delete | This deletes a user
[**desiredserversServerType**](AdminApi.md#desiredserversServerType) | **POST** /admin/server_type/{ServerTypeID}/desired | This API add servers to the specified server type
[**getAdminApplicationDetail**](AdminApi.md#getAdminApplicationDetail) | **GET** /admin/applications/{ApplicationID}/detail | This provides information on the given application.
[**getAdminCoreDetail**](AdminApi.md#getAdminCoreDetail) | **GET** /admin/core/{CoreID}/detail | This provides information on the given core.
[**getAdminCores**](AdminApi.md#getAdminCores) | **GET** /admin/cores | This provides a list of core systems
[**getAdminEngineConfigSectionKey**](AdminApi.md#getAdminEngineConfigSectionKey) | **GET** /admin/engine/{EngineID}/config/{ConfigSection}/{ConfigKey} | This provides a config section key for the engine
[**getAdminOrganizationDetail**](AdminApi.md#getAdminOrganizationDetail) | **GET** /admin/organization/{OrganizationID}/detail | This gets organization detail by ID
[**getAdminOrganizationTokens**](AdminApi.md#getAdminOrganizationTokens) | **GET** /admin/organization/{OrganizationID}/tokens | This provides information on the given organization tokens.
[**getAdminOrganizations**](AdminApi.md#getAdminOrganizations) | **GET** /admin/organizations | This provides a list of organizations
[**getAdminPermissionDetail**](AdminApi.md#getAdminPermissionDetail) | **GET** /admin/users/permission/{PermissionID}/detail | This gets permission detail by ID
[**getAdminRoleDetail**](AdminApi.md#getAdminRoleDetail) | **GET** /admin/users/role/{RoleID}/detail | This gets role detail by ID
[**getAdminServiceConfig**](AdminApi.md#getAdminServiceConfig) | **GET** /admin/service/{ServiceID}/config | This provides all the config for the service
[**getAdminServiceConfigSection**](AdminApi.md#getAdminServiceConfigSection) | **GET** /admin/service/{ServiceID}/config/{ConfigSection} | This provides all the config for the service
[**getAdminServiceConfigSectionKey**](AdminApi.md#getAdminServiceConfigSectionKey) | **GET** /admin/service/{ServiceID}/config/{ConfigSection}/{ConfigKey} | This provides a config section key for the service
[**getAdminServiceInstances**](AdminApi.md#getAdminServiceInstances) | **GET** /admin/service/instances | This lists the service instances available for a system
[**getAdminStatus**](AdminApi.md#getAdminStatus) | **GET** /admin/status | This provides information on the status of the aiWARE edge
[**getAdminTokenDetail**](AdminApi.md#getAdminTokenDetail) | **GET** /admin/token/{TokenID}/detail | Get the token info by ID
[**getAdminTokenPermissions**](AdminApi.md#getAdminTokenPermissions) | **GET** /admin/token/{TokenID}/permissions | This provides a list of all token permissions for a token by TokenID
[**getAdminTokens**](AdminApi.md#getAdminTokens) | **GET** /admin/tokens | This provides information about all tokens.
[**getAdminUserDetail**](AdminApi.md#getAdminUserDetail) | **GET** /admin/user/{UserID}/detail | This provides information on the given user.
[**getAdminUserPermissions**](AdminApi.md#getAdminUserPermissions) | **GET** /admin/user/{UserID}/permissions | This provides a list of all user permissions for an user by UserID
[**getAdminUserTokens**](AdminApi.md#getAdminUserTokens) | **GET** /admin/user/{UserID}/tokens | This provides information on the given user.
[**getAdminUsers**](AdminApi.md#getAdminUsers) | **GET** /admin/users | This provides a list of users in the system
[**getAdminUsersPermission**](AdminApi.md#getAdminUsersPermission) | **GET** /admin/users/permissions | This provides a list of all user permissions in the system
[**getAdminUsersRoles**](AdminApi.md#getAdminUsersRoles) | **GET** /admin/users/roles | This provides a list of user role in the system
[**getApplications**](AdminApi.md#getApplications) | **GET** /admin/applications | Get the list of applications deployed and available on aiWARE
[**getBacklogSummary**](AdminApi.md#getBacklogSummary) | **GET** /admin/backlog/summary | This provides summary information on the current backlog
[**getConfig**](AdminApi.md#getConfig) | **GET** /admin/config | This provides all the config for the cluster
[**getConfigSection**](AdminApi.md#getConfigSection) | **GET** /admin/config/{ConfigSection} | This provides all the config for the cluster
[**getConfigSectionKey**](AdminApi.md#getConfigSectionKey) | **GET** /admin/config/{ConfigSection}/{ConfigKey} | This provides a config section key for the cluster
[**getEnginesForResource**](AdminApi.md#getEnginesForResource) | **GET** /admin/resource/{ResourceID}/engines | Get list of engines for resource
[**getLicenseDetail**](AdminApi.md#getLicenseDetail) | **GET** /admin/licenses/{LicenseID}/detail | This gets detail on a license key
[**getLicenses**](AdminApi.md#getLicenses) | **GET** /admin/licenses | This provides a licenses on the system
[**getResource**](AdminApi.md#getResource) | **GET** /admin/resource/{ResourceID} | Get a resource definition
[**getResources**](AdminApi.md#getResources) | **GET** /admin/resources | Get the list of resources
[**getResourcesForEngine**](AdminApi.md#getResourcesForEngine) | **GET** /admin/engine/{EngineID}/resources | Get list of resources for engine
[**getResourcesForHost**](AdminApi.md#getResourcesForHost) | **GET** /admin/host/{HostID}/resources | Get list of resources for host
[**getResourcesForService**](AdminApi.md#getResourcesForService) | **GET** /admin/service/{ServiceID}/resources | Get list of resources for service
[**getServerType**](AdminApi.md#getServerType) | **GET** /admin/server_type/{ServerTypeID}/detail | This provides detail on the server type
[**getServerTypeEngineRunning**](AdminApi.md#getServerTypeEngineRunning) | **GET** /admin/server_types/running_engines | This lists the running engine with server types
[**getServerTypeEngineRunningDetail**](AdminApi.md#getServerTypeEngineRunningDetail) | **GET** /admin/server_type/{ServerTypeID}/engine/{EngineID}/detail | This gets the detail of server type - running engine
[**getServerTypes**](AdminApi.md#getServerTypes) | **GET** /admin/server_types | This lists the server types available on the system
[**getServices**](AdminApi.md#getServices) | **GET** /admin/services | This lists the services available on the system
[**loginUser**](AdminApi.md#loginUser) | **POST** /admin/users/login | This logs a user in if successful
[**oauthLoginUser**](AdminApi.md#oauthLoginUser) | **POST** /admin/users/oauth2_login | This logs a user in if successful with OAuth2
[**registerUser**](AdminApi.md#registerUser) | **POST** /admin/users/register | This registers a new user
[**removeEngineForResource**](AdminApi.md#removeEngineForResource) | **POST** /admin/resource/{ResourceID}/engine/{EngineID}/delete | This API removes the engine to the resource
[**removeserversServerType**](AdminApi.md#removeserversServerType) | **POST** /admin/server_type/{ServerTypeID}/remove | This API removes servers from the specified server type
[**resetAllocTable**](AdminApi.md#resetAllocTable) | **POST** /admin/backlog/reset-alloc | This resets the alloc table
[**updateApplication**](AdminApi.md#updateApplication) | **POST** /admin/applications/{ApplicationID}/update | This updates an application
[**updateConfigAll**](AdminApi.md#updateConfigAll) | **POST** /admin/config | This gets the config for the cluster
[**updateConfigSection**](AdminApi.md#updateConfigSection) | **POST** /admin/config/{ConfigSection} | This gets the config for the cluster
[**updateConfigSectionKey**](AdminApi.md#updateConfigSectionKey) | **POST** /admin/config/{ConfigSection}/{ConfigKey} | This updates the config for the cluster for a given key
[**updateEnginesForResource**](AdminApi.md#updateEnginesForResource) | **POST** /admin/resource/{ResourceID}/engine/update | This API updates the specified server type-running engine
[**updateOrganization**](AdminApi.md#updateOrganization) | **POST** /admin/organization/{OrganizationID}/update | This updates a organization
[**updatePermission**](AdminApi.md#updatePermission) | **POST** /admin/users/permission/{PermissionID}/update | This updates a permission
[**updateResource**](AdminApi.md#updateResource) | **POST** /admin/resource/{ResourceID}/update | This API updates the specified resource
[**updateResourceState**](AdminApi.md#updateResourceState) | **POST** /admin/resource/{ResourceID}/updatestate | This API updates the state of the specified resource
[**updateRole**](AdminApi.md#updateRole) | **POST** /admin/users/role/{RoleID}/update | This updates a role
[**updateServerType**](AdminApi.md#updateServerType) | **POST** /admin/server_type/{ServerTypeID}/update | This API updates the specified server type
[**updateServerTypeEngineRunning**](AdminApi.md#updateServerTypeEngineRunning) | **POST** /admin/server_type/{ServerTypeID}/engine/{EngineID}/update | This API updates the specified server type-running engine
[**updateToken**](AdminApi.md#updateToken) | **POST** /admin/token/{TokenID}/update | This updates a token
[**updateUser**](AdminApi.md#updateUser) | **POST** /admin/user/{UserID}/update | This updates a user
[**userPasswordForgot**](AdminApi.md#userPasswordForgot) | **POST** /admin/users/password/forgot | This api will help users to reset their password when they forgot
[**userPasswordReset**](AdminApi.md#userPasswordReset) | **POST** /admin/users/password/reset | Helps users to reset their password
[**userPasswordUpdate**](AdminApi.md#userPasswordUpdate) | **POST** /admin/users/password/update | This api will help users to update their password



## addEngineToResource

> AddEngineForResourceResponse addEngineToResource(resourceID, opts)

This API adds the engine to the resource

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let resourceID = null; // String | ID of Resource
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'addEngineForResourceRequest': new AiwareJsClient.AddEngineForResourceRequest() // AddEngineForResourceRequest | Add Engine Mapping for Resource
};
apiInstance.addEngineToResource(resourceID, opts, (error, data, response) => {
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
 **resourceID** | [**String**](.md)| ID of Resource | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **addEngineForResourceRequest** | [**AddEngineForResourceRequest**](AddEngineForResourceRequest.md)| Add Engine Mapping for Resource | [optional] 

### Return type

[**AddEngineForResourceResponse**](AddEngineForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## addServiceToResource

> AddServiceForResourceResponse addServiceToResource(resourceID, opts)

This API adds the service to the resource

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let resourceID = null; // String | ID of Resource
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'addServiceForResourceRequest': new AiwareJsClient.AddServiceForResourceRequest() // AddServiceForResourceRequest | Add Service Mapping for Resource
};
apiInstance.addServiceToResource(resourceID, opts, (error, data, response) => {
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
 **resourceID** | [**String**](.md)| ID of Resource | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **addServiceForResourceRequest** | [**AddServiceForResourceRequest**](AddServiceForResourceRequest.md)| Add Service Mapping for Resource | [optional] 

### Return type

[**AddServiceForResourceResponse**](AddServiceForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## addserversServerType

> AdminOperationResponse addserversServerType(serverTypeID, opts)

This API add servers to the specified server type

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serverTypeID = null; // String | ID of Server Type
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'addServersToServerTypeRequest': new AiwareJsClient.AddServersToServerTypeRequest() // AddServersToServerTypeRequest | Add Servers Server Type
};
apiInstance.addserversServerType(serverTypeID, opts, (error, data, response) => {
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
 **serverTypeID** | [**String**](.md)| ID of Server Type | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **addServersToServerTypeRequest** | [**AddServersToServerTypeRequest**](AddServersToServerTypeRequest.md)| Add Servers Server Type | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## adminTerminateCluster

> adminTerminateCluster(opts)

This terminates the cluster

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'adminOperationRequest': new AiwareJsClient.AdminOperationRequest() // AdminOperationRequest | ClusterID
};
apiInstance.adminTerminateCluster(opts, (error, data, response) => {
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
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **adminOperationRequest** | [**AdminOperationRequest**](AdminOperationRequest.md)| ClusterID | [optional] 

### Return type

null (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## applyLicense

> LicenseDetail applyLicense(opts)

This applies a license to aiWARE

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'createLicenseDetail': new AiwareJsClient.CreateLicenseDetail() // CreateLicenseDetail | 
};
apiInstance.applyLicense(opts, (error, data, response) => {
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
 **createLicenseDetail** | [**CreateLicenseDetail**](CreateLicenseDetail.md)|  | [optional] 

### Return type

[**LicenseDetail**](LicenseDetail.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## checkAuth

> AdminAuthResponse checkAuth(adminAuthRequest, opts)

This check auth for a token

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let adminAuthRequest = new AiwareJsClient.AdminAuthRequest(); // AdminAuthRequest | The input for check auth
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.checkAuth(adminAuthRequest, opts, (error, data, response) => {
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
 **adminAuthRequest** | [**AdminAuthRequest**](AdminAuthRequest.md)| The input for check auth | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminAuthResponse**](AdminAuthResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## clearBacklog

> AdminCoreCreateResponse clearBacklog(opts)

This clears some or all of the currently queued tasks

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'status': new AiwareJsClient.EngineStatusEnum(), // EngineStatusEnum | Field to match the current status
  'engineID': "engineID_example", // String | Filter by engine id
  'modifiedBefore': 789, // Number | Filter by items modified before expressed as timestamp
  'modifiedAfter': 789, // Number | Filter by items modified after expressed as timestamp
  'createdBefore': 789, // Number | Filter items where created date is before this date
  'createdAfter': 789 // Number | Filter items where created date is after this date
};
apiInstance.clearBacklog(opts, (error, data, response) => {
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
 **status** | [**EngineStatusEnum**](.md)| Field to match the current status | [optional] 
 **engineID** | **String**| Filter by engine id | [optional] 
 **modifiedBefore** | **Number**| Filter by items modified before expressed as timestamp | [optional] 
 **modifiedAfter** | **Number**| Filter by items modified after expressed as timestamp | [optional] 
 **createdBefore** | **Number**| Filter items where created date is before this date | [optional] 
 **createdAfter** | **Number**| Filter items where created date is after this date | [optional] 

### Return type

[**AdminCoreCreateResponse**](AdminCoreCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## createAdminApplication

> AdminApplicationCreateResponse createAdminApplication(adminApplicationCreateRequest, opts)

This creates a new application

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let adminApplicationCreateRequest = new AiwareJsClient.AdminApplicationCreateRequest(); // AdminApplicationCreateRequest | The input for createApplication
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createAdminApplication(adminApplicationCreateRequest, opts, (error, data, response) => {
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
 **adminApplicationCreateRequest** | [**AdminApplicationCreateRequest**](AdminApplicationCreateRequest.md)| The input for createApplication | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminApplicationCreateResponse**](AdminApplicationCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createAdminCore

> AdminCoreCreateResponse createAdminCore(adminCoreCreateRequest, opts)

This creates a new core

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let adminCoreCreateRequest = new AiwareJsClient.AdminCoreCreateRequest(); // AdminCoreCreateRequest | The input for createCor
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createAdminCore(adminCoreCreateRequest, opts, (error, data, response) => {
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
 **adminCoreCreateRequest** | [**AdminCoreCreateRequest**](AdminCoreCreateRequest.md)| The input for createCor | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminCoreCreateResponse**](AdminCoreCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createAdminOrganization

> AdminOrganizationCreateResponse createAdminOrganization(adminOrganizationCreateRequest, opts)

This updates the config for the cluster for a given key

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let adminOrganizationCreateRequest = new AiwareJsClient.AdminOrganizationCreateRequest(); // AdminOrganizationCreateRequest | The input for createOrganization
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createAdminOrganization(adminOrganizationCreateRequest, opts, (error, data, response) => {
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
 **adminOrganizationCreateRequest** | [**AdminOrganizationCreateRequest**](AdminOrganizationCreateRequest.md)| The input for createOrganization | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOrganizationCreateResponse**](AdminOrganizationCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createPermission

> AdminPermissionCreateResponse createPermission(adminPermissionCreateRequest, opts)

This creates a new permission

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let adminPermissionCreateRequest = new AiwareJsClient.AdminPermissionCreateRequest(); // AdminPermissionCreateRequest | The input for createPermission
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createPermission(adminPermissionCreateRequest, opts, (error, data, response) => {
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
 **adminPermissionCreateRequest** | [**AdminPermissionCreateRequest**](AdminPermissionCreateRequest.md)| The input for createPermission | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminPermissionCreateResponse**](AdminPermissionCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createResource

> CreateResourceResponse createResource(createResourceRequest, opts)

This API creates a new resource definition such as a database, nsq or redis DB.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let createResourceRequest = new AiwareJsClient.CreateResourceRequest(); // CreateResourceRequest | The fields for a resource definition
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createResource(createResourceRequest, opts, (error, data, response) => {
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
 **createResourceRequest** | [**CreateResourceRequest**](CreateResourceRequest.md)| The fields for a resource definition | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateResourceResponse**](CreateResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createRole

> AdminRoleCreateResponse createRole(adminRoleCreateRequest, opts)

This creates a new role

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let adminRoleCreateRequest = new AiwareJsClient.AdminRoleCreateRequest(); // AdminRoleCreateRequest | The input for createRole
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createRole(adminRoleCreateRequest, opts, (error, data, response) => {
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
 **adminRoleCreateRequest** | [**AdminRoleCreateRequest**](AdminRoleCreateRequest.md)| The input for createRole | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminRoleCreateResponse**](AdminRoleCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createServerType

> CreateServerTypeResponse createServerType(createServerTypeRequest, opts)

This creates a new server type

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let createServerTypeRequest = new AiwareJsClient.CreateServerTypeRequest(); // CreateServerTypeRequest | The input for createServerType
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createServerType(createServerTypeRequest, opts, (error, data, response) => {
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
 **createServerTypeRequest** | [**CreateServerTypeRequest**](CreateServerTypeRequest.md)| The input for createServerType | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateServerTypeResponse**](CreateServerTypeResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createServerTypeEngineRunning

> CreateServerTypeEngineRunningResponse createServerTypeEngineRunning(createServerTypeEngineRunningRequest, opts)

This creates a new server_type_engine_running

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let createServerTypeEngineRunningRequest = new AiwareJsClient.CreateServerTypeEngineRunningRequest(); // CreateServerTypeEngineRunningRequest | The input for createServerTypeEngineRunning
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createServerTypeEngineRunning(createServerTypeEngineRunningRequest, opts, (error, data, response) => {
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
 **createServerTypeEngineRunningRequest** | [**CreateServerTypeEngineRunningRequest**](CreateServerTypeEngineRunningRequest.md)| The input for createServerTypeEngineRunning | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateServerTypeEngineRunningResponse**](CreateServerTypeEngineRunningResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createToken

> AdminTokenCreateResponse createToken(adminTokenCreateRequest, opts)

This creates a new token

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let adminTokenCreateRequest = new AiwareJsClient.AdminTokenCreateRequest(); // AdminTokenCreateRequest | The input for createToken
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createToken(adminTokenCreateRequest, opts, (error, data, response) => {
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
 **adminTokenCreateRequest** | [**AdminTokenCreateRequest**](AdminTokenCreateRequest.md)| The input for createToken | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminTokenCreateResponse**](AdminTokenCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createUser

> AdminUserCreateResponse createUser(adminUserCreateRequest, opts)

This creates a new user

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let adminUserCreateRequest = new AiwareJsClient.AdminUserCreateRequest(); // AdminUserCreateRequest | The input for createUser
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.createUser(adminUserCreateRequest, opts, (error, data, response) => {
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
 **adminUserCreateRequest** | [**AdminUserCreateRequest**](AdminUserCreateRequest.md)| The input for createUser | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserCreateResponse**](AdminUserCreateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## deleteApplication

> AdminApplicationDeleteResponse deleteApplication(applicationID, opts)

This deletes an application

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let applicationID = null; // String | ID of Application
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.deleteApplication(applicationID, opts, (error, data, response) => {
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
 **applicationID** | [**String**](.md)| ID of Application | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminApplicationDeleteResponse**](AdminApplicationDeleteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## deleteLicense

> AdminOperationResponse deleteLicense(licenseID, opts)

This deletes a license from aiWARE

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let licenseID = "licenseID_example"; // String | License ID
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.deleteLicense(licenseID, opts, (error, data, response) => {
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
 **licenseID** | **String**| License ID | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## deleteResource

> AdminOperationResponse deleteResource(resourceID, opts)

This deletes the specified resource

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let resourceID = null; // String | ID of Resource
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.deleteResource(resourceID, opts, (error, data, response) => {
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
 **resourceID** | [**String**](.md)| ID of Resource | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## deleteRole

> AdminRoleDeleteResponse deleteRole(roleID, opts)

This deletes a role

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let roleID = null; // String | ID of Role
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.deleteRole(roleID, opts, (error, data, response) => {
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
 **roleID** | [**String**](.md)| ID of Role | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminRoleDeleteResponse**](AdminRoleDeleteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## deleteServerType

> AdminOperationResponse deleteServerType(serverTypeID, opts)

This API deletes the specified server type

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serverTypeID = null; // String | ID of Server Type
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.deleteServerType(serverTypeID, opts, (error, data, response) => {
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
 **serverTypeID** | [**String**](.md)| ID of Server Type | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## deleteServerTypePost

> AdminOperationResponse deleteServerTypePost(serverTypeID, opts)

This API deletes the specified server type

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serverTypeID = null; // String | ID of Server Type
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'deleteServerTypeRequest': new AiwareJsClient.DeleteServerTypeRequest() // DeleteServerTypeRequest | Engine Instance Info
};
apiInstance.deleteServerTypePost(serverTypeID, opts, (error, data, response) => {
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
 **serverTypeID** | [**String**](.md)| ID of Server Type | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **deleteServerTypeRequest** | [**DeleteServerTypeRequest**](DeleteServerTypeRequest.md)| Engine Instance Info | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## deleteServerTypeRunningEngine

> AdminOperationResponse deleteServerTypeRunningEngine(serverTypeID, engineID, opts)

This API deletes the running engine for a server type

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serverTypeID = null; // String | ID of Server Type
let engineID = null; // String | ID of Engine
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.deleteServerTypeRunningEngine(serverTypeID, engineID, opts, (error, data, response) => {
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
 **serverTypeID** | [**String**](.md)| ID of Server Type | 
 **engineID** | [**String**](.md)| ID of Engine | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## deleteToken

> AdminTokenDeleteResponse deleteToken(tokenID, opts)

This deletes a token

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let tokenID = null; // String | ID of Token
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.deleteToken(tokenID, opts, (error, data, response) => {
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
 **tokenID** | [**String**](.md)| ID of Token | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminTokenDeleteResponse**](AdminTokenDeleteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## deleteUser

> AdminUserDeleteResponse deleteUser(userID, opts)

This deletes a user

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let userID = null; // String | ID of User
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.deleteUser(userID, opts, (error, data, response) => {
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
 **userID** | [**String**](.md)| ID of User | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserDeleteResponse**](AdminUserDeleteResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## desiredserversServerType

> AdminOperationResponse desiredserversServerType(serverTypeID, opts)

This API add servers to the specified server type

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serverTypeID = null; // String | ID of Server Type
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'desiredServersToServerTypeRequest': new AiwareJsClient.DesiredServersToServerTypeRequest() // DesiredServersToServerTypeRequest | Set Servers for Server Type
};
apiInstance.desiredserversServerType(serverTypeID, opts, (error, data, response) => {
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
 **serverTypeID** | [**String**](.md)| ID of Server Type | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **desiredServersToServerTypeRequest** | [**DesiredServersToServerTypeRequest**](DesiredServersToServerTypeRequest.md)| Set Servers for Server Type | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## getAdminApplicationDetail

> AdminApplicationGetDetailResponse getAdminApplicationDetail(applicationID, opts)

This provides information on the given application.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let applicationID = null; // String | ID of Application
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminApplicationDetail(applicationID, opts, (error, data, response) => {
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
 **applicationID** | [**String**](.md)| ID of Application | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminApplicationGetDetailResponse**](AdminApplicationGetDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminCoreDetail

> AdminCoreGetDetailResponse getAdminCoreDetail(coreID, opts)

This provides information on the given core.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let coreID = null; // String | ID of Core
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminCoreDetail(coreID, opts, (error, data, response) => {
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
 **coreID** | [**String**](.md)| ID of Core | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminCoreGetDetailResponse**](AdminCoreGetDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminCores

> GetCoresResponse getAdminCores(opts)

This provides a list of core systems

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminCores(opts, (error, data, response) => {
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

[**GetCoresResponse**](GetCoresResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminEngineConfigSectionKey

> AdminEngineConfigSectionKeyResponse getAdminEngineConfigSectionKey(engineID, configSection, configKey, opts)

This provides a config section key for the engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let engineID = "engineID_example"; // String | EngineID of node-red container request
let configSection = "configSection_example"; // String | Config Section Entry
let configKey = "configKey_example"; // String | Config Key
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminEngineConfigSectionKey(engineID, configSection, configKey, opts, (error, data, response) => {
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
 **configSection** | **String**| Config Section Entry | 
 **configKey** | **String**| Config Key | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminEngineConfigSectionKeyResponse**](AdminEngineConfigSectionKeyResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/csv, text/html, text/plain


## getAdminOrganizationDetail

> AdminOrganizationGetDetailResponse getAdminOrganizationDetail(organizationID, opts)

This gets organization detail by ID

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let organizationID = null; // String | ID of Organization
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminOrganizationDetail(organizationID, opts, (error, data, response) => {
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
 **organizationID** | [**String**](.md)| ID of Organization | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOrganizationGetDetailResponse**](AdminOrganizationGetDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminOrganizationTokens

> AdminOrganizationGetTokensResponse getAdminOrganizationTokens(organizationID, opts)

This provides information on the given organization tokens.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let organizationID = null; // String | ID of Organization
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminOrganizationTokens(organizationID, opts, (error, data, response) => {
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
 **organizationID** | [**String**](.md)| ID of Organization | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOrganizationGetTokensResponse**](AdminOrganizationGetTokensResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminOrganizations

> AdminOrganizationsGetResponse getAdminOrganizations(opts)

This provides a list of organizations

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'organizationID': null, // String | Filter by organizationID
  'organizationName': "organizationName_example", // String | Filter by organizationName
  'orderBy': "orderBy_example" // String | The value should be in [organizationName, organizationID, createdTime, basePriority]
};
apiInstance.getAdminOrganizations(opts, (error, data, response) => {
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
 **organizationID** | [**String**](.md)| Filter by organizationID | [optional] 
 **organizationName** | **String**| Filter by organizationName | [optional] 
 **orderBy** | **String**| The value should be in [organizationName, organizationID, createdTime, basePriority] | [optional] 

### Return type

[**AdminOrganizationsGetResponse**](AdminOrganizationsGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminPermissionDetail

> AdminPermissionDetailResponse getAdminPermissionDetail(permissionID, opts)

This gets permission detail by ID

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let permissionID = null; // String | ID of Permission
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminPermissionDetail(permissionID, opts, (error, data, response) => {
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
 **permissionID** | [**String**](.md)| ID of Permission | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminPermissionDetailResponse**](AdminPermissionDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminRoleDetail

> AdminRoleDetailResponse getAdminRoleDetail(roleID, opts)

This gets role detail by ID

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let roleID = null; // String | ID of Role
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminRoleDetail(roleID, opts, (error, data, response) => {
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
 **roleID** | [**String**](.md)| ID of Role | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminRoleDetailResponse**](AdminRoleDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminServiceConfig

> AdminServiceConfigResponse getAdminServiceConfig(serviceID, opts)

This provides all the config for the service

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serviceID = null; // String | ID of the service
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'configKey': "configKey_example" // String | Config Key
};
apiInstance.getAdminServiceConfig(serviceID, opts, (error, data, response) => {
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
 **serviceID** | [**String**](.md)| ID of the service | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **configKey** | **String**| Config Key | [optional] 

### Return type

[**AdminServiceConfigResponse**](AdminServiceConfigResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminServiceConfigSection

> AdminServiceConfigSectionResponse getAdminServiceConfigSection(serviceID, configSection, opts)

This provides all the config for the service

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serviceID = null; // String | ID of the service
let configSection = "configSection_example"; // String | Config Section Entry
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminServiceConfigSection(serviceID, configSection, opts, (error, data, response) => {
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
 **serviceID** | [**String**](.md)| ID of the service | 
 **configSection** | **String**| Config Section Entry | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminServiceConfigSectionResponse**](AdminServiceConfigSectionResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminServiceConfigSectionKey

> AdminServiceConfigSectionKeyResponse getAdminServiceConfigSectionKey(serviceID, configSection, configKey, opts)

This provides a config section key for the service

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serviceID = null; // String | ID of the service
let configSection = "configSection_example"; // String | Config Section Entry
let configKey = "configKey_example"; // String | Config Key
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminServiceConfigSectionKey(serviceID, configSection, configKey, opts, (error, data, response) => {
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
 **serviceID** | [**String**](.md)| ID of the service | 
 **configSection** | **String**| Config Section Entry | 
 **configKey** | **String**| Config Key | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminServiceConfigSectionKeyResponse**](AdminServiceConfigSectionKeyResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/csv, text/html, text/plain


## getAdminServiceInstances

> GetAdminServiceInstancesResponse getAdminServiceInstances(opts)

This lists the service instances available for a system

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminServiceInstances(opts, (error, data, response) => {
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

[**GetAdminServiceInstancesResponse**](GetAdminServiceInstancesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminStatus

> EngineInstanceInfo getAdminStatus(opts)

This provides information on the status of the aiWARE edge

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'format': new AiwareJsClient.StatusFormatEnum(), // StatusFormatEnum | If specified, this limits the jobs or tasks to follow status
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminStatus(opts, (error, data, response) => {
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
 **format** | [**StatusFormatEnum**](.md)| If specified, this limits the jobs or tasks to follow status | [optional] 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceInfo**](EngineInstanceInfo.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/csv, text/html, text/plain


## getAdminTokenDetail

> TokenDetail getAdminTokenDetail(tokenID, opts)

Get the token info by ID

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let tokenID = null; // String | ID of Token
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminTokenDetail(tokenID, opts, (error, data, response) => {
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
 **tokenID** | [**String**](.md)| ID of Token | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**TokenDetail**](TokenDetail.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminTokenPermissions

> AdminTokenPermissionsGetResponse getAdminTokenPermissions(tokenID, opts)

This provides a list of all token permissions for a token by TokenID

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let tokenID = null; // String | ID of Token
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminTokenPermissions(tokenID, opts, (error, data, response) => {
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
 **tokenID** | [**String**](.md)| ID of Token | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminTokenPermissionsGetResponse**](AdminTokenPermissionsGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminTokens

> AdminGetTokensResponse getAdminTokens(opts)

This provides information about all tokens.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'direction': "'DESC'", // String | the sort order.  ASC or DESC.
  'startCreatedTime': 789, // Number | The unix timestamp
  'endCreatedTime': 789, // Number | The unix timestamp
  'startExpireTime': 789, // Number | The unix timestamp
  'endExpireTime': 789, // Number | The unix timestamp
  'tokenID': null, // String | Filter by token IDs
  'organizationIDs': null, // String | Filter by organization IDs
  'hostID': null, // String | Filter by host IDs
  'userID': null, // String | Filter by user IDs
  'engineInstanceID': null, // String | Filter by engine instance IDs
  'type': new AiwareJsClient.TokenTypeEnum(), // TokenTypeEnum | Filter by token type
  'orderBy': "orderBy_example", // String | It should be in [createdTime, expirationTime, tokenType]
  'roleIDs': null, // String | Filters by role
  'accessAllOrganization': true // Boolean | 
};
apiInstance.getAdminTokens(opts, (error, data, response) => {
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
 **startCreatedTime** | **Number**| The unix timestamp | [optional] 
 **endCreatedTime** | **Number**| The unix timestamp | [optional] 
 **startExpireTime** | **Number**| The unix timestamp | [optional] 
 **endExpireTime** | **Number**| The unix timestamp | [optional] 
 **tokenID** | [**String**](.md)| Filter by token IDs | [optional] 
 **organizationIDs** | [**String**](.md)| Filter by organization IDs | [optional] 
 **hostID** | [**String**](.md)| Filter by host IDs | [optional] 
 **userID** | [**String**](.md)| Filter by user IDs | [optional] 
 **engineInstanceID** | [**String**](.md)| Filter by engine instance IDs | [optional] 
 **type** | [**TokenTypeEnum**](.md)| Filter by token type | [optional] 
 **orderBy** | **String**| It should be in [createdTime, expirationTime, tokenType] | [optional] 
 **roleIDs** | [**String**](.md)| Filters by role | [optional] 
 **accessAllOrganization** | **Boolean**|  | [optional] 

### Return type

[**AdminGetTokensResponse**](AdminGetTokensResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminUserDetail

> AdminUserGetDetailResponse getAdminUserDetail(userID, opts)

This provides information on the given user.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let userID = null; // String | ID of User
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminUserDetail(userID, opts, (error, data, response) => {
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
 **userID** | [**String**](.md)| ID of User | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserGetDetailResponse**](AdminUserGetDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminUserPermissions

> AdminUserPermissionsGetResponse getAdminUserPermissions(userID, opts)

This provides a list of all user permissions for an user by UserID

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let userID = null; // String | ID of User
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminUserPermissions(userID, opts, (error, data, response) => {
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
 **userID** | [**String**](.md)| ID of User | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserPermissionsGetResponse**](AdminUserPermissionsGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminUserTokens

> AdminUserGetTokensResponse getAdminUserTokens(userID, opts)

This provides information on the given user.

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let userID = null; // String | ID of User
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminUserTokens(userID, opts, (error, data, response) => {
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
 **userID** | [**String**](.md)| ID of User | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserGetTokensResponse**](AdminUserGetTokensResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminUsers

> AdminUsersGetResponse getAdminUsers(opts)

This provides a list of users in the system

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'offset': 56, // Number | the number of users to skip before getting the result set
  'limit': 100, // Number | the number of users to return.
  'orderBy': "'created_date_time'", // String | the field to sort
  'direction': "'DESC'", // String | the sort order
  'status': "status_example", // String | the value should be in [active, trial, inactive, deleted]
  'name': "name_example", // String | Name of user
  'userName': "userName_example", // String | userName of user
  'email': "email_example", // String | email of user
  'roleIDs': null, // String | Filters by role
  'organizationIDs': null, // String | Filters by internal organization ID
  'accessAllOrganization': true, // Boolean | A user can access to all organization or not.
  'isSuperAdmin': true // Boolean | 
};
apiInstance.getAdminUsers(opts, (error, data, response) => {
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
 **offset** | **Number**| the number of users to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of users to return. | [optional] [default to 100]
 **orderBy** | **String**| the field to sort | [optional] [default to &#39;created_date_time&#39;]
 **direction** | **String**| the sort order | [optional] [default to &#39;DESC&#39;]
 **status** | **String**| the value should be in [active, trial, inactive, deleted] | [optional] 
 **name** | **String**| Name of user | [optional] 
 **userName** | **String**| userName of user | [optional] 
 **email** | **String**| email of user | [optional] 
 **roleIDs** | [**String**](.md)| Filters by role | [optional] 
 **organizationIDs** | [**String**](.md)| Filters by internal organization ID | [optional] 
 **accessAllOrganization** | **Boolean**| A user can access to all organization or not. | [optional] 
 **isSuperAdmin** | **Boolean**|  | [optional] 

### Return type

[**AdminUsersGetResponse**](AdminUsersGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminUsersPermission

> AdminUsersPermissionsGetResponse getAdminUsersPermission(opts)

This provides a list of all user permissions in the system

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getAdminUsersPermission(opts, (error, data, response) => {
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

[**AdminUsersPermissionsGetResponse**](AdminUsersPermissionsGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getAdminUsersRoles

> AdminUsersRolesGetResponse getAdminUsersRoles(opts)

This provides a list of user role in the system

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'roleID': null, // String | Filter by role ID
  'roleName': "roleName_example", // String | Filter by roleName
  'orderBy': "orderBy_example" // String | The value should be in [roleName, createdTime]
};
apiInstance.getAdminUsersRoles(opts, (error, data, response) => {
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
 **roleID** | [**String**](.md)| Filter by role ID | [optional] 
 **roleName** | **String**| Filter by roleName | [optional] 
 **orderBy** | **String**| The value should be in [roleName, createdTime] | [optional] 

### Return type

[**AdminUsersRolesGetResponse**](AdminUsersRolesGetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getApplications

> GetApplicationsResponse getApplications(opts)

Get the list of applications deployed and available on aiWARE

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'applicationStatusQueryOptional': new AiwareJsClient.ApplicationStatusEnum(), // ApplicationStatusEnum | status
  'applicationTypeQueryOptional': new AiwareJsClient.ApplicationTypeEnum(), // ApplicationTypeEnum | type
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'orderBy': "orderBy_example" // String | The value should be in [applicationName, createdTime]
};
apiInstance.getApplications(opts, (error, data, response) => {
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
 **applicationStatusQueryOptional** | [**ApplicationStatusEnum**](.md)| status | [optional] 
 **applicationTypeQueryOptional** | [**ApplicationTypeEnum**](.md)| type | [optional] 
 **offset** | **Number**| the number of data to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of items to return. | [optional] [default to 10]
 **orderBy** | **String**| The value should be in [applicationName, createdTime] | [optional] 

### Return type

[**GetApplicationsResponse**](GetApplicationsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getBacklogSummary

> GetBacklogSummaryResponse getBacklogSummary(opts)

This provides summary information on the current backlog

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getBacklogSummary(opts, (error, data, response) => {
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

[**GetBacklogSummaryResponse**](GetBacklogSummaryResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getConfig

> AdminConfigResponse getConfig(opts)

This provides all the config for the cluster

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'configSection': new AiwareJsClient.ConfigSectionEnum(), // ConfigSectionEnum | Config Section Entry
  'configKey': "configKey_example", // String | Config Key
  'deprecated': true, // Boolean | 
  'secure': true, // Boolean | 
  'isOverridden': true // Boolean | 
};
apiInstance.getConfig(opts, (error, data, response) => {
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
 **configSection** | [**ConfigSectionEnum**](.md)| Config Section Entry | [optional] 
 **configKey** | **String**| Config Key | [optional] 
 **deprecated** | **Boolean**|  | [optional] 
 **secure** | **Boolean**|  | [optional] 
 **isOverridden** | **Boolean**|  | [optional] 

### Return type

[**AdminConfigResponse**](AdminConfigResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getConfigSection

> AdminConfigSectionResponse getConfigSection(configSection, opts)

This provides all the config for the cluster

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let configSection = "configSection_example"; // String | Config Section Entry
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getConfigSection(configSection, opts, (error, data, response) => {
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
 **configSection** | **String**| Config Section Entry | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminConfigSectionResponse**](AdminConfigSectionResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getConfigSectionKey

> AdminConfigSectionKeyResponse getConfigSectionKey(configSection, configKey, opts)

This provides a config section key for the cluster

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let configSection = "configSection_example"; // String | Config Section Entry
let configKey = "configKey_example"; // String | Config Key
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getConfigSectionKey(configSection, configKey, opts, (error, data, response) => {
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
 **configSection** | **String**| Config Section Entry | 
 **configKey** | **String**| Config Key | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminConfigSectionKeyResponse**](AdminConfigSectionKeyResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/csv, text/html, text/plain


## getEnginesForResource

> GetEnginesForResourceResponse getEnginesForResource(resourceID, opts)

Get list of engines for resource

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let resourceID = null; // String | ID of Resource
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getEnginesForResource(resourceID, opts, (error, data, response) => {
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
 **resourceID** | [**String**](.md)| ID of Resource | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetEnginesForResourceResponse**](GetEnginesForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getLicenseDetail

> LicenseDetail getLicenseDetail(licenseID, opts)

This gets detail on a license key

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let licenseID = "licenseID_example"; // String | License ID
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getLicenseDetail(licenseID, opts, (error, data, response) => {
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
 **licenseID** | **String**| License ID | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**LicenseDetail**](LicenseDetail.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getLicenses

> GetLicensesResponse getLicenses(opts)

This provides a licenses on the system

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getLicenses(opts, (error, data, response) => {
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

[**GetLicensesResponse**](GetLicensesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getResource

> GetResourceResponse getResource(resourceID, opts)

Get a resource definition

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let resourceID = null; // String | ID of Resource
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getResource(resourceID, opts, (error, data, response) => {
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
 **resourceID** | [**String**](.md)| ID of Resource | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetResourceResponse**](GetResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getResources

> GetResourcesResponse getResources(opts)

Get the list of resources

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'engineIDs': "engineIDs_example", // String | Field to provide the input to get engines by Engine ID list. Separated by commas
  'resourceType': "resourceType_example", // String | Filter by resourceType
  'offset': 789, // Number | the number of data to skip before getting the result set
  'limit': 10, // Number | the number of items to return.
  'direction': "'DESC'", // String | the sort order.  ASC or DESC.
  'orderBy': "orderBy_example" // String | The sort column to use
};
apiInstance.getResources(opts, (error, data, response) => {
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
 **engineIDs** | **String**| Field to provide the input to get engines by Engine ID list. Separated by commas | [optional] 
 **resourceType** | **String**| Filter by resourceType | [optional] 
 **offset** | **Number**| the number of data to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of items to return. | [optional] [default to 10]
 **direction** | **String**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **orderBy** | **String**| The sort column to use | [optional] 

### Return type

[**GetResourcesResponse**](GetResourcesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getResourcesForEngine

> GetResourcesForEngineResponse getResourcesForEngine(engineID, opts)

Get list of resources for engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let engineID = null; // String | ID of Engine
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getResourcesForEngine(engineID, opts, (error, data, response) => {
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

[**GetResourcesForEngineResponse**](GetResourcesForEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getResourcesForHost

> GetResourcesForHostResponse getResourcesForHost(hostID, opts)

Get list of resources for host

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let hostID = null; // String | ID of Host
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getResourcesForHost(hostID, opts, (error, data, response) => {
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

[**GetResourcesForHostResponse**](GetResourcesForHostResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getResourcesForService

> GetResourcesForServiceResponse getResourcesForService(serviceID, opts)

Get list of resources for service

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serviceID = null; // String | ID of the service
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getResourcesForService(serviceID, opts, (error, data, response) => {
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
 **serviceID** | [**String**](.md)| ID of the service | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetResourcesForServiceResponse**](GetResourcesForServiceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getServerType

> GetServerTypeResponse getServerType(serverTypeID, opts)

This provides detail on the server type

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serverTypeID = null; // String | ID of Server Type
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getServerType(serverTypeID, opts, (error, data, response) => {
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
 **serverTypeID** | [**String**](.md)| ID of Server Type | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetServerTypeResponse**](GetServerTypeResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getServerTypeEngineRunning

> GetServerTypeRunningEnginesResponse getServerTypeEngineRunning(opts)

This lists the running engine with server types

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'serverTypeID': "serverTypeID_example", // String | Filter by serverTypeID
  'engineID': "engineID_example", // String | Filter by engine id
  'offset': 789, // Number | the number of records to skip before getting the result set
  'limit': 100 // Number | the number of records to return.
};
apiInstance.getServerTypeEngineRunning(opts, (error, data, response) => {
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
 **serverTypeID** | **String**| Filter by serverTypeID | [optional] 
 **engineID** | **String**| Filter by engine id | [optional] 
 **offset** | **Number**| the number of records to skip before getting the result set | [optional] 
 **limit** | **Number**| the number of records to return. | [optional] [default to 100]

### Return type

[**GetServerTypeRunningEnginesResponse**](GetServerTypeRunningEnginesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getServerTypeEngineRunningDetail

> GetServerTypeRunningEngineDetailResponse getServerTypeEngineRunningDetail(serverTypeID, engineID, opts)

This gets the detail of server type - running engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serverTypeID = null; // String | ID of Server Type
let engineID = null; // String | ID of Engine
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getServerTypeEngineRunningDetail(serverTypeID, engineID, opts, (error, data, response) => {
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
 **serverTypeID** | [**String**](.md)| ID of Server Type | 
 **engineID** | [**String**](.md)| ID of Engine | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetServerTypeRunningEngineDetailResponse**](GetServerTypeRunningEngineDetailResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getServerTypes

> GetServerTypesResponse getServerTypes(runMode, opts)

This lists the server types available on the system

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let runMode = "runMode_example"; // String | Filer by run mode
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.getServerTypes(runMode, opts, (error, data, response) => {
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
 **runMode** | **String**| Filer by run mode | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetServerTypesResponse**](GetServerTypesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getServices

> GetAdminServicesResponse getServices(opts)

This lists the services available on the system

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'tags': "tags_example" // String | Filter by tags
};
apiInstance.getServices(opts, (error, data, response) => {
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
 **tags** | **String**| Filter by tags | [optional] 

### Return type

[**GetAdminServicesResponse**](GetAdminServicesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## loginUser

> AdminUserLoginResponse loginUser(opts)

This logs a user in if successful

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'adminUserLoginRequest': new AiwareJsClient.AdminUserLoginRequest() // AdminUserLoginRequest | This logs in the user
};
apiInstance.loginUser(opts, (error, data, response) => {
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
 **adminUserLoginRequest** | [**AdminUserLoginRequest**](AdminUserLoginRequest.md)| This logs in the user | [optional] 

### Return type

[**AdminUserLoginResponse**](AdminUserLoginResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## oauthLoginUser

> AdminUserLoginResponse oauthLoginUser(opts)

This logs a user in if successful with OAuth2

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'adminUserOAuth2LoginRequest': new AiwareJsClient.AdminUserOAuth2LoginRequest() // AdminUserOAuth2LoginRequest | This logs in the user with the OAuth2 response
};
apiInstance.oauthLoginUser(opts, (error, data, response) => {
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
 **adminUserOAuth2LoginRequest** | [**AdminUserOAuth2LoginRequest**](AdminUserOAuth2LoginRequest.md)| This logs in the user with the OAuth2 response | [optional] 

### Return type

[**AdminUserLoginResponse**](AdminUserLoginResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## registerUser

> AdminUserRegisterResponse registerUser(adminUserRegisterRequest, opts)

This registers a new user

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let adminUserRegisterRequest = new AiwareJsClient.AdminUserRegisterRequest(); // AdminUserRegisterRequest | The input for registerUser
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.registerUser(adminUserRegisterRequest, opts, (error, data, response) => {
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
 **adminUserRegisterRequest** | [**AdminUserRegisterRequest**](AdminUserRegisterRequest.md)| The input for registerUser | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserRegisterResponse**](AdminUserRegisterResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## removeEngineForResource

> RemoveEngineForResourceResponse removeEngineForResource(resourceID, engineID, opts)

This API removes the engine to the resource

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let resourceID = null; // String | ID of Resource
let engineID = null; // String | ID of Engine
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'removeEngineForResourceRequest': new AiwareJsClient.RemoveEngineForResourceRequest() // RemoveEngineForResourceRequest | Remove Engine Mapping for Resource
};
apiInstance.removeEngineForResource(resourceID, engineID, opts, (error, data, response) => {
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
 **resourceID** | [**String**](.md)| ID of Resource | 
 **engineID** | [**String**](.md)| ID of Engine | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **removeEngineForResourceRequest** | [**RemoveEngineForResourceRequest**](RemoveEngineForResourceRequest.md)| Remove Engine Mapping for Resource | [optional] 

### Return type

[**RemoveEngineForResourceResponse**](RemoveEngineForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## removeserversServerType

> AdminOperationResponse removeserversServerType(serverTypeID, opts)

This API removes servers from the specified server type

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serverTypeID = null; // String | ID of Server Type
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'removeServersToServerTypeRequest': new AiwareJsClient.RemoveServersToServerTypeRequest() // RemoveServersToServerTypeRequest | Update Server Type
};
apiInstance.removeserversServerType(serverTypeID, opts, (error, data, response) => {
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
 **serverTypeID** | [**String**](.md)| ID of Server Type | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **removeServersToServerTypeRequest** | [**RemoveServersToServerTypeRequest**](RemoveServersToServerTypeRequest.md)| Update Server Type | [optional] 

### Return type

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## resetAllocTable

> AdminOperationResponse resetAllocTable(opts)

This resets the alloc table

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.resetAllocTable(opts, (error, data, response) => {
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

[**AdminOperationResponse**](AdminOperationResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## updateApplication

> AdminApplicationUpdateResponse updateApplication(applicationID, adminApplicationUpdateRequest, opts)

This updates an application

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let applicationID = null; // String | ID of Application
let adminApplicationUpdateRequest = new AiwareJsClient.AdminApplicationUpdateRequest(); // AdminApplicationUpdateRequest | The input for updateApplication
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateApplication(applicationID, adminApplicationUpdateRequest, opts, (error, data, response) => {
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
 **applicationID** | [**String**](.md)| ID of Application | 
 **adminApplicationUpdateRequest** | [**AdminApplicationUpdateRequest**](AdminApplicationUpdateRequest.md)| The input for updateApplication | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminApplicationUpdateResponse**](AdminApplicationUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateConfigAll

> AdminConfigUpdateResponse updateConfigAll(adminConfigUpdateRequest, opts)

This gets the config for the cluster

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let adminConfigUpdateRequest = new AiwareJsClient.AdminConfigUpdateRequest(); // AdminConfigUpdateRequest | Config Update for core
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'configSection': new AiwareJsClient.ConfigSectionEnum(), // ConfigSectionEnum | Config Section Entry
  'configKey': "configKey_example", // String | Config Key
  'deprecated': true, // Boolean | 
  'secure': true, // Boolean | 
  'isOverridden': true // Boolean | 
};
apiInstance.updateConfigAll(adminConfigUpdateRequest, opts, (error, data, response) => {
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
 **adminConfigUpdateRequest** | [**AdminConfigUpdateRequest**](AdminConfigUpdateRequest.md)| Config Update for core | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **configSection** | [**ConfigSectionEnum**](.md)| Config Section Entry | [optional] 
 **configKey** | **String**| Config Key | [optional] 
 **deprecated** | **Boolean**|  | [optional] 
 **secure** | **Boolean**|  | [optional] 
 **isOverridden** | **Boolean**|  | [optional] 

### Return type

[**AdminConfigUpdateResponse**](AdminConfigUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateConfigSection

> AdminConfigUpdateSectionResponse updateConfigSection(configSection, adminConfigUpdateSectionRequest, opts)

This gets the config for the cluster

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let configSection = "configSection_example"; // String | Config Section Entry
let adminConfigUpdateSectionRequest = new AiwareJsClient.AdminConfigUpdateSectionRequest(); // AdminConfigUpdateSectionRequest | The input for createConfigSection
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateConfigSection(configSection, adminConfigUpdateSectionRequest, opts, (error, data, response) => {
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
 **configSection** | **String**| Config Section Entry | 
 **adminConfigUpdateSectionRequest** | [**AdminConfigUpdateSectionRequest**](AdminConfigUpdateSectionRequest.md)| The input for createConfigSection | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminConfigUpdateSectionResponse**](AdminConfigUpdateSectionResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/csv, text/html, text/plain


## updateConfigSectionKey

> AdminConfigUpdateSectionKeyResponse updateConfigSectionKey(configSection, configKey, adminConfigUpdateSectionKeyRequest, opts)

This updates the config for the cluster for a given key

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let configSection = "configSection_example"; // String | Config Section Entry
let configKey = "configKey_example"; // String | Config Key
let adminConfigUpdateSectionKeyRequest = new AiwareJsClient.AdminConfigUpdateSectionKeyRequest(); // AdminConfigUpdateSectionKeyRequest | The input for createSectionKey
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateConfigSectionKey(configSection, configKey, adminConfigUpdateSectionKeyRequest, opts, (error, data, response) => {
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
 **configSection** | **String**| Config Section Entry | 
 **configKey** | **String**| Config Key | 
 **adminConfigUpdateSectionKeyRequest** | [**AdminConfigUpdateSectionKeyRequest**](AdminConfigUpdateSectionKeyRequest.md)| The input for createSectionKey | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminConfigUpdateSectionKeyResponse**](AdminConfigUpdateSectionKeyResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/csv, text/html, text/plain


## updateEnginesForResource

> UpdateEnginesForResourceResponse updateEnginesForResource(resourceID, opts)

This API updates the specified server type-running engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let resourceID = null; // String | ID of Resource
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'updateEnginesForResourceRequest': new AiwareJsClient.UpdateEnginesForResourceRequest() // UpdateEnginesForResourceRequest | Update Engine Mapping for Resource
};
apiInstance.updateEnginesForResource(resourceID, opts, (error, data, response) => {
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
 **resourceID** | [**String**](.md)| ID of Resource | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **updateEnginesForResourceRequest** | [**UpdateEnginesForResourceRequest**](UpdateEnginesForResourceRequest.md)| Update Engine Mapping for Resource | [optional] 

### Return type

[**UpdateEnginesForResourceResponse**](UpdateEnginesForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateOrganization

> AdminOrganizationUpdateResponse updateOrganization(organizationID, adminOrganizationUpdateRequest, opts)

This updates a organization

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let organizationID = null; // String | ID of Organization
let adminOrganizationUpdateRequest = new AiwareJsClient.AdminOrganizationUpdateRequest(); // AdminOrganizationUpdateRequest | The input for updateOrganization
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateOrganization(organizationID, adminOrganizationUpdateRequest, opts, (error, data, response) => {
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
 **organizationID** | [**String**](.md)| ID of Organization | 
 **adminOrganizationUpdateRequest** | [**AdminOrganizationUpdateRequest**](AdminOrganizationUpdateRequest.md)| The input for updateOrganization | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOrganizationUpdateResponse**](AdminOrganizationUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updatePermission

> AdminPermissionUpdateResponse updatePermission(permissionID, adminPermissionUpdateRequest, opts)

This updates a permission

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let permissionID = null; // String | ID of Permission
let adminPermissionUpdateRequest = new AiwareJsClient.AdminPermissionUpdateRequest(); // AdminPermissionUpdateRequest | The input for updatePermission
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updatePermission(permissionID, adminPermissionUpdateRequest, opts, (error, data, response) => {
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
 **permissionID** | [**String**](.md)| ID of Permission | 
 **adminPermissionUpdateRequest** | [**AdminPermissionUpdateRequest**](AdminPermissionUpdateRequest.md)| The input for updatePermission | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminPermissionUpdateResponse**](AdminPermissionUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateResource

> UpdateResourceResponse updateResource(resourceID, updateResourceRequest, opts)

This API updates the specified resource

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let resourceID = null; // String | ID of Resource
let updateResourceRequest = new AiwareJsClient.UpdateResourceRequest(); // UpdateResourceRequest | Update Resource
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateResource(resourceID, updateResourceRequest, opts, (error, data, response) => {
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
 **resourceID** | [**String**](.md)| ID of Resource | 
 **updateResourceRequest** | [**UpdateResourceRequest**](UpdateResourceRequest.md)| Update Resource | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**UpdateResourceResponse**](UpdateResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateResourceState

> updateResourceState(resourceID, updateResourceStateRequest, opts)

This API updates the state of the specified resource

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let resourceID = null; // String | ID of Resource
let updateResourceStateRequest = new AiwareJsClient.UpdateResourceStateRequest(); // UpdateResourceStateRequest | Update Resource State
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateResourceState(resourceID, updateResourceStateRequest, opts, (error, data, response) => {
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
 **resourceID** | [**String**](.md)| ID of Resource | 
 **updateResourceStateRequest** | [**UpdateResourceStateRequest**](UpdateResourceStateRequest.md)| Update Resource State | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

null (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateRole

> AdminRoleUpdateResponse updateRole(roleID, adminRoleUpdateRequest, opts)

This updates a role

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let roleID = null; // String | ID of Role
let adminRoleUpdateRequest = new AiwareJsClient.AdminRoleUpdateRequest(); // AdminRoleUpdateRequest | The input for updateRole
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateRole(roleID, adminRoleUpdateRequest, opts, (error, data, response) => {
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
 **roleID** | [**String**](.md)| ID of Role | 
 **adminRoleUpdateRequest** | [**AdminRoleUpdateRequest**](AdminRoleUpdateRequest.md)| The input for updateRole | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminRoleUpdateResponse**](AdminRoleUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateServerType

> UpdateServerTypeResponse updateServerType(serverTypeID, opts)

This API updates the specified server type

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serverTypeID = null; // String | ID of Server Type
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'serverTypeDetail': new AiwareJsClient.ServerTypeDetail() // ServerTypeDetail | Update Server Type
};
apiInstance.updateServerType(serverTypeID, opts, (error, data, response) => {
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
 **serverTypeID** | [**String**](.md)| ID of Server Type | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **serverTypeDetail** | [**ServerTypeDetail**](ServerTypeDetail.md)| Update Server Type | [optional] 

### Return type

[**UpdateServerTypeResponse**](UpdateServerTypeResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateServerTypeEngineRunning

> UpdateServerTypeEngineRunningResponse updateServerTypeEngineRunning(serverTypeID, engineID, opts)

This API updates the specified server type-running engine

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let serverTypeID = null; // String | ID of Server Type
let engineID = null; // String | ID of Engine
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'updateServerTypeEngineRunningRequest': new AiwareJsClient.UpdateServerTypeEngineRunningRequest() // UpdateServerTypeEngineRunningRequest | Update Server Type - Running Engine
};
apiInstance.updateServerTypeEngineRunning(serverTypeID, engineID, opts, (error, data, response) => {
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
 **serverTypeID** | [**String**](.md)| ID of Server Type | 
 **engineID** | [**String**](.md)| ID of Engine | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **updateServerTypeEngineRunningRequest** | [**UpdateServerTypeEngineRunningRequest**](UpdateServerTypeEngineRunningRequest.md)| Update Server Type - Running Engine | [optional] 

### Return type

[**UpdateServerTypeEngineRunningResponse**](UpdateServerTypeEngineRunningResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateToken

> AdminTokenUpdateResponse updateToken(tokenID, adminTokenUpdateRequest, opts)

This updates a token

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let tokenID = null; // String | ID of Token
let adminTokenUpdateRequest = new AiwareJsClient.AdminTokenUpdateRequest(); // AdminTokenUpdateRequest | The input for updateToken
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateToken(tokenID, adminTokenUpdateRequest, opts, (error, data, response) => {
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
 **tokenID** | [**String**](.md)| ID of Token | 
 **adminTokenUpdateRequest** | [**AdminTokenUpdateRequest**](AdminTokenUpdateRequest.md)| The input for updateToken | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminTokenUpdateResponse**](AdminTokenUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateUser

> AdminUserUpdateResponse updateUser(userID, adminUserUpdateRequest, opts)

This updates a user

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let userID = null; // String | ID of User
let adminUserUpdateRequest = new AiwareJsClient.AdminUserUpdateRequest(); // AdminUserUpdateRequest | The input for updateUser
let opts = {
  'xCorrelationId': "xCorrelationId_example" // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
};
apiInstance.updateUser(userID, adminUserUpdateRequest, opts, (error, data, response) => {
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
 **userID** | [**String**](.md)| ID of User | 
 **adminUserUpdateRequest** | [**AdminUserUpdateRequest**](AdminUserUpdateRequest.md)| The input for updateUser | 
 **xCorrelationId** | **String**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserUpdateResponse**](AdminUserUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## userPasswordForgot

> AdminUserPasswordForgotResponse userPasswordForgot(opts)

This api will help users to reset their password when they forgot

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'adminUserPasswordForgotRequest': new AiwareJsClient.AdminUserPasswordForgotRequest() // AdminUserPasswordForgotRequest | Needs to provide the info to reset user's password when they forgot
};
apiInstance.userPasswordForgot(opts, (error, data, response) => {
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
 **adminUserPasswordForgotRequest** | [**AdminUserPasswordForgotRequest**](AdminUserPasswordForgotRequest.md)| Needs to provide the info to reset user&#39;s password when they forgot | [optional] 

### Return type

[**AdminUserPasswordForgotResponse**](AdminUserPasswordForgotResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## userPasswordReset

> AdminUserPasswordResetResponse userPasswordReset(opts)

Helps users to reset their password

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'adminUserPasswordResetRequest': new AiwareJsClient.AdminUserPasswordResetRequest() // AdminUserPasswordResetRequest | Needs to provide the info to reset password
};
apiInstance.userPasswordReset(opts, (error, data, response) => {
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
 **adminUserPasswordResetRequest** | [**AdminUserPasswordResetRequest**](AdminUserPasswordResetRequest.md)| Needs to provide the info to reset password | [optional] 

### Return type

[**AdminUserPasswordResetResponse**](AdminUserPasswordResetResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## userPasswordUpdate

> AdminUserPasswordUpdateResponse userPasswordUpdate(opts)

This api will help users to update their password

### Example

```javascript
import AiwareJsClient from 'aiware-js-client';
let defaultClient = AiwareJsClient.ApiClient.instance;
// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new AiwareJsClient.AdminApi();
let opts = {
  'xCorrelationId': "xCorrelationId_example", // String | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request
  'adminUserPasswordUpdateRequest': new AiwareJsClient.AdminUserPasswordUpdateRequest() // AdminUserPasswordUpdateRequest | Users provide the password info to change
};
apiInstance.userPasswordUpdate(opts, (error, data, response) => {
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
 **adminUserPasswordUpdateRequest** | [**AdminUserPasswordUpdateRequest**](AdminUserPasswordUpdateRequest.md)| Users provide the password info to change | [optional] 

### Return type

[**AdminUserPasswordUpdateResponse**](AdminUserPasswordUpdateResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

