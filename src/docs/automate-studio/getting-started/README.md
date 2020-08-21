# Getting Started with Automate Studio

Learn to build your first flow in just a few minutes with this quickstart guide of Automate Studio.

## Step 0: Learn about the Building Blocks

Before we create a flow, let's quickly look at the main concepts you need to know about.

<div class="collapse-accordion"><ul><li>
                <input type="checkbox" id="list-item-1">
                <label for="list-item-1"><span class="expandText">Click here to learn about the main concepts</span><span class="collpaseText">Click here to close this section.</span></label>
                <ul>
                    <li>

The 4 main concepts you need to know about are:

1. **Nodes:** These are the shapes in the editor that represent discrete steps in your flow.
2. **Wires:** These are the lines that connect the nodes together.
3. **Flow:** This is an overall term for the "graph" (or node-and-wire model) that you define by dropping and connecting your nodes on the canvas.
4. **Message:** The `msg` variable is the highest level variable that is sent from one node to another at flow runtime.

?> Tip: Hover your cursor over a node in the palette in the left menu to learn what a given type of node does.

![node-hover](automate-0-studioNodeHover.png)

### Nodes Are Easy to Work With

&#9642; To put a node in your graph, just drag any node from the node palette to the canvas, and let go of the mouse.

&#9642; Single-click a node on the canvas to select it. When it is selected, hit the Delete or Backspace key on your keyboard to delete it. 

&#9642; Click and drag from the _output_ endpoint on the right side of a node, to the _input_ endpoint on the left side of a second node, to connect two nodes with a wire.

&#9642; Use Ctrl-Z to Undo any action.

</li>                  
</ul>
</li>          
</ul>
</div>

## Step 1: Create a Flow

<div class="collapse-accordion"><ul><li>
                <input type="checkbox" id="list-item-2">
                <label for="list-item-2"><span class="expandText">Click here to learn how to create a flow</span><span class="collpaseText">Click here to close this section.</span></label>
                <ul>
                    <li>
                    
If you haven't already done so, create your free account at [https://developer.veritone.com/automate-studio/overview](https://developer.veritone.com).

1\. In the upper right corner of that page, click the CREATE NEW button. The **Create New Flow Engine** page will open.

![Create New Flow page](Automate-1.png)

2\. You can click the SELECT A TEMPLATE button in the upper right, if you want to select a prebuilt, templated flow to edit.
Otherwise, enter a **Name** and an optional **Description** for your flow, then accept the other defaults and click the CREATE button at the bottom of the page.
After a few seconds, the Automate Studio design-time environment will open.

</li>                  
</ul>
</li>          
</ul>
</div>

## Step 2: Build and Test Your Flow

You've got the lingo, now let's start building!

<div class="collapse-accordion"><ul><li>
                <input type="checkbox" id="list-item-3">
                <label for="list-item-3"><span class="expandText">Click here to learn how to build and test a flow</span><span class="collpaseText">Click here to close this section.</span></label>
                <ul>
                    <li>
                    
In this super-simple example, we'll create a 3-node flow that displays your user information. 

1\. From the node palette on the left, drag an **inject** node (visible under Common) onto the canvas.

2\. Also drag an **api** node (visible under aiWARE), and a **debug** node (from Common) onto the canvas. And click the _bug_ icon in the information pane, on the right, to enable the display of debug messages. Your canvas should look liker this:

![3 nodes](NodeDrop2.gif)

3\. Click and drag from the output of the first node to the input of the second node. When you let go of the mouse button, a wire will appear.

4\. Create a wire from the middle node to the **debug** node.

5\. Double-click on the middle node (the **aiWARE api** node). Notice that a detail pane opens, allowing you to edit the **api** node's contents.

6\. Delete the existing contents and Paste the following:

```graphql
query {
  me {
    name
    id
  }
}
```

> When your flow executes, this simple GraphQL query will retrieve your user info.

7\. Click the blue **DONE** button in the upper right part of the edit pane. The pane goes away.

Nice! Now your flow is ready to run.

### Test the Flow

Click once on the ballot-box square at the left edge of the first node (the node labelled "timestamp"). This runs the flow, from start to finish.

Look to see that your Debug pane (on the right) is showing details from the query. You should see something like this:

![debug message pane](Automate-debug.png)

