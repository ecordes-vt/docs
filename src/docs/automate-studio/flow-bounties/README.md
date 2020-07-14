<!--TODO: Replace all references to "VDA", "Developer Application", and "Developer App" with "Veritone Developer"-->

# Automate Studio Flow Bounties

<style>
    div.featureBox {
        -webkit-box-shadow: -2px 2px 6px 3px rgba(207,208,209,1);
        -moz-box-shadow: -2px 2px 6px 3px rgba(207,208,209,1);
        box-shadow: -2px 2px 6px 3px rgba(207,208,209,1);
        width: 425px;
        height: 150px;
        padding: 7px;
        font-size: 80%;
        display: flex;
        background: #FAFAFA;
        position: relative;
    }

    div.featureColumn {
        position:relative;
        left:25px;
        width: 500px;
    }
    
    div.featureText {
        position: relative; 
        top: -40px;
    }

    div.featureImage {
        width: 50px;
        height: 50px;
    }

    div.do-more-aiware-featureColumn {
        position:relative;
        left:25px;
        width: 400px;
    }
    
    div.do-more-aiwareFeatureText {
        width: 75%;
        position: relative; 
        top: -40px;
    }

    div.newsSectionColumn{
        width: 975px;
        position:relative;
        left:10px;
        display: flex
    }
    
    div.newsDateColumn {
        width: 175px
    }

    div.newsColumn {
        width: 800px
    }

    div.buttonColumn {
        width: 760px;
        display: flex;
        margin: 0;
        position: absolute;
        left: 365px;
    }

    #view-more-templates-btn {
        display: block;
        color: #2F80ED;
        border: 1px solid #2F80ED;
        width: 250px;
        height: 30px;
        position: relative;
        left: 15px;
        text-align: center;
        padding: 5px;
        position: relative;
        text-decoration: none;
    }

    #learn-automate-studio-btn {
        display: block;
        background-color: #2F80ED;
        color: #FFF;
        width: 300px;
        height: 30px;
        text-decoration: none;
        text-align: center;
        padding: 5px;
        position: relative;
    }

    .date-text {
        background-color: #d9d9d7;
        width: 110px;
        border-radius: 10px;
        font-size: 95%;
        padding: 4px 6px;  
        text-align: center
    }

    a.link {
        position: relative;
        bottom: -120px;
        left: -367px;
    }

    #propose-flow-bounty-btn {
        display: block;
        color: #2F80ED;
        border: 1px solid #2F80ED;
        width: 210px;
        height: 30px;
        text-align: center;
        padding: 3px;
        position: relative;
        text-decoration: none;
        left: 385px;
    }

    .description-text {
        font-size: 110%
    }

</style>

## What are Automate Flow Bounties? {docsify-ignore}
Below you will find a wishlist of Automate flows that we, at Veritone, hope to have 3rd party developers help us build. In order to incentivize building these flows, we have placed bounties on them. For each flow a developer creates, the specified bounty will be paid out. 

