# Automate Studio Blog

*Welcome! This is the aiWARE team's section for sharing our thoughts on Automate Studio and how we think it fits with aiWARE and making AI more accessible to non-engineers and non-Data Scientists*

## Blog 4: Sentiment Analysis on Your Helpdesk Tickets

*Blog Date: 2020-09-24*

*In this blog post, we’ll learn about how Sentiment analysis processes the support tickets loaded from a sample Helpdesk system (in this case Help Scout) and process the body text with Sentiment analysis and send the results back to the helpdesk system for the Customer Support team to use in their customer service reporting.*

Various studies have found that Customer Success and support teams typically have the least support in the form of sophisticated tools and attempt to overcompensate for these shortcomings by over hiring staff. The result is an inconsistently trained and motivated workforce that in turn leads to wildly disproportionate overhead. However, Customer Success and Support teams can regain both efficiency and effectiveness by adopting a metrics focused approach to triage and understanding each customer cumulatively from all their prior interactions.

In this blog, we’ll do a quick dive on how Veritone’s Automate Studio can enable a new kind of data driven approach to enabling your Customer Service teams to more quickly understand and triage your customers they are trying to support.

In a common Customer Service scenario, the Customer Service teams will all be operating out of a centralized Helpdesk system that collects tickets submitted by customers and leads through various channels including social media, web portals, and email to the support line.

We can assume that all the tickets of interest are already consolidated in a centralized Helpdesk system like Help Scout, and now the Customer Service team needs help understanding the sentiment of each customer inquiry as a way to both prioritize and filter by various needs.

Using Automate Studio, we can visualize the flow and with some additional logic, customize both our integration as well as the flow of data and which Cognitive AI engines to use. In this case, our goal is to download all of the active helpdesk tickets and process the body text with sentiment analysis and write the results back to Help Scout as a tag. The flow will look something like this:

Once our flow is deployed to run as an engine on aiWARE’s horizontally scaling framework, we can invoke the engine to run with this GraphQL API call:

```graphql
# Igniter + Flow engine job
# Write your query or mutation here
mutation createYourFlowEngineJobWithIgniter {
  createJob(input: {
    target: {
       startDateTime:1574311000
       stopDateTime: 1574315000
    }
    ##V3 Prod Cluster
    clusterId :"rt-1cdc1d6d-a500-467a-bc46-d3c5bf3d6901"
    ##Tasks with IOFolders
    tasks: [
        {
          # "correlationTaskId": "IG_TASK_ID",
          # "dueDateTime": "0001-01-01T00:00:00Z",
          # V3 Igniter Engine
          engineId: "5305265c-d566-4716-8904-debf7e0ac857"
          ioFolders: [
            {
              referenceId: "IG_OUTPUT"
              mode: chunk
              type: output
            }
          ]
          executionPreferences: 
          	{
              priority: -99
            }
        }
        {
          # This is the task that is an instance of the flow engine you created in Automate Studio!
          # Hello Igniter test Flow
          engineId: "4b06ac66-c04b-4f00-ba9c-b07e2f73aa24"
          ioFolders: [
            {
              referenceId: "MY_INPUT"
              mode: chunk
              type: input
            }
          ]
          executionPreferences: 
          	{
              priority: -99
            }
        }
      ]
    ##Routes : A route connect a parent output folder to a child input folder
    routes: [
        {
          ## Igniter V3F route
          parentIoFolderReferenceId: "IG_OUTPUT"
          childIoFolderReferenceId: "MY_INPUT"
          options: {}
        }
      ]
  }) {
    id
    targetId
    clusterId
    tasks {
      records{
        id
        engineId
        payload
        taskPayload
        status
        output
        ioFolders {
          referenceId
          type
          mode
        }
      }
    }
    routes {
      parentIoFolderReferenceId
      childIoFolderReferenceId
    }
  }
}
```

One of the lesser known features that aiWARE offers is the ability to schedule *any* engine, and flow engines can benefit from this feature as well. This is a sample GraphQL API operation for scheduling a flow to run on a time-based interval:

```graphql
mutation createScheduleJob {
  createScheduledJob(input:
    {
      name: "qv3TestEverye5Minute"
      runMode:Recurring
      recurringScheduleParts: [ 
      {
        #Schedule the job to run every 5 minutes
        repeatIntervalUnit : Minutes
        repeatInterval: 5
    
      }]
      jobTemplates:[
        {
          # PROD V3
          clusterId: "rt-1cdc1d6d-a500-467a-bc46-d3c5bf3d6901"
          taskTemplates : [
          {
           #Igniter engine V3F
           engineId: "9e611ad7-2d3b-48f6-a51b-0a1ba40fe255"
         },
        {
          #Flow Engine
          engineId: "352556c7-de07-4d55-b33f-74b1cf237f25"
        }
          ]
        }
      ]
    }
  )
    {
      id
    } 
}
```

