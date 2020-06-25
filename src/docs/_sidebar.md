<!-- markdownlint-disable no-inline-html first-line-h1 -->

<!-- Sidebar Logo -->

<a href="/"><div class="logo"><img src="https://static.veritone.com/assets/favicon/favicon.ico" alt="Veritone logo"/><span class="logo-text">Veritone Docs<span></div></a>

- [Cognitive Technology](new/README.cognitiveTech.md)
- [Example Topic](new/README.topic.md)

- [What is Veritone aiWARE?](overview/)
  
  - [Build with aiWARE](developer/)
  - [aiWARE Features](overview/?id=key-platform-features)
  - [How to get started?](quickstart/?id=quickstarts)
  - [aiWARE Architecture](overview/architecture-overview/)
  - [Veritone Applications](apps/)

  - [Architecture Overview](overview/architecture-overview/)
  - [Working with Self-Hosted aiWARE](overview/aiWARE-in-depth/)
    - [Installation](overview/aiWARE-in-depth/edge-installation)
    - [Controller](overview/aiWARE-in-depth/controller)
    - [Engines](overview/aiWARE-in-depth/engines)
    - [Job Processing](overview/aiWARE-in-depth/job-processing)
    - [File System](overview/aiWARE-in-depth/file-system)
    - [Stream Ingestor 2](overview/aiWARE-in-depth/stream-ingestor)

