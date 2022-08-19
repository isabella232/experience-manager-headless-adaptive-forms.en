---
title: Headless Adaptive Forms architecture
description: Headless Adaptive Forms architecture
keywords: headless, adaptive form, architecture
hide: yes
exl-id: ee7096d8-89e2-41e0-85e7-b26457df96fb
---
# Headless Adaptive Forms Architecture {#architecture}

A typical Headless Adaptive Form architecture constitutes an Adobe Experience Manager Server, JSON structure of forms, various frontend apps for channel-specific form renditions.

![Architecture](/help/assets/headless-af-architecture.png)

**Channel Agnostic Form Representation**: A Headless Adaptive form is represented as a .json file. JSON structure defines components, constraints, and structure of a form.

**Adobe Experience Manager Server**: Adobe Experience Manager provides backend capabilities like:  

* RESTful APIs to list, fetch, pre-fill, validate, submit, track submission status of headless forms.
* Visual editor to easily develop a Headless Adaptive Forms.
* Forms Data Model to receive or send data to disparate data sources.
* Workflow engine to automate complex tasks. 

**Front-end Apps**: Front-end apps like, SPA (Single Page Applications), Mobile Apps, JavaScript Apps, to consume the JSON Form Representation and render the form on a client. 

**Forms Web SDK (Client-Side Runtime)**: Forms Web SDK is a client-side JavaScript library. It allows you to apply client-side validations on form fields, maintain state of the form, and provides hooks to connect form with UI layer or adaptive forms rendered component. It allows customers to validate constrains applied to various fields of a form and hooks to connect JSON structure of form to the UI framework. The Forms Web SDK has the following components:
* **Business rule processor**: The business rule processor accepts the forms JSON structure as input, manages the state of the form fields, executes rules, and event handlers present in the JSON.
* **React binder**: Provides hooks over controller to add state to Form Components. It is also helpful in pre-filling a form.
* **Components library**: It provides React Spectrum Components and uses hooks in React Binder module to add state to those components.

<!-- **View Library (UI Layer)**: A custom form application built in a front-end language. You can use react, Angular, Flutter, NPM, Vue.js, Ionic, BootStrap, or any other language to built front end. You can also use the Headless Adaptive Forms Super Component, provided out-of-the-box, inside a react application to render a headless adaptive form. Headless Adaptive Forms super component makes use of OOTB react spectrum -based form components to render the Headless adaptive form. 

Core-Components: It enables use to render an Adaptive Form using JSON structure. It uses rule grammar to help create dynamic field interactions. The rule grammar is based on [JSON formula](http://github.com/adobe/json-formula/). You can develop your own renderer or embed the React based Adaptive Forms renderer, provided OOTB, in your front-end app to render the form. -->

**JSON Formula**: It is an implementation of form expression grammar. The grammar is a mashup of spreadsheet-like functions and operators and [JMESPath](https://jmespath.org/) a JSON query language.  It helps you query JSON structure and create rules for headless adaptive forms.  You can also use the [playground](https://opensource.adobe.com/json-formula/dist/index.html) to explore JSON formula syntax and capabilities.
