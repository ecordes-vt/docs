# Getting Started

## Designing your flows

For your flow to successfully run as an engine on the aiWARE engine processing framework, each flow needs to be designed so that it can accept incoming webhooks from the engine framework and communicate back.

This design is reflected by the “Readyz” and “Process” http in and http response nodes.

While these nodes might not look obviously necessary for the logic to run in Automate Studio, this is how the flow receives messages from aiWARE and is orchestrated at large.

For more information on engine creation generally and a deeper dive into how engine toolkit would be implemented through code, check out the Engine Toolkit section [here](developer/engines/toolkit)

## Debugging your flows

Your debugging experience in Automate Studio can be thought of as two steps:

1. running the flow in the Automate Studio runtime
2. debugging the output of the logic you configured in previous nodes

You can use several types of input nodes to run your node, and keep in mind that this run is intended to simulate how the flow will behave running as a flow engine on aiWARE’s processing framework. Drag an inject node onto the canvas, wire it to the node containing your logic that you wish to process next, click deploy to save your changes and operationalize the flow in Automate Studio, and then click the “inject button” on the left side of the node.

To view your logic outputs, drag the debug node from the palette menu on the left and connect an output wire from one or more nodes that you wish to evaluate. The outputs sent to the debug node are then logged on the right hand menu in the “debug” tab with the “bug” icon.
