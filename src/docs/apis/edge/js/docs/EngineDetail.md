# AiwareJsClient.EngineDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**applicationIDsJSON** | **String** | JSON Data for application_id | [optional] 
**childPriorityAdjustmentOnComplete** | **Number** | When this task completes, adjust the priority of child tasks by this value | [optional] 
**cpuShares** | **Number** |  | [optional] 
**createdDateTime** | **Date** | This is the datetime the core was created | [optional] 
**dependencyJSON** | **String** | JSON Data for dependency | [optional] 
**dontrunComplete** | **Boolean** | If true, do not run this engine.  Complete as soon as possible and do not assign work. | [optional] 
**edgeVersion** | **Number** | edge version of the engine | [optional] 
**engineCategoryID** | **String** | The UUID of the Engine Category | [optional] 
**engineID** | **String** |  | [optional] 
**engineName** | **String** | Name of the Engine | [optional] 
**engineOutputType** | [**EngineTypeEnum**](EngineTypeEnum.md) |  | [optional] 
**engineState** | [**EngineStateEnum**](EngineStateEnum.md) |  | [optional] 
**engineType** | [**EngineTypeEnum**](EngineTypeEnum.md) |  | [optional] 
**fieldsJSON** | **String** | JSON Data for fields | [optional] 
**idleTimeout** | **Number** |  | [optional] 
**internalOrganizationID** | **String** |  | [optional] 
**jwtRightsJSON** | **String** | JSON Data for jwt_rights | [optional] 
**maxProcessingSecondsPerWorkItem** | **Number** |  | [optional] 
**maxWaitSecondsForChunk** | **Number** |  | [optional] 
**minAvailable** | **Number** |  | [optional] 
**minRunning** | **Number** |  | [optional] 
**modifiedDateTime** | **Date** | This is the datetime the core was last modified. | [optional] 
**numChunksPerWorkItem** | **Number** |  | [optional] 
**parallelProcessing** | **Boolean** | If true, the engine can handle multiple instances working against the same chunk task. | [optional] 
**parentCompleteBeforeStart** | **Boolean** | If true, the engine waits for the parent(s) to be complete before starting | [optional] 
**preload** | **Boolean** | If it is &#x60;true&#x60;, that means the engine need to pull docker image to local | [optional] 
**priorityAdjustment** | **Number** | On new tasks with this engine, add this value to the priority of that task | [optional] 
**replacementEngineID** | **String** |  | [optional] 
**updateStatusInterval** | **Number** |  | [optional] 
**validationJSON** | **String** | JSON Data for validation | [optional] 


