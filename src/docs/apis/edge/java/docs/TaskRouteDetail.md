

# TaskRouteDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**endpoint** | [**UUID**](UUID.md) | This is endpoint to be used for this route.  This does not have to be unique. |  [optional]
**firstWriteDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the the first byte or chunk was written |  [optional]
**lastWriteDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the the last byte or chunk was  written |  [optional]
**taskChildId** | **String** | This is the task child id.  On create, this is the taskCorrelationId |  [optional]
**taskChildInputCount** | **Integer** | This is the count of bytes or chunks available to the child. |  [optional]
**taskChildInputId** | **String** | This is the task child input id.  On create, this is the correlationId for the input IO Folder |  [optional]
**taskChildInputRemainingCount** | **Integer** | This is the count of bytes or chunks remaining to the child. |  [optional]
**taskChildNumEngines** | **Integer** | This is the number of engine instances running against this task. |  [optional]
**taskParentId** | **String** | This is the task parent id.  On create, this is the taskCorrelationId |  [optional]
**taskParentOutputCount** | **Integer** | This is the count of bytes or chunks produced by the parent. |  [optional]
**taskParentOutputId** | **String** | This is the task parent output id.  On create, this is the correlationId for the output IO Folder |  [optional]



