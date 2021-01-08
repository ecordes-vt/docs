

# CreateUserDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accessAllOrganization** | **Boolean** | A user can access to all organization or not. |  [optional]
**displayName** | **String** |  |  [optional]
**email** | **String** |  |  [optional]
**expiration** | **Long** | The unix timestamp for the user expiration. If 0, then it does not expire |  [optional]
**internalOrganizationID** | [**UUID**](UUID.md) |  |  [optional]
**inviteRequested** | **Boolean** |  |  [optional]
**inviteURL** | **String** |  |  [optional]
**isSuperAdmin** | **Boolean** | This can be only updated to true by another super admin. |  [optional]
**kvpJSON** | **String** |  |  [optional]
**organizationIDs** | [**List&lt;UUID&gt;**](UUID.md) | This is a list of Org ID that the user can access to. |  [optional]
**password** | **String** |  |  [optional]
**passwordChangeRequired** | **Boolean** |  |  [optional]
**roleIDs** | [**List&lt;UUID&gt;**](UUID.md) |  |  [optional]
**status** | [**UserStatusEnum**](UserStatusEnum.md) |  |  [optional]
**userID** | [**UUID**](UUID.md) |  |  [optional]
**userName** | **String** |  |  [optional]
**userSettingsJSON** | **String** |  |  [optional]



