---
title: AEM Headless Adaptive Forms Overview
description: Overview for AEM Headless Adaptive Forms.
---

# Headless Adaptive Forms Overview

Adobe Experience Manager Headless Adaptive Forms is an API-first form builder platform for developers and business users. You can use Headless Adaptive Forms to build and natively render a form in any website, an application or email. You can also use Headless Adaptive Forms to build custom data capture experiences for voice based or non-visual inteactions. Headless adaptive forms provide:

* A channel agnostic JSON representation of forms for easy consumption in any application.
* Web SDK to natively render a headless adaptive form in a website.
* Rule engine to build dynamic forms and validations.
* Submission services to submit a form to any endpoint.
* Direct Submission of data to endpoint or storage system of your choice without saving data in any intermiediate data system. 

![Build and natively render a form in any website, an application, or non-visual inteactions](/help/assets/headless-forms-for-any-device.jpg)



Headless Adaptive Forms are for everyone. However, at the beta stage, we expect developers and designers familiar with modern JavaScript frameworks to use the Headless Adaptive Forms. Developers can leverage their existing expertise in frontend languages like React to build beautiful enterprise class form experiences.

## Why Adobe Experience Manager Headless Adaptive Forms?

Our headless forms are based on an open-specification (JSON representation of form and Rules grammer) developed by Adobe and provide native SDKs to manage form state, validate form content, and connect a form to a UI framework of your choice, providing you freedom to concentrate on bulding great user experiences while leaving complex backend tasks on Adobe. You have freedom to develop your own components to render a form using any UI framework or programming language or use OOTB react components to render a form. Along with the specification, Headless Adaptive Forms would add the following user-friendly backend tools and services for complex tasks as beta progresses:

* Workflow engine to automate complex tasks.
* Visual editor to easily develop a Headless Adaptive Forms.
* Support to generate Document of Record automatically and on-demand.
* HTTP APIs to invoke a business logic.
* Forms Data Model to receive or send data to disparate data sources.
* Pre-filling a form based on user-profile or available data.

## How Headless Adaptive Form work?

A Headless Adaptive Form is essentially a JSON representaion (Schema) complete with fields (Text box, choices, and many more) and corresponding rules (Conditional logic) to add dynamism to the form. You can use the schema in your application or website to natively render your forms. A single schema can serve multiple webpages and applications without making any app or website specfic changes to it.

![How Headless Adaptive Form works](/help/assets/how-headless-adaprive-forms-work.png)

You can use React component shipped with Headless Adaptive Forms to render an Adaptive Form or build your own custom component to natively render a Headless Form in a Website or an application or use any UI framework or programming language to build your own components to render your forms.

## How to join the beta program?

You can send an email to [headless-af-beta@adobe.com](headless-af-beta@adobe.com) from your official email ID to join the beta program.

## Artifacts available in beta release

In the journey to bring Adobe Experience Manager Headless Adaptive Forms to you, the following artifacts are available in the beta release:

### API Specifications

Headless Adaptive Forms specification provides a detailed information on all the components, constraints, and methods available for Headless Adaptive Forms. The specification is available in [HTML](https://git.corp.adobe.com/pages/livecycle/af2-docs/spec/0.10.0/index.html) and [PDF](https://git.corp.adobe.com/pages/livecycle/af2-docs/spec/0.10.0/index.pdf) formats.

### Forms Web SDK

Forms Web SDK provides the APIs to validate constrains applied to various fields of a form and hooks to connect JSON representation of form to the UI framework. The following components of Web SDK are available:

* @aemforms/forms-super-component - 0.11.0
* @aemforms/forms-react-components - 0.11.0
* @aemforms/forms-core - 0.11.0

### Storybook

[API playground](https://git.corp.adobe.com/pages/livecycle/af2-web-runtime/story/?path=/story/adaptive-form-introduction--page) provides an overview of different components of Headless Adaptive Forms. It also provides a list of all the supported components, their corresponding properties, and constraints.

<!-- ## Architecture

A typical headless adaptive form architetcure constitutes JSON representation, Web SDK, and UI Layer.

![Architecture](/help/assets/architecture.png)

**JSON representation**: A headless adaptive form is represented as a .json file. JSON representation defines components, constraints, and structure of a form.

**Forms Web SDK**: Forms Web SDK is a client-side JavaScript library. It allows you apply server-side validations on form fields, maintain state of the form, and provides hooks to connect form with UI layer or adaptive forms super component. Forms Web SDK is a client-side JavaScript library that allows customers to validate constrains applied to various fields of a form and hooks to connect JSON representation of form to the UI framework.  The Forms Web SDK has the following components:
• **Business rule processor**: The business rule processor accepts the forms JSON representation as input, manages the state of the form fields, executes rules, and event handlers present in the JSON.
• **React binder**: Provides hooks over controller to add state to Form Components. It is also helpful in pre-filling a form.
• **Components library**: It provides react Spectrum Components and uses hooks in React Binder module to add state to those components.

**View Library (UI Layer)**: A custom form application built in a front-end language. You can use react, Angular, Flutter, NPM, Vue.js, Ionic, BootStrap, or any other language to built front end. You can also use the Headless Adaptive Forms Super Component, provided out-of-the-box, inside a react application to render a headless adaptive form. Headless adaptive forms super component makes use of OOTB react spectrum -based form components to render the Headless adaptive form.

**Adaptive forms renderer**: It enables use to redner an Adaptive Form using JSON representation. It uses rule grammar to help create dynamic field interactions. The rule grammar is based on [JSON formula](http://github.com/adobe/json-formula/).  

**JSON Formula**: It is an implementation of form expression grammar. The grammar is a mashup of spreadsheet-like functions and operators and [JMESPath](https://jmespath.org/) a JSON query language.  It helps you query JSON representation and create rules for headless adaptive forms.  You can also use the [playground](https://opensource.adobe.com/json-formula/dist/index.html) to explore JSON formula syntax and capabilities.  -->


## Frequently asked questions (FAQ) {#headless-adaptive-forms-faq}

**Should I know React.js to use Headless Adaptive Forms?**
You can use any framework, library, or language to render Headless Adaptive Forms and use our REST APIs to validate and submit the forms. Web SDK and React component provided out of the box are for your convenience. You can develop your own components and are not limited to use these.

**Where is captured data stored?**

**Is Headless Adaptive Forms HIPPA complaint?**





