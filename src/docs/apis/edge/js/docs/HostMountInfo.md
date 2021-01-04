# AiwareJsClient.HostMountInfo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cacheNumber** | **Number** | the cache number for the nfs mount.  0 is /cache, 1 is /cache/1, ... | [optional] 
**ips** | **[String]** | The host name or IP to mount. | [optional] 
**localPath** | **String** | The mount on the local filesystem | [optional] 
**mountType** | [**HostMountTypeEnum**](HostMountTypeEnum.md) |  | [optional] 
**options** | **String** | a comma separated list of options to pass into the mount commmand.  An example is nfsvers&#x3D;4,rsize&#x3D;1048576,wsize&#x3D;1048576,hard,timeo&#x3D;600,retrans&#x3D;2,noresvport | [optional] 
**port** | **Number** | The port the NFS service is listening on | [optional] 
**priority** | **Number** | The priority to mount them.  Lowest first to highest numbers.  For example, /cache is 10, /cache/1 is 100. If they have the same priority then they are run in random order for the priority number. | [optional] 
**serverPath** | **String** | The mount path to mount | [optional] 