## How do I Claim a Bounty? {docsify-ignore}
Claiming a bounty is quite simple!
1. View the details for the flow you are interested in building.
2. Fill out the [form](https://forms.gle/tkVjfrtyBDrXyoji7) to claim the flow.
3. Build the flow according to the specifications
4. When complete, submit this form to get the flow approved.
5. Get Paid!

## How do I Propose a Wishlist Flow? {docsify-ignore}
If you want to propose a new flow that is neither in our library or wish list, fill out this [form](https://forms.gle/C6G5oQJiDaqdyWGR7). A Veritone team member will review it and either approve it or get back to you with feedback on your proposal. Once it is approved, you will see it added to the wishlist below!



<hr>

## Automate Flow Wishlist {docsify-ignore}
<br>
<div style="display: flex">
    <div class="featureColumn">
        <div class="featureBox"> 
            <div class="featureText">
                <h3>Compliance Remixer</h3>
                <div class="description-text">As a user in the Compliance & Legal team at a Media & Entertainment company, I need to be able to quickly scan each clip within a larger production video to quickly contextualize where the ad appears in the video.</div>
            </div>
            <a class="link" href="/#/automate-studio/flow-bounties/flow-bounty-details/compliance-remixer"> DETAILS</a>
        </div>
        </br>
        </br>
        <div class="featureBox"> 
            <div class="featureText">
                <h3>Scrape Classification</h3>
                <div class="description-text">As a CMS/GraphQL user, I can create a job that invokes an Automation engine to scrape a website and process the content for either topic extraction or content classification (or both!)</div>
            </div>
            <a class="link" href="/#/automate-studio/flow-bounties/flow-bounty-details/scrape-classification"> DETAILS</a>
        </div>
        </br>
        </br>
        <div class="featureBox"> 
            <div class="featureText">
                <h3>Twitter Classification</h3>
                <div class="description-text">This flow engine scrapes the tweets of a provided Twitter user and processes each tweet to create topics associated with each tweet.</div>
            </div>
            <a class="link" href="/#/automate-studio/flow-bounties/flow-bounty-details/twitter-classification"> DETAILS</a>
        </div>
        </br>
        </br>
        <div class="featureBox"> 
            <div class="featureText">
                <h3>Face Detector and Redactor</h3>
                <div class="description-text">This flow engine process Face Recognition against a specified library and then runs a redaction process against any entities detected that were provided in the engine's custom fields.</div>
            </div>
            <a class="link" href="/#/automate-studio/flow-bounties/flow-bounty-details/face-detector-redactor"> DETAILS</a>
        </div>
        </br>
        </br>
        <div class="featureBox"> 
            <div class="featureText">
                <h3>YouTube Scraper</h3>
                <div class="description-text">This flow accepts a payload including a YouTubeVideoId value that it then uses to ingest the video, transcribes it, and then runs topic extraction on that transcript. The topic transcription results are written to an SDO which is then correlated to that TDO that was created.</div>
            </div>
            <a class="link" href="/#/automate-studio/flow-bounties/flow-bounty-details/youtube-scraper"> DETAILS</a>
        </div>
        </br>
        </br>
        <div class="featureBox"> 
            <div class="featureText">
                <h3>Trigger & Scrape</h3>
                <div class="description-text">When a new mention is created, an event subscription triggers this specific flow engine to run. The Flow engine evaluates the event payload determining if the mention was created on a "Cognitive Search profile evaluating for a string value" and then sends an alert to a designated input.</div>
            </div>
            <a class="link" href="/#/automate-studio/flow-bounties/flow-bounty-details/trigger-and-scrape"> DETAILS</a>
        </div>
    </div>
    <div class="featureColumn">
        <div class="featureBox"> 
            <div class= "featureText">
                <h3>Zoom Analyst</h3>
                <div class="description-text">Analyze a live zoom call : live transcript with speaker separation. Text analytics. Fast search, playback and clipping of snippets of a call for sharing.</div>
            </div>
            <a class="link" href="/#/automate-studio/flow-bounties/flow-bounty-details/zoom-analyst"> DETAILS</a>
        </div>
        </br>
        </br>
        <div class="featureBox">  
            <div class= "featureText">
                <h3>Face Alerter</h3>
                <div class="description-text">This flow engine processes Face Recognition against image or video file chunks and if the chunk outputs match the entity names provided in the engine custom field at runtime, a text message is sent to the phone number provided in a custom field for that engine at setup time.</div>
            </div>
            <a class="link" href="/#/automate-studio/flow-bounties/flow-bounty-details/face-alerter"> DETAILS</a>
        </div>
        </br>
        </br>
        <div class="featureBox"> 
            <div class="featureText">
                <h3>Audio Content Classification and Entity Extraction</h3>
                <div class="description-text">A flow engine that transcribes audio, then runs content classification and entity extraction on the transcribed text.</div>
            </div>
            <a class="link" href="/#/automate-studio/flow-bounties/flow-bounty-details/audio-content-classification"> DETAILS</a>
        </div>
        </br>
        </br>
        <div class="featureBox"> 
            <div class="featureText">
                <h3>Customer Happiness Bot</h3>
                <div class="description-text">A Flow engine that connects to HelpScout, retrieves the specified logs (and accepts a "query":{} object that stores params to query the user's HelpScout org with, and processes the logs with Sentiment analysis.</div>
            </div>
            <a class="link" href="/#/automate-studio/flow-bounties/flow-bounty-details/customer-happiness-bot"> DETAILS</a>
        </div>
        </br>
        </br>
        <div class="featureBox"> 
            <div class="featureText">
                <h3>Email Sentiment Extracter</h3>
                <div class="description-text">A Flow engine that accepts incoming csv & text files webhooked to an HTTP Adapter endpoint sent from an email provider of your choice (eg Mandrill, Sendgrid) and process with a sentiment analysis engine and (1) write the results to a TDO, (2) write the results back to a callbackUrl field if provided by the sender.</div>
            </div>
            <a class="link" href="/#/automate-studio/flow-bounties/flow-bounty-details/email-sentiment-extracter"> DETAILS</a>
        </div>
        </br>
        </br>
        <div class="featureBox"> 
            <div class="featureText">
                <h3>Twitter Temp Bot</h3>
                <div class="description-text">Scrape tweets from either a user (or given users) or a topic/hashtag and run sentiment analysis.</div>
            </div>
            <a class="link" href="/#/automate-studio/flow-bounties/flow-bounty-details/twitter-temp-bot"> DETAILS</a>
        </div>
    </div>
</div>



