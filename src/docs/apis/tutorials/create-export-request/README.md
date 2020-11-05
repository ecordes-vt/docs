# Creating Export Requests

Export requests can be made to export data out of aiWARE in specific formats.
They are requested via the [`createExportRequest` mutation](/apis/reference/mutation/?id=createexportrequest).

An example mutation might look like this:

```graphql
mutation createExportRequest {
 createExportRequest(input: {
   includeMedia: true
   tdoData: [{tdoId: "96972470"}, {tdoId: "77041379"}]
   outputConfigurations:[
     {
       engineId:"<engine ID>"
       categoryId:"67cd4dd0-2f75-445d-a6f0-2f297d6cd182"
       formats:[
         {
           extension:"ttml"
           options: {
             maxCharacterPerLine:32
             newLineOnPunctuation: true
           }
         }
       ]
     }
   ]
 }) {
   id
   status
   organizationId
   createdDateTime
   modifiedDateTime
   requestorId
   assetUri
 }
}
```

See the [API reference](https://api.veritone.com/v3/graphqldocs/createexportrequest.doc.html) for full documentation on all the available parameters.

## Supported Formats

The following lists the formats that are supported, as well as the options that affect that format.
Multiple formats can be requested in the same operation by including multiple specifications in the `formats` array.
Defaults for the options are provided in square brackets.

### Plain Text
* Extension to request: `txt`
* Format: [Plain Text](https://en.wikipedia.org/wiki/Plain_text)
* Options: 
  * `maxCharacterPerLine` [60]
  * `newLineOnPunctuation` [false]
  * `timeGapToSeparateParagraphMs` [0]
  * `fileExtension` [txt]

### Microsoft Word
* Extension to request: `docx`
* Format: [Microsoft Word](https://www.microsoft.com/en-us/microsoft-365/word)
* Options: 
  * `maxCharacterPerLine` [60]
  * `newLineOnPunctuation` [false]
  * `timeGapToSeparateParagraphMs` [0]
  * `fileExtension` [docx]

### Avid DS Subtitle
* Extension to request: `txtAvid`
* Format: [Avid DS subtitle](https://avid.secure.force.com/pkb/articles/en_US/Troubleshooting/en274573?retURL=%2Fpkb%2Farticles%2Fen_US%2FTroubleshooting%2Fen274573&popup=true)
* Options:
  * `maxCharacterPerLine` [30]
  * `newLineOnPunctuation` [false]
  * `timeGapToSeparateParagraphMs` [1000]
  * `linesPerScreen` [3] 
  * `timeGapToSeparateScreenMs` [5000] 
  * `withSpeakerData` [false]
  * `fileExtension` [txtAvid]

### SubRip
* Extension to request: `srt`
* Format: [SubRip](https://en.wikipedia.org/wiki/SubRip)
* Options:
  * `maxCharacterPerLine` [32]
  * `newLineOnPunctuation` [false]
  * `timeGapToSeparateParagraphMs` [1000] 
  * `linesPerScreen` [2]
  * `timeGapToSeparateScreenMs` [5000] 
  * `withSpeakerData` [false]
  * `fileExtension` [srt]

### Timed Text Markup Language
* Extension to request: `ttml`
* Format: [Timed Text Markup Language](https://www.w3.org/TR/2018/REC-ttml2-20181108/)
* Options:
  * `maxCharacterPerLine` [80] 
  * `newLineOnPunctuation` [false]
  * `timeGapToSeparateParagraphMs` [1000] 
  * `linesPerScreen` [1] 
  * `timeGapToSeparateScreenMs` [5000] 
  * `withSpeakerData` [false]
  * `fileExtension` [ttml]

### WebVTT
* Extension to request: `vtt`
* Format: [WebVTT](https://www.w3.org/TR/webvtt1/)
* Options:
  * `maxCharacterPerLine` [32] 
  * `newLineOnPunctuation` [false]
  * `timeGapToSeparateParagraphMs` [1000] 
  * `linesPerScreen` [2] 
  * `timeGapToSeparateScreenMs` [5000] 
  * `withSpeakerData` [false]
  * `fileExtension` [vtt]

### Veritone Standard
* Extension to request: `vlf`
* Format: [JSON: Veritone standard](https://docs.veritone.com/#/developer/engines/standards/engine-output/)
  * The `series` data array (and only the `series` data) from the requested engine's output file.
* Options:
  * `fileExtension` [vlf]

The `createExportRequest` is almost exclusively used to export caption files, so most of the formats only work
with outputs from Transcription engines (specifically: engine outputs that contain `series.words`).
The exception to this is the Veritone Standard (`vlf`) export which will export any engine's `series` data as 
raw JSON.


## Options

The (optional) `options` block for each format configures specific parameters for each requested export.
Not all options apply to all formats, see the list of supported formats above for which options you can use for which format.

| Option | Effect on Export |
| ---- | ---- |
| `maxCharacterPerLine` | Limits the maximum number of characters that fit on a single line. |
| `newLineOnPunctuation` | When `true` a new line will be started after punctuation that indicates a sentence has ended. This includes period `.`, question mark `?`, or exclamation point `!`. |
| `timeGapToSeparateParagraphMs` | The maximum length of time (in milliseconds) there can be a pause in speaking before a new line is started. |
| `linesPerScreen` | For formats that display blocks of lines as captions, this limits the maximum number of lines that can be in a block. |
| `timeGapToSeparateScreenMs` | The maximum length of time (in milliseconds) there can be a pause in speaking before a new block of text is started. |
| `withSpeakerData` | When `true` and speaker data is provided, this will force a new line to start whenever the speaker changes. It will also cause the output to include the current speaker's name. |
| `fileExtension` | Overrides the default extension for the output file. By default, the output file uses the `extension` that was requested in the export. However, if this option is provided then the `fileExtension` will be used for the output file instead. This is useful for formats like TTML where some applications require that TTML files have a `.ttml` extension, but others require that TTML files have a `.xml` extension. |

## Including Speaker Data

If you specify `withSpeakerData:true` in your request, then speaker data will be included in the output files.
Speaker data will be looked for in the following locations.

### Speaker Data Included with Transcription

If the transcription engine exports speaker data along with the words, it is assumed to be in the `object.label` 
field of the series. For example, the transcription might contain a series like the following:

```json
{
  "series": [
    {
      "startTimeMs":36600,
      "stopTimeMs":39300,
      "language":"en",
      "words":
      [
        { 
          "word":"legume",
          "confidence":0.78,
          "bestPath":true,
          "utteranceLength":1
        }
      ],
      "object": {
        "type": "speaker",
        "label": "Hammurabi"
      }
    }
  ]
}
```

In this case, the speaker of the word "legume" is "Hammurabi", and the export might contain something like

```
SPEAKER: Hammurabi (00:00:28:18 - 00:00:39:09)
Bring me a legume!
```

Of course, this assumes that the speaker for "Bring", "me" and "a" is also Hammurabi.

### Speaker Data from a Different Engine

Most often, the transcription engine will not include the speaker data, and a separate engine from the "Speaker Detection"
category (ID `a856c447-1030-4fb0-917f-08179f949c4e`) will also be run. 
In this case, the output from these engines will need to be merged to create the export. 
However, the export code needs to know which Speaker Detection data should be used, since there could be data from multiple
Speaker Detection engines available.

To identify the Speaker Detection data which should be used, a configuration for the desired engine must be specified.

> The configuration for the Speaker Detection engine may or may not have any `formats` fields defined. 
Formats for the Speaker Detection engine aren't normally requested in practice since the speaker data 
will already be in the export.

For example, if the Transcription data is from engine `c0e55cde-340b-44d7-bb42-2e0d65e98255`
and the Speaker Detection data is from engine `06c3f1d7-7424-407b-a3b5-6ef61154fc0b`, the following would request
a SRT export which includes the speaker data. Note that this assumes that the TDO has both engine's output
in it.

```graphql
mutation createExportRequest {
  createExportRequest(
    input: {
      includeMedia: true
      tdoData: [ {tdoId: "1230863020"} ]
      outputConfigurations: [
        {
          # transcription engine with the words
          engineId: "c0e55cde-340b-44d7-bb42-2e0d65e98255"
          categoryId: "67cd4dd0-2f75-445d-a6f0-2f297d6cd182"
          formats: [
            {
              extension: "srt"
              options: {
                newLineOnPunctuation: true
                withSpeakerData: true
              }
            }
          ]
        }
        {
          # speaker detection engine with the speaker data
          engineId: "06c3f1d7-7424-407b-a3b5-6ef61154fc0b"
          categoryId: "a856c447-1030-4fb0-917f-08179f949c4e"
          formats: [
            # formats is a required field, but we can leave it empty
          ]
        }
      ]
    }
  ) {
   id
   status
   organizationId
   createdDateTime
   modifiedDateTime
   requestorId
   assetUri
 }
}
```

?> The engine that generated the Speaker Detection data _must_ be in category "Speaker Detection" 
(ID `a856c447-1030-4fb0-917f-08179f949c4e`) to be identified as containing speaker data.

