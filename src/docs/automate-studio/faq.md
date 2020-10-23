# FAQ: Veritone Automate Studio

## What can I do with Veritone Automate Studio?

We recommend starting with this question: _What kind of process do you or your customers still have to manually address with humans actively in the process loop?_ You can use Veritone Automate Studio to address those pain points and rapidly develop new solutions that automate those processes, thus moving your end-users to the edge of the loop.

## How technical do I need to be to use Automate Studio?

Veritone Automate Studio is a visual workflow tool that uses [Node-RED](https://nodered.org/)'s underlying technology, so basic familiarity with coding principles would be helpful, though not a hard requirement. The Flow Designer is visually driven, so coding is not required.

If you are interested in going deeper, we recommend Codecademy's [free course](https://www.codecademy.com/learn/introduction-to-javascript) on JavaScript or equivalent instruction to really drill into some of the Flow Designer's deeper features.

## How much familiarity do I need with Veritone's data model?

At a minimum, basic familiarity with our [GraphQL schema](https://api.veritone.com/v3/graphqldocs/) is necessary. We have introduced a number of aiWARE nodes specifically for abstracting away some knowledge of GraphQL to make it easier for users to jump straight into incorporating AI into their workflows.

## Can I expect to run my Flow directly in Automate Studio for a long period of time?

Yes. There are two runtimes that your flows can run on: 

- The first is the Automate Studio runtime, which is powered by Node-RED. The Automate Studio editor session will shut down after a period of inactivity is detected.
- The second is the Veritone engine framework on which all of Veritone's engines run. Keep in mind that Automate Studio's runtime is not directly connected to Veritone's engine runtime, which is why we have included special nodes to simulate the Veritone engine runtime framework _within_ Automate Studio.

## What is an "Automation Engine?"

This phrase serves as a description of a Flow once it has been deployed "as an Engine" to run on Veritone's engine framework.

## Can I use Automate Studio to create new Cognitive Engines?

Yes! We have adapted Automate Studio's underlying Node-RED open source technology to run as a new kind of Engine build runtime on Veritone's realtime framework. This means that cognitive engines can also be created in Automate Studio without having to configure Docker files and write the same level of code.

## What does "Beta" mean for Automate Studio?

At Veritone, we have been using Automate Studio internally to experiment with new cognition classes and engines, rapidly develop new features, and build new AI solutions that we have then taken to market. Sharing this product in Beta with our customers gives us the chance to hear your feedback directly, and release new enhancements faster, while giving you a powerful new tool to customize Veritone's cognitive capabilities even more for your organization.

## I have an idea or feedback for Automate

We always love hearing suggestions from our developer community and end customers! You can share your thoughts by sending your feedback to support@aiware.com!

You can also build your own nodes, submit to the Node-RED repo and flag Veritone to review them and incorporate into the official aiWARE palette.
