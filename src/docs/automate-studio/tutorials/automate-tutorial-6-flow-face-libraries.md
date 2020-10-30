# Use Production Data to Enhance your Face Recognition process

While Machine learning was proclaimed to eliminate the need for human defined rules based systems, there is still a need for the technology after all. The great news for us is that while human defined rulesets are a little longer in tooth, the practice has become elevated and accessible to more people so that more arduous tasks are automatable with AI/ML models and there more manageable. The example of this that we’re examining today is the concept of using a Flow that we developed in Veritone’s Automate Studio to find all of the detected faces that were not recognized and populate those faces as new Unrecognized Persons in our Library that we can then train on.

In this case, our problem we want to solve is how we can collect all of the unrecognized faces output from our Face Recognition process, compile those faces and attempt to dedupe them as best we can, and create a new entity for each unrecognized face in our Libraries application. This enables us to collect the entities we missed for additional processing and refining, limiting the direct involvement of human labor and only applying when absolutely necessary.

## What you’ll need

This tutorial will reference two different aiWARE applications, Automate Studio and Libraries. 

We’ll author our custom flow logic in Automate Studio and use Libraries to store our training dataset (micromodel) that serves as the dataset from which we want to identify similarities with the input media files (images and video) that the Cognitive AI models process at runtime.

## Making it all work together

Let’s first look at our finished flow:

![flow-library-face-builder](/_automateBlog6-facebuilderbot.png)

As we can see in this flow, we are going to take an input from the edge processing framework that kicks off this processing job. Remember, we design these flows to run as engines on aiWARE. These engines are horizontally scaling so we don’t have to think too hard about optimizing a single flow instance and the entire lifecycle of each piece of custom logic (whether created in Automate Studio as a flow or custom code in a docker file) is handled for us.

Let’s also introduce ourselves to the Veritone Libraries app. The Libraries app can easily get lost amongst the various functionality of other Veritone applications including CMS and Discovery.

As its name suggests, Libraries app stores the various Libraries which are collections of micromodels that the relevant AI Cognitive engines are pre-trained on and then reference those micromodels at engine runtime to evaluate against the inputted media file.

Here is an example of a Library named “Home Automation” that contains a single Person entity. The _entity_ contains the _entityIdentifiers_ which are sample pieces of data that the AI model uses when predicting a match against the content it is processing at runtime.

![libraries-example](/_automateBlog6-libraries.png)

Now that we have a better understanding of how the Libraries app and the underlying data model factors in to our end goal of collecting production data to refine our ability to improve the quality of our AI cognitive processes, we can deconstruct what each section of the flow is doing:

1. After accepting our input message from the Edge processing framework we retrieve a few key pieces of information like the job ID
1. Once the original Face Recognition processing job has completed, we then query the _engineResults_ object with the Veritone GraphQL API to retrieve the list of cognitive results, displayed back as a timeseries where a Face was detected, the bounding poly of the faces, and if the face was recognized, the Library entityID that the face from the media file was matched with
1. The flow then loops through all of the _unrecognized_ faces and attempts to group the faces using some custom logic inferring similarity by bounding poly location within a certain time duration
1. Once the flow has finished iterating through the list of unrecognized faces and grouping the faces as best it can, the flow has a list of “grouped faces” that we need it to send back to our Libraries app so we can store this new information
1. With our grouping of unrecognized faces, we create a new _entity_ for each face grouping. The entity name is formatted “Unrecognized Entity {number}”
1. Next, we retrieve the image created from each bounding poly and use the reference to create a new buffer image which we then write as an _entityIdentifier_  associated to the _entity_ record created in the previous step
1. With the creation of the _entityIdentifier_ records, the flow is complete and sends a success message to aiWARE to then end the task process.
