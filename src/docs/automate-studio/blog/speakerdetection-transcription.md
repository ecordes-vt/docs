# How I learned to stop worrying and manage my AI with Automate

Both Enterprises and startups alike are discovering that developing an AI/ML model itself is only a piece of the overall challenge in producing an AI/ML model that can be useful to their users in a production context. As we’ll discover in this blog post however, Automate Studio bridges the logical gaps between determining which cognitive engines to run and then acting on the results from that cognitive processing in a way that can be quickly setup and deployed into a production context.

In this example, we’ll dive into a real world use-case as well an example of how to solve that problem with a flow created in Automate Studio. In this case, we need to produce a transcript that is also separated by each detected speaker. Before we get started in Automate Studio, we can illustrate this workflow in the process diagram below:

You can see how more of these steps are not only concurrently executed, but because of the interoperability of the cognitive outputs, we can now construct business logic that safely assumes consistency of results from each AI/ML model, regardless of the original creator, and that permits us to create a Speaker Separated Transcript that conforms to the file specifications defined by the customer (eg a TTML file for Broadcast captioning)

Automate Studio was built to enable orchestrating and running AI/ML processing for the rest of us who are not Data Scientists, Machine Learning engineers, or DevOps, so we can all apply AI/ML to their own lives and problem sets.

In this screenshot below, you can see how we implemented the use-case above as a visual workflow in Automate Studio. Each of the shapes displayed below executes a key piece of logic, whether invoking the AI/ML models to run against a specified file path, or handling key lifecycle aspects of the flow itself to ensure successful horizontal scaling on the Veritone aiWARE processing framework.

You can see the entire flow for this-use case we defined using Automate Studio in the image above: the flow takes an input of a media file’s reference path, we orchestrate two AI/ML cognitive models, we merge the results, create a new file, and write the new file to a third party storage system.

Once the flow logic has created our container for this new piece of media, we then orchestrate two AI Cognitive models (referred to as “cognitive engines” when run on our aiWARE processing framework) to concurrently process the audio file for both NLP transcription and speaker separation. 

The flow waits for both processes to finish, then merges the “cognitive output” results together.

This flow is just one example of how Automate Studio pushes humans to become supervisors at the edge of previously manual workflow loops, and if you are reading this and would like to join us in this mission as a partner, [consider signing up for Automate Studio](https://veritone.com/onboarding/#/signUp?type=automate&Lead_Source_Detail=Automate%20Blog%20Speaker%20Separated%20Transcription) and checking out our Early Adopters Program where we [offer bounties](https://docs.veritone.com/#/automate-studio/flow-bounties/README) for helping create AI/ML powered flows like the one we just discussed.
