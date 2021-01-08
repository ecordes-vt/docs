# AiwareJsClient.ResourceDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**URI** | **String** | Resource URI. This field is presented only in responses | [optional] 
**uRITemplate** | **String** | URI template in the go template format. | [optional] 
**bindingType** | [**ResourceBindingTypeEnum**](ResourceBindingTypeEnum.md) |  | [optional] 
**createdBy** | **String** |  | [optional] 
**createdDateTime** | **Date** | This is the datetime the core was created | [optional] 
**hostID** | **String** |  | [optional] 
**modifiedBy** | **String** |  | [optional] 
**modifiedDateTime** | **Date** | This is the datetime the core was last modified. | [optional] 
**name** | **String** | The name of the resource | [optional] 
**nsqadmin** | **String** | This is the nsqadmin \&quot;host:port\&quot;. | [optional] 
**nsqd** | **String** | This is the nsqd \&quot;host:port\&quot;. | [optional] 
**nsqlookupd** | **String** | This is the nsqlookupd \&quot;host:port\&quot;. | [optional] 
**params** | **String** | JSON encoded field | [optional] 
**pgDatabase** | **String** | If postgres, this is the name of the postgres database | [optional] 
**pgPass** | **String** | If postgres, this is the user password.  This will be encrypted in storage | [optional] 
**pgUser** | **String** | If postgres, this is the user name | [optional] 
**redisDB** | **Number** | This is the redis DB number. | [optional] 
**redisToken** | **String** | If Redis, this is the Redis token. | [optional] 
**resourceID** | **String** | Resource ID | [optional] 
**resourceState** | [**ResourceStateEnum**](ResourceStateEnum.md) |  | [optional] 
**resourceType** | [**ResourceTypeEnum**](ResourceTypeEnum.md) |  | [optional] 


