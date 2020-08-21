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
# Call Center Automated Responses for Key Conversation Topics
[status/Development/Undeveloped/red]


## Overview <!-- <!-- {docsify-ignore} --> -->
Provide call center operators responses to questions asked by the customer in real-time, without the operator having to search themselves.

## Details <!-- {docsify-ignore} -->
The proposed flow takes an audio file as input, converts its speech to text, and detects questions. This is extremely useful for a text analyzer to determine if a given sentence generated from an audio file is a question or not. The question will be passed to Google search API and get the top 5 results for the topic.
</br>
Output: The questions detected and top 5 Google Search results for each.
</br>
</br>
<a target="_blank" href="#" id="claim-this-flow-btn">CLAIMED</a>
<hr>