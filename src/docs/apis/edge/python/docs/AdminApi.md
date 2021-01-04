# client.AdminApi

All URIs are relative to *https://api.aiware.com/edge/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_engine_to_resource**](AdminApi.md#add_engine_to_resource) | **POST** /admin/resource/{ResourceID}/engine | This API adds the engine to the resource
[**add_service_to_resource**](AdminApi.md#add_service_to_resource) | **POST** /admin/resource/{ResourceID}/service | This API adds the service to the resource
[**addservers_server_type**](AdminApi.md#addservers_server_type) | **POST** /admin/server_type/{ServerTypeID}/add | This API add servers to the specified server type
[**admin_terminate_cluster**](AdminApi.md#admin_terminate_cluster) | **POST** /admin/terminate | This terminates the cluster
[**apply_license**](AdminApi.md#apply_license) | **POST** /admin/licenses/apply | This applies a license to aiWARE
[**check_auth**](AdminApi.md#check_auth) | **POST** /admin/auth | This check auth for a token
[**clear_backlog**](AdminApi.md#clear_backlog) | **POST** /admin/backlog/clear | This clears some or all of the currently queued tasks
[**create_admin_application**](AdminApi.md#create_admin_application) | **POST** /admin/applications/create | This creates a new application
[**create_admin_core**](AdminApi.md#create_admin_core) | **POST** /admin/cores/create | This creates a new core
[**create_admin_organization**](AdminApi.md#create_admin_organization) | **POST** /admin/organizations/create | This updates the config for the cluster for a given key
[**create_permission**](AdminApi.md#create_permission) | **POST** /admin/users/permission/create | This creates a new permission
[**create_resource**](AdminApi.md#create_resource) | **POST** /admin/resource/create | This API creates a new resource definition such as a database, nsq or redis DB.
[**create_role**](AdminApi.md#create_role) | **POST** /admin/users/role/create | This creates a new role
[**create_server_type**](AdminApi.md#create_server_type) | **POST** /admin/server_types/create | This creates a new server type
[**create_server_type_engine_running**](AdminApi.md#create_server_type_engine_running) | **POST** /admin/server_types/running_engine/create | This creates a new server_type_engine_running
[**create_token**](AdminApi.md#create_token) | **POST** /admin/tokens/create | This creates a new token
[**create_user**](AdminApi.md#create_user) | **POST** /admin/users/create | This creates a new user
[**delete_application**](AdminApi.md#delete_application) | **POST** /admin/applications/{ApplicationID}/delete | This deletes an application
[**delete_license**](AdminApi.md#delete_license) | **DELETE** /admin/licenses/{LicenseID}/delete | This deletes a license from aiWARE
[**delete_resource**](AdminApi.md#delete_resource) | **POST** /admin/resource/{ResourceID}/delete | This deletes the specified resource
[**delete_role**](AdminApi.md#delete_role) | **POST** /admin/users/role/{RoleID}/delete | This deletes a role
[**delete_server_type**](AdminApi.md#delete_server_type) | **DELETE** /admin/server_type/{ServerTypeID}/delete | This API deletes the specified server type
[**delete_server_type_post**](AdminApi.md#delete_server_type_post) | **POST** /admin/server_type/{ServerTypeID}/delete | This API deletes the specified server type
[**delete_server_type_running_engine**](AdminApi.md#delete_server_type_running_engine) | **DELETE** /admin/server_type/{ServerTypeID}/engine/{EngineID}/delete | This API deletes the running engine for a server type
[**delete_token**](AdminApi.md#delete_token) | **POST** /admin/token/{TokenID}/delete | This deletes a token
[**delete_user**](AdminApi.md#delete_user) | **POST** /admin/user/{UserID}/delete | This deletes a user
[**desiredservers_server_type**](AdminApi.md#desiredservers_server_type) | **POST** /admin/server_type/{ServerTypeID}/desired | This API add servers to the specified server type
[**get_admin_application_detail**](AdminApi.md#get_admin_application_detail) | **GET** /admin/applications/{ApplicationID}/detail | This provides information on the given application.
[**get_admin_core_detail**](AdminApi.md#get_admin_core_detail) | **GET** /admin/core/{CoreID}/detail | This provides information on the given core.
[**get_admin_cores**](AdminApi.md#get_admin_cores) | **GET** /admin/cores | This provides a list of core systems
[**get_admin_engine_config_section_key**](AdminApi.md#get_admin_engine_config_section_key) | **GET** /admin/engine/{EngineID}/config/{ConfigSection}/{ConfigKey} | This provides a config section key for the engine
[**get_admin_organization_detail**](AdminApi.md#get_admin_organization_detail) | **GET** /admin/organization/{OrganizationID}/detail | This gets organization detail by ID
[**get_admin_organization_tokens**](AdminApi.md#get_admin_organization_tokens) | **GET** /admin/organization/{OrganizationID}/tokens | This provides information on the given organization tokens.
[**get_admin_organizations**](AdminApi.md#get_admin_organizations) | **GET** /admin/organizations | This provides a list of organizations
[**get_admin_permission_detail**](AdminApi.md#get_admin_permission_detail) | **GET** /admin/users/permission/{PermissionID}/detail | This gets permission detail by ID
[**get_admin_role_detail**](AdminApi.md#get_admin_role_detail) | **GET** /admin/users/role/{RoleID}/detail | This gets role detail by ID
[**get_admin_service_config**](AdminApi.md#get_admin_service_config) | **GET** /admin/service/{ServiceID}/config | This provides all the config for the service
[**get_admin_service_config_section**](AdminApi.md#get_admin_service_config_section) | **GET** /admin/service/{ServiceID}/config/{ConfigSection} | This provides all the config for the service
[**get_admin_service_config_section_key**](AdminApi.md#get_admin_service_config_section_key) | **GET** /admin/service/{ServiceID}/config/{ConfigSection}/{ConfigKey} | This provides a config section key for the service
[**get_admin_service_instances**](AdminApi.md#get_admin_service_instances) | **GET** /admin/service/instances | This lists the service instances available for a system
[**get_admin_status**](AdminApi.md#get_admin_status) | **GET** /admin/status | This provides information on the status of the aiWARE edge
[**get_admin_token_detail**](AdminApi.md#get_admin_token_detail) | **GET** /admin/token/{TokenID}/detail | Get the token info by ID
[**get_admin_token_permissions**](AdminApi.md#get_admin_token_permissions) | **GET** /admin/token/{TokenID}/permissions | This provides a list of all token permissions for a token by TokenID
[**get_admin_tokens**](AdminApi.md#get_admin_tokens) | **GET** /admin/tokens | This provides information about all tokens.
[**get_admin_user_detail**](AdminApi.md#get_admin_user_detail) | **GET** /admin/user/{UserID}/detail | This provides information on the given user.
[**get_admin_user_permissions**](AdminApi.md#get_admin_user_permissions) | **GET** /admin/user/{UserID}/permissions | This provides a list of all user permissions for an user by UserID
[**get_admin_user_tokens**](AdminApi.md#get_admin_user_tokens) | **GET** /admin/user/{UserID}/tokens | This provides information on the given user.
[**get_admin_users**](AdminApi.md#get_admin_users) | **GET** /admin/users | This provides a list of users in the system
[**get_admin_users_permission**](AdminApi.md#get_admin_users_permission) | **GET** /admin/users/permissions | This provides a list of all user permissions in the system
[**get_admin_users_roles**](AdminApi.md#get_admin_users_roles) | **GET** /admin/users/roles | This provides a list of user role in the system
[**get_applications**](AdminApi.md#get_applications) | **GET** /admin/applications | Get the list of applications deployed and available on aiWARE
[**get_backlog_summary**](AdminApi.md#get_backlog_summary) | **GET** /admin/backlog/summary | This provides summary information on the current backlog
[**get_config**](AdminApi.md#get_config) | **GET** /admin/config | This provides all the config for the cluster
[**get_config_section**](AdminApi.md#get_config_section) | **GET** /admin/config/{ConfigSection} | This provides all the config for the cluster
[**get_config_section_key**](AdminApi.md#get_config_section_key) | **GET** /admin/config/{ConfigSection}/{ConfigKey} | This provides a config section key for the cluster
[**get_engines_for_resource**](AdminApi.md#get_engines_for_resource) | **GET** /admin/resource/{ResourceID}/engines | Get list of engines for resource
[**get_license_detail**](AdminApi.md#get_license_detail) | **GET** /admin/licenses/{LicenseID}/detail | This gets detail on a license key
[**get_licenses**](AdminApi.md#get_licenses) | **GET** /admin/licenses | This provides a licenses on the system
[**get_resource**](AdminApi.md#get_resource) | **GET** /admin/resource/{ResourceID} | Get a resource definition
[**get_resources**](AdminApi.md#get_resources) | **GET** /admin/resources | Get the list of resources
[**get_resources_for_engine**](AdminApi.md#get_resources_for_engine) | **GET** /admin/engine/{EngineID}/resources | Get list of resources for engine
[**get_resources_for_host**](AdminApi.md#get_resources_for_host) | **GET** /admin/host/{HostID}/resources | Get list of resources for host
[**get_resources_for_service**](AdminApi.md#get_resources_for_service) | **GET** /admin/service/{ServiceID}/resources | Get list of resources for service
[**get_server_type**](AdminApi.md#get_server_type) | **GET** /admin/server_type/{ServerTypeID}/detail | This provides detail on the server type
[**get_server_type_engine_running**](AdminApi.md#get_server_type_engine_running) | **GET** /admin/server_types/running_engines | This lists the running engine with server types
[**get_server_type_engine_running_detail**](AdminApi.md#get_server_type_engine_running_detail) | **GET** /admin/server_type/{ServerTypeID}/engine/{EngineID}/detail | This gets the detail of server type - running engine
[**get_server_types**](AdminApi.md#get_server_types) | **GET** /admin/server_types | This lists the server types available on the system
[**get_services**](AdminApi.md#get_services) | **GET** /admin/services | This lists the services available on the system
[**login_user**](AdminApi.md#login_user) | **POST** /admin/users/login | This logs a user in if successful
[**oauth_login_user**](AdminApi.md#oauth_login_user) | **POST** /admin/users/oauth2_login | This logs a user in if successful with OAuth2
[**register_user**](AdminApi.md#register_user) | **POST** /admin/users/register | This registers a new user
[**remove_engine_for_resource**](AdminApi.md#remove_engine_for_resource) | **POST** /admin/resource/{ResourceID}/engine/{EngineID}/delete | This API removes the engine to the resource
[**removeservers_server_type**](AdminApi.md#removeservers_server_type) | **POST** /admin/server_type/{ServerTypeID}/remove | This API removes servers from the specified server type
[**reset_alloc_table**](AdminApi.md#reset_alloc_table) | **POST** /admin/backlog/reset-alloc | This resets the alloc table
[**update_application**](AdminApi.md#update_application) | **POST** /admin/applications/{ApplicationID}/update | This updates an application
[**update_config_all**](AdminApi.md#update_config_all) | **POST** /admin/config | This gets the config for the cluster
[**update_config_section**](AdminApi.md#update_config_section) | **POST** /admin/config/{ConfigSection} | This gets the config for the cluster
[**update_config_section_key**](AdminApi.md#update_config_section_key) | **POST** /admin/config/{ConfigSection}/{ConfigKey} | This updates the config for the cluster for a given key
[**update_engines_for_resource**](AdminApi.md#update_engines_for_resource) | **POST** /admin/resource/{ResourceID}/engine/update | This API updates the specified server type-running engine
[**update_organization**](AdminApi.md#update_organization) | **POST** /admin/organization/{OrganizationID}/update | This updates a organization
[**update_permission**](AdminApi.md#update_permission) | **POST** /admin/users/permission/{PermissionID}/update | This updates a permission
[**update_resource**](AdminApi.md#update_resource) | **POST** /admin/resource/{ResourceID}/update | This API updates the specified resource
[**update_resource_state**](AdminApi.md#update_resource_state) | **POST** /admin/resource/{ResourceID}/updatestate | This API updates the state of the specified resource
[**update_role**](AdminApi.md#update_role) | **POST** /admin/users/role/{RoleID}/update | This updates a role
[**update_server_type**](AdminApi.md#update_server_type) | **POST** /admin/server_type/{ServerTypeID}/update | This API updates the specified server type
[**update_server_type_engine_running**](AdminApi.md#update_server_type_engine_running) | **POST** /admin/server_type/{ServerTypeID}/engine/{EngineID}/update | This API updates the specified server type-running engine
[**update_token**](AdminApi.md#update_token) | **POST** /admin/token/{TokenID}/update | This updates a token
[**update_user**](AdminApi.md#update_user) | **POST** /admin/user/{UserID}/update | This updates a user
[**user_password_forgot**](AdminApi.md#user_password_forgot) | **POST** /admin/users/password/forgot | This api will help users to reset their password when they forgot
[**user_password_reset**](AdminApi.md#user_password_reset) | **POST** /admin/users/password/reset | Helps users to reset their password
[**user_password_update**](AdminApi.md#user_password_update) | **POST** /admin/users/password/update | This api will help users to update their password


# **add_engine_to_resource**
> AddEngineForResourceResponse add_engine_to_resource(resource_id, x_correlation_id=x_correlation_id, add_engine_for_resource_request=add_engine_for_resource_request)

This API adds the engine to the resource

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    resource_id = 'resource_id_example' # str | ID of Resource
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
add_engine_for_resource_request = client.AddEngineForResourceRequest() # AddEngineForResourceRequest | Add Engine Mapping for Resource (optional)

    try:
        # This API adds the engine to the resource
        api_response = api_instance.add_engine_to_resource(resource_id, x_correlation_id=x_correlation_id, add_engine_for_resource_request=add_engine_for_resource_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->add_engine_to_resource: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resource_id** | [**str**](.md)| ID of Resource | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **add_engine_for_resource_request** | [**AddEngineForResourceRequest**](AddEngineForResourceRequest.md)| Add Engine Mapping for Resource | [optional] 

### Return type

[**AddEngineForResourceResponse**](AddEngineForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The response of UpdateEngineMappingForResource |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_service_to_resource**
> AddServiceForResourceResponse add_service_to_resource(resource_id, x_correlation_id=x_correlation_id, add_service_for_resource_request=add_service_for_resource_request)

This API adds the service to the resource

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    resource_id = 'resource_id_example' # str | ID of Resource
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
add_service_for_resource_request = client.AddServiceForResourceRequest() # AddServiceForResourceRequest | Add Service Mapping for Resource (optional)

    try:
        # This API adds the service to the resource
        api_response = api_instance.add_service_to_resource(resource_id, x_correlation_id=x_correlation_id, add_service_for_resource_request=add_service_for_resource_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->add_service_to_resource: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resource_id** | [**str**](.md)| ID of Resource | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **add_service_for_resource_request** | [**AddServiceForResourceRequest**](AddServiceForResourceRequest.md)| Add Service Mapping for Resource | [optional] 

### Return type

[**AddServiceForResourceResponse**](AddServiceForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The response of AddEngineForResourceResponse |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **addservers_server_type**
> AdminOperationResponse addservers_server_type(server_type_id, x_correlation_id=x_correlation_id, add_servers_to_server_type_request=add_servers_to_server_type_request)

This API add servers to the specified server type

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    server_type_id = 'server_type_id_example' # str | ID of Server Type
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
add_servers_to_server_type_request = client.AddServersToServerTypeRequest() # AddServersToServerTypeRequest | Add Servers Server Type (optional)

    try:
        # This API add servers to the specified server type
        api_response = api_instance.addservers_server_type(server_type_id, x_correlation_id=x_correlation_id, add_servers_to_server_type_request=add_servers_to_server_type_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->addservers_server_type: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_type_id** | [**str**](.md)| ID of Server Type | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **add_servers_to_server_type_request** | [**AddServersToServerTypeRequest**](AddServersToServerTypeRequest.md)| Add Servers Server Type | [optional] 

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
**200** | List of engines |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **admin_terminate_cluster**
> admin_terminate_cluster(x_correlation_id=x_correlation_id, admin_operation_request=admin_operation_request)

This terminates the cluster

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
admin_operation_request = client.AdminOperationRequest() # AdminOperationRequest | ClusterID (optional)

    try:
        # This terminates the cluster
        api_instance.admin_terminate_cluster(x_correlation_id=x_correlation_id, admin_operation_request=admin_operation_request)
    except ApiException as e:
        print("Exception when calling AdminApi->admin_terminate_cluster: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **admin_operation_request** | [**AdminOperationRequest**](AdminOperationRequest.md)| ClusterID | [optional] 

### Return type

void (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **apply_license**
> LicenseDetail apply_license(x_correlation_id=x_correlation_id, create_license_detail=create_license_detail)

This applies a license to aiWARE

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
create_license_detail = client.CreateLicenseDetail() # CreateLicenseDetail |  (optional)

    try:
        # This applies a license to aiWARE
        api_response = api_instance.apply_license(x_correlation_id=x_correlation_id, create_license_detail=create_license_detail)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->apply_license: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **create_license_detail** | [**CreateLicenseDetail**](CreateLicenseDetail.md)|  | [optional] 

### Return type

[**LicenseDetail**](LicenseDetail.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful operation |  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **check_auth**
> AdminAuthResponse check_auth(admin_auth_request, x_correlation_id=x_correlation_id)

This check auth for a token

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    admin_auth_request = client.AdminAuthRequest() # AdminAuthRequest | The input for check auth
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This check auth for a token
        api_response = api_instance.check_auth(admin_auth_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->check_auth: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **admin_auth_request** | [**AdminAuthRequest**](AdminAuthRequest.md)| The input for check auth | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminAuthResponse**](AdminAuthResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clear_backlog**
> AdminCoreCreateResponse clear_backlog(x_correlation_id=x_correlation_id, status=status, engine_id=engine_id, modified_before=modified_before, modified_after=modified_after, created_before=created_before, created_after=created_after)

This clears some or all of the currently queued tasks

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
status = client.EngineStatusEnum() # EngineStatusEnum | Field to match the current status (optional)
engine_id = 'engine_id_example' # str | Filter by engine id (optional)
modified_before = 56 # int | Filter by items modified before expressed as timestamp (optional)
modified_after = 56 # int | Filter by items modified after expressed as timestamp (optional)
created_before = 56 # int | Filter items where created date is before this date (optional)
created_after = 56 # int | Filter items where created date is after this date (optional)

    try:
        # This clears some or all of the currently queued tasks
        api_response = api_instance.clear_backlog(x_correlation_id=x_correlation_id, status=status, engine_id=engine_id, modified_before=modified_before, modified_after=modified_after, created_before=created_before, created_after=created_after)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->clear_backlog: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **status** | [**EngineStatusEnum**](.md)| Field to match the current status | [optional] 
 **engine_id** | **str**| Filter by engine id | [optional] 
 **modified_before** | **int**| Filter by items modified before expressed as timestamp | [optional] 
 **modified_after** | **int**| Filter by items modified after expressed as timestamp | [optional] 
 **created_before** | **int**| Filter items where created date is before this date | [optional] 
 **created_after** | **int**| Filter items where created date is after this date | [optional] 

### Return type

[**AdminCoreCreateResponse**](AdminCoreCreateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_admin_application**
> AdminApplicationCreateResponse create_admin_application(admin_application_create_request, x_correlation_id=x_correlation_id)

This creates a new application

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    admin_application_create_request = client.AdminApplicationCreateRequest() # AdminApplicationCreateRequest | The input for createApplication
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This creates a new application
        api_response = api_instance.create_admin_application(admin_application_create_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->create_admin_application: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **admin_application_create_request** | [**AdminApplicationCreateRequest**](AdminApplicationCreateRequest.md)| The input for createApplication | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminApplicationCreateResponse**](AdminApplicationCreateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_admin_core**
> AdminCoreCreateResponse create_admin_core(admin_core_create_request, x_correlation_id=x_correlation_id)

This creates a new core

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    admin_core_create_request = client.AdminCoreCreateRequest() # AdminCoreCreateRequest | The input for createCor
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This creates a new core
        api_response = api_instance.create_admin_core(admin_core_create_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->create_admin_core: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **admin_core_create_request** | [**AdminCoreCreateRequest**](AdminCoreCreateRequest.md)| The input for createCor | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminCoreCreateResponse**](AdminCoreCreateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_admin_organization**
> AdminOrganizationCreateResponse create_admin_organization(admin_organization_create_request, x_correlation_id=x_correlation_id)

This updates the config for the cluster for a given key

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    admin_organization_create_request = client.AdminOrganizationCreateRequest() # AdminOrganizationCreateRequest | The input for createOrganization
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This updates the config for the cluster for a given key
        api_response = api_instance.create_admin_organization(admin_organization_create_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->create_admin_organization: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **admin_organization_create_request** | [**AdminOrganizationCreateRequest**](AdminOrganizationCreateRequest.md)| The input for createOrganization | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOrganizationCreateResponse**](AdminOrganizationCreateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_permission**
> AdminPermissionCreateResponse create_permission(admin_permission_create_request, x_correlation_id=x_correlation_id)

This creates a new permission

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    admin_permission_create_request = client.AdminPermissionCreateRequest() # AdminPermissionCreateRequest | The input for createPermission
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This creates a new permission
        api_response = api_instance.create_permission(admin_permission_create_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->create_permission: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **admin_permission_create_request** | [**AdminPermissionCreateRequest**](AdminPermissionCreateRequest.md)| The input for createPermission | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminPermissionCreateResponse**](AdminPermissionCreateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_resource**
> CreateResourceResponse create_resource(create_resource_request, x_correlation_id=x_correlation_id)

This API creates a new resource definition such as a database, nsq or redis DB.

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    create_resource_request = client.CreateResourceRequest() # CreateResourceRequest | The fields for a resource definition
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API creates a new resource definition such as a database, nsq or redis DB.
        api_response = api_instance.create_resource(create_resource_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->create_resource: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_resource_request** | [**CreateResourceRequest**](CreateResourceRequest.md)| The fields for a resource definition | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateResourceResponse**](CreateResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of the Create Resource API |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_role**
> AdminRoleCreateResponse create_role(admin_role_create_request, x_correlation_id=x_correlation_id)

This creates a new role

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    admin_role_create_request = client.AdminRoleCreateRequest() # AdminRoleCreateRequest | The input for createRole
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This creates a new role
        api_response = api_instance.create_role(admin_role_create_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->create_role: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **admin_role_create_request** | [**AdminRoleCreateRequest**](AdminRoleCreateRequest.md)| The input for createRole | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminRoleCreateResponse**](AdminRoleCreateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_server_type**
> CreateServerTypeResponse create_server_type(create_server_type_request, x_correlation_id=x_correlation_id)

This creates a new server type

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    create_server_type_request = client.CreateServerTypeRequest() # CreateServerTypeRequest | The input for createServerType
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This creates a new server type
        api_response = api_instance.create_server_type(create_server_type_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->create_server_type: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_server_type_request** | [**CreateServerTypeRequest**](CreateServerTypeRequest.md)| The input for createServerType | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateServerTypeResponse**](CreateServerTypeResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_server_type_engine_running**
> CreateServerTypeEngineRunningResponse create_server_type_engine_running(create_server_type_engine_running_request, x_correlation_id=x_correlation_id)

This creates a new server_type_engine_running

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    create_server_type_engine_running_request = client.CreateServerTypeEngineRunningRequest() # CreateServerTypeEngineRunningRequest | The input for createServerTypeEngineRunning
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This creates a new server_type_engine_running
        api_response = api_instance.create_server_type_engine_running(create_server_type_engine_running_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->create_server_type_engine_running: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_server_type_engine_running_request** | [**CreateServerTypeEngineRunningRequest**](CreateServerTypeEngineRunningRequest.md)| The input for createServerTypeEngineRunning | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**CreateServerTypeEngineRunningResponse**](CreateServerTypeEngineRunningResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_token**
> AdminTokenCreateResponse create_token(admin_token_create_request, x_correlation_id=x_correlation_id)

This creates a new token

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    admin_token_create_request = client.AdminTokenCreateRequest() # AdminTokenCreateRequest | The input for createToken
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This creates a new token
        api_response = api_instance.create_token(admin_token_create_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->create_token: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **admin_token_create_request** | [**AdminTokenCreateRequest**](AdminTokenCreateRequest.md)| The input for createToken | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminTokenCreateResponse**](AdminTokenCreateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_user**
> AdminUserCreateResponse create_user(admin_user_create_request, x_correlation_id=x_correlation_id)

This creates a new user

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    admin_user_create_request = client.AdminUserCreateRequest() # AdminUserCreateRequest | The input for createUser
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This creates a new user
        api_response = api_instance.create_user(admin_user_create_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->create_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **admin_user_create_request** | [**AdminUserCreateRequest**](AdminUserCreateRequest.md)| The input for createUser | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserCreateResponse**](AdminUserCreateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_application**
> AdminApplicationDeleteResponse delete_application(application_id, x_correlation_id=x_correlation_id)

This deletes an application

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    application_id = 'application_id_example' # str | ID of Application
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This deletes an application
        api_response = api_instance.delete_application(application_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->delete_application: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_id** | [**str**](.md)| ID of Application | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminApplicationDeleteResponse**](AdminApplicationDeleteResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_license**
> AdminOperationResponse delete_license(license_id, x_correlation_id=x_correlation_id)

This deletes a license from aiWARE

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    license_id = 'license_id_example' # str | License ID
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This deletes a license from aiWARE
        api_response = api_instance.delete_license(license_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->delete_license: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **license_id** | **str**| License ID | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_resource**
> AdminOperationResponse delete_resource(resource_id, x_correlation_id=x_correlation_id)

This deletes the specified resource

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    resource_id = 'resource_id_example' # str | ID of Resource
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This deletes the specified resource
        api_response = api_instance.delete_resource(resource_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->delete_resource: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resource_id** | [**str**](.md)| ID of Resource | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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
**204** | Delete a particular resource |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_role**
> AdminRoleDeleteResponse delete_role(role_id, x_correlation_id=x_correlation_id)

This deletes a role

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    role_id = 'role_id_example' # str | ID of Role
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This deletes a role
        api_response = api_instance.delete_role(role_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->delete_role: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **role_id** | [**str**](.md)| ID of Role | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminRoleDeleteResponse**](AdminRoleDeleteResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_server_type**
> AdminOperationResponse delete_server_type(server_type_id, x_correlation_id=x_correlation_id)

This API deletes the specified server type

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    server_type_id = 'server_type_id_example' # str | ID of Server Type
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API deletes the specified server type
        api_response = api_instance.delete_server_type(server_type_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->delete_server_type: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_type_id** | [**str**](.md)| ID of Server Type | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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
**200** | Delete a particular server type |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_server_type_post**
> AdminOperationResponse delete_server_type_post(server_type_id, x_correlation_id=x_correlation_id, delete_server_type_request=delete_server_type_request)

This API deletes the specified server type

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    server_type_id = 'server_type_id_example' # str | ID of Server Type
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
delete_server_type_request = client.DeleteServerTypeRequest() # DeleteServerTypeRequest | Engine Instance Info (optional)

    try:
        # This API deletes the specified server type
        api_response = api_instance.delete_server_type_post(server_type_id, x_correlation_id=x_correlation_id, delete_server_type_request=delete_server_type_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->delete_server_type_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_type_id** | [**str**](.md)| ID of Server Type | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **delete_server_type_request** | [**DeleteServerTypeRequest**](DeleteServerTypeRequest.md)| Engine Instance Info | [optional] 

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
**204** | Delete a particular engine |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_server_type_running_engine**
> AdminOperationResponse delete_server_type_running_engine(server_type_id, engine_id, x_correlation_id=x_correlation_id)

This API deletes the running engine for a server type

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    server_type_id = 'server_type_id_example' # str | ID of Server Type
engine_id = 'engine_id_example' # str | ID of Engine
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API deletes the running engine for a server type
        api_response = api_instance.delete_server_type_running_engine(server_type_id, engine_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->delete_server_type_running_engine: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_type_id** | [**str**](.md)| ID of Server Type | 
 **engine_id** | [**str**](.md)| ID of Engine | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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
**200** | The response for delete server type-running engine |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_token**
> AdminTokenDeleteResponse delete_token(token_id, x_correlation_id=x_correlation_id)

This deletes a token

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    token_id = 'token_id_example' # str | ID of Token
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This deletes a token
        api_response = api_instance.delete_token(token_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->delete_token: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token_id** | [**str**](.md)| ID of Token | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminTokenDeleteResponse**](AdminTokenDeleteResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_user**
> AdminUserDeleteResponse delete_user(user_id, x_correlation_id=x_correlation_id)

This deletes a user

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    user_id = 'user_id_example' # str | ID of User
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This deletes a user
        api_response = api_instance.delete_user(user_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->delete_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**str**](.md)| ID of User | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserDeleteResponse**](AdminUserDeleteResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **desiredservers_server_type**
> AdminOperationResponse desiredservers_server_type(server_type_id, x_correlation_id=x_correlation_id, desired_servers_to_server_type_request=desired_servers_to_server_type_request)

This API add servers to the specified server type

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    server_type_id = 'server_type_id_example' # str | ID of Server Type
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
desired_servers_to_server_type_request = client.DesiredServersToServerTypeRequest() # DesiredServersToServerTypeRequest | Set Servers for Server Type (optional)

    try:
        # This API add servers to the specified server type
        api_response = api_instance.desiredservers_server_type(server_type_id, x_correlation_id=x_correlation_id, desired_servers_to_server_type_request=desired_servers_to_server_type_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->desiredservers_server_type: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_type_id** | [**str**](.md)| ID of Server Type | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **desired_servers_to_server_type_request** | [**DesiredServersToServerTypeRequest**](DesiredServersToServerTypeRequest.md)| Set Servers for Server Type | [optional] 

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
**200** | Response to operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_application_detail**
> AdminApplicationGetDetailResponse get_admin_application_detail(application_id, x_correlation_id=x_correlation_id)

This provides information on the given application.

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    application_id = 'application_id_example' # str | ID of Application
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides information on the given application.
        api_response = api_instance.get_admin_application_detail(application_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_application_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_id** | [**str**](.md)| ID of Application | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminApplicationGetDetailResponse**](AdminApplicationGetDetailResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_core_detail**
> AdminCoreGetDetailResponse get_admin_core_detail(core_id, x_correlation_id=x_correlation_id)

This provides information on the given core.

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    core_id = 'core_id_example' # str | ID of Core
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides information on the given core.
        api_response = api_instance.get_admin_core_detail(core_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_core_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **core_id** | [**str**](.md)| ID of Core | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminCoreGetDetailResponse**](AdminCoreGetDetailResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_cores**
> GetCoresResponse get_admin_cores(x_correlation_id=x_correlation_id)

This provides a list of core systems

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides a list of core systems
        api_response = api_instance.get_admin_cores(x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_cores: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetCoresResponse**](GetCoresResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_engine_config_section_key**
> AdminEngineConfigSectionKeyResponse get_admin_engine_config_section_key(engine_id, config_section, config_key, x_correlation_id=x_correlation_id)

This provides a config section key for the engine

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    engine_id = 'engine_id_example' # str | EngineID of node-red container request
config_section = 'config_section_example' # str | Config Section Entry
config_key = 'config_key_example' # str | Config Key
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides a config section key for the engine
        api_response = api_instance.get_admin_engine_config_section_key(engine_id, config_section, config_key, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_engine_config_section_key: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | **str**| EngineID of node-red container request | 
 **config_section** | **str**| Config Section Entry | 
 **config_key** | **str**| Config Key | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminEngineConfigSectionKeyResponse**](AdminEngineConfigSectionKeyResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv, text/html, text/plain

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_organization_detail**
> AdminOrganizationGetDetailResponse get_admin_organization_detail(organization_id, x_correlation_id=x_correlation_id)

This gets organization detail by ID

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    organization_id = 'organization_id_example' # str | ID of Organization
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This gets organization detail by ID
        api_response = api_instance.get_admin_organization_detail(organization_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_organization_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | [**str**](.md)| ID of Organization | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOrganizationGetDetailResponse**](AdminOrganizationGetDetailResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_organization_tokens**
> AdminOrganizationGetTokensResponse get_admin_organization_tokens(organization_id, x_correlation_id=x_correlation_id)

This provides information on the given organization tokens.

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    organization_id = 'organization_id_example' # str | ID of Organization
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides information on the given organization tokens.
        api_response = api_instance.get_admin_organization_tokens(organization_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_organization_tokens: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | [**str**](.md)| ID of Organization | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOrganizationGetTokensResponse**](AdminOrganizationGetTokensResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_organizations**
> AdminOrganizationsGetResponse get_admin_organizations(x_correlation_id=x_correlation_id, offset=offset, limit=limit, organization_id=organization_id, organization_name=organization_name, order_by=order_by)

This provides a list of organizations

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
organization_id = 'organization_id_example' # str | Filter by organizationID (optional)
organization_name = 'organization_name_example' # str | Filter by organizationName (optional)
order_by = 'order_by_example' # str | The value should be in [organizationName, organizationID, createdTime, basePriority] (optional)

    try:
        # This provides a list of organizations
        api_response = api_instance.get_admin_organizations(x_correlation_id=x_correlation_id, offset=offset, limit=limit, organization_id=organization_id, organization_name=organization_name, order_by=order_by)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_organizations: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **organization_id** | [**str**](.md)| Filter by organizationID | [optional] 
 **organization_name** | **str**| Filter by organizationName | [optional] 
 **order_by** | **str**| The value should be in [organizationName, organizationID, createdTime, basePriority] | [optional] 

### Return type

[**AdminOrganizationsGetResponse**](AdminOrganizationsGetResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_permission_detail**
> AdminPermissionDetailResponse get_admin_permission_detail(permission_id, x_correlation_id=x_correlation_id)

This gets permission detail by ID

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    permission_id = 'permission_id_example' # str | ID of Permission
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This gets permission detail by ID
        api_response = api_instance.get_admin_permission_detail(permission_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_permission_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **permission_id** | [**str**](.md)| ID of Permission | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminPermissionDetailResponse**](AdminPermissionDetailResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_role_detail**
> AdminRoleDetailResponse get_admin_role_detail(role_id, x_correlation_id=x_correlation_id)

This gets role detail by ID

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    role_id = 'role_id_example' # str | ID of Role
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This gets role detail by ID
        api_response = api_instance.get_admin_role_detail(role_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_role_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **role_id** | [**str**](.md)| ID of Role | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminRoleDetailResponse**](AdminRoleDetailResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_service_config**
> AdminServiceConfigResponse get_admin_service_config(service_id, x_correlation_id=x_correlation_id, config_key=config_key)

This provides all the config for the service

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    service_id = 'service_id_example' # str | ID of the service
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
config_key = 'config_key_example' # str | Config Key (optional)

    try:
        # This provides all the config for the service
        api_response = api_instance.get_admin_service_config(service_id, x_correlation_id=x_correlation_id, config_key=config_key)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_service_config: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service_id** | [**str**](.md)| ID of the service | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **config_key** | **str**| Config Key | [optional] 

### Return type

[**AdminServiceConfigResponse**](AdminServiceConfigResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_service_config_section**
> AdminServiceConfigSectionResponse get_admin_service_config_section(service_id, config_section, x_correlation_id=x_correlation_id)

This provides all the config for the service

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    service_id = 'service_id_example' # str | ID of the service
config_section = 'config_section_example' # str | Config Section Entry
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides all the config for the service
        api_response = api_instance.get_admin_service_config_section(service_id, config_section, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_service_config_section: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service_id** | [**str**](.md)| ID of the service | 
 **config_section** | **str**| Config Section Entry | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminServiceConfigSectionResponse**](AdminServiceConfigSectionResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_service_config_section_key**
> AdminServiceConfigSectionKeyResponse get_admin_service_config_section_key(service_id, config_section, config_key, x_correlation_id=x_correlation_id)

This provides a config section key for the service

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    service_id = 'service_id_example' # str | ID of the service
config_section = 'config_section_example' # str | Config Section Entry
config_key = 'config_key_example' # str | Config Key
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides a config section key for the service
        api_response = api_instance.get_admin_service_config_section_key(service_id, config_section, config_key, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_service_config_section_key: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service_id** | [**str**](.md)| ID of the service | 
 **config_section** | **str**| Config Section Entry | 
 **config_key** | **str**| Config Key | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminServiceConfigSectionKeyResponse**](AdminServiceConfigSectionKeyResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv, text/html, text/plain

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_service_instances**
> GetAdminServiceInstancesResponse get_admin_service_instances(x_correlation_id=x_correlation_id)

This lists the service instances available for a system

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This lists the service instances available for a system
        api_response = api_instance.get_admin_service_instances(x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_service_instances: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetAdminServiceInstancesResponse**](GetAdminServiceInstancesResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_status**
> EngineInstanceInfo get_admin_status(format=format, x_correlation_id=x_correlation_id)

This provides information on the status of the aiWARE edge

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    format = client.StatusFormatEnum() # StatusFormatEnum | If specified, this limits the jobs or tasks to follow status (optional)
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides information on the status of the aiWARE edge
        api_response = api_instance.get_admin_status(format=format, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **format** | [**StatusFormatEnum**](.md)| If specified, this limits the jobs or tasks to follow status | [optional] 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**EngineInstanceInfo**](EngineInstanceInfo.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv, text/html, text/plain

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_token_detail**
> TokenDetail get_admin_token_detail(token_id, x_correlation_id=x_correlation_id)

Get the token info by ID

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    token_id = 'token_id_example' # str | ID of Token
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get the token info by ID
        api_response = api_instance.get_admin_token_detail(token_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_token_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token_id** | [**str**](.md)| ID of Token | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**TokenDetail**](TokenDetail.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_token_permissions**
> AdminTokenPermissionsGetResponse get_admin_token_permissions(token_id, x_correlation_id=x_correlation_id)

This provides a list of all token permissions for a token by TokenID

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    token_id = 'token_id_example' # str | ID of Token
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides a list of all token permissions for a token by TokenID
        api_response = api_instance.get_admin_token_permissions(token_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_token_permissions: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token_id** | [**str**](.md)| ID of Token | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminTokenPermissionsGetResponse**](AdminTokenPermissionsGetResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_tokens**
> AdminGetTokensResponse get_admin_tokens(x_correlation_id=x_correlation_id, offset=offset, limit=limit, direction=direction, start_created_time=start_created_time, end_created_time=end_created_time, start_expire_time=start_expire_time, end_expire_time=end_expire_time, token_id=token_id, organization_i_ds=organization_i_ds, host_id=host_id, user_id=user_id, engine_instance_id=engine_instance_id, type=type, order_by=order_by, role_i_ds=role_i_ds, access_all_organization=access_all_organization)

This provides information about all tokens.

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
direction = 'DESC' # str | the sort order.  ASC or DESC. (optional) (default to 'DESC')
start_created_time = 56 # int | The unix timestamp (optional)
end_created_time = 56 # int | The unix timestamp (optional)
start_expire_time = 56 # int | The unix timestamp (optional)
end_expire_time = 56 # int | The unix timestamp (optional)
token_id = 'token_id_example' # str | Filter by token IDs (optional)
organization_i_ds = 'organization_i_ds_example' # str | Filter by organization IDs (optional)
host_id = 'host_id_example' # str | Filter by host IDs (optional)
user_id = 'user_id_example' # str | Filter by user IDs (optional)
engine_instance_id = 'engine_instance_id_example' # str | Filter by engine instance IDs (optional)
type = client.TokenTypeEnum() # TokenTypeEnum | Filter by token type (optional)
order_by = 'order_by_example' # str | It should be in [createdTime, expirationTime, tokenType] (optional)
role_i_ds = 'role_i_ds_example' # str | Filters by role (optional)
access_all_organization = True # bool |  (optional)

    try:
        # This provides information about all tokens.
        api_response = api_instance.get_admin_tokens(x_correlation_id=x_correlation_id, offset=offset, limit=limit, direction=direction, start_created_time=start_created_time, end_created_time=end_created_time, start_expire_time=start_expire_time, end_expire_time=end_expire_time, token_id=token_id, organization_i_ds=organization_i_ds, host_id=host_id, user_id=user_id, engine_instance_id=engine_instance_id, type=type, order_by=order_by, role_i_ds=role_i_ds, access_all_organization=access_all_organization)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_tokens: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **direction** | **str**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **start_created_time** | **int**| The unix timestamp | [optional] 
 **end_created_time** | **int**| The unix timestamp | [optional] 
 **start_expire_time** | **int**| The unix timestamp | [optional] 
 **end_expire_time** | **int**| The unix timestamp | [optional] 
 **token_id** | [**str**](.md)| Filter by token IDs | [optional] 
 **organization_i_ds** | [**str**](.md)| Filter by organization IDs | [optional] 
 **host_id** | [**str**](.md)| Filter by host IDs | [optional] 
 **user_id** | [**str**](.md)| Filter by user IDs | [optional] 
 **engine_instance_id** | [**str**](.md)| Filter by engine instance IDs | [optional] 
 **type** | [**TokenTypeEnum**](.md)| Filter by token type | [optional] 
 **order_by** | **str**| It should be in [createdTime, expirationTime, tokenType] | [optional] 
 **role_i_ds** | [**str**](.md)| Filters by role | [optional] 
 **access_all_organization** | **bool**|  | [optional] 

### Return type

[**AdminGetTokensResponse**](AdminGetTokensResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_user_detail**
> AdminUserGetDetailResponse get_admin_user_detail(user_id, x_correlation_id=x_correlation_id)

This provides information on the given user.

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    user_id = 'user_id_example' # str | ID of User
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides information on the given user.
        api_response = api_instance.get_admin_user_detail(user_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_user_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**str**](.md)| ID of User | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserGetDetailResponse**](AdminUserGetDetailResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_user_permissions**
> AdminUserPermissionsGetResponse get_admin_user_permissions(user_id, x_correlation_id=x_correlation_id)

This provides a list of all user permissions for an user by UserID

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    user_id = 'user_id_example' # str | ID of User
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides a list of all user permissions for an user by UserID
        api_response = api_instance.get_admin_user_permissions(user_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_user_permissions: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**str**](.md)| ID of User | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserPermissionsGetResponse**](AdminUserPermissionsGetResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_user_tokens**
> AdminUserGetTokensResponse get_admin_user_tokens(user_id, x_correlation_id=x_correlation_id)

This provides information on the given user.

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    user_id = 'user_id_example' # str | ID of User
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides information on the given user.
        api_response = api_instance.get_admin_user_tokens(user_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_user_tokens: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**str**](.md)| ID of User | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserGetTokensResponse**](AdminUserGetTokensResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_users**
> AdminUsersGetResponse get_admin_users(x_correlation_id=x_correlation_id, offset=offset, limit=limit, order_by=order_by, direction=direction, status=status, name=name, user_name=user_name, email=email, role_i_ds=role_i_ds, organization_i_ds=organization_i_ds, access_all_organization=access_all_organization, is_super_admin=is_super_admin)

This provides a list of users in the system

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
offset = 56 # int | the number of users to skip before getting the result set (optional)
limit = 100 # int | the number of users to return. (optional) (default to 100)
order_by = 'created_date_time' # str | the field to sort (optional) (default to 'created_date_time')
direction = 'DESC' # str | the sort order (optional) (default to 'DESC')
status = 'status_example' # str | the value should be in [active, trial, inactive, deleted] (optional)
name = 'name_example' # str | Name of user (optional)
user_name = 'user_name_example' # str | userName of user (optional)
email = 'email_example' # str | email of user (optional)
role_i_ds = 'role_i_ds_example' # str | Filters by role (optional)
organization_i_ds = 'organization_i_ds_example' # str | Filters by internal organization ID (optional)
access_all_organization = True # bool | A user can access to all organization or not. (optional)
is_super_admin = True # bool |  (optional)

    try:
        # This provides a list of users in the system
        api_response = api_instance.get_admin_users(x_correlation_id=x_correlation_id, offset=offset, limit=limit, order_by=order_by, direction=direction, status=status, name=name, user_name=user_name, email=email, role_i_ds=role_i_ds, organization_i_ds=organization_i_ds, access_all_organization=access_all_organization, is_super_admin=is_super_admin)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_users: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **offset** | **int**| the number of users to skip before getting the result set | [optional] 
 **limit** | **int**| the number of users to return. | [optional] [default to 100]
 **order_by** | **str**| the field to sort | [optional] [default to &#39;created_date_time&#39;]
 **direction** | **str**| the sort order | [optional] [default to &#39;DESC&#39;]
 **status** | **str**| the value should be in [active, trial, inactive, deleted] | [optional] 
 **name** | **str**| Name of user | [optional] 
 **user_name** | **str**| userName of user | [optional] 
 **email** | **str**| email of user | [optional] 
 **role_i_ds** | [**str**](.md)| Filters by role | [optional] 
 **organization_i_ds** | [**str**](.md)| Filters by internal organization ID | [optional] 
 **access_all_organization** | **bool**| A user can access to all organization or not. | [optional] 
 **is_super_admin** | **bool**|  | [optional] 

### Return type

[**AdminUsersGetResponse**](AdminUsersGetResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_users_permission**
> AdminUsersPermissionsGetResponse get_admin_users_permission(x_correlation_id=x_correlation_id)

This provides a list of all user permissions in the system

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides a list of all user permissions in the system
        api_response = api_instance.get_admin_users_permission(x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_users_permission: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUsersPermissionsGetResponse**](AdminUsersPermissionsGetResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_admin_users_roles**
> AdminUsersRolesGetResponse get_admin_users_roles(x_correlation_id=x_correlation_id, offset=offset, limit=limit, role_id=role_id, role_name=role_name, order_by=order_by)

This provides a list of user role in the system

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
role_id = 'role_id_example' # str | Filter by role ID (optional)
role_name = 'role_name_example' # str | Filter by roleName (optional)
order_by = 'order_by_example' # str | The value should be in [roleName, createdTime] (optional)

    try:
        # This provides a list of user role in the system
        api_response = api_instance.get_admin_users_roles(x_correlation_id=x_correlation_id, offset=offset, limit=limit, role_id=role_id, role_name=role_name, order_by=order_by)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_admin_users_roles: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **role_id** | [**str**](.md)| Filter by role ID | [optional] 
 **role_name** | **str**| Filter by roleName | [optional] 
 **order_by** | **str**| The value should be in [roleName, createdTime] | [optional] 

### Return type

[**AdminUsersRolesGetResponse**](AdminUsersRolesGetResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_applications**
> GetApplicationsResponse get_applications(x_correlation_id=x_correlation_id, application_status_query_optional=application_status_query_optional, application_type_query_optional=application_type_query_optional, offset=offset, limit=limit, order_by=order_by)

Get the list of applications deployed and available on aiWARE

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
application_status_query_optional = client.ApplicationStatusEnum() # ApplicationStatusEnum | status (optional)
application_type_query_optional = client.ApplicationTypeEnum() # ApplicationTypeEnum | type (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
order_by = 'order_by_example' # str | The value should be in [applicationName, createdTime] (optional)

    try:
        # Get the list of applications deployed and available on aiWARE
        api_response = api_instance.get_applications(x_correlation_id=x_correlation_id, application_status_query_optional=application_status_query_optional, application_type_query_optional=application_type_query_optional, offset=offset, limit=limit, order_by=order_by)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_applications: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **application_status_query_optional** | [**ApplicationStatusEnum**](.md)| status | [optional] 
 **application_type_query_optional** | [**ApplicationTypeEnum**](.md)| type | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **order_by** | **str**| The value should be in [applicationName, createdTime] | [optional] 

### Return type

[**GetApplicationsResponse**](GetApplicationsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of applications |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_backlog_summary**
> GetBacklogSummaryResponse get_backlog_summary(x_correlation_id=x_correlation_id)

This provides summary information on the current backlog

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides summary information on the current backlog
        api_response = api_instance.get_backlog_summary(x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_backlog_summary: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetBacklogSummaryResponse**](GetBacklogSummaryResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_config**
> AdminConfigResponse get_config(x_correlation_id=x_correlation_id, config_section=config_section, config_key=config_key, deprecated=deprecated, secure=secure, is_overridden=is_overridden)

This provides all the config for the cluster

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
config_section = client.ConfigSectionEnum() # ConfigSectionEnum | Config Section Entry (optional)
config_key = 'config_key_example' # str | Config Key (optional)
deprecated = True # bool |  (optional)
secure = True # bool |  (optional)
is_overridden = True # bool |  (optional)

    try:
        # This provides all the config for the cluster
        api_response = api_instance.get_config(x_correlation_id=x_correlation_id, config_section=config_section, config_key=config_key, deprecated=deprecated, secure=secure, is_overridden=is_overridden)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_config: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **config_section** | [**ConfigSectionEnum**](.md)| Config Section Entry | [optional] 
 **config_key** | **str**| Config Key | [optional] 
 **deprecated** | **bool**|  | [optional] 
 **secure** | **bool**|  | [optional] 
 **is_overridden** | **bool**|  | [optional] 

### Return type

[**AdminConfigResponse**](AdminConfigResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_config_section**
> AdminConfigSectionResponse get_config_section(config_section, x_correlation_id=x_correlation_id)

This provides all the config for the cluster

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    config_section = 'config_section_example' # str | Config Section Entry
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides all the config for the cluster
        api_response = api_instance.get_config_section(config_section, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_config_section: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **config_section** | **str**| Config Section Entry | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminConfigSectionResponse**](AdminConfigSectionResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_config_section_key**
> AdminConfigSectionKeyResponse get_config_section_key(config_section, config_key, x_correlation_id=x_correlation_id)

This provides a config section key for the cluster

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    config_section = 'config_section_example' # str | Config Section Entry
config_key = 'config_key_example' # str | Config Key
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides a config section key for the cluster
        api_response = api_instance.get_config_section_key(config_section, config_key, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_config_section_key: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **config_section** | **str**| Config Section Entry | 
 **config_key** | **str**| Config Key | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminConfigSectionKeyResponse**](AdminConfigSectionKeyResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv, text/html, text/plain

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_engines_for_resource**
> GetEnginesForResourceResponse get_engines_for_resource(resource_id, x_correlation_id=x_correlation_id)

Get list of engines for resource

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    resource_id = 'resource_id_example' # str | ID of Resource
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get list of engines for resource
        api_response = api_instance.get_engines_for_resource(resource_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_engines_for_resource: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resource_id** | [**str**](.md)| ID of Resource | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetEnginesForResourceResponse**](GetEnginesForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | This returns a set of engine IDs |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_license_detail**
> LicenseDetail get_license_detail(license_id, x_correlation_id=x_correlation_id)

This gets detail on a license key

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    license_id = 'license_id_example' # str | License ID
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This gets detail on a license key
        api_response = api_instance.get_license_detail(license_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_license_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **license_id** | **str**| License ID | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**LicenseDetail**](LicenseDetail.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_licenses**
> GetLicensesResponse get_licenses(x_correlation_id=x_correlation_id)

This provides a licenses on the system

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides a licenses on the system
        api_response = api_instance.get_licenses(x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_licenses: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetLicensesResponse**](GetLicensesResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_resource**
> GetResourceResponse get_resource(resource_id, x_correlation_id=x_correlation_id)

Get a resource definition

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    resource_id = 'resource_id_example' # str | ID of Resource
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get a resource definition
        api_response = api_instance.get_resource(resource_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_resource: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resource_id** | [**str**](.md)| ID of Resource | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetResourceResponse**](GetResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | This returns a resource definition |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_resources**
> GetResourcesResponse get_resources(x_correlation_id=x_correlation_id, engine_i_ds=engine_i_ds, resource_type=resource_type, offset=offset, limit=limit, direction=direction, order_by=order_by)

Get the list of resources

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
engine_i_ds = 'engine_i_ds_example' # str | Field to provide the input to get engines by Engine ID list. Separated by commas (optional)
resource_type = 'resource_type_example' # str | Filter by resourceType (optional)
offset = 56 # int | the number of data to skip before getting the result set (optional)
limit = 10 # int | the number of items to return. (optional) (default to 10)
direction = 'DESC' # str | the sort order.  ASC or DESC. (optional) (default to 'DESC')
order_by = 'order_by_example' # str | The sort column to use (optional)

    try:
        # Get the list of resources
        api_response = api_instance.get_resources(x_correlation_id=x_correlation_id, engine_i_ds=engine_i_ds, resource_type=resource_type, offset=offset, limit=limit, direction=direction, order_by=order_by)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_resources: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **engine_i_ds** | **str**| Field to provide the input to get engines by Engine ID list. Separated by commas | [optional] 
 **resource_type** | **str**| Filter by resourceType | [optional] 
 **offset** | **int**| the number of data to skip before getting the result set | [optional] 
 **limit** | **int**| the number of items to return. | [optional] [default to 10]
 **direction** | **str**| the sort order.  ASC or DESC. | [optional] [default to &#39;DESC&#39;]
 **order_by** | **str**| The sort column to use | [optional] 

### Return type

[**GetResourcesResponse**](GetResourcesResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of resources |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_resources_for_engine**
> GetResourcesForEngineResponse get_resources_for_engine(engine_id, x_correlation_id=x_correlation_id)

Get list of resources for engine

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    engine_id = 'engine_id_example' # str | ID of Engine
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get list of resources for engine
        api_response = api_instance.get_resources_for_engine(engine_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_resources_for_engine: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **engine_id** | [**str**](.md)| ID of Engine | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetResourcesForEngineResponse**](GetResourcesForEngineResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | This returns a set of resources |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_resources_for_host**
> GetResourcesForHostResponse get_resources_for_host(host_id, x_correlation_id=x_correlation_id)

Get list of resources for host

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    host_id = 'host_id_example' # str | ID of Host
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get list of resources for host
        api_response = api_instance.get_resources_for_host(host_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_resources_for_host: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host_id** | [**str**](.md)| ID of Host | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetResourcesForHostResponse**](GetResourcesForHostResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | This returns a set of resources |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_resources_for_service**
> GetResourcesForServiceResponse get_resources_for_service(service_id, x_correlation_id=x_correlation_id)

Get list of resources for service

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    service_id = 'service_id_example' # str | ID of the service
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # Get list of resources for service
        api_response = api_instance.get_resources_for_service(service_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_resources_for_service: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service_id** | [**str**](.md)| ID of the service | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetResourcesForServiceResponse**](GetResourcesForServiceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | This returns a set of resources |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_type**
> GetServerTypeResponse get_server_type(server_type_id, x_correlation_id=x_correlation_id)

This provides detail on the server type

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    server_type_id = 'server_type_id_example' # str | ID of Server Type
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This provides detail on the server type
        api_response = api_instance.get_server_type(server_type_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_server_type: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_type_id** | [**str**](.md)| ID of Server Type | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetServerTypeResponse**](GetServerTypeResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_type_engine_running**
> GetServerTypeRunningEnginesResponse get_server_type_engine_running(x_correlation_id=x_correlation_id, server_type_id=server_type_id, engine_id=engine_id, offset=offset, limit=limit)

This lists the running engine with server types

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
server_type_id = 'server_type_id_example' # str | Filter by serverTypeID (optional)
engine_id = 'engine_id_example' # str | Filter by engine id (optional)
offset = 56 # int | the number of records to skip before getting the result set (optional)
limit = 100 # int | the number of records to return. (optional) (default to 100)

    try:
        # This lists the running engine with server types
        api_response = api_instance.get_server_type_engine_running(x_correlation_id=x_correlation_id, server_type_id=server_type_id, engine_id=engine_id, offset=offset, limit=limit)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_server_type_engine_running: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **server_type_id** | **str**| Filter by serverTypeID | [optional] 
 **engine_id** | **str**| Filter by engine id | [optional] 
 **offset** | **int**| the number of records to skip before getting the result set | [optional] 
 **limit** | **int**| the number of records to return. | [optional] [default to 100]

### Return type

[**GetServerTypeRunningEnginesResponse**](GetServerTypeRunningEnginesResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_type_engine_running_detail**
> GetServerTypeRunningEngineDetailResponse get_server_type_engine_running_detail(server_type_id, engine_id, x_correlation_id=x_correlation_id)

This gets the detail of server type - running engine

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    server_type_id = 'server_type_id_example' # str | ID of Server Type
engine_id = 'engine_id_example' # str | ID of Engine
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This gets the detail of server type - running engine
        api_response = api_instance.get_server_type_engine_running_detail(server_type_id, engine_id, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_server_type_engine_running_detail: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_type_id** | [**str**](.md)| ID of Server Type | 
 **engine_id** | [**str**](.md)| ID of Engine | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetServerTypeRunningEngineDetailResponse**](GetServerTypeRunningEngineDetailResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_server_types**
> GetServerTypesResponse get_server_types(run_mode, x_correlation_id=x_correlation_id)

This lists the server types available on the system

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    run_mode = 'run_mode_example' # str | Filer by run mode
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This lists the server types available on the system
        api_response = api_instance.get_server_types(run_mode, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_server_types: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **run_mode** | **str**| Filer by run mode | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**GetServerTypesResponse**](GetServerTypesResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_services**
> GetAdminServicesResponse get_services(x_correlation_id=x_correlation_id, tags=tags)

This lists the services available on the system

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
tags = 'tags_example' # str | Filter by tags (optional)

    try:
        # This lists the services available on the system
        api_response = api_instance.get_services(x_correlation_id=x_correlation_id, tags=tags)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->get_services: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **tags** | **str**| Filter by tags | [optional] 

### Return type

[**GetAdminServicesResponse**](GetAdminServicesResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **login_user**
> AdminUserLoginResponse login_user(x_correlation_id=x_correlation_id, admin_user_login_request=admin_user_login_request)

This logs a user in if successful

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
admin_user_login_request = client.AdminUserLoginRequest() # AdminUserLoginRequest | This logs in the user (optional)

    try:
        # This logs a user in if successful
        api_response = api_instance.login_user(x_correlation_id=x_correlation_id, admin_user_login_request=admin_user_login_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->login_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **admin_user_login_request** | [**AdminUserLoginRequest**](AdminUserLoginRequest.md)| This logs in the user | [optional] 

### Return type

[**AdminUserLoginResponse**](AdminUserLoginResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauth_login_user**
> AdminUserLoginResponse oauth_login_user(x_correlation_id=x_correlation_id, admin_user_o_auth2_login_request=admin_user_o_auth2_login_request)

This logs a user in if successful with OAuth2

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
admin_user_o_auth2_login_request = client.AdminUserOAuth2LoginRequest() # AdminUserOAuth2LoginRequest | This logs in the user with the OAuth2 response (optional)

    try:
        # This logs a user in if successful with OAuth2
        api_response = api_instance.oauth_login_user(x_correlation_id=x_correlation_id, admin_user_o_auth2_login_request=admin_user_o_auth2_login_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->oauth_login_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **admin_user_o_auth2_login_request** | [**AdminUserOAuth2LoginRequest**](AdminUserOAuth2LoginRequest.md)| This logs in the user with the OAuth2 response | [optional] 

### Return type

[**AdminUserLoginResponse**](AdminUserLoginResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register_user**
> AdminUserRegisterResponse register_user(admin_user_register_request, x_correlation_id=x_correlation_id)

This registers a new user

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    admin_user_register_request = client.AdminUserRegisterRequest() # AdminUserRegisterRequest | The input for registerUser
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This registers a new user
        api_response = api_instance.register_user(admin_user_register_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->register_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **admin_user_register_request** | [**AdminUserRegisterRequest**](AdminUserRegisterRequest.md)| The input for registerUser | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserRegisterResponse**](AdminUserRegisterResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_engine_for_resource**
> RemoveEngineForResourceResponse remove_engine_for_resource(resource_id, engine_id, x_correlation_id=x_correlation_id, remove_engine_for_resource_request=remove_engine_for_resource_request)

This API removes the engine to the resource

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    resource_id = 'resource_id_example' # str | ID of Resource
engine_id = 'engine_id_example' # str | ID of Engine
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
remove_engine_for_resource_request = client.RemoveEngineForResourceRequest() # RemoveEngineForResourceRequest | Remove Engine Mapping for Resource (optional)

    try:
        # This API removes the engine to the resource
        api_response = api_instance.remove_engine_for_resource(resource_id, engine_id, x_correlation_id=x_correlation_id, remove_engine_for_resource_request=remove_engine_for_resource_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->remove_engine_for_resource: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resource_id** | [**str**](.md)| ID of Resource | 
 **engine_id** | [**str**](.md)| ID of Engine | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **remove_engine_for_resource_request** | [**RemoveEngineForResourceRequest**](RemoveEngineForResourceRequest.md)| Remove Engine Mapping for Resource | [optional] 

### Return type

[**RemoveEngineForResourceResponse**](RemoveEngineForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The response of RemoveEngineMappingForResource |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **removeservers_server_type**
> AdminOperationResponse removeservers_server_type(server_type_id, x_correlation_id=x_correlation_id, remove_servers_to_server_type_request=remove_servers_to_server_type_request)

This API removes servers from the specified server type

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    server_type_id = 'server_type_id_example' # str | ID of Server Type
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
remove_servers_to_server_type_request = client.RemoveServersToServerTypeRequest() # RemoveServersToServerTypeRequest | Update Server Type (optional)

    try:
        # This API removes servers from the specified server type
        api_response = api_instance.removeservers_server_type(server_type_id, x_correlation_id=x_correlation_id, remove_servers_to_server_type_request=remove_servers_to_server_type_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->removeservers_server_type: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_type_id** | [**str**](.md)| ID of Server Type | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **remove_servers_to_server_type_request** | [**RemoveServersToServerTypeRequest**](RemoveServersToServerTypeRequest.md)| Update Server Type | [optional] 

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
**200** | List of engines |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reset_alloc_table**
> AdminOperationResponse reset_alloc_table(x_correlation_id=x_correlation_id)

This resets the alloc table

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This resets the alloc table
        api_response = api_instance.reset_alloc_table(x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->reset_alloc_table: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

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
**200** | Returns the status on the operation |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_application**
> AdminApplicationUpdateResponse update_application(application_id, admin_application_update_request, x_correlation_id=x_correlation_id)

This updates an application

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    application_id = 'application_id_example' # str | ID of Application
admin_application_update_request = client.AdminApplicationUpdateRequest() # AdminApplicationUpdateRequest | The input for updateApplication
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This updates an application
        api_response = api_instance.update_application(application_id, admin_application_update_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_application: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_id** | [**str**](.md)| ID of Application | 
 **admin_application_update_request** | [**AdminApplicationUpdateRequest**](AdminApplicationUpdateRequest.md)| The input for updateApplication | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminApplicationUpdateResponse**](AdminApplicationUpdateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_config_all**
> AdminConfigUpdateResponse update_config_all(admin_config_update_request, x_correlation_id=x_correlation_id, config_section=config_section, config_key=config_key, deprecated=deprecated, secure=secure, is_overridden=is_overridden)

This gets the config for the cluster

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    admin_config_update_request = client.AdminConfigUpdateRequest() # AdminConfigUpdateRequest | Config Update for core
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
config_section = client.ConfigSectionEnum() # ConfigSectionEnum | Config Section Entry (optional)
config_key = 'config_key_example' # str | Config Key (optional)
deprecated = True # bool |  (optional)
secure = True # bool |  (optional)
is_overridden = True # bool |  (optional)

    try:
        # This gets the config for the cluster
        api_response = api_instance.update_config_all(admin_config_update_request, x_correlation_id=x_correlation_id, config_section=config_section, config_key=config_key, deprecated=deprecated, secure=secure, is_overridden=is_overridden)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_config_all: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **admin_config_update_request** | [**AdminConfigUpdateRequest**](AdminConfigUpdateRequest.md)| Config Update for core | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **config_section** | [**ConfigSectionEnum**](.md)| Config Section Entry | [optional] 
 **config_key** | **str**| Config Key | [optional] 
 **deprecated** | **bool**|  | [optional] 
 **secure** | **bool**|  | [optional] 
 **is_overridden** | **bool**|  | [optional] 

### Return type

[**AdminConfigUpdateResponse**](AdminConfigUpdateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_config_section**
> AdminConfigUpdateSectionResponse update_config_section(config_section, admin_config_update_section_request, x_correlation_id=x_correlation_id)

This gets the config for the cluster

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    config_section = 'config_section_example' # str | Config Section Entry
admin_config_update_section_request = client.AdminConfigUpdateSectionRequest() # AdminConfigUpdateSectionRequest | The input for createConfigSection
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This gets the config for the cluster
        api_response = api_instance.update_config_section(config_section, admin_config_update_section_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_config_section: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **config_section** | **str**| Config Section Entry | 
 **admin_config_update_section_request** | [**AdminConfigUpdateSectionRequest**](AdminConfigUpdateSectionRequest.md)| The input for createConfigSection | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminConfigUpdateSectionResponse**](AdminConfigUpdateSectionResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, text/csv, text/html, text/plain

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_config_section_key**
> AdminConfigUpdateSectionKeyResponse update_config_section_key(config_section, config_key, admin_config_update_section_key_request, x_correlation_id=x_correlation_id)

This updates the config for the cluster for a given key

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    config_section = 'config_section_example' # str | Config Section Entry
config_key = 'config_key_example' # str | Config Key
admin_config_update_section_key_request = client.AdminConfigUpdateSectionKeyRequest() # AdminConfigUpdateSectionKeyRequest | The input for createSectionKey
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This updates the config for the cluster for a given key
        api_response = api_instance.update_config_section_key(config_section, config_key, admin_config_update_section_key_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_config_section_key: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **config_section** | **str**| Config Section Entry | 
 **config_key** | **str**| Config Key | 
 **admin_config_update_section_key_request** | [**AdminConfigUpdateSectionKeyRequest**](AdminConfigUpdateSectionKeyRequest.md)| The input for createSectionKey | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminConfigUpdateSectionKeyResponse**](AdminConfigUpdateSectionKeyResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, text/csv, text/html, text/plain

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_engines_for_resource**
> UpdateEnginesForResourceResponse update_engines_for_resource(resource_id, x_correlation_id=x_correlation_id, update_engines_for_resource_request=update_engines_for_resource_request)

This API updates the specified server type-running engine

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    resource_id = 'resource_id_example' # str | ID of Resource
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
update_engines_for_resource_request = client.UpdateEnginesForResourceRequest() # UpdateEnginesForResourceRequest | Update Engine Mapping for Resource (optional)

    try:
        # This API updates the specified server type-running engine
        api_response = api_instance.update_engines_for_resource(resource_id, x_correlation_id=x_correlation_id, update_engines_for_resource_request=update_engines_for_resource_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_engines_for_resource: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resource_id** | [**str**](.md)| ID of Resource | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **update_engines_for_resource_request** | [**UpdateEnginesForResourceRequest**](UpdateEnginesForResourceRequest.md)| Update Engine Mapping for Resource | [optional] 

### Return type

[**UpdateEnginesForResourceResponse**](UpdateEnginesForResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The response of UpdateEngineMappingForResource |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_organization**
> AdminOrganizationUpdateResponse update_organization(organization_id, admin_organization_update_request, x_correlation_id=x_correlation_id)

This updates a organization

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    organization_id = 'organization_id_example' # str | ID of Organization
admin_organization_update_request = client.AdminOrganizationUpdateRequest() # AdminOrganizationUpdateRequest | The input for updateOrganization
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This updates a organization
        api_response = api_instance.update_organization(organization_id, admin_organization_update_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_organization: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | [**str**](.md)| ID of Organization | 
 **admin_organization_update_request** | [**AdminOrganizationUpdateRequest**](AdminOrganizationUpdateRequest.md)| The input for updateOrganization | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminOrganizationUpdateResponse**](AdminOrganizationUpdateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_permission**
> AdminPermissionUpdateResponse update_permission(permission_id, admin_permission_update_request, x_correlation_id=x_correlation_id)

This updates a permission

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    permission_id = 'permission_id_example' # str | ID of Permission
admin_permission_update_request = client.AdminPermissionUpdateRequest() # AdminPermissionUpdateRequest | The input for updatePermission
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This updates a permission
        api_response = api_instance.update_permission(permission_id, admin_permission_update_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_permission: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **permission_id** | [**str**](.md)| ID of Permission | 
 **admin_permission_update_request** | [**AdminPermissionUpdateRequest**](AdminPermissionUpdateRequest.md)| The input for updatePermission | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminPermissionUpdateResponse**](AdminPermissionUpdateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_resource**
> UpdateResourceResponse update_resource(resource_id, update_resource_request, x_correlation_id=x_correlation_id)

This API updates the specified resource

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    resource_id = 'resource_id_example' # str | ID of Resource
update_resource_request = client.UpdateResourceRequest() # UpdateResourceRequest | Update Resource
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API updates the specified resource
        api_response = api_instance.update_resource(resource_id, update_resource_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_resource: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resource_id** | [**str**](.md)| ID of Resource | 
 **update_resource_request** | [**UpdateResourceRequest**](UpdateResourceRequest.md)| Update Resource | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**UpdateResourceResponse**](UpdateResourceResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of the Update Resource API |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_resource_state**
> update_resource_state(resource_id, update_resource_state_request, x_correlation_id=x_correlation_id)

This API updates the state of the specified resource

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    resource_id = 'resource_id_example' # str | ID of Resource
update_resource_state_request = client.UpdateResourceStateRequest() # UpdateResourceStateRequest | Update Resource State
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This API updates the state of the specified resource
        api_instance.update_resource_state(resource_id, update_resource_state_request, x_correlation_id=x_correlation_id)
    except ApiException as e:
        print("Exception when calling AdminApi->update_resource_state: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resource_id** | [**str**](.md)| ID of Resource | 
 **update_resource_state_request** | [**UpdateResourceStateRequest**](UpdateResourceStateRequest.md)| Update Resource State | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

void (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Result of the Update Resource State API |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_role**
> AdminRoleUpdateResponse update_role(role_id, admin_role_update_request, x_correlation_id=x_correlation_id)

This updates a role

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    role_id = 'role_id_example' # str | ID of Role
admin_role_update_request = client.AdminRoleUpdateRequest() # AdminRoleUpdateRequest | The input for updateRole
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This updates a role
        api_response = api_instance.update_role(role_id, admin_role_update_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_role: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **role_id** | [**str**](.md)| ID of Role | 
 **admin_role_update_request** | [**AdminRoleUpdateRequest**](AdminRoleUpdateRequest.md)| The input for updateRole | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminRoleUpdateResponse**](AdminRoleUpdateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_server_type**
> UpdateServerTypeResponse update_server_type(server_type_id, x_correlation_id=x_correlation_id, server_type_detail=server_type_detail)

This API updates the specified server type

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    server_type_id = 'server_type_id_example' # str | ID of Server Type
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
server_type_detail = client.ServerTypeDetail() # ServerTypeDetail | Update Server Type (optional)

    try:
        # This API updates the specified server type
        api_response = api_instance.update_server_type(server_type_id, x_correlation_id=x_correlation_id, server_type_detail=server_type_detail)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_server_type: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_type_id** | [**str**](.md)| ID of Server Type | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **server_type_detail** | [**ServerTypeDetail**](ServerTypeDetail.md)| Update Server Type | [optional] 

### Return type

[**UpdateServerTypeResponse**](UpdateServerTypeResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_server_type_engine_running**
> UpdateServerTypeEngineRunningResponse update_server_type_engine_running(server_type_id, engine_id, x_correlation_id=x_correlation_id, update_server_type_engine_running_request=update_server_type_engine_running_request)

This API updates the specified server type-running engine

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    server_type_id = 'server_type_id_example' # str | ID of Server Type
engine_id = 'engine_id_example' # str | ID of Engine
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
update_server_type_engine_running_request = client.UpdateServerTypeEngineRunningRequest() # UpdateServerTypeEngineRunningRequest | Update Server Type - Running Engine (optional)

    try:
        # This API updates the specified server type-running engine
        api_response = api_instance.update_server_type_engine_running(server_type_id, engine_id, x_correlation_id=x_correlation_id, update_server_type_engine_running_request=update_server_type_engine_running_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_server_type_engine_running: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_type_id** | [**str**](.md)| ID of Server Type | 
 **engine_id** | [**str**](.md)| ID of Engine | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **update_server_type_engine_running_request** | [**UpdateServerTypeEngineRunningRequest**](UpdateServerTypeEngineRunningRequest.md)| Update Server Type - Running Engine | [optional] 

### Return type

[**UpdateServerTypeEngineRunningResponse**](UpdateServerTypeEngineRunningResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The response of UpdateServerTypeEngineRunning |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**400** | Invalid argument.  Please see the error response for more information. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**401** | Not authorized |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**403** | Forbidden |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**404** | Not Found |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**405** | The request is not allowed. |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**429** | Too Many Requests |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**501** | Not Implemented |  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |
**503** | System Unavailable |  * Retry-After -  <br>  * X-Aiware-Version -  <br>  * X-Correlation-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_token**
> AdminTokenUpdateResponse update_token(token_id, admin_token_update_request, x_correlation_id=x_correlation_id)

This updates a token

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    token_id = 'token_id_example' # str | ID of Token
admin_token_update_request = client.AdminTokenUpdateRequest() # AdminTokenUpdateRequest | The input for updateToken
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This updates a token
        api_response = api_instance.update_token(token_id, admin_token_update_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_token: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token_id** | [**str**](.md)| ID of Token | 
 **admin_token_update_request** | [**AdminTokenUpdateRequest**](AdminTokenUpdateRequest.md)| The input for updateToken | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminTokenUpdateResponse**](AdminTokenUpdateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_user**
> AdminUserUpdateResponse update_user(user_id, admin_user_update_request, x_correlation_id=x_correlation_id)

This updates a user

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    user_id = 'user_id_example' # str | ID of User
admin_user_update_request = client.AdminUserUpdateRequest() # AdminUserUpdateRequest | The input for updateUser
x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)

    try:
        # This updates a user
        api_response = api_instance.update_user(user_id, admin_user_update_request, x_correlation_id=x_correlation_id)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->update_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**str**](.md)| ID of User | 
 **admin_user_update_request** | [**AdminUserUpdateRequest**](AdminUserUpdateRequest.md)| The input for updateUser | 
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 

### Return type

[**AdminUserUpdateResponse**](AdminUserUpdateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **user_password_forgot**
> AdminUserPasswordForgotResponse user_password_forgot(x_correlation_id=x_correlation_id, admin_user_password_forgot_request=admin_user_password_forgot_request)

This api will help users to reset their password when they forgot

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
admin_user_password_forgot_request = client.AdminUserPasswordForgotRequest() # AdminUserPasswordForgotRequest | Needs to provide the info to reset user's password when they forgot (optional)

    try:
        # This api will help users to reset their password when they forgot
        api_response = api_instance.user_password_forgot(x_correlation_id=x_correlation_id, admin_user_password_forgot_request=admin_user_password_forgot_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->user_password_forgot: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **admin_user_password_forgot_request** | [**AdminUserPasswordForgotRequest**](AdminUserPasswordForgotRequest.md)| Needs to provide the info to reset user&#39;s password when they forgot | [optional] 

### Return type

[**AdminUserPasswordForgotResponse**](AdminUserPasswordForgotResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **user_password_reset**
> AdminUserPasswordResetResponse user_password_reset(x_correlation_id=x_correlation_id, admin_user_password_reset_request=admin_user_password_reset_request)

Helps users to reset their password

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
admin_user_password_reset_request = client.AdminUserPasswordResetRequest() # AdminUserPasswordResetRequest | Needs to provide the info to reset password (optional)

    try:
        # Helps users to reset their password
        api_response = api_instance.user_password_reset(x_correlation_id=x_correlation_id, admin_user_password_reset_request=admin_user_password_reset_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->user_password_reset: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **admin_user_password_reset_request** | [**AdminUserPasswordResetRequest**](AdminUserPasswordResetRequest.md)| Needs to provide the info to reset password | [optional] 

### Return type

[**AdminUserPasswordResetResponse**](AdminUserPasswordResetResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **user_password_update**
> AdminUserPasswordUpdateResponse user_password_update(x_correlation_id=x_correlation_id, admin_user_password_update_request=admin_user_password_update_request)

This api will help users to update their password

### Example

* Api Key Authentication (api_key):
```python
from __future__ import print_function
import time
import client
from client.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to https://api.aiware.com/edge/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = client.Configuration(
    host = "https://api.aiware.com/edge/v1",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Enter a context with an instance of the API client
with client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = client.AdminApi(api_client)
    x_correlation_id = 'x_correlation_id_example' # str | Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request (optional)
admin_user_password_update_request = client.AdminUserPasswordUpdateRequest() # AdminUserPasswordUpdateRequest | Users provide the password info to change (optional)

    try:
        # This api will help users to update their password
        api_response = api_instance.user_password_update(x_correlation_id=x_correlation_id, admin_user_password_update_request=admin_user_password_update_request)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AdminApi->user_password_update: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_correlation_id** | **str**| Correlation Id that can be passed, traced in the server and will be returned in the response if present in the request | [optional] 
 **admin_user_password_update_request** | [**AdminUserPasswordUpdateRequest**](AdminUserPasswordUpdateRequest.md)| Users provide the password info to change | [optional] 

### Return type

[**AdminUserPasswordUpdateResponse**](AdminUserPasswordUpdateResponse.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

