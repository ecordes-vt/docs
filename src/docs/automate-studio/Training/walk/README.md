# Automate Studio Training: Working with Flows

![Flow development](flowdev.png)

**APPROXIMATE READING TIME: 18 MINUTES**

Welcome to the second unit of Automate Studio training. In this unit, we'll go into more depth on how to work with nodes; best practices for flow design; and concepts related to aiWARE integration. We'll cover:

* [Flow Creation Strategy](#flow-creation-strategy)
* [Understanding the `msg` object](#understanding-the-aposmsgapos-object)
* [Working with the Change node](#working-with-the-change-node-nbspnbsp-img-srcdocsautomate-studiotrainingwalknode-changepng-styleheight40pxvertical-align-middle)
* [Working with the Function node](#working-with-the-function-node-nbspnbsp-img-srcdocsautomate-studiotrainingwalknode-functionpng-styleheight40pxvertical-align-middle)
* [How to use GraphQL in the API node](#working-with-the-aposapiapos-node-nbspnbsp-img-srcdocsautomate-studiotrainingwalknode-apipng-styleheight40pxvertical-align-middle)
* [Understanding engines, builds, and jobs](#understanding-engines-builds-and-jobs)

While it's not strictly necessary for you to have already worked through the [previous training unit](automate-studio/Training/crawl), we will assume you're familiar with basic terminology around flows, like _nodes_, _wires_, _sidebar_, etc.; and we'll assume you've already created your free Automate Studio account. 

> Sign up [here](https://www.veritone.com/onboarding/#/signUp?type=automate) to create an account and gain immediate access to the Studio designer.

Ready? Let's dive in!

## Flow Creation Strategy

The flows you create in Automate Studio are essentially custom applications that can take data in, modify it in some way, then send the modified data out.

<img src="docs/automate-studio/Training/walk/input-output.png" style="width:75%;"/>

There's certainly more than one way to design a flow, but we've found that &mdash; until you become an advanced user &mdash; it's usually best to think of the development process _tail-end-first_.
In other words:

1\. Start by thinking about the desired _outcome_ of your flow. What will the data look like at the conclusion of the flow? Where will it end up going?

2\. Consider where the input data will come from. What is the data's mimetype? Where does it live? 

3\. What needs to happen to the data in order to produce the desired output? What kind(s) of cognitive processing need to be done? Do you need to normalize the data first, or can it be processed as-is?

These are just some of the considerations you'll want to take into account. You might also want to consider whether the process you have in mind might need to be broken down into _sub-flows_ (which is easy to do wusing the **Create subflow** command in the main Menu). And you'll want to consider whether the flow will run on a scheduled basis, or just on-demand.

But when you're first starting to think about the flow, think about what the data will look like coming _out_ of the flow; compare that to how the data looks at the start of the flow. Then think about all the in-between processing that might need to happen.

### Getting Data into a Flow

While the open-source [Node-RED](https://nodered.org/) app on which Automate Studio is based is capable of consuming data in a variety of ways, Automate Studio is currently designed to support two main scenarios:

1\. If your flow will run on a periodic (or scheduled) basis, you can use an **http-request** node to go out and fetch an HTML page (or potentially other data) via an HTTP request to a web server. This means you can _pull_ data from a server.

2\. If your flow will be invoked as part of an aiWARE [job](quickstart/jobs/?id=working-with-jobs), you can _push_ data to your flow via HTTP POST. (We'll see, in some detail, exactly how to do that in the _next_ training unit.)

?> If your flow falls into the first category, the first node in your flow needs to be an **inject** node. (The Properties tab on that node will allow you to set up the flow's invocation interval, the number of desired invocations, and so on.)
If your flow falls into the second category, the first node in your flow needs to be an **aiware-in** node. (We'll talk about how to use that kind of node in the next unit.)

## Understanding the &apos;msg&apos; Object

Every flow in Automate Studio relies on a `msg` object to pass information from node to node. You do not need to do anything special to make the `msg` object come into existence. It is created automatically by Automate Studio.

The `msg` object is an all-purpose object that you can modify (or not modify) as you see fit. It has global scope and visibility, meaning that it is visible (accessible; usable) to all nodes, and all sub-flows, of a given flow. 

The `msg` object is a JavaScript object (sometimes called a JSON object). It contains a `payload` property (or "field") by default. The _value_ of that field may change as various nodes process your data. You can inspect the `payload` field's value at design time by wiring a Debug node to any node in your flow, and checking the Debug panel after running the flow.

> **Tip:** If you wire separate Debug nodes to some or all of your flow's existing nodes, and set each Debug node to output "complete msg object," then run the flow, you will see messages from all Debug nodes in the debug panel in the sidebar. In this way, you can see how the `msg` object changes from node to node.

You can create new properties of your own on the `msg` object (see the discussion of the Function node, below). For example, if you were to want to keep a running total of some kind during a flow, you could create the `total` field in a Change node, by editing the node's properties so that it Sets the `msg.total` field to some initial value. (This would _create_ the `total` property, and initialize it, all in one go.) You could then update `msg.total` in subsequent Function nodes.

Generally speaking, you will retrieve data, at the end of a flow, from the `msg.payload` field. However, you're not required to do this! If you've created additional custom fields, you can use those, if the occasion warrants. You can create, and use, as many custom fields on the `msg` object as you want.

## Working with the Change node &nbsp;&nbsp; <img src="docs/automate-studio/Training/walk/node-change.png" style="height:40px;vertical-align: middle;"/>

The Change node can be used to create a new property on `msg` and/or to set the _value_ of a property, without having to use a Function node. When all you need to do is adjust a property, the Change node is slightly more convenient than a Function node.

In the Properties dialog for a Change node, you can use a dropdown picklist to select from several available operations:

* **Set** - Sets a property. The value can be a variety of different types, or can be taken from an existing message or context property.
* **Change** - Use this to search and replace parts of a message property.
* **Move** - Move or rename a property.
* **Delete** - Delete a property.

Note that a tiny **+ add** button (in the Properties pane) allows you to chain together as many sequential operations as you wish.

## Working with the Function node &nbsp;&nbsp; <img src="docs/automate-studio/Training/walk/node-function.png" style="height:40px;vertical-align: middle;"/>

The Function node allows you to specify custom logic (in the form of JavaScript) that will execute at runtime. 

Note that the code entered into the Function node represents the body of a function. The most simple function simply returns the message exactly as-is:

`return msg;`

> Be sure to include this line at the end of your code. If your function returns null, then no message is passed on and the flow ends. Likewise, returning a number or string will result in an error.

Bear in mind, your JavaScript code will execute in the context of the Node.js app that runs Automate on the Automate Studio server, _not_ in the context of your web browser. That means your code does _not_ have access to a `window` object, nor to `console.log()`, etc. That limitation aside, you can use all of JavaScript's own native objects (and the standard Node.js packages), to do any type of computation you need to do.

### Multiple Outputs

The function node's edit dialog allows the number of outputs to be changed. If the node is wired  to more than one output, an array of messages can be returned by the function to send to the various connected outputs.

This makes it easy to write a function that sends the message to different outputs depending on some condition. For example, the following function would send anything on topic `translaation` to the second output rather than the first:

```javascript
if (msg.topic === "translation") {
   return [ null, msg ];
} else {
   return [ msg, null ];
}
```

For more information on the Function node, be sure to consult the [Node-RED documentation](https://nodered.org/docs/user-guide/writing-functions).

## Working with the &apos;api&apos; Node &nbsp;&nbsp; <img src="docs/automate-studio/Training/walk/node-api.png" style="height:40px;vertical-align: middle;"/>

Unlike the Change and Function nodes, which are core Node-RED nodes, the **api** node is a custom Automate Studio node. It allows you to provide a GraphQL query or mutation that will be submitted to the aiWARE server at runtime.

An example of the kind of query (or mutation) you can submit is shown below.

```graphql
mutation createTDO {
  createTDO(input: { startDateTime: 1548432520, stopDateTime: 1548436341 }) {
    id
    status
  }
}
```

This mutation asks the server to create an empty [Temporal Data Object (TDO)](apis/jobs-tasks-tdos?id=tdo-temporal-data-object), and return its `id` and `status`.

?> The TDO is aiWARE's general-purpose container object for passing job data around. A TDO contains information about media files, and after a job is run, it will contain one or more entries in an `assets` array. The entries associate job data (by reference, using `signedUri` fields that point to the stored cognition results) with the TDO in question. Read more about TDOs [here](apis/jobs-tasks-tdos?id=tdo-temporal-data-object).

You can use the **aiWARE api** node to execute any of the more than 200 API calls available in aiWARE's GraphQL API. The return value will be a JSON object, which can be accessed as the value of `msg.payload`.

Note that the **aiWARE api** node has one input port and two output ports. The top (or first) output port will contain the `msg` if the query executed without error. If the query was malformed or produced an error, the bottom (or second) output port will contain the error message (again as a JSON object on `msg.payload`).

> We recommend you develop, test, and debug GraphQL queries in the [GraphQL Playground app](https://api.veritone.com/v3/graphql) before copying queries/mutations into **aiWARE api** nodes.

Other custom aiWARE nodes exist for convenience purposes, but the **aiWARE api** node is special: It unlocks the full power of aiWARE by making more than 200 queries and mutations available for you to use any time you want. Anything you can do with aiWARE's APIs can be done from within an **aiWARE api** node!

## Understanding Engines, Builds, and Jobs

In aiWARE, _jobs_ are composed of _tasks_ that call on [_engines_](developer/engines/) to do the actual work (of cognition, say). Engines are pluggable processing modules that conform to certain API contracts. Engines run inside Docker containers and are accessed via HTTP. One of the benefits of containerization is that an engine can be implemented in essentially any programming language. It can even be implemented as a Node-RED instance running a flow.

> When you deploy a flow into the aiWARE platform, you are deploying it as a so-called "chunk engine" (sometimes also called a segment engine). Learn more about chunk engines [here](developer/engines/processing-modes/?id=engine-processing-modes).

When you create a flow in Automate Studio, your edits are silently auto-saved (as you work) into the current _Build_ of your flow. Think of your flow as an application, which you are building a _version_ of. You might work on a particular version of your flow over a period of days, across multiple Automate Studio sessions. It might contain dozens (or even hundreds) of auto-saves, but you are still working on a particular flow version &mdash; a particular Build.

Auto-saves are (of cuorse) automatic, but sometimes you will proactively initiate a Save with the Save button at the top of the canvas UI. Clicking this button tells Automate Studio that you wish to save your work _as a distinct Build_.

Any Build you create can be selected for deployment into aiWARE. You can initiate deployment using the Deploy button at the top of the canvas UI.

Only one Build of a flow (or any other kind of engine) can ever have a status of **Deployed** at a given time. (That's the Build that will _run_ when a job or task calls for your flow to swing into action.) Your non-deployed Builds will continue to exist, of course, but they will have some status other than Deployed.

The possible statuses of an engine (or flow) build are:

```pre
approved
available
deleted
deploying
deployed
deployFailed
disapproved
fetching
invalid
paused
pending
uploaded
```

> You can see the status of your Build(s) in your Flow Details page. Click the **Flow Details** button at the top of the canvas. The three-dots menu on the right of each row will contain context-appropriate commands that let you change a build's status.

## What's Next?

You're probably curious to know how to kick off some kind of cognition inside a flow, and deploy your flow in such a way that you can POST data to it, live. Those are some of the topics we'll be covering in the next installment of this training series.

For extra information on deployment of cognitive flows, be sure to see [Getting Started with Automate Studio](automate-studio/getting-started/README).