- [Getting Started](quickstart/)
  - [Working with Jobs](quickstart/jobs/)
  - <span class="app-developer">[I'm an Application Developer](quickstart/app-developer/)</span>
  - <span class="ml-integrator">[I'm a Solutions Engineer](quickstart/ml-integrator/)</span>
  - <span class="ml-explorer">[I'm a Data or Biz Analyst](quickstart/ml-explorer/)</span>
  - <span class="engine-developer">[I'm an Engine Developer](quickstart/engine-developer/)</span>

- [API Reference](apis/)

  - [Working with the GraphQL API](apis/using-graphql.md)
    - [Mutation Methods](apis/reference/mutation/)
    - [Query Methods](apis/reference/query/)
    - [The Veritone API Data Model](apis/data-model.md)
    - [Using GraphQL](apis/using-graphql.md)
    - [Authentication](apis/authentication.md)
    - [Error Codes](apis/error-codes.md)
    - [Jobs, Tasks, and TDOs](apis/jobs-tasks-tdos.md)
    - [Job Quickstart Guide](apis/job-quickstart/)
    - [Search Quickstart Guide](apis/search-quickstart/)
    - [Using Eventing](apis/eventing/eventing.md)
    - [Endpoints](apis/endpoints/)
    - [API Examples](apis/examples)
      - [GraphQL API Basics](apis/tutorials/graphql-basics.md)
      - [Clean up TDO data](apis/tutorials/cleanup-tdo.md)
      - [Creating Export Requests](apis/tutorials/create-export-request/)
      - [Posting Engine Results](apis/tutorials/engine-results.md)
      - [Lookup Available Engines](apis/tutorials/get-engines.md)
      - [Error Handling in the GraphQL API](apis/tutorials/graphql-error-handling.md)
      - [Uploading and Processing Files](apis/tutorials/upload-and-process.md)
      - [Uploading Large Files](apis/tutorials/uploading-large-files.md)
      - [Handling File Upload Errors](apis/tutorials/file-upload-error-handling.md)
      - [Authentication and Authorization Tokens](apis/tutorials/tokens.md)
      - [Paging](apis/tutorials/paging.md)
      - [Asset Types](apis/tutorials/asset-types.md)

  - [Working with the Edge REST API](apis/edge/index.html)

- [Tutorials](apis/tutorials/)
  - [GraphQL API Basics](apis/tutorials/graphql-basics.md)
  - [Clean up TDO data](apis/tutorials/cleanup-tdo.md)
  - [Creating Export Requests](apis/tutorials/create-export-request/)
  - [Posting Engine Results](apis/tutorials/engine-results.md)
  - [Lookup Available Engines](apis/tutorials/get-engines.md)
  - [Error Handling in the GraphQL API](apis/tutorials/graphql-error-handling.md)
  - [Uploading and Processing Files](apis/tutorials/upload-and-process.md)
  - [Uploading Large Files](apis/tutorials/uploading-large-files.md)
  - [Handling File Upload Errors](apis/tutorials/file-upload-error-handling.md)
  - [Authentication and Authorization Tokens](apis/tutorials/tokens.md)
  - [Paging](apis/tutorials/paging.md)
  - [Asset Types](apis/tutorials/asset-types.md)

- [Build with Automate Studio](automate-studio/)
  - [Getting Started](automate-studio/getting-started/README)
  - [Flow Examples](automate-studio/flow-examples/README)
  - [FAQ](automate-studio/faq)
  
- [Build **Applications**](developer/applications/)

  - [Quickstart](developer/applications/quick-start/)
    - [Step 1 - Register Your Application](developer/applications/quick-start/step-1.md)
    - [Step 2 - Set Up Authentication](developer/applications/quick-start/step-2.md)
    - [Step 3 - Add APIs and Components](developer/applications/quick-start/step-3.md)
    - [Step 4 - Submit Your Application](developer/applications/quick-start/step-4.md)
    - [Step 5 - Deploy Your Application](developer/applications/quick-start/step-5.md)
  - [Tutorial: Build Your Own AI App](developer/applications/app-tutorial/)
    - [Step 1: Register Your App](developer/applications/app-tutorial/app-tutorial-step-1.md)
    - [Step 2: Set Up Authentication](developer/applications/app-tutorial/app-tutorial-step-2.md)
    - [Step 3: Add Processing Logic](developer/applications/app-tutorial/app-tutorial-step-3.md)
    - [Step 4: Run Object Detection on a Video](developer/applications/app-tutorial/app-tutorial-step-4.md)
  - [Application Integration](developer/applications/integration/)
  - [Context Menu Extensions](developer/applications/context-menu-extensions.md)
  - [OAuth](developer/applications/oauth.md)
  - [Resources](developer/applications/resources.md)
  - [FAQ](developer/applications/faq.md)

- [Build **Engines**](developer/engines/)

  - [Getting Started](developer/engines/getting-started/)
    - [Path to Monetization](developer/engines/getting-started/path-to-monetization/)
    - [Support](developer/engines/getting-started/support/)
    - [Technologies Used](developer/engines/getting-started/technologies/)
  - [Overview: Building **Cognitive Engines**](developer/engines/cognitive/)
    - Audio
      - [Audio Fingerprinting](developer/engines/cognitive/audio/audio-fingerprinting/)
    - Biometrics
      - [Face Detection](developer/engines/cognitive/biometrics/face-detection/)
      - [Face Recognition](developer/engines/cognitive/biometrics/face-recognition/)
    - Data
      - [Data Correlation](developer/engines/cognitive/data/correlation/)
      - [Geolocation](developer/engines/cognitive/data/geolocation/)
    - Facial Features
      - [Facial Features](developer/engines/cognitive/facial-features/)
    - Speech
      - [Speaker Detection](developer/engines/cognitive/speech/speaker-detection/)
      - [Speaker Recognition](developer/engines/cognitive/speech/speaker-recognition/)
      - [Transcription](developer/engines/cognitive/speech/transcription/)
    - Text
      - [Anomaly Detection](developer/engines/cognitive/text/anomaly-detection/)
      - [Content Classification](developer/engines/cognitive/text/content-classification/)
      - [Entity Extraction](developer/engines/cognitive/text/entity-extraction/)
      - [Keyword Extraction](developer/engines/cognitive/text/keyword-extraction/)
      - [Language Identification](developer/engines/cognitive/text/language-identification/)
      - [Sentiment Analysis](developer/engines/cognitive/text/sentiment/)
      - [Summarization](developer/engines/cognitive/text/summarization/)
      - [Text Extraction](developer/engines/cognitive/text/text-extraction/)
      - [Translation](developer/engines/cognitive/text/translation/)
        - [Extracted Text Translation](developer/engines/cognitive/text/translation/extracted-text/)
        - [Plain Text Translation](developer/engines/cognitive/text/translation/plain-text/)
        - [Recognized Text (OCR) Translation](developer/engines/cognitive/text/translation/recognized-text/)
        - [Rich Text Translation](developer/engines/cognitive/text/translation/rich-text/)
        - [Transcript Translation](developer/engines/cognitive/text/translation/transcript/)
    - Verification
      - [Face Verification](developer/engines/cognitive/verification/face-verification/)
      - [Speaker Verification](developer/engines/cognitive/verification/speaker-verification/)
    - Vision
      - [Image classification](developer/engines/cognitive/vision/image-classification/)
      - [License Plate Recognition (ALPR)](developer/engines/cognitive/vision/license-plate/)
      - [Logo Detection](developer/engines/cognitive/vision/logo-detection/)
      - [Object Detection](developer/engines/cognitive/vision/object-detection/)
      - [Text Recognition (OCR)](developer/engines/cognitive/vision/text-recognition/)
  - [Overview: **Correlation Engines**](developer/engines/correlation/)
  - [Engine Developer's Toolkit (V3F)](developer/edge/engines)
  - [Tutorial: Build Your Own Engine](developer/engines/tutorial/)
    - [Step 0 - Introduction and Project Setup](developer/engines/tutorial/)
    - [Step 1 - Register Your Project with Veritone](developer/engines/tutorial/engine-tutorial-step-1.md)
    - [Step 2 - Use Docker to Create a Build](developer/engines/tutorial/engine-tutorial-step-2.md)
    - [Step 3 - Test Your Build Locally](developer/engines/tutorial/engine-tutorial-step-3.md)
    - [Step 4 - Upload Your Build to Veritone](developer/engines/tutorial/engine-tutorial-step-4.md)
    - [Step 5 - Test Your Engine in aiWARE](developer/engines/tutorial/engine-tutorial-step-5.md)
  - [Deeper Dive: Customizing Engine Output](developer/engines/tutorial/customizing-engine-output.md)
  - [Deeper Dive: Customizing Engine Input](developer/engines/tutorial/engine-custom-fields)
  - [Deeper Dive: How to Train an Engine](developer/engines/tutorial/engine-training-tutorial)
  - [Engine Approval Process](developer/engines/approval/)
  - [Deployment Models](developer/engines/deployment-model/)
  - [Processing Modes](developer/engines/processing-modes/)
    - [Segment Engine Processing](developer/engines/processing-modes/segment-processing/)
    - [Stream Engine Processing](developer/engines/processing-modes/stream-processing/)
  - [Engine Standards](developer/engines/standards/)
    - [Engine Output (vtn-standard)](developer/engines/standards/engine-output/)
    - [Engine Manifest](developer/engines/standards/engine-manifest/)
      <!-- - [Message Types](developer/engines/standards/message-types/)-->
  - [Custom Fields](developer/engines/custom-fields/)
  - [Polling](developer/engines/polling/)
  - [Callbacks](developer/engines/callbacks/)
  - [Testing & Debugging](developer/engines/testing-and-debugging/)
  
  - [Building **Adapters**](developer/adapters/)

    - [Quickstart](developer/adapters/quick-start/)
      - [Step 1 - Register Your Adapter](developer/adapters/quick-start/step-1.md)
      - [Step 2 - Construct Your Code for the Veritone Platform](developer/adapters/quick-start/step-2.md)
      - [Step 3 - Create Your Manifest File](developer/adapters/quick-start/step-3.md)
      - [Step 4 - Package and Upload a Build](developer/adapters/quick-start/step-4.md)
      - [Step 5 - Submit Your Build for Approval](developer/adapters/quick-start/step-5.md)
      - [Step 6 - Deploy Your Adapter](developer/adapters/quick-start/step-6.md)
    - [Construction Guidelines](developer/adapters/guidelines.md)
    - [Adapter Manifest](developer/adapters/manifest.md)

  - [Working with **Structured Data**](developer/data/)

    - [Quickstart](developer/data/quick-start/)

  - [Working with **Libraries**](developer/libraries/)

    - [Library-enabled Engines](developer/libraries/engines.md)
    - [Training Engines](developer/libraries/training.md)
    - [Running Engines](developer/libraries/running.md)

  - [Machine Box](/developer/machine-box/)

    - [API guidelines](/developer/machine-box/api-guidelines)
    - [Setup](/developer/machine-box/setup/)
      - [Install Docker](/developer/machine-box/setup/docker)
      - [Box Keys](/developer/machine-box/setup/box-key)
    - [Boxes](/developer/machine-box/boxes/)
      - [Facebox](/developer/machine-box/boxes/facebox-overview)
        - [Facebox tutorial: Teaching Facebox](/developer/machine-box/boxes/teaching-facebox)
      - [Tagbox](/developer/machine-box/boxes/tagbox)
        - [Tagbox tutorial: Recognizing images](/developer/machine-box/boxes/tagbox/recognizing-images)
      - [Textbox](/developer/machine-box/boxes/textbox)
      - [Classificationbox](/developer/machine-box/boxes/classificationbox)
        - [Best practices for using Classificationbox](/developer/machine-box/boxes/classificationbox/best-practices)
      - [Nudebox](/developer/machine-box/boxes/nudebox)
      - [Objectbox](/developer/machine-box/boxes/objectbox)
      - [Fakebox](/developer/machine-box/boxes/fakebox)

  - [Resources: Data Science](developer/resources/)
  - [Developer Terms & Conditions](developer/terms-and-conditions.md)

- [Benchmark AI Engines](benchmark/)

- [Partner with Veritone](developer/benefits.md)

- [aiWARE Glossary](overview/glossary/)
