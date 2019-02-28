# General Object Detection Engine Output Example

## Engine Output

General detected objects can be reported in engine output by specifying an `object` of `type: object`.
An object definition can exist in either the object array (for non-time-based detections)
or in an `object` key in the `series` array (for time-based detections).

Here is an example of proper engine output for objects detected within a time series:

[](vtn-standard-series.example.json ':include :type=code json')

TODO: Add an example for objects outside a time series

The official engine output json-schema is available
[here](/schemas/vtn-standard/object.json ':ignore').