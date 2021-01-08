

# CreateResourceDetail

This is the create request for a resource object
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**urITemplate** | **String** | URI template in the go template format. |  [optional]
**bindingType** | [**ResourceBindingTypeEnum**](ResourceBindingTypeEnum.md) |  |  [optional]
**hostID** | [**UUID**](UUID.md) |  |  [optional]
**name** | **String** | The name of the resource |  [optional]
**params** | **String** | JSON encoded field |  [optional]
**pgDatabase** | **String** | If postgres, this is the name of the postgres database |  [optional]
**pgPass** | **String** | If postgres, this is the user password.  This will be encrypted in storage |  [optional]
**pgUser** | **String** | If postgres, this is the user name |  [optional]
**redisDB** | **Long** | This is the redis DB number. |  [optional]
**redisToken** | **String** | If Redis, this is the Redis token. |  [optional]
**resourceState** | [**ResourceStateEnum**](ResourceStateEnum.md) |  |  [optional]
**resourceType** | [**ResourceTypeEnum**](ResourceTypeEnum.md) |  |  [optional]



