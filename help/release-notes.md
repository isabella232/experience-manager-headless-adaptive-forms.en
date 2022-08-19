---
title: AEM Headless Adaptive Forms Overview
description: Overview for AEM Headless Adaptive Forms.
hide: yes
exl-id: cd7c7972-376c-489f-a684-f479d92c37e7
---
# Release notes

Welcome to Experience Manager Headless Adaptive Forms Beta release. Read on for resources and instructions to get started and make the best of the release.

You can use Adobe Experience Manager Headless Adaptive Forms to build forms applications using front-end UI frameworks like React, Angular, and more and use Adaptive Forms Web SDK for capabilities like state management, validation, and integrations with various other touchpoints.

The beta release provides you access to use Headless Adaptive Forms in a [local development environment](setup-development-environment.md). You can use the local development environment to build and test headless adaptive forms.

Headless Adaptive Forms receives improvements on an ongoing basis. To stay up to date with the most recent developments, visit this page regularly. This page provides you with information about early access, latest releases, new features, improvements, bug fixes, deprecated functionality, special instructions, and future plans for changes. 

## July 2022 (v0.22.1)

### New features

* Introduced the `validateFormData` API. It validates all the components against the rules and constraints an returns the list of errors. The validation takes place on the server.
* Introduced the `FormLoad` event.
* Introduced the `importData` and `exportData`.
* You can now dynamically add or remove items, that expect unqiue values, from a repeatable panel. You can use the `minItems` and `maxitems` constraint to set limit of item.
* You can now use constraint to set maximum file upload size, accepted file types, minimum files, and maximum files to upload.

### Improvements and bug fixes

* The service was executing some event handlers twice. The issue is fixed.
* Fixing Data Generation with different values of dataRef, name and type.

## Artifacts available in beta release

In the journey to bring Adobe Experience Manager Headless Adaptive Forms to you, the following artifacts are available in the beta release:

<!-- ### React Renderer component -->


### AEM Forms as a Cloud Service SDK

AEM Forms as a Cloud Service SDK to help you create, store, and fetch Headless Adaptive Forms. It also helps provide prefill, server-side rule validation, and submit services for Headless adaptive forms.

### Forms Web SDK

Forms Web SDK provides the APIs to validate constraints applied to various fields of a form and hooks to connect JSON schema of form to the UI framework. It also provides     React Renderer​ for Headless Adaptive Forms to help integrate a Headless Adaptive Form to your application. The following components of Web SDK are available:

* **[@aemforms/af-react-components](https://www.npmjs.com/package/@aemforms/af-react-components)** 
* **[@aemforms/af-react-renderer](https://www.npmjs.com/package/@aemforms/af-react-renderer)**
* **[@aemforms/af-core](https://www.npmjs.com/package/@aemforms/af-core)**


#### Storybook

[Storybook](https://opensource.adobe.com/aem-forms-af-runtime/storybook/) provides an overview of different components of Headless Adaptive Forms. It also provides a list of all the supported components, their corresponding properties, and constraints.

### Forms Core Component  

<!-- Forms components are the structural elements that constitute the content of the form being authored. These components provide various form fields and ability to customize those fields. -->

Core Components are a set of standardized Web Content Management (WCM) components to help you speed up development time and reduce maintenance cost of your forms. The Forms Container component is a core component. It helps you embed and render a JSON schema of Headless Adaptive Form in Adaptive Forms editor of Forms as a Cloud Service SDK.  

### Adaptive Forms V2 Specifications

Headless Adaptive Forms specification provides a detailed information on all the components, constraints, and methods available to define Headless Adaptive Forms. The specification is available in [PDF](/help/assets/Headless-Adaptive-Form-Specification.pdf) format.

### HTTP and JS API

[HTTP APIs](https://opensource.adobe.com/aem-forms-af-runtime/api/) allow you to list, fetch, validate, submit, track submission status of headless forms. [JS APIs](https://opensource.adobe.com/aem-forms-af-runtime/jsdocs/) helps you use Headless Adaptive Forms with any JavaScript based UI framework. 

### Visual Studio Code Plugin

[Visual Studio Code extension](/help/assets/adaptive-form-builder-0.11.0.vsix) to help create a valid JSON schema. It provides IntelliSense support and validation for JSON schema of forms along with common funcions like add, delete, or rename components of a JSON schema.  

## What's next

The following features would be available in upcoming releases:

* HTTP APIs to invoke a business logic.
* Server-side capabilities (Prefill, server-side validation, generating Document of Record (DoR), Submitting to a Form Data Model or using Form Data Models for creating rules, and more).
* Continuous improvements to specifications and headless adaptive form runtime.
* Use  Adaptive Forms editor for easier management and authoring Headless Adaptive Forms.
