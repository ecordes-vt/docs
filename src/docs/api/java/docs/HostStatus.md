

# HostStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cpUUtilized** | **Float** | The CPU of the container as a percentage from 0-100 |  [optional]
**gpUAvailable** | **Integer** | The number of GPU available |  [optional]
**containerStatus** | [**List&lt;HostStatusContainer&gt;**](HostStatusContainer.md) |  |  [optional]
**diskAvailableOptAiware** | **Long** | The available bytes in the /opt/aiware partition |  [optional]
**diskAvailableRoot** | **Long** | The available bytes in the root partition |  [optional]
**engineToolkitVersion** | **String** | The version of engine toolkit format to be gitbranch:gitcommit:epochBuildDate |  [optional]
**hostID** | [**UUID**](UUID.md) |  |  [optional]
**memoryAvailable** | **Long** | The available memory to the container in bytes |  [optional]
**memoryUsed** | **Long** | The memory used by container in bytes |  [optional]
**numCPU** | **Integer** | Total CPU |  [optional]
**numContainers** | **Integer** | The number of containers running |  [optional]
**numEngineInstances** | **Integer** | The number of engine instances running |  [optional]
**numGPU** | **Integer** | Total GPU |  [optional]
**vCPUAvailable** | **Integer** | The number of vCPUs available.  THis is calculated by Number of CPUs * % available * 1024 |  [optional]



