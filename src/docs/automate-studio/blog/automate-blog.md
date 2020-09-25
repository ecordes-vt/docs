# Automate Studio Blog

*Welcome! This is the aiWARE team's section for sharing our thoughts on Automate Studio and how we think it fits with aiWARE and making AI more accessible to non-engineers and non-Data Scientists *

## Blog 2: AI recognized your face. Now what?

*Blog date: 2020-09-09*

Conversations about Face Recognition and its various risks are as popular topics for discussion as the various use-cases around Face Recognition. But how can we make this topic not only more approachable but also more useful for people who are not engineers and Data Scientists?

The way everyone usually starts out is by talking about a use-case that frames both the problem and how the technology in question can be used to solve it in a new and more efficient way.

In this case, Face Recognition refers to a category of AI cognition that performs a two-step operation:

1. Processing an image of a video (which is a series of images) and detecting faces
1. Then looping through the list of detected faces and attempting to “recognize” faces by comparing certain signatures against a pre-loaded library of faces determined by the user who kicked off the original operation

With that definition in mind, what use-case could this technology solve? Well, an increasingly common use-case is using Face Recognition as part of a Biometric identity layer where the user’s face is included as part of a process to verify identity and unlock either the device or perform some follow up action like alerting a predefined recipient with an email or text message.

There’s certainly an argument that this use-case could be solved with “a few lines of code” (how often have we heard that!) but what if we are not software engineers ourselves? And all the software engineers are busy? And even if we were engineers, are we going to build the scaffolding, monitoring, and framework to safely and repeatedly run the AI models on demand from any number of customers?

A quick scan of the screenshot below shows that Automate Studio addresses these questions with its drag and drop interface, with each of those “nodes” executing logic defined by the user designing the flow in Automate Studio’s editor.

As we examine this flow, we can break the flow up into separate sections for ingesting the data, analyzing the data, formatting a text message, using a third party SMS service (Twilio in this case) to send the SMS to the designated recipient and then shutting the flow down. Each of these steps are visually represented and executed as logic that can then be scalably run for both you, and any other users that you want to share your flows with.

What do you want to build with AI models now that so many of them are available and usable in one place? If you have an idea, consider [signing up for Automate Studio](https://veritone.com/onboarding/#/signUp?type=automate&Lead_Source_Detail=Automate%20Blog%20Face%20Recognition%20Flow) and see what you can do with 20+ categories of AI cognition.

Feel free to reach out to us with any questions, and we also have bounties out for any of these [unclaimed flow ideas](https://docs.veritone.com/#/automate-studio/flow-bounties/README) that you might be interested in taking on!

## Blog 1: Orchestrating AI with Automate Studio

*Blog Date: 2020-09-02*

Both Enterprises and startups alike are discovering that developing an AI/ML model itself is only a piece of the overall challenge in producing an AI/ML model that can be useful to their users in a production context. As we’ll discover in this blog post however, Automate Studio bridges the logical gaps between determining which cognitive engines to run and then acting on the results from that cognitive processing in a way that can be quickly setup and deployed into a production context.

In this example, we’ll dive into a real world use-case as well an example of how to solve that problem with a flow created in Automate Studio. In this case, we need to produce a transcript that is also separated by each detected speaker. Before we get started in Automate Studio, we can illustrate this workflow in the process diagram below:

![process-diagram](/_automateBlog1-img1.png)

You can see how more of these steps are not only concurrently executed, but because of the interoperability of the cognitive outputs, we can now construct business logic that safely assumes consistency of results from each AI/ML model, regardless of the original creator, and that permits us to create a Speaker Separated Transcript that conforms to the file specifications defined by the customer (eg a TTML file for Broadcast captioning)

Automate Studio was built to enable orchestrating and running AI/ML processing for the rest of us who are not Data Scientists, Machine Learning engineers, or DevOps, so we can all apply AI/ML to their own lives and problem sets.

In this screenshot below, you can see how we implemented the use-case above as a visual workflow in Automate Studio. Each of the shapes displayed executes a key piece of logic, whether invoking the AI/ML models to run against a specified file path, or handling key lifecycle aspects of the flow itself to ensure successful horizontal scaling on the Veritone aiWARE processing framework.

![flow-screencap](/_automateBlog1-img2.png)

You can see the entire flow for this-use case we defined using Automate Studio in the image above: the flow takes an input of a media file’s reference path, we orchestrate two AI/ML cognitive models, we merge the results, create a new file, and write the new file to a third party storage system.

Once the flow logic has created our container for this new piece of media, we then orchestrate two AI Cognitive models (referred to as “cognitive engines” when run on our aiWARE processing framework) to concurrently process the audio file for both NLP transcription and speaker separation.

The flow waits for both processes to finish, then merges the “cognitive output” results together.

This flow is just one example of how Automate Studio pushes humans to become supervisors at the edge of previously manual workflow loops, and if you are reading this and would like to join us in this mission as a partner, [consider signing up for Automate Studio](https://veritone.com/onboarding/#/signUp?type=automate&Lead_Source_Detail=Automate%20Blog%20Speaker%20Separated%20Transcription) and checking out our Early Adopters Program where we [offer bounties](https://docs.veritone.com/#/automate-studio/flow-bounties/README) for helping create AI/ML powered flows like the one we just discussed.
