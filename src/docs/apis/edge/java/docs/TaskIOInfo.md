

# TaskIOInfo

This is the task IO Object that provides paramenters for the input and output
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**correlationId** | **String** | On create, this field will be used to look up task routes for binding. |  [optional]
**createdDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the task was created |  [optional]
**id** | [**UUID**](UUID.md) | This is the IO Id.  On create, this is not set. |  [optional]
**mode** | [**TaskIOModeEnum**](TaskIOModeEnum.md) |  |  [optional]
**modifiedDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the task was last modified. |  [optional]
**optionsJSON** | **String** | Any options for this input or output folder for the task to use on processing |  [optional]
**type** | [**TaskIOTypeEnum**](TaskIOTypeEnum.md) |  |  [optional]