What do you want to build with AI models now that so many of them are available and usable in one place? If you have an idea, consider [signing up for Automate Studio](https://veritone.com/onboarding/#/signUp?type=automate&Lead_Source_Detail=Automate%20Blog4%20Sentiment%20Helpdesk%20Flow) and see what you can do with 20+ categories of AI cognition.

Feel free to reach out to us with any questions, and we also have bounties out for any of these [unclaimed flow ideas](https://docs.veritone.com/#/automate-studio/flow-bounties/README) that you might be interested in taking on!

## Blog 3: Your AI flow, for the World

*Blog Date: 2020-09-16*

The concept of a business process is as old as human labor itself, even with Egyptian manuals meticulously describing the process for various goods production. With the growth of software development in the 1980s and the subsequent boom and bust cycles of the commercial internet in the 1990s, new languages developed for how people could navigate-- and manipulate-- new a new kind of internet native content.

In the Fourth Industrial revolution, AI is now heralded as a leading technological factor, but this potential risks falling short without meaningful tools for a broader group of people to manage, orchestrate, and share their AI models to meaningfully capitalize on the foundational layers set in the previous decades. With the cambrian explosion of AI models, we believe Veritone’s Automate Studio can make these various categories of AI cognition understandable and practical for use by non-engineers to solve their business and personal challenges.

We’ll look at an example of a flow engine created in Automate Studio that uses the NLP/Transcription cognitive category and how that flow can be used by organizations and individuals completely separate from the original flow creator. Before we dive in let’s first understand why both those components matter.

A helpful way to think of Artificial Intelligence (AI) is to consider it as a process for taking in one type of file format, like an audio or video file and producing a new kind of file based on what the AI model predicts it should output. That’s right, these AI models are basically doing a sophisticated kind of guessing, based on how and what they have been trained to predict on. For example, Transcription AI models are trained to analyze a piece of audio and guess what the words being spoken are based on several factors including what human language the model was trained to understand.  We can already see that this means we will need many different kinds of AI machine learning models to perform specialized tasks and this means we will need a system to evaluate the Cognitive Results from each process and then orchestrate what we want to do next based on the results.

The internet made us more interconnected with social media like Twitter and Facebook, but even businesses were able to connect more quickly and efficiently with APIs (Application Programming Interface) designed specifically to be used by users and services across the web to quickly communicate with each other. The web APIs are particularly important because they enable completely separate applications to securely and rapidly share information with each other.

With that background, we can see how Automate Studio builds in both these concepts and enables non-engineers and non-Data Scientists to construct their own AI workflows with a drag-and-drop approach that executes the logic they define.

Further, Automate Studio is built on aiWARE which handles the versioning and lifecycle management of both the AI models as well as the workflows themselves which means as an Automate Studio user, you can focus on solving problems with the variety of AI tools now at your fingertips. And potentially even more intriguing, each of these flows can be shared and run with any number of organizations and users even if they were not the original creators. Any Veritone user that has the engine shared with their organization can define a custom API endpoint using Veritone’s public APIs and expose that engine to run. This means users can now effectively use Veritone APIs to create their own custom logic powered by Automate Studio and Veritone’s suite of AI cognitive engines and expose that custom logic to the world.

What do you want to build with AI models now that so many of them are available and usable in one place? If you have an idea, consider [signing up for Automate Studio](https://veritone.com/onboarding/#/signUp?type=automate&Lead_Source_Detail=Automate%20Blog3%20%20AI%20API) and see what you can do with 20+ categories of AI cognition.

Feel free to reach out to us with any questions, and we also have bounties out for any of these [unclaimed flow ideas](https://docs.veritone.com/#/automate-studio/flow-bounties/README) that you might be interested in taking on!

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

![face-alerter-flow](/_automateBlog2-img1.png)

As we examine this flow, we can break the flow up into separate sections for ingesting the data, analyzing the data, formatting a text message, using a third party SMS service (Twilio in this case) to send the SMS to the designated recipient and then shutting the flow down. Each of these steps are visually represented and executed as logic that can then be scalably run for both you, and any other users that you want to share your flows with.

What do you want to build with AI models now that so many of them are available and usable in one place? If you have an idea, consider [signing up for Automate Studio](https://veritone.com/onboarding/#/signUp?type=automate&Lead_Source_Detail=Automate%20Blog2%20Face%20Recognition%20Flow) and see what you can do with 20+ categories of AI cognition.

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

This flow is just one example of how Automate Studio pushes humans to become supervisors at the edge of previously manual workflow loops, and if you are reading this and would like to join us in this mission as a partner, [consider signing up for Automate Studio](https://veritone.com/onboarding/#/signUp?type=automate&Lead_Source_Detail=Automate%20Blog1%20Speaker%20Separated%20Transcription) and checking out our Early Adopters Program where we [offer bounties](https://docs.veritone.com/#/automate-studio/flow-bounties/README) for helping create AI/ML powered flows like the one we just discussed.
