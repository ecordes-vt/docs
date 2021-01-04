

# EngineErrorTimeRangesCountsInfo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count** | **Long** | Total amount of engine error with a particular status and a time range |  [optional]
**endDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | Start of a time range |  [optional]
**engineID** | [**UUID**](UUID.md) |  |  [optional]
**engineName** | **String** | Engine name |  [optional]
**startDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | Start of a time range |  [optional]
**values** | [**List&lt;List&lt;Long&gt;&gt;**](List.md) | This is an array of failed task count by engine_id in a time range. Item format [timestamp, count] |  [optional]



