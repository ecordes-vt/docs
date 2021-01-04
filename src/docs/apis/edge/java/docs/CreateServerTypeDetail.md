

# CreateServerTypeDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
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
**disableLaunchingBacklogEngines** | **Boolean** |  |  [optional]
**gpuType** | [**GPUEnum**](GPUEnum.md) |  |  [optional]
**hasGPU** | **Boolean** |  |  [optional]
**isAutoScaleActive** | **Boolean** |  |  [optional]
**maxServers** | **Long** |  |  [optional]
**memoryBytes** | **Long** |  |  [optional]
**minServers** | **Long** |  |  [optional]
**numGPU** | **Long** |  |  [optional]
**onlyOrganizationId** | [**UUID**](UUID.md) |  |  [optional]
**runModes** | [**List&lt;RunModeEnum&gt;**](RunModeEnum.md) | run modes |  [optional]
**serverConfigJSON** | **String** |  |  [optional]
**serverProvider** | [**ServerProviderEnum**](ServerProviderEnum.md) |  |  [optional]
**serverTypeID** | [**UUID**](UUID.md) |  |  [optional]
**vcpus** | **Long** |  |  [optional]



