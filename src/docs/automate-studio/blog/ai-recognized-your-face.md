# AI recognized your face. Now what?

*Blog date: 2020-09-09*

Conversations about Face Recognition and its various risks are as popular topics for discussion as the various use-cases around Face Recognition. But how can we make this topic not only more approachable but also more useful for people who are not engineers and Data Scientists?

The way everyone usually starts out is by talking about a use-case that frames both the problem and how the technology in question can be used to solve it in a new and more efficient way.

In this case, Face Recognition refers to a category of AI cognition that performs a two-step operation:

1\. Processing an image of a video (which is a series of images) and detecting faces
2\. Then looping through the list of detected faces and attempting to “recognize” faces by comparing certain signatures against a pre-loaded library of faces determined by the user who kicked off the original operation.

With that definition in mind, what use-case could this technology solve? Well, an increasingly common use-case is using Face Recognition as part of a Biometric identity layer where the user’s face is included as part of a process to verify identity and unlock either the device or perform some follow up action like alerting a predefined recipient with an email or text message.

There’s certainly an argument that this use-case could be solved with “a few lines of code” (how often have we heard that!), but what if we are not software engineers ourselves? And all the software engineers are busy? And even if we were engineers, are we going to build the scaffolding, monitoring, and framework to safely and repeatedly run the AI models on demand from any number of customers?

A quick scan of the screenshot below shows that Automate Studio addresses these questions with its drag and drop interface, with each of those “nodes” executing logic defined by the user designing the flow in Automate Studio’s editor.

![face-alerter-flow](/_automateBlog2-img1.png)

As we examine this flow, we can break the flow up into separate sections for ingesting the data, analyzing the data, formatting a text message, using a third party SMS service (Twilio in this case) to send the SMS to the designated recipient and then shutting the flow down. Each of these steps are visually represented and executed as logic that can then be scalably run for both you, and any other users that you want to share your flows with.

What do you want to build with AI models now that so many of them are available and usable in one place? If you have an idea, consider [signing up for Automate Studio](https://veritone.com/onboarding/#/signUp?type=automate&Lead_Source_Detail=Automate%20Blog2%20Face%20Recognition%20Flow) and see what you can do with 20+ categories of AI cognition.

Feel free to reach out to us with any questions, and we also have bounties out for any of these [unclaimed flow ideas](https://docs.veritone.com/#/automate-studio/flow-bounties/README) that you might be interested in taking on!
