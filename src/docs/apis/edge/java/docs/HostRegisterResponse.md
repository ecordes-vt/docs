

# HostRegisterResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**configProperties** | [**HostRegisterResponseConfigProperties**](HostRegisterResponseConfigProperties.md) |  |  [optional]
**hostID** | [**UUID**](UUID.md) | Old or NEW Host ID dependinng on whether it was registered before |  [optional]
**hostToken** | [**UUID**](UUID.md) | API Token for Host to use going forward. |  [optional]
**mount** | [**List&lt;HostMountInfo&gt;**](HostMountInfo.md) |  |  [optional]
**status** | [**HostAction**](HostAction.md) |  |  [optional]



