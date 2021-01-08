# TaskRouteDetail
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**endpoint** | [**UUID**](UUID.md) | This is endpoint to be used for this route.  This does not have to be unique. | [optional] [default to null]
**firstWriteDateTime** | [**Date**](DateTime.md) | This is the datetime the the first byte or chunk was written | [optional] [default to null]
**lastWriteDateTime** | [**Date**](DateTime.md) | This is the datetime the the last byte or chunk was  written | [optional] [default to null]
**taskChildId** | [**String**](string.md) | This is the task child id.  On create, this is the taskCorrelationId | [optional] [default to null]
**taskChildInputCount** | [**Integer**](integer.md) | This is the count of bytes or chunks available to the child. | [optional] [default to null]
**taskChildInputId** | [**String**](string.md) | This is the task child input id.  On create, this is the correlationId for the input IO Folder | [optional] [default to null]
**taskChildInputRemainingCount** | [**Integer**](integer.md) | This is the count of bytes or chunks remaining to the child. | [optional] [default to null]
**taskChildNumEngines** | [**Integer**](integer.md) | This is the number of engine instances running against this task. | [optional] [default to null]
**taskParentId** | [**String**](string.md) | This is the task parent id.  On create, this is the taskCorrelationId | [optional] [default to null]
**taskParentOutputCount** | [**Integer**](integer.md) | This is the count of bytes or chunks produced by the parent. | [optional] [default to null]
**taskParentOutputId** | [**String**](string.md) | This is the task parent output id.  On create, this is the correlationId for the output IO Folder | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

