---
title: Headless adaptive forms architecture
description: Headless adaptive forms architecture
keywords: headless, adaptive form, architecture
---

# Headless Adaptive Forms Architecture {#architecture}

A typical Headless Adaptive Form architecture  constitutes an Adobe Experience Manager Server, JSON representation of Forms, various frontend apps for channel-specific form renditions.

![Architecture](/help/assets/headless-af-architecture.png)

**Channel Agnostic Form Representation**: A Headless Adaptive form is represented as a .json file. JSON representation defines components, constraints, and structure of a form.

**Adobe Experience Manager Server**: Adobe Experience Manager provides backend capabilities like:  

* RESTful APIs to list, fetch, pre-fill, validate, submit, track submission status of headless forms.
* Visual editor to easily develop a Headless Adaptive Forms.
* Forms Data Model to receive or send data to disparate data sources.
* Workflow engine to automate complex tasks. 

**Front-end Apps**: Front-end apps like, SPA (Single Page Applications), Mobile Apps, JavaScript Apps, to consume the JSON Form Representation and render the form on a client. 

**Forms Web SDK (Client-Side Runtime)**: Forms Web SDK is a client-side JavaScript library. It allows you to apply server-side validations on form fields, maintain state of the form, and provides hooks to connect form with UI layer or adaptive forms rendered component. It allows customers to validate constrains applied to various fields of a form and hooks to connect JSON representation of form to the UI framework. The Forms Web SDK has the following components:
• **Business rule processor**: The business rule processor accepts the forms JSON representation as input, manages the state of the form fields, executes rules, and event handlers present in the JSON.
• **React binder**: Provides hooks over controller to add state to Form Components. It is also helpful in pre-filling a form.
• **Components library**: It provides react Spectrum Components and uses hooks in React Binder module to add state to those components.

<!-- **View Library (UI Layer)**: A custom form application built in a front-end language. You can use react, Angular, Flutter, NPM, Vue.js, Ionic, BootStrap, or any other language to built front end. You can also use the Headless Adaptive Forms Super Component, provided out-of-the-box, inside a react application to render a headless adaptive form. Headless adaptive forms super component makes use of OOTB react spectrum -based form components to render the Headless adaptive form. -->

**JSON Formula**: It is an implementation of form expression grammar. The grammar is a mashup of spreadsheet-like functions and operators and [JMESPath](https://jmespath.org/) a JSON query language.  It helps you query JSON representation and create rules for headless adaptive forms.  You can also use the [playground](https://opensource.adobe.com/json-formula/dist/index.html) to explore JSON formula syntax and capabilities.


## Artifacts available in beta release

In the journey to bring Adobe Experience Manager Headless Adaptive Forms to you, the following artifacts are available in the beta release:


<!-- ### React Renderer component -->


### Forms Web SDK

Forms Web SDK provides the APIs to validate constraints applied to various fields of a form and hooks to connect JSON representation of form to the UI framework. The following components of Web SDK are available:

* **@aemforms/forms-super-component - 0.11.0**: It enables use to render an Adaptive Form using JSON representation. It uses rule grammar to help create dynamic field interactions. The rule grammar is based on [JSON formula](http://github.com/adobe/json-formula/). You can develop your own renderer or embed the React based Adaptive Forms renderer, provided OOTB, in your front-end app to render the form.
* **@aemforms/forms-react-components - 0.11.0**
* **@aemforms/forms-core - 0.11.0**: It is a set of core components included in the Web


#### JavaScript Libraries

#### Storybook

[API playground](https://git.corp.adobe.com/pages/livecycle/af2-web-runtime/story/?path=/story/adaptive-form-introduction--page) provides an overview of different components of Headless Adaptive Forms. It also provides a list of all the supported components, their corresponding properties, and constraints.

### Forms Core Components  

Forms components are the structural elements that constitute the content of the form being authored. These components provide various form fields and ability to customize those fields. 

Core Components are a set of standardized Web Content Management (WCM) components to help you speed up development time and reduce maintenance cost of your forms.

### Specifications

Headless Adaptive Forms specification provides a detailed information on all the components, constraints, and methods available for Headless Adaptive Forms. The specification is available in [HTML](https://git.corp.adobe.com/pages/livecycle/af2-docs/spec/0.10.0/index.html) and [PDF](https://git.corp.adobe.com/pages/livecycle/af2-docs/spec/0.10.0/index.pdf) formats.

### HTTP API

HTTP APIs allow you to list, fetch, validate, submit, track submission status of headless forms.

### Visual Studio Code Plugin

Visual Studio Code extension to help create a valid JSON representation. It provides intellisese support and validation for JSON representation of forms.  

![JSON Form Model And Rendition](/help/assets/rendered-headless-form.png)