<!--TODO: Replace all references to "VDA", "Developer Application", and "Developer App" with "Veritone Developer"-->
<style>
    #claim-this-flow-btn {
        display: block;
        color: #2F80ED;
        border: 1px solid #2F80ED;
        width: 170px;
        height: 30px;
        text-align: center;
        padding: 3px;
        position: relative;
        text-decoration: none;
        left: 40%;
    }
</style>
# Twitter Classification
[cognitivecategory/ContentClassification/lightgrey]
[status/Development/Undeveloped/red]


## Overview {docsify-ignore}
This flow engine scrapes the tweets of a provided Twitter user and processes each tweet to create topics associated with each tweet.

## Details {docsify-ignore}
1. An empty TemporalDataObject (TDO) is created for each run of the Flow engine
2. Each tweet is written to a Structured Data Object (SDO) in aiWARE
3. At the same time, each tweet's content is processed by a topic extraction engine (eg, ZettaCloud)
4. Each result is written back to the SDO, and the SDOs are correlated to the TDO created at start time

<a href="https://forms.gle/tkVjfrtyBDrXyoji7" id="claim-this-flow-btn">CLAIM THIS BOUNTY!</a>
<hr>