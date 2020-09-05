# How I learned to stop worrying and manage my AI with Automate

Both Enterprises and startups alike are discovering that developing an AI/ML model itself is only a quarter of the overall challenge of producing an AI/ML model that can be useful to users in a production context. As we’ll discover in this blog post however, Automate Studio bridges the logical gaps between determining which cognitive engines to run and then acting on the results from that cognitive processing in a way that can be quickly setup and deployed into a production context.
In particular, we’ll be diving into a flow created in Automate Studio that solves a common use-case across a variety of industries and departments where the user needs to produce a transcript that is also separated by each detected speaker. 
The ask sounds simple enough but let’s break this workflow down into a series of steps that a human would have to perform to accomplish this task, seen in this process diagram below:

You can see how more of these steps are not only concurrently executed, but because of the interoperability of the cognitive outputs, we can now construct business logic that safely assumes consistency of results from each AI/ML model, regardless of the original creator, and that permits us to create a Speaker Separated Transcript that conforms to the file specifications defined by the customer (eg a TTML file for Broadcast captioning)

Now that we have our workflow designed with this new reference process diagram, we can more effectively direct ourselves into how we implement this solution using Veritone Automate Studio.

Automate Studio was built to enable orchestrating and running AI/ML processing for the rest of us who are not Data Scientists, Machine Learning engineers, or DevOps, so we can all apply AI/ML to their own lives and problem sets.

In this screenshot below, you can see how we implemented the use-case above as a visual workflow in Automate Studio. Each of the shapes displayed below executes a key piece of logic, whether invoking the AI/ML models to run against a specified file path, or handling key lifecycle aspects of the flow itself to ensure successful horizontal scaling on the Veritone aiWARE processing framework.

You can see the entire flow for this-use case we defined using Automate Studio in the image above: the flow takes an input of a media file’s reference path, we orchestrate two AI/ML cognitive models, we merge the results, create a new file, and write the new file to a third party storage system.

As we drill into the flow created in the Automate Studio editor, we can see that the shapes implemented actually map fairly closely to the most recent visual process diagram we created above.
The flow first takes in a piece of input data, in this case a payload that contains a file path of the file we want to start processing, we then create a “container” in aiWARE to house both that media file and any additional AI cognitive outputs (eg transcripts, JSON metadata) created from processing the media associated to that container in the future.
	Once the flow logic has created our container for this new piece of media, we then orchestrate two AI Cognitive models (referred to as “cognitive engines” when run on our aiWARE processing framework) to concurrently process the audio file for both NLP transcription and speaker separation. 


The flow waits for both processes to finish, then merges the “cognitive output” results together.

As we discovered earlier, the node shapes contain logic that executes, and nodes that contain other nodes are called “subflows.” The last section of the flow consists of a subflow wherein each node performs some data preparation steps, creates an actual TTML file, and finally writes to our web storage of choice with an S3 connector node.

Before we write to S3, our logic first retrieves and parses the cognitive outputs--each one stored and retrieved in our vtn-standard JSON format--with some custom business logic that we can easily create to match each specialized use-case. In this case, we are creating a TTML file that has use-cases for time-correlating Spoken Word to Audio/Visual content in industries as diverse as broadcast media and law enforcement for cybercrimes investigations.

This flow is just one example of how Automate Studio pushes humans to become supervisors at the edge of previously manual workflow loops, and if you are reading this and would like to join us in this mission as a partner, consider signing up for Automate Studio and checking out our Early Adopters Program where we offer bounties for helping create AI/ML powered flows like the one we just discussed.
