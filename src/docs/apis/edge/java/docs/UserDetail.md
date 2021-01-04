

# UserDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accessAllOrganization** | **Boolean** | A user can access to all organization or not. |  [optional]
**createdBy** | [**UUID**](UUID.md) |  |  [optional]
**createdDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the core was created |  [optional]
**datePasswordLastUpdated** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the password was last updated |  [optional]
**displayName** | **String** |  |  [optional]
**email** | **String** |  |  [optional]
**expiration** | [**OffsetDateTime**](OffsetDateTime.md) | This is the expiration datetime for the current user |  [optional]
**internalOrganizationID** | [**UUID**](UUID.md) |  |  [optional]
**isSuperAdmin** | **Boolean** |  |  [optional]
**isSynchronized** | **Boolean** | This user was synchronized or not. |  [optional]
**kvpJSON** | **String** |  |  [optional]
**lastLoggedIn** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the user last logged in |  [optional]
**modifiedBy** | [**UUID**](UUID.md) |  |  [optional]
**modifiedDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the core was last modified. |  [optional]
**organizationIDs** | [**List&lt;UUID&gt;**](UUID.md) | This is a list of Org ID that the user can access to. |  [optional]
**passwordChangeRequired** | **Boolean** |  |  [optional]
**permissionIDs** | **List&lt;String&gt;** |  |  [optional]
**roleIDs** | [**List&lt;UUID&gt;**](UUID.md) |  |  [optional]
**status** | [**UserStatusEnum**](UserStatusEnum.md) |  |  [optional]
**userID** | [**UUID**](UUID.md) |  |  [optional]
**userName** | **String** |  |  [optional]
**userSettingsJSON** | **String** |  |  [optional]



