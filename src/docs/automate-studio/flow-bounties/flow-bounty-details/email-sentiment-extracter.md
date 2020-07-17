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
# Email Sentiment Extracter
[status/Development/Undeveloped/red]


## Overview {docsify-ignore}
A flow engine that accepts csv & text files webhooked to an HTTP Adapter endpoint sent from an email provider of your choice (eg Mandrill, Sendgrid) and processes them with a sentiment analysis engine then: 
1. writes the results to a TDO
2. writes the results back to a callbackUrl field if provided by the sender.
</br>
</br>
<a target="_blank" href="https://forms.gle/tkVjfrtyBDrXyoji7" id="claim-this-flow-btn">CLAIM THIS FLOW!</a>
<hr>