# Getting Started

Deploy AI solutions & automation, fast!
Learn to build your first flow in just a few minutes with this quickstart guide of Automate Studio.

## Step 1: Let's start with the building blocks

There are 3 key concepts we would like you to know:

1. Nodes: these are the shapes in the editor that input data, execute logic, and output that data to the next node until the last node in the flow graph.
2. Flow: this is an overall term for the "graph" that you define by dropping and connecting your nodes on the canvas.
3. Msg: the `msg` variable is the highest level variable that is sent from one node to another at flow runtime.

?> Tip: Hover your cursor over a node in the palette in the left menu to learn what it does.

![node-hover](automate-0-studioNodeHover.png)

## Step 2: Run and debug your flow

You've got the lingo, now let's start building!
In this sample flow below, the flow will display the user information. Connect the wire from the aiWARE api node to the green "debug" node like below and then click the blue Deploy button.
Nice! Now that you have connected your nodes together and deployed your changes, let's review what we have done:

1. We connected our api node to our debug node to display that output.
2. We then click the Deploy button to save our latest change. Once we have saved our changes, we can then run the latest version of this flow in the Automate Studio editor runtime.
3. Now, click the blue inject node to "inject" a `msg` JSON object into the flow.

![node-hover](automate-1-deployandsaveflow.gif)

## Step 3: Design your business logic

Design your custom business logic to reach the desired output. For example, you can click and drag a node from the Function menu in the palette into the center of your workspace.

?> Tip: Where is your data? Consider your data sources and how your logic in the flow connects one data silo to another.

## Step 4: Deploy your flow as an aiWARE Engine

You may have noticed that a snackbar notification appears in the bottom left corner of the screen after clicking the "Deploy" button to view your engine in Developer.
Tip: you can read more about flows and aiWARE's engine framework here.
Clicking the Deploy button saves the draft as a new flow engine build that is viewable in your Developer app.

![into-developer](automate-2-deploy-intoDeveloper.gif | width=1400px)

## Step 5: Manage your new Automation Engine

You can manage, and deploy AI engines and applications in the Developer app.
Here in Developer, we are in an engine detail page and observe we have a new build record in this engine that has a Ready status. You can think of "builds" as draft versions of an engine.

Next, click on the “Submit” button next to the build, and then when the status changes, click the newly available “Deploy” button, to promote this version to the one actually that processes data.

![developer-builds](automate-3-developerbuilds.gif)

Right now, the Developer app UI does not support the creation of new Automate Engines (we are working on it!). The easiest way to create a new Automation Engine is via the GraphQL API in api.veritone.com/v3/graphiql.

?> If you are using the “My Little Hello World” flow engine in your org, you can skip this step for now.

```javascript
mutation createFlowEng{
  createEngine(input:{
    name:"Andy's Dev Flow Engine - Batch"
    description:"Test flow engine for determining if batch right off the bat works"
    categoryId:"c5458876-43d2-41e8-a340-f734702df04a"
    deploymentModel:NonNetworkIsolated
    edgeVersion:3
    libraryRequired:false
    useCases:["batch testing","flow testing"]
    industries:["Media and entertainment","Other"]
    testingDetails:{
      email:"andrew+devtest2020029@veritone.com"
      mediaFileUri:""
    }
    isPublic:false
    manifest:{
      engineId:"12db1483-70d6-4b5a-8a65-fe310017f8f9"
      runtime:"nodeRed"
      engineMode:"batch"
      supportedInputTypes: ["application/json"]
    }
  }){
    id
    name
  }
}
```

## Step 6: Run and view your engine results

You can run your new Engine and view the results in 2 easy steps:
First, run this mutation in the [Veritone GraphiQL tool](https://api.veritone.com/v3/graphiql)

```javascript
mutation runYourFlow {
  createJob(input: {
    clusterId:"rt-1cdc1d6d-a500-467a-bc46-d3c5bf3d6901"
    #V3 Prod cluster
    targetId:"952071774"
    #this is the Media File ID
    tasks:[
      {
        engineId:"365c246c-6409-456a-826d-92ca72539a0a"
        # Your Little Hello World Flow
      }
    ]
  }) {
    id
    #Make sure you save this ID when you run the createJob mutation!!
    tasks {
      records {
        id
      }
    }
  }
}
```

You can monitor and the progress of your Flow engine task using either the CMS application, or by running this query:

```javascript
query flowJob{
  job(id:"<job id>"){
  # Get the job id after running the createJob mutation above and use it here
    id
    status
    tasks{
      records{
        id
        taskOutput
        status
        engine{
          name
        }
      }
    }
  }
}
```

Secondly, navigate to the CMS app using the app switcher (top right), and select the file as seen in the GIF below. When the engine completes, you can view a new output of that engine as well as a notification sent to the email of your Veritone account!

![node-hover](automate-4-cms-runflow.gif)

**Congrats!** You’ve built and run your first flow engine.
Now, take for a spin the existing pre-built flows in your organization, or create your own flow engines.

?> Need help or have a question? Contact us in our [Slack Community.](http://veritonedev.slack.com/)
