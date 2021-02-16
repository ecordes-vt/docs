<!-- markdownlint-disable -->

<style>
aside  {
  border-style: solid;
  border-radius: 9px;
  border-width: 2.2px;
  border-color:#ccc;
  padding: 5px;
  background: #e6e8ef;
}

aside.small {
  display:inline;
  font-size:9pt;
  position:relative; top:-4px;
}

.topruled {
  border-top-width: 1.2px;
  border-top-style: solid;
  border-top-color: rgb(76, 76, 100);
  line-height:45%;
}
.bottomruled {
  border-bottom-width: 1.2px;
  border-bottom-style: solid;
  border-bottom-color: rgb(76, 76, 100);
  line-height:45%;
}
</style>

<h2 style="display: inline;">Step 1: Register your engine with Veritone &nbsp;</h2>&nbsp;&nbsp;<aside class="small">
<b>ESTIMATED TIME:</b> 10 minutes </aside> &nbsp;

<!-- DISABLE VIDEO
<div style="width: 35%">
<iframe src="https://player.vimeo.com/video/375527586?color=ff9933&title=0&byline=0&portrait=0" style="border:0;top:0;left:0;width:75%;height:75%;" allow="autoplay; fullscreen" allowfullscreen></iframe></div>
<script src="https://player.vimeo.com/api/player.js"></script>
-->

Assuming you've already accomplished the prerequisites outlined in [Before You Begin](/developer/engines/tutorial/?id=before-you-begin), your first step in creating an engine (yes, even before writing any code!) should be to register the engine with Veritone.

> In this step, you'll obtain a Veritone-assigned Engine ID, and generate your `manifest.json` file using a simple online UI.

1\. Go to [https://developer.veritone.com/](https://developer.veritone.com/) and sign in.

2\. Click on the blue **NEW** button (upper left) and select **ENGINE** from the dropdown list. The first page of the New Engine wizard opens. (This is the Functionality page.)

3\. Determine the Engine Class that applies to your engine; scroll down if need be; click into the associated widget (to expose more choices); and select the capability that applies to your engine.
In our case, the Hello World engine is a **Text** engine with **Keyword Extraction** capability.

![Choose an engine capability](NewEngine-Capability.png)

4\. Scroll down the page, to **Engine Mode**. Click on the *Segment* tile.

![Click on the Segment-mode tile](NewEngine-Mode.png)

5\. Scroll down to **Supported Input Types**. Click the Supported Formats flyout control, and check each checkbox for each MIME type that applies. Since the Hello World engine supports text input, we've selected `text/html`, `text/plain`, and `text/plain;charset=utf-8`.

![Select the input content types](NewEngine-MIME-type.png)

6\. If your engine requires custom input options at runtime (for example, if your engine needs to know a 2-letter ISO 639-1 language code on a per-job basis; or any other custom config options), use the **ADD CUSTOM FIELD** button under **Custom Fields** to set this up. (Read more about [Custom Fields](/developer/engines/custom-fields/).)

7\. Click the **NEXT** button (lower right corner of page) to proceed to the next page of the wizard. (This is the Testing Detail page.)

![Select deployment model](NewEngine-Testing.png)

8\. Enter an e-mail address where certification test results can be sent. (The [engine certification and approval process](/developer/engines/approval/?id=engine-certification-and-approval-process) is automatic.) Optionally specify the public URL of any media file that should be used for testing of your engine. Also, optionally provide information about any Custom Payload Fields your engine will rely on.

> If you see a prompt of "Are you sure you want to continue?", click **CONTINUE ANYWAY**. You can come back later to supply default job mutations. (Your engine will work fine without them.)

9\. Click the **NEXT** button (lower right corner of page) to proceed to the next page of the wizard. (This is the Deployment Model page.)

![Select deployment model](NewEngine-deployment.png)

Since the Hello World engine does not need to interact with any external web endpoints, it's okay to select **Network Isolated**.

10\. Click **NEXT** to go to the next page of the wizard. (This is the final wizard page, called Customize.)

11\. Check your engine's Name (edit it as need be), add an optional Descriptor (10 charactsers, max), add a Description, specify an optional icon, and provide other information about the engine.

> A Name that conforms to Veritone's naming conventions will be generated for your engine automatically. We recommend that names follow a pattern of &lt;Capability&gt;-&lt;Organization&gt;-&lt;Mode&gt;-&lt;Descriptor&gt;-&lt;Edge Cluster Version&gt;.

![Add Name and Description](NewEngine-Naming.png)

12\. Click the **REVIEW** button (lower right) to bring up an **Engine Summary** dialog in which you can check the accuracy of the selections you've made in the wizard thus far.

> Use the **BACK** button as necessary to go back through your earlier selections and edit them.

![Engine Summary dialog](NewEngine-summary.png)

13\. Click the **CREATE ENGINE PROFILE** button to exit out of the wizard and be taken to a **Builds** overview page (which has two tabs: **BUILDS** and **TASKS**).
_Note that your engine's ID is shown near the top of the page, under the engine name._

![Builds overview page](NewEngine-manifest-1.png)

> You can return to this page any time. Either bookmark the page, or simply click the ENGINES heading in the nav sidebar at [https://developer.veritone.com](https://developer.veritone.com), then pick the engine of interest from your list of engines.

### Create Your manifest.json File

Now that you've registered your project with Veritone Developer, you can generate a `manifest.json` file.

1\. Go to the **Builds** page. (Click ENGINES in the nav sidebar and choose your engine from the list of engines.) See the last screen shot.

2\. Find the **GENERATE MANIFEST** button and click it. A **Manifest** dialog appears, containing the text of your `manifest.json` file.

![manifest](NewEngine-manifest-2.png)

3\. Download the `manifest.json` file into your project directory (or use the copy-to-clipboard button and paste it into a file called `manifest.json` in your project).

4\. Edit the manifest as necessary to amend any fields that might not be accurate or complete. (For more information: Read about [Engine Manifests](/developer/engines/standards/engine-manifest/?id=engine-manifest).)

## Recap and Cheat Sheet

In this lesson, we learned how to: 
* Obtain an **Engine ID** as a byproduct of registering an engine project with Veritone.
* Specify the **Class** and **Capability** of your engine using the engine onboarding wizard at [https://developer.veritone.com/](https://developer.veritone.com/).
* Specify your engine's _processing mode_ (Chunk vs. Stream).
* Specify the engine's supported input-data MIME types.
* Select a _deployment model_ (e.g. Network Isolated vs. External Access).
* Specify the engine's Name, and other metadata.
* Use the UI at [https://developer.veritone.com/](https://developer.veritone.com/) to generate a `manifest.json` file for your engine.

**NEXT**: [Use Docker to create an engine build ⇨](/developer/engines/tutorial/engine-tutorial-step-2)
