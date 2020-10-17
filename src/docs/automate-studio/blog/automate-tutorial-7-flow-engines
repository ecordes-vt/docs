# How to think about Automate Studio and Flow Engines

Visual workflow tools are not a new concept in the history of computing, and have been around even as computing was transforming from intellectual plaything into itself a transformative element in consumer daily life. With the rocket ship trajectory not just of the internet in the last decade but the adoption of cloud based services accessible exclusively through an internet connection, more and more people discovered they also had ambitions to create their own services and goods through these tools regardless of technical training. With Automate Studio, our mission is to provide the abilities of authoring AI solutions to non-engineers and we have done this in a few key ways: we use the open source Node-RED visual workflow technology as our underlying editor and we have taken the tool and developed it so that it can scale horizontally for high-load workflows as needed. This is why we should take a minute to understand at high level what is going on underneath the Automate Studio hood.

## The Basics

To understand this better, we should understand that “horizontal scaling” refers to a process running multiple times against the same holistic input, where the holistic input is divided up into smaller amounts of work, and that is what each process works on. In Veritone-talk, we call the defined process an “engine” and when the engine is assigned to work on piece of work, that is a _task_. There is a little more to it than that, but you now have a better handle on how the aiWARE platform (on which your flows authored in Automate Studio run on) handles the concept of horizontal scaling.

## How Automate Studio works with this

In our context, Automate Studio is the editor in which you can author your own custom logic, whether that is a simple email alert that is sent to a specific recipient defined in the flow itself, or more complex orchestration of multiple other AI cognitive engines. Automate Studio is the designer canvas and you can run logic within the editor, but this is effectively a way to _debug your engine_ within the editor. Keep in mind that the flow engine in which the logic is defined _must be deployed and run as an engine_ to be available to other users in your organization as well as any users in other organizations the flow engine is intended to be shared with.

The illustration below will give you a good idea about what the lifecycle of authoring all the way to deploying your flow will usually look like:

![automate-studio-lifecycle](/_automateBlog7-lifecycle-img1.png)

## Designing a flow engine

Now that we understand how our work in the Automate Studio editor fits into the broader lifecycle of creating and running flow engines, we can finally dig in to certain key aspects that a flow needs to be designed with to successfully run.

These considerations can be enumerated like this:

- How can the flow engine receive intended data from the aiWARE processing framework?
- How can the flow engine communicate back to the aiWARE processing framework?
- Are there other aiWARE objects that the flow is interacting with?
- If so, how will the flow engine have the right permissions to perform the intended operations defined within the flow at engine runtime?

Luckily, these questions are solved with the custom _aiware_ node palette that comes by default with your instance of Automate Studio.

![automate-studio-lifecycle](/_automateBlog7-lifecycle-img2.png)

We can see these nodes put to use in the flow illustrated above. The _aiware in_ node handles incoming messages sent _into_ the flow when running as an engine on the aiWARE processing framework. The flow then executes, evaluating the data within the message (sent as a JSON) and then branches in two directions: if everything executed successfully and no errors were thrown, then the flow returns an OK message (sent as a 200 REST status code) back to aiWARE, and if an error _was_ detected, then an Internal Error message (sent as a 500 REST status code) is sent instead.

If nothing else, know that the _aiware in_ and _aiware out_ nodes will be essential for getting your flow to successfully run on the aiWARE processing framework.
