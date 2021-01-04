

# LicenseDetail

This provides the detailed information about the license.
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currentAPI** | **Long** | The current number of API calls allowed by the license. |  [optional]
**currentBytes** | **Long** | The current number of bytes to be processed under this license. |  [optional]
**currentTasks** | **Long** | The current number of tasks that can be processed on the system. |  [optional]
**licenseExpiration** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the license will expire |  [optional]
**licenseID** | [**UUID**](UUID.md) | License ID |  [optional]
**licenseKey** | **String** | This is the encoded license string |  [optional]
**licenseValidation** | **String** | This contains the validation information for the license |  [optional]
**maxAPI** | **Long** | The maximum number of API calls allowed by the license. If 0, then unlimited. |  [optional]
**maxBytes** | **Long** | The maximum number of bytes to be processed under this license.  If 0, then unlimited. |  [optional]
**maxHosts** | **Long** | The maximum number of hosts allowed in the system.  If 0, then unlimited. |  [optional]
**maxTasks** | **Long** | The maximum number of tasks that can be processed on the system. If 0, then unlimited. |  [optional]



