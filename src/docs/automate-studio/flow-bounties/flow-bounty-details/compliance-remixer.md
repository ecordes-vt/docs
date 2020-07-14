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

# Compliance Remixer
[cognitivecategory/Automation/lightgrey]
[status/Development/Undeveloped/red]



## Overview {docsify-ignore}
As a user in the Compliance & Legal team at a Media & Entertainment company producing media that includes commercial and other forms of native advertising featuring objects in the media paid to be there by another company, I need to be able to quickly scan each clip within a larger production video to quickly contextualize where the ad appears in the video  

## Details {docsify-ignore}
Currently, Veritone & aiWARE solve this problem in Discovery and CMS by placing yellow markers on the Video timelines where the Cognitive Outputs appear, but as a legal user in the Compliance team, I may not have immediate access to this application, and I do not want to scrub thorough the video timeline, I would rather see a compilation clip showing me all the appearances cut together

## Proposed Solution {docsify-ignore}
A flow that is invoked when a TDO CME option is selected on a dropdown that: gathers all the timestamps of the cognitive outputs found on that video (across all classifications processed on that TDO) Buffers 7 seconds before and after that found cognitive output Clips each buffered marker Assembles the clips together Stores the clips as a new asset against the TDO Emails the clip as an attachment to the requesting user

<a href="https://forms.gle/tkVjfrtyBDrXyoji7" id="claim-this-flow-btn">CLAIM THIS BOUNTY!</a>

<hr>