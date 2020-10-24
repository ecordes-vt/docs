# How to Build an API Integration with Automate Studio (and more!)

In this tutorial, we're going to illustrate some common "node patterns" (we tend to also call them "recipes") that you can repeatably use to construct your own flows, enabling you to integrate aiWARE's AI congition with your existing proprietary and third party systems.

## Creating API Integrations

We have found that one of the most common reasons across industries is to rapidly develop a solution that can run AI cognitive processing on incoming media and write the results to other third party services that your organization uses in order to make improved decisions.

![flow-recipe-api-request-1](_automateBlog8-sample1)

This recipe is so powerful in part because of its simplicity and also in that it can be applied to integrate with a number of other services with minimal modification to the base recipe.

When we examine the recipe in further detail, we see that it simply consists of two nodes: a `function` node and an `http request` node.

![flow-recipe-api-request-2](_automateBlog8-sample1)

The function node is used to store the definition of specific variables that you can change to suit your needs. We’ve left some pretty thorough comments in the function node itself to explain what each property does, but here’s a high level explanation for each here:

- bearerAuth - this is a “temporary” variable (it is not propagated from the function node to downstream nodes) that is then used in the “Authorization” header in the _msg.headers_ property (see msg.headers section)
- msg.method - The `http request` node has four options in the dropdown but can be overridden with a msg-level property that we can define. This allows us to choose less common options like PATCH or PUT
- msg.url - This is synonymous with the term “endpoint” or “uri” (uniform resource identifier) which is what we’re using to store the url that specifies which API endpoint resource we want to request an action be performed on
- msg.headers - this property stores the Headers that we need to include in our API request to ensure that the API service that we are requesting can successfully authenticate and authorize that we are who we say we are to then perform our requested operation
- msg.payload - This property stores the body of our request. Depending on the API service that you are integrating into, only API requests using POST or PATCH will expect a msg.payload body value because Web APIs usually conform to POST and PATCH implying that you are requesting a change be made to the underlying data

## Polling the Veritone GraphQL API

Even as webhooks have (quite rightly so) become more popular, not all third party API services support the webhook pattern that send data back to you when an asynchronous process has finished, and therefore you will find yourself needing to “poll” an API from time to time. A “poll” is simply making the same API request on a scheduled interval, evaluating the result, and then based on the result retrieved, either continuing to poll the API or moving on to the next action specified in your logic, either as code or as the case here, defined your flow.

![flow-recipe-api-poll](_automateBlog8-sample3)

In this specific example, we poll the Veritone GraphQL, specifically checking on a specific asynchronous engine job process with an `aiware api` node that executes the query on the engine job, using mustache syntax to merge in the _jobId_ variable to retrieve the _status_ of the job. The `switch` node then evaluates the status value and if it is not complete, sends the msg object back to the `api` node first to a `delay` node so we don’t overwhelm the API with excessive requests, and then re-executes the query. This polling continues until the status is either complete or failed, and the msg object is routed accordingly.

## Create a file and send to S3

As Amazon Web Service has proliferated, there is a high probability you will find yourself needing to create and write files _from aiWARE_ to an S3 bucket. The great news for you is that this pattern is so common, we created a generalizable flow recipe for you to easily do just that.

![flow-recipe-s3-writel](_automateBlog8-sample4)

This flow recipe is an example of how to take a merged aiware results and turn the string into a text file that is written to designated S3 bucket.
