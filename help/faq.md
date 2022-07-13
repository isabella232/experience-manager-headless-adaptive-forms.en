---
title: Frequently asked questions
description: Frequently asked questions
keywords: headless, adaptive form, FAQ
hide: yes
exl-id: 5bfc307d-96a3-4007-b65f-32176ecdb710
---
# Frequently asked questions (FAQ) {#headless-adaptive-forms-faq}

**Should I know React.js to use Headless Adaptive Forms?**
You can use any framework, library, or language to render Headless Adaptive Forms and use our REST APIs to validate and submit the forms. Web SDK and React components provided out of the box are for your convenience. You can develop your own components and are not limited to use these.

**Did Adobe release a new AEM Archetype for Headless Adaptive forms?**

You can use Archetype 37 with flag `includeFormsheadless` or later flag to create an AEM project with Headless Adaptive Forms functionality.

**Do I require Forms as a Cloud Service sandbox to use Headless Adaptive forms?**

Headless Adaptive Forms are available only for Forms as a Cloud Service at this moment. You can set up a local development environment to create and test forms with an application or website on your machine before deploying or uploading the form to Cloud Service sandbox.

**Do I need an archetype project to develop Headless Adaptive forms?** 

Archetype project makes it easier to create, store, and deploy a headless adaptive form on a Forms Cloud service environment. During the beta phase, it is required to deploy an Archetype 37 based project to get stared with creating a Headless Adaptive Forms on a Cloud Service environment.

**Where can I get a preview or playground to Headless forms?** 

You can use [container component in Forms as a Cloud service environment](render-first-headless-adaptive-form.md) or you can modify a [storybook](https://opensource.adobe.com/aem-forms-af-runtime/storybook/?path=/story/reference-examples--introduction) example to preview a Headless Adaptive Form.

![](/help/assets/storybook-eample.png)

**Is it possible to build custom components for headless adaptive forms?**

Headless Adaptive Forms are based on [standard specification](/help/assets/Headless-Adaptive-Form-Specification.pdf). Headless Adaptive Forms include react components OOTB. You can extend the specification ot use it to build custom components. For example, components for Chakra UI, Flutter, Vue.js, and more.

<!-- **Do Headless Adaptive Forms support cascading fields?**

Headless Adaptive Forms look up for fields/Cascading fields. What you see in the second field depends on what you chose in the first field.  -->

**Do Headless Adaptive Forms allow prefilling forms with personalized data?**

Headless Adaptive Forms allows prefilling forms with personalized data. The [Storybook](https://opensource.adobe.com/aem-forms-af-runtime/storybook/?path=/story/reference-examples--prefill-form-with-personalised-data) provides an example of how to prefill a Headless Adaptive Form.

**Can I use  existing Adaptive Forms editor to create a Headless Adaptive Form?**

At this moment, you use the Adaptive Form Editor to specify the JSON representation and set submit action for the forms. Support for drag-and-drop components, applying rules using editor, and more editor-related options would be available later in the beta phase. Keep a watch on release notes. 

**Can I use Headless Adaptive Forms with Anugular SPA?**

You can use the Web SDK to integrate Headless Adaptive Forms with Anugular SPA. It is independent of any framework. You can use React SDK as a reference. 
