---
title: AEM Headless Adaptive Forms Overview
description: Overview for AEM Headless Adaptive Forms.
---

# Release notes

Welcome to Experience Manager Headless Adaptive Forms alpha release. Read on for resources and instructions to get started and make the best of the release.

You can use Adobe Experience Manager Headless Adaptive Forms to build forms applications using front-end UI frameworks like React, Angular, Flutter, NPM, Vue.js, Ionic, Chakra UI, BootStrap, and more and use Adaptive Forms Web SDK for capabilities like state management, validation, and integrations with various other touchpoints.

The alpha release provides you access to Headless Adaptive Forms specifications, Web SDK, and documentation and other tools required to help you create and author forms.

## April 2022 Release

* When a form field is of type String and has no data constraints, the validation state of such field is always set to true. Improved validation state styling of such fields to always show a green tick mark.

* When data for an adaptive form is set dynamically (using the dataref property), it causes the form to re-render. Improved the adaptive forms super component to use the onFocus property on to retain the original focus.

## March 2022 Release

* User interface of the File Attachment features is now spectrum-compliant.
* Added [data bindings](https://git.corp.adobe.com/pages/livecycle/af2-web-runtime/story/?path=/story/reference-examples--data-bindings) and [data prefill](https://git.corp.adobe.com/pages/livecycle/af2-web-runtime/story/?path=/story/reference-examples--prefill-form-with-personalised-data) examples to [Storybook](https://git.corp.adobe.com/pages/livecycle/af2-web-runtime/story/?path=/story/adaptive-form-introduction--page)
* Added support for transparent panels.

## Artifacts available in alpha release

In the journey to bring Adobe Experience Manager Headless Adaptive Forms to you, the following artifacts are available in the alpha release:

### API Specifications

Headless Adaptive Forms specification provides a detailed information on all the components, constraints, and methods available for Headless Adaptive Forms. The specification is available in [HTML](https://git.corp.adobe.com/pages/livecycle/af2-docs/spec/0.10.0/index.html) and [PDF](https://git.corp.adobe.com/pages/livecycle/af2-docs/spec/0.10.0/index.pdf) formats.

### Forms Web SDK

Forms Web SDK provides the APIs to validate constrains applied to various fields of a form and hooks to connect JSON representation of form to the UI framework. The following components of Web SDK are available:

* @aemforms/forms-super-component - 0.10.1-alpha.3
* @aemforms/forms-react-components - 0.10.2-alpha.3
* @aemforms/forms-core - 0.10.1-alpha.3

### Storybook

[API playground](https://git.corp.adobe.com/pages/livecycle/af2-web-runtime/story/?path=/story/adaptive-form-introduction--page) provides an overview of different components of Headless Adaptive Forms. It also provides a list of all the supported components, their corresponding properties, and constraints.

## What's next

The following features would be available in upcoming releases:

* HTTP APIs to invoke a business logic
* Server-side capabilities
* Editor (Authoring UI) for Headless adaptive forms
* Forms business logic (prefill, submit, server-side validation, Document of Record (DoR) and more)
* Continuous improvements to specifications and headless adaptive form runtime