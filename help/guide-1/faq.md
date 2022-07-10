# Frequently asked questions (FAQ) {#headless-adaptive-forms-faq}

**Should I know React.js to use Headless Adaptive Forms?**
You can use any framework, library, or language to render Headless Adaptive Forms and use our REST APIs to validate and submit the forms. Web SDK and React component provided out of the box are for your convenience. You can develop your own components and are not limited to use these.

**Where is captured data stored?**

<!-- The data is handed to the configured REST endpoint. You can also configure a Form Data Model (FDM) to receive or send data to disparate data sources (FDM feature would be available in a subsequent beta release.)

<!-- **Is Headless Adaptive Forms HIPPA complaint?** -->

**Did Adobe release a new AEM Archetype for Headless Adaptive forms?**

You can use Archetype 37 or later to include Headless Adaptive forms functionaliy in your Forms as a Cloud Service environment.

**Do I require a Forms as a Cloud Service sandbox to use Headless Adaptive forms?**

Headless Adaptive forms are available only for Forms as a Cloud Service at this moment. You can setup a local development environment to create and test forms with an application or website on your machine before deploying or uploading the form to Cloud Service sandbox.

**Do I need an archetype project to develop Headless Adaptive forms?** 

Archetype project makes it easier to create, store, and deploy a headless adaptive forms on a Forms Cloud service environment. During the beta phase, it is required to deploy an Archetype 37 based project to get stared with creating a Headless Adaptive Forms on a Forms as a Cloud Service environment.

**Where can I get a preview or playground to Headless forms?** 

You can use [container component in Forms as a Cloud service environment](render-first-headless-adaptive-form.md) or you can modify an [API Playground](https://opensource.adobe.com/aem-forms-af-runtime/storybook/?path=/story/reference-examples--introduction) (playbook) example to preview a Headless Adaptive Form.

![](/help/assets/storybook-eample.png)

**Is it possible to build custom components for headless adaptive forms?**

Headless Adaptive Forms are based on [standard specification](/help/assets/Headless-Adaptive-Form-Specification.pdf). Headless Adaptive Forms include react components OOTB. You can extend the specification ot use it to build custom components. For example, components for Chakra UI, Flutter, Vue.js, and more.

**Do Headless Adaptive Forms support lookup for fields?**

Headless Adaptive Forms lookup for fields/Cascading fields. What you see in the second field depends on what you chose in the first field.  

**Do Headless Adaptive Forms allows prefilling forms with personalized data?**

Headless Adaptive Forms allows prefilling forms with personalized data.[API Playground](https://opensource.adobe.com/aem-forms-af-runtime/storybook/?path=/story/reference-examples--prefill-form-with-personalised-data) (playbook) provides an example on how to prefill a Headless Adaptive Form.

**Can I convert an existing Headful Adaptive Form to Headless Adaptive Form?**

**Can I use  existing Adaptive Forms editor to create a Headless Adaptive Form?**

At this moment, you use the Adaptive Form Editor to specify the JSON represenation and set submit action for the forms. Support for drag-and-drop components, applying rules using editor, and more editor related options would be available later in the beta phase. Keep a watch on release notes. 