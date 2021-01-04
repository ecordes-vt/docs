

# TaskIO

An input or output folder.  For type output, all fields required. For type input, only id is required.
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | The io id |  [optional]
**inputFolders** | [**List&lt;TaskIOFolder&gt;**](TaskIOFolder.md) | For each output, link into the input(s) folders. |  [optional]
**ioMode** | [**TaskIOModeEnum**](TaskIOModeEnum.md) |  |  [optional]
**ioType** | [**TaskIOTypeEnum**](TaskIOTypeEnum.md) |  |  [optional]
**options** | **Object** | Options for generating the output, e.g. frame rates, output media format etc. |  [optional]



