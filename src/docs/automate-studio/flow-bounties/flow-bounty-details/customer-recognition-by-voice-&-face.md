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
# Call Center Customer Recognition by Voice & Face
[status/Development/Undeveloped/red]


## Overview <!-- {docsify-ignore} -->
The flow will use voice recognition and face recognition engine to recognize the customer from an existing library. If the customer is not in the library, the flow can call another flow to add the caller to the library automatically.
## Details <!-- {docsify-ignore} -->
1. Inputs: 
   - An audio chunk from the call between customer and agent
   - A video chunk from the call between customer and agent, if exists 
   - Library ID of the Contact Center, Entity ID of the speaking agent.
2. Process audio for voice recognition (exclude the voice of the agent which will appear in the result).
3. Process video for face detection, and then face recognition.
4. The output of the two engines (audio and video recognition) will be the name of the customer with a confidence level.
5. If the confidence level is above XX% (configurable), return: “Voice and face match <customer name> at XX% confidence level”.
6. Otherwise, return: “Couldn’t find a match”.

</br>
</br>
<a target="_blank" href="#" id="claim-this-flow-btn">CLAIMED</a>
<hr>