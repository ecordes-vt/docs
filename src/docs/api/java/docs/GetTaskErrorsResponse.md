

# GetTaskErrorsResponse

This is the response for get Task error list Request
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count** | **Integer** | Total records for the query |  [optional]
**endDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime of the end of the stats period |  [optional]
**error** | [**Error**](Error.md) |  |  [optional]
**limit** | **Integer** | the number of records to return. |  [optional]
**offset** | **Integer** | the number of records to skip before getting the result set |  [optional]
**result** | [**List&lt;TaskErrorInfo&gt;**](TaskErrorInfo.md) |  |  [optional]
**startDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime of the beginning of the stats period |  [optional]
**success** | **Boolean** | If true, the operation was successful. |  [optional]



