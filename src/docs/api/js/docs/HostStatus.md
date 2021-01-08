# AiwareJsClient.HostStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cPUUtilized** | **Number** | The CPU of the container as a percentage from 0-100 | [optional] 
**gPUAvailable** | **Number** | The number of GPU available | [optional] 
**containerStatus** | [**[HostStatusContainer]**](HostStatusContainer.md) |  | [optional] 
**diskAvailableOptAiware** | **Number** | The available bytes in the /opt/aiware partition | [optional] 
**diskAvailableRoot** | **Number** | The available bytes in the root partition | [optional] 
**engineToolkitVersion** | **String** | The version of engine toolkit format to be gitbranch:gitcommit:epochBuildDate | [optional] 
**hostID** | **String** |  | [optional] 
**memoryAvailable** | **Number** | The available memory to the container in bytes | [optional] 
**memoryUsed** | **Number** | The memory used by container in bytes | [optional] 
**numCPU** | **Number** | Total CPU | [optional] 
**numContainers** | **Number** | The number of containers running | [optional] 
**numEngineInstances** | **Number** | The number of engine instances running | [optional] 
**numGPU** | **Number** | Total GPU | [optional] 
**vCPUAvailable** | **Number** | The number of vCPUs available.  THis is calculated by Number of CPUs * % available * 1024 | [optional] 


