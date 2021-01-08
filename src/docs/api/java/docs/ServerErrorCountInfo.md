

# ServerErrorCountInfo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count** | **Long** | This is the total of error for current service. |  [optional]
**endDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | End of a time range |  [optional]
**errorCode** | **String** |  |  [optional]
**service** | **String** |  |  [optional]
**startDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | Start of a time range |  [optional]
**values** | [**List&lt;List&lt;Long&gt;&gt;**](List.md) | This is an array of data count by time for current errorCode. Item format [timestamp, count] |  [optional]



