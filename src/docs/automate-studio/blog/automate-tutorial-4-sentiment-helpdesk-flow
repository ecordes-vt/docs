# Analyzing your helpdesk tickets for Customer Sentiment

*Blog Date: 2020-09-24*

*In this tutorial, we’ll learn about how Sentiment analysis processes the support tickets loaded from a sample Helpdesk system (in this case Help Scout) and process the body text with Sentiment analysis and send the results back to the helpdesk system for the Customer Support team to use in their customer service reporting.*

Various studies have found that Customer Success and support teams typically have the least support in the form of sophisticated tools and attempt to overcompensate for these shortcomings by over hiring staff. The result is an inconsistently trained and motivated workforce that in turn leads to wildly disproportionate overhead. However, Customer Success and Support teams can regain both efficiency and effectiveness by adopting a metrics focused approach to triage and understanding each customer cumulatively from all their prior interactions. In this blog, we’ll do a quick dive on how Veritone’s Automate Studio can enable a new kind of data driven approach to enabling your Customer Service teams to more quickly understand and triage your customers they are trying to support. 

In a common Customer Service scenario, the Customer Service teams will all be operating out of a centralized Helpdesk system that collects tickets submitted by customers and leads through various channels including social media, web portals, and email to the support line.

We can assume that all the tickets of interest are already consolidated in a centralized Helpdesk system like Help Scout, and now the Customer Service team needs help understanding the sentiment of each customer inquiry as a way to both prioritize and filter by various needs. Using Automate Studio, we can visualize the flow and with some additional logic, customize both our integration as well as the flow of data and which Cognitive AI engines to use. In this case, our goal is to download all of the active helpdesk tickets and process the body text with sentiment analysis and write the results back to Help Scout as a tag. The flow will look something like this:

![helpdesk-sentiment-flow](/_automateBlog4-img1.png)

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
          # Your intended flow engine
          engineId: "<your flow engine id>"
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
          engineId: "<Your intended flow engine>"
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
