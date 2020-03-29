# Flow Examples

Use these flow walkthroughs to quickly get a sense of what Automate Studio and flow engines can by understanding how these introductory and real use-cases of flow engines were created, step by step.

## Confidence Bot

The Confidence Bot runs as a flow engine and displays the confidence score of each word as part of the transcript that can be viewed both from the API as well as the CMS UI.

![confidence bot flow](src/docs/developer/flow/confidence-bot-flow.png)

### Tutorial Steps

1. The start of the Confidence Bot flow evaluates an inbound chunk sent from the Edge processing framework. The `inject` node payload mocks what the JSON of this chunk will resemble when it is injected into the flow engine at runtime.
2. First, the flow assigns some variables with the `change` node and then using the *tdoId*, we create a transcription processing job, assign two new variables and then use the aiWARE Poll subflow to poll the transcription engine job.
3. Once the transcription job has finished, we then query the newly created asset for the transcription engine results.
4. Next, the flow then parses the transcript and creates a new file that contains both the transcribed words *and* the confidence score next to each word.
5. The flow then retrieves the active user details associated with creating this flow engine request, formats the email with an aiWARE HTML template (you are welcome to reuse and modify! :blue_heart: ) and then sends to the user who created the processing request!

## Logo Recognition

This flow example illustrates how you can publish flows in Automate Studio as cognitive engines that introduce new cognitive models onto aiWARE.

![logo recognition](src/docs/developer/flow/automate-logo-recognition.png)

?> Note: There are multiple ways to creative cognitive engines, including running the cognitive model and wrapping in the engine or (as seen in this example) making calls to a third party API to send each chunk message (eg, a slice of a file) to that service for processing.

### Tutorial Steps

1. Like any flow in Automate Studio, we can read the logic from left to right like reading a book, and let’s examine this flow by slicing it up into thirds.
2. In the first third of this flow, we see two *http in* nodes as well as an *http response* node. These nodes are part of the webhook pattern for how the flow engine communicates with aiWARE at runtime.
3. This is what the engine toolkit expects, and all flow engines need to conform to this design to successfully run as engines on aiWARE.
4. The *function* node performs a filtering function, checking the msg.payload properties of the chunk payload that is injected into the flow engine at runtime and evaluating if the message is indeed a “media_chunk” and the “mimeType” is “image/jpeg.”
5. If there are chunk messages injected into the flow engine at runtime that do not meet the criteria, the if statement formats an ignore msg that is then sent back as the http response at runtime.
6. The middle third of the flow is the most straightforward. Starting with the “set payload and headers” function node, we prepare the properties in the `msg` for making an API http request to the Logo Recognition service, in this case, Google’s Logo Recognition model.
7. Each image chunk is sent to the Google Logo API and returns a response that the http request node captures and sends to the “transform VTN” function node, which parses the response, and assuming the response was successful, formats the updated chunk message to include the cognitive results and then propagates the entire `msg` to the “output to Edge” *http response* node.
8. Behind the scenes (and outside the flow engine runtime), aiWARE Edge will stitch the results of the Logo Recognition process back together and attach the output data (as an asset) to the Temporal Data Object that the user invoked the engine to run on.

!> Please note: you will need your own Google API key if you are trying to run and publish your own version of this flow engine.
