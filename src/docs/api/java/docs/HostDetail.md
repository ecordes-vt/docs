

# HostDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**agentCommitID** | **String** | The agent ID |  [optional]
**agentLabel** | **String** | The build label for the agent |  [optional]
**agentVersionNumber** | **String** | the agent version |  [optional]
**cloudProviderInstanceID** | **String** | The instance id for the cloud provider |  [optional]
**controllerPort** | **Long** | Controller Port |  [optional]
**createdDateTime** | [**OffsetDateTime**](OffsetDateTime.md) |  |  [optional]
**dbPort** | **Long** | DB Port |  [optional]
**dockerHostID** | **String** | This is the docker host ID |  [optional]
**dockerInfo** | **String** | The output from &#x60;docker info&#x60; |  [optional]
**drain** | **Boolean** | It should indicate whether the server is draining or not |  [optional]
**drainDetail** | **String** | More information if available on the drain action |  [optional]
**drainReason** | [**HostDrainReasonEnum**](HostDrainReasonEnum.md) |  |  [optional]
**expirationDateTime** | [**OffsetDateTime**](OffsetDateTime.md) |  |  [optional]
**gpuAvailable** | **Long** | This is the number of GPU available on the host |  [optional]
**gpuType** | **String** | This is the type of GPU such as Tesla K80 |  [optional]
**hostID** | **String** | This is the host id |  [optional]
**ips** | **List&lt;String&gt;** | An array of IPs either IPv4 or IPv6 that are valid for this host |  [optional]
**isAPI** | **Boolean** | Is this host core api |  [optional]
**isActive** | **Boolean** | Is this host active |  [optional]
**isApps** | **Boolean** | Is this host core apps |  [optional]
**isAssigned** | **Boolean** | Is this host assigned |  [optional]
**isAutomate** | **Boolean** | Is this host automate |  [optional]
**isController** | **Boolean** | Is this host a controller |  [optional]
**isDB** | **Boolean** | Is this host a db server |  [optional]
**isES** | **Boolean** | Is this host elasticsearch |  [optional]
**isEngine** | **Boolean** | Is this host an engine |  [optional]
**isEventing** | **Boolean** | Is this host eventing |  [optional]
**isLB** | **Boolean** | Is this host load balancer |  [optional]
**isNFS** | **Boolean** | Is this host an nfs server |  [optional]
**isNSQ** | **Boolean** | Is this host nsq |  [optional]
**isPrometheus** | **Boolean** | Is this host prometheus |  [optional]
**isRedis** | **Boolean** | Is this host redis |  [optional]
**isRegistry** | **Boolean** | Is this host a docker registry |  [optional]
**lastUpdateDateTime** | [**OffsetDateTime**](OffsetDateTime.md) |  |  [optional]
**memory** | **Long** | This is the memory in bytes |  [optional]
**modifiedDateTime** | [**OffsetDateTime**](OffsetDateTime.md) |  |  [optional]
**nfsPartition** | **Long** | NFS Partition number |  [optional]
**nfsPort** | **Long** | NFS Port |  [optional]
**numCPU** | **Long** | This is the number of CPUs on the host |  [optional]
**numEngines** | **Long** | This is the number of engines on the host |  [optional]
**numGPU** | **Long** | This is the number of GPUs on the host |  [optional]
**registryPort** | **Long** | Registry Port |  [optional]
**runModes** | **String** | This is the mode of server type to run |  [optional]
**serverTypeID** | [**UUID**](UUID.md) | This is the server type |  [optional]
**serverTypeName** | **String** | This is the name of server type |  [optional]
**shouldExpire** | **Boolean** | Should this host expire.  Default to false. |  [optional]
**suggestedRuntimeTTL** | **Integer** | The length of time this host suggest it should be up |  [optional]
**terminationDateTime** | [**OffsetDateTime**](OffsetDateTime.md) |  |  [optional]
**terminationDetail** | **String** | More information if available on the termination |  [optional]
**terminationReason** | [**HostTerminationReasonEnum**](HostTerminationReasonEnum.md) |  |  [optional]
**vcpuAvailable** | **Long** | This is the number of vcpu availables on the host |  [optional]



