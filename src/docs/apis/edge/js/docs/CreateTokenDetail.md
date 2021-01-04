# AiwareJsClient.CreateTokenDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accessAllOrganization** | **Boolean** |  | [optional] 
**apiRateLimitHour** | **Number** |  | [optional] 
**bytesRateLimitHour** | **Number** |  | [optional] 
**engineInstanceID** | **String** |  | [optional] 
**expiration** | **Number** | The unix timestamp for the token expiration. If 0, then it does not expire | [optional] 
**hostID** | **String** |  | [optional] 
**kvpJSON** | **String** |  | [optional] 
**maxAPI** | **Number** |  | [optional] 
**maxBytes** | **Number** |  | [optional] 
**maxTasks** | **Number** |  | [optional] 
**organizationIDs** | **[String]** | This is a list of Org ID that the token can access to. If accessAllOrganization is true, this value will be override. | [optional] 
**roleIDs** | **[String]** |  | [optional] 
**taskRateLimitHour** | **Number** |  | [optional] 
**type** | [**TokenTypeEnum**](TokenTypeEnum.md) |  | [optional] 
**userID** | **String** |  | [optional] 


