

# UpdateTokenDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accessAllOrganization** | **Boolean** |  |  [optional]
**apiRateLimitHour** | **Long** |  |  [optional]
**bytesRateLimitHour** | **Long** |  |  [optional]
**engineInstanceID** | [**UUID**](UUID.md) |  |  [optional]
**expiration** | **Long** | The unix timestamp for the token expiration. If 0, then it does not expire |  [optional]
**hostID** | [**UUID**](UUID.md) |  |  [optional]
**kvpJSON** | **String** |  |  [optional]
**maxAPI** | **Long** |  |  [optional]
**maxBytes** | **Long** |  |  [optional]
**maxTasks** | **Long** |  |  [optional]
**organizationIDs** | [**List&lt;UUID&gt;**](UUID.md) | This is a list of Org ID that the token can access to. If accessAllOrganization is true, this value will be override. |  [optional]
**roleIDs** | [**List&lt;UUID&gt;**](UUID.md) |  |  [optional]
**taskRateLimitHour** | **Long** |  |  [optional]
**type** | [**TokenTypeEnum**](TokenTypeEnum.md) |  |  [optional]
**userID** | [**UUID**](UUID.md) |  |  [optional]



