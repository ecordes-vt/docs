# Getting Started

Deploy AI solutions & automation, fast! 
Learn to build your first flow in just a few minutes with this quickstart guide of Automate Studio.

## Step 1: Let's start with the building blocks

There are 3 key concepts we would like you to know:
1. Nodes: these are the shapes in the editor that input data, execute logic, and output that data to the next node until the last node in the flow graph
2. Flow: this is an overall term for the "graph" that you define by dropping and connecting your nodes on the canvas
3. Msg: the `msg` variable is the highest level variable that is sent from one node to another at flow runtime

?> Tip: Hover your cursor over a node in the palette in the left menu to learn what it does.

## Step 2: Run and debug your flow

You've got the lingo, now let's start building! 
In this sample flow below, the flow will display the user information. Connect the wire from the aiWARE api node to the green "debug" node like below and then click the blue Deploy button.
Nice! Now that you have connected your nodes together and deployed your changes, let's review what we have done:
1. We connected our api node to our debug node to display that output
2. We then click the Deploy button to save our latest change. Once we have saved our changes, we can then run the latest version of this flow in the Automate Studio editor runtime
3. Now, click the blue inject node to "inject" a JSON into the flow.

## Step 3: Design your business logic
Design your custom business logic to reach the desired output. For example, you can click and drag a node from the Function menu in the palette into the center of your workspace.

?> Tip: Where is your data? Consider your data sources and how your logic in the flow connects one data silo to another.

## Step 4: Deploy your flow as an aiWARE Engine

You may have noticed that a snackbar notification appears in the bottom left corner of the screen after clicking the "Deploy" button to view your engine in Developer.
Tip: you can read more about flows and aiWARE's engine framework here.
Clicking the Deploy button saves the draft as a new flow engine build that is viewable in your Developer app.

## Step 5: Manage your new Automation Engine

You can manage, and deploy AI engines and applications in the Developer app.
Here in Developer, we are in an engine detail page and observe we have a new build record in this engine that has a Ready status. You can think of "builds" as draft versions of an engine. 
Tip: Flow engines, builds, and how to think about them (link).
Next, click on the “Submit” button next to the build, and then the “Deploy” button, to promote this version to the one actually that processes data.

## Step 6: Run and view your engine results

You can run your new Engine and view the results in 2 easy steps:
First, run this mutation in the [Veritone GraphiQL tool](https://api.veritone.com/v3/graphiql)
```
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
    tasks {
      records {
        id
      }
    }
  }
}
```

Secondly, navigate to the CMS app using the app switcher (top right), and select the file as seen in the GIF below. When the engine completes, you can view a new output of that engine as well as a notification sent to the email of your Veritone account!

**Congrats!** You’ve built and run your first flow engine. 
Now, take for a spin the existing pre-built flows in your organization, or create your own flow engines.

?> Need help or have a question? Contact us in our Slack Community.
