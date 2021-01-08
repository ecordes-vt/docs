# AiwareJsClient.CreateUserDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accessAllOrganization** | **Boolean** | A user can access to all organization or not. | [optional] 
**displayName** | **String** |  | [optional] 
**email** | **String** |  | [optional] 
**expiration** | **Number** | The unix timestamp for the user expiration. If 0, then it does not expire | [optional] 
**internalOrganizationID** | **String** |  | [optional] 
**inviteRequested** | **Boolean** |  | [optional] 
**inviteURL** | **String** |  | [optional] 
**isSuperAdmin** | **Boolean** | This can be only updated to true by another super admin. | [optional] 
**kvpJSON** | **String** |  | [optional] 
**organizationIDs** | **[String]** | This is a list of Org ID that the user can access to. | [optional] 
**password** | **String** |  | [optional] 
**passwordChangeRequired** | **Boolean** |  | [optional] 
**roleIDs** | **[String]** |  | [optional] 
**status** | [**UserStatusEnum**](UserStatusEnum.md) |  | [optional] 
**userID** | **String** |  | [optional] 
**userName** | **String** |  | [optional] 
**userSettingsJSON** | **String** |  | [optional] 


