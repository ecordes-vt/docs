

# ServerTypeDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activeHostCount** | **Long** |  |  [optional]
**agentStartupScript** | **String** |  |  [optional]
**awsAmi** | **String** |  |  [optional]
**awsInstanceProfile** | **String** |  |  [optional]
**awsInstanceType** | **String** |  |  [optional]
**awsKeyName** | **String** |  |  [optional]
**awsSecurityGroups** | **List&lt;String&gt;** | aws subnets |  [optional]
**awsSpot** | **Boolean** |  |  [optional]
**awsSpotMaxPrice** | **Float** |  |  [optional]
**awsSpotPersistent** | **Boolean** |  |  [optional]
**awsSubnets** | **List&lt;String&gt;** | aws subnets |  [optional]
**awsTagsJSON** | **String** |  |  [optional]
**awsUserData** | **String** |  |  [optional]
**createdDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the core was created |  [optional]
**disableLaunchingBacklogEngines** | **Boolean** |  |  [optional]
**drainingHostCount** | **Long** |  |  [optional]
**gpuType** | [**GPUEnum**](GPUEnum.md) |  |  [optional]
**hasGPU** | **Boolean** |  |  [optional]
**isAutoScaleActive** | **Boolean** |  |  [optional]
**maxServers** | **Long** |  |  [optional]
**memoryBytes** | **Long** |  |  [optional]
**minServers** | **Long** |  |  [optional]
**modifiedDateTime** | [**OffsetDateTime**](OffsetDateTime.md) | This is the datetime the core was last modified. |  [optional]
**numGPU** | **Long** |  |  [optional]
**onlyOrganizationId** | [**UUID**](UUID.md) |  |  [optional]
**pendingHostCount** | **Long** |  |  [optional]
**runModes** | [**List&lt;RunModeEnum&gt;**](RunModeEnum.md) | run modes |  [optional]
**serverConfigJSON** | **String** |  |  [optional]
**serverProvider** | [**ServerProviderEnum**](ServerProviderEnum.md) |  |  [optional]
**serverTypeID** | [**UUID**](UUID.md) |  |  [optional]
**vcpus** | **Long** |  |  [optional]



