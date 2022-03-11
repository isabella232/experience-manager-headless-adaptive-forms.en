---
title: AEM Headless Adaptive Forms Overview
description: Overview for AEM Headless Adaptive Forms.
---

# Headless Adaptive Forms Overview

You can use Adobe Experience Manager Headless Adaptive Forms to build forms applications using front-end UI like React, Angular, Flutter, NPM, Vue.js, Ionic, Chakra UI, BootStrap, and more and use Headless Adaptive Forms Web SDK for capabilities like state management, validation and integrations with various other touchpoints.

For example, an organization We.Org is looking to digitize their customer enrollment journey. Their developers are well versed at using Angular to build frontend solutions. They are looking to build a custom front-end while offloading form validation and electronic signatures to specialized solutions.

Adobe Experience Manager Headless Adaptive Forms provides such organizations freedom to build forms using their existing expertise in frontend languages while providing support to use back-end capabilities to create enterprise class forms experience.

## Architecture

A typical headless adaptive form architetcure constitutes JSON representation, Web SDK, and UI Layer.

![Architecture](/help/assets/architecture.png)

**JSON representation**: A headless adaptive form is represented as a .json file. JSON representation defines components, constraints, and structure of a form.

**Forms Web SDK**: Forms Web SDK is a client-side JavaScript library. It allows you apply server-side validations on form fields, maintain state of the form, and provides hooks to connect form with UI layer or adaptive forms super component. Forms Web SDK is a client-side JavaScript library that allows customers to validate constrains applied to various fields of a form and hooks to connect JSON representation of form to the UI framework.  The Forms Web SDK has the following components:
• **Business rule processor**: The business rule processor accepts the forms JSON representation as input, manages the state of the form fields, executes rules, and event handlers present in the JSON.
• **React binder**: Provides hooks over controller to add state to Form Components. It is also helpful in pre-filling a form.
• **Components library**: It provides react Spectrum Components and uses hooks in React Binder module to add state to those components.

**View Library (UI Layer)**: A custom form application built in a front-end language. You can use react, Angular, Flutter, NPM, Vue.js, Ionic, BootStrap, or any other language to built front end. You can also use the Headless Adaptive Forms Super Component, provided out-of-the-box, inside a react application to render a headless adaptive form. Headless adaptive forms super component makes use of OOTB react spectrum -based form components to render the Headless adaptive form.

**Adaptive forms super component**: It enables use to create an adaptive form using JSON representation. It helps you declaratively create a form. It uses rule grammar to help create dynamic field interactions. The rule grammar is based on [JSON formula](http://github.com/adobe/json-formula/).  

**JSON Formula**: It is an implementation of form expression grammar. The grammar is a mashup of spreadsheet-like functions and operators and [JMESPath](https://jmespath.org/) a JSON query language.  It helps you query JSON representation and create rules for headless adaptive forms.  You can also use the [playground](https://opensource.adobe.com/json-formula/dist/index.html) to explore JSON formula syntax and capabilities.  