#### What Just Happened

Automate Studio ran your flow and executed the `me` GraphQL query by submitting it to Veritone's GraphQL server.
The JSON results returned by the server got appended to your flow's `msg.payload` variable.
(Every flow has a global `msg` object that gets passed from node to node.)

</li>                  
</ul>
</li>          
</ul>
</div>

## Step 3: Design your Business Logic

Design your custom business logic to achieve the desired output. Drag and drop various node types as appropriate. For example, you can click and drag a **function** node from the Function menu in the palette into the center of your workspace, edit its settings, and connect it to other nodes. (Double-click any node, at any time, to explore and/or edit its settings.)

?> **Tip:** Where is your data? Consider your data sources and how your logic in the flow connects one data silo to another.

> **Note:** If you change a node's settings, be sure to click the **Done** button in the Edit pane to save your edits.

## Step 4: Save and Deploy Your Flow

Your flow will be auto-saved every few seconds. You don't have to do anything to save your work. (If a particular node in your flow diagram contains unsaved changes, it will appear with a small blue-filled circle above it. The circle disappears after an auto-save.)

> **Tip:** If you ever need to re-open your flow in the canvas, find it in the [Engines Overview page](https://developer.veritone.com/engines/overview), and single-click it to open that flow's Builds page. From the Builds page, you can open any build (any prior "save" of your flow) in Automate.

Clicking the **Deploy** button brings up a dialog that lets you specify whether to run the flow immediately, or Deploy only.
When you deploy a flow, you are making that particular build available as an active (visible and invokable) _engine_ in aiWARE. It can be specified by ID in GraphQL mutations, used in Tasks, and so on, within your Organization.

## Step 5: Manage your new Automation Engine

You can manage AI engines, flows, and applications in the Veritone Developer app. Flows are listed in the [Engines Overview page](https://developer.veritone.com/engines/overview). You can click into any listed flow to see its Builds page. On the Builds page, you can see and manage every build's status.
Below, you can see we're in an engine detail page, and you can see we have a new build record for this engine that has a Ready status. (Think of "builds" as draft versions of an engine.) 

> **Tip:** If you ever want to delete a build, first be sure to Pause it (if it's Deployed and active) first. Then user the Delete command in the kebob menu on the right edge of the build's row.

![developer-builds](automate-3-developerbuilds.gif)

## Step 6: Run Your Flow in a Job

In this section, we are going to create a Job in aiWARE that uses our automation engine (i.e., our flow). 
Once we have created this job, we can send custom payloads to our engine's endpoint. Let's do it!

<div class="collapse-accordion"><ul><li>
                <input type="checkbox" id="list-item-6">
                <label for="list-item-6"><span class="expandText">Click here to learn how to run your flow in aiWARE</span><span class="collpaseText">Click here to close this section.</span></label>
                <ul>
                    <li>
                    
First, run this mutation in the [Sandbox](https://api.veritone.com/v3/graphiql)

```graphql
mutation createYourFlowEngineJob {
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
          # "correlationTaskId": "PA_TASK_ID",
          # "dueDateTime": "0001-01-01T00:00:00Z",
          engineId: "bb544ade-461c-11ea-8604-a3b3a83f5182"
          ioFolders: [
            {
              referenceId: "PA_OUTPUT"
              mode: chunk
              type: output
            }
          ]
        }
        {
          # This is the task that is an instance of the flow engine you created in Automate Studio!
          engineId: "<your flow engine id!>"
          ioFolders: [
            {
              referenceId: "MY_INPUT"
              mode: chunk
              type: input
            }
          ]
        }
      ]
    ##Routes : A route connect a parent output folder to a child input folder
    routes: [
        {
          ## HTTP Push Adapter route
          # The endpoint MUST be a UUID, you can generate one from a website
          endpoint: "< YOUR ENDPOINT GUID >"
          parentIoFolderReferenceId: "PA_OUTPUT"
          childIoFolderReferenceId: "MY_INPUT"
          options: {}
        }
      ]
  }) {
    targetId
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

Secondly, we can now send our own payloads to this REST endpoint:

?> You can make REST requests with the cURL program in your computer's Terminal, or you can use a GUI app like Postman or Insomnia

```cURL
Method: POST
Url: https://controller-v3f.aws-prod-rt.veritone.com/edge/v1/proc/endpoint/{Your Endpoint GUID here!}

Body:
{ "edgePayload":
  {
  "tdoId":"<File ID from your org>",
  "sendTo":"<your email>",
  "firstName":"<your firstname>"
  }
}
```

It is only necessary to make POST request to your custom endpoint with this sample payload. The logic we constructed in the flow earlier was created to handle this payload and serve as an example of all the cool things we can build orchestrating our own cognition in the flow engine!

Once a payload body was submitted to the REST endpoint, navigate to CMS app using the app switcher (top right), and select the file as seen in the GIF below. When the engine completes, you can view a new output of that engine as well as a notification sent to the email of your Veritone account!

![node-hover](automate-4-cms-runflow.gif)

</li>                  
</ul>
</li>          
</ul>
</div>

**Congrats!** You’ve built and run your first flow engine.
Now, take for a spin the existing pre-built flows in your organization, or create your own flow engines.

?> Need help or have a question? Contact us in our [Slack Community.](http://veritonedev.slack.com/)

<style>
label {
        color: #fff;
    }
    
    .markdown-section code {
        border-radius: 2px;
        color: #322;
        font-size: .8rem;
        margin: 0 2px;
        padding: 3px 5px;
        white-space: pre-wrap;
    }

    .collapse-accordion ul {
        list-style: none;
        margin: 0;
        padding: 0;
    }

    .collapse-accordion label {
        display: block;
        cursor: pointer;
        padding: 9px 30px;
        border: 1px solid #fff;
        border-radius: 7px;
        border-bottom: none;
        background-color: #766;
        position: relative;
    }

    .collapse-accordion label:hover {
        background: #999;
    }

    .collapse-accordion label:after {
        content: "";
        position: absolute;
        width: 8px;
        height: 8px;
        text-indent: -9999px;
        border-top: 1px solid #f2f2f2;
        border-left: 1px solid #f2f2f2;
        -webkit-transition: all .3s ease-in-out;
        transition: all .3s ease-in-out;
        text-decoration: none;
        color: transparent;
        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
        transform: rotate(135deg);
        left: 10px;
        top: 50%;
        margin-top: -5px;
    }

    .collapse-accordion input[type="checkbox"]:checked+label:after {
        transform: rotate(-135deg);
        top: 20px;
    }

.collapse-accordion input[type="radio"]:checked+label:after {
        transform: rotate(-135deg);
        top: 20px;
    }

    .collapse-accordion label.last {
        border-bottom: 1px solid #fff;
    }

    .collapse-accordion ul ul li {
        padding: 10px;
        
    }


    .collapse-accordion input[type="checkBox"] {
        position: absolute;
        left: -9999px;
    }
.collapse-accordion input[type="radio"] {
        position: absolute;
        left: -9999px;
    }

    .collapse-accordion input[type="checkBox"]~ul {
        height: 0;
        transform: scaleY(0);
      transition: transform .2s ease-out;
    }
.collapse-accordion input[type="radio"]~ul {
        height: 0;
        transform: scaleY(0);
  transition: transform .5s ease-out;
    }

    .collapse-accordion input[type="checkBox"]:checked~ul {
        height: 100%;
        transform-origin: top;
        transition: transform .5s ease-out;
        transform: scaleY(1);
    }

.collapse-accordion input[type="radio"]:checked~ul {
        height: 100%;
        transform-origin: top;
        transition: transform .2s ease-out;
        transform: scaleY(1);
    }

    .collapse-accordion input[type="checkBox"]:checked+label {
        background:#966;
        border-bottom: 1px solid #fff;
    }
.collapse-accordion input[type="radio"]:checked+label {
        background: red;
        border-bottom: 1px solid #fff;
    }

    .collapse-accordion input[type="checkbox"]:checked+label .collpaseText {
        display: block;
    }

.collapse-accordion input[type="radio"]:checked+label .collpaseText {
        display: block;
    }

    .collapse-accordion input[type="checkbox"]:checked+label .expandText {
        display: none;
    }

.collapse-accordion input[type="radio"]:checked+label .expandText {
        display: none;
    }

    .collpaseText {
        display: none;
    }

.info {
  margin-top: 50px;
color: #000;
  font-size: 24px;
}
.info span {
  color: red;
}
</style>