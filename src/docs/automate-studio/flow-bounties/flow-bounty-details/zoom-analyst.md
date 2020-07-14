<!--TODO: Replace all references to "VDA", "Developer Application", and "Developer App" with "Veritone Developer"-->

# Zoom Analyst
[cognitivecategory/NaturalLanguageProcessing/lightgrey]
[status/Development/Undeveloped/red]


## Overview {docsify-ignore}
Analyze a live zoom call: live transcript with speaker separation. Text analytics. Fast search, playback and clipping of snippets of a call for sharing.

## Details {docsify-ignore}
User Flow:
<br>
User can connect the app to as many Google calendars as they want
Log of all analyzed calls, including the status to show live calls.
Real-time call analysis should have sub 5 second lag (2 would be preferable).
<br>
<br>
Actions:
<br>
User can click on a call to bring up the analysis dashboard (~ Illuminate)
<br>
User can direct click the link in the calendar: www.ZOOMAnalysis.com?callguid={CALL_GUID}
<br>
Hooks into Redact, Library, Collections, Share, etc..
<br>
<br>
Automate Flows under the covers:
 1. When a user connects a calendar - Call Job #1
 2. When a user disconnects a calendar - Flow Not Shown
<hr>