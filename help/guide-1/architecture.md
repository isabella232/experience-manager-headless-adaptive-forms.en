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

**Forms Web SDK (Client-Side Runtime)**: Forms Web SDK is a client-side JavaScript library. It allows you to apply client-side validations on form fields, maintain state of the form, and provides hooks to connect form with UI layer or adaptive forms rendered component. It allows customers to validate constrains applied to various fields of a form and hooks to connect JSON representation of form to the UI framework. The Forms Web SDK has the following components:
* **Business rule processor**: The business rule processor accepts the forms JSON representation as input, manages the state of the form fields, executes rules, and event handlers present in the JSON.
* **React binder**: Provides hooks over controller to add state to Form Components. It is also helpful in pre-filling a form.
* **Components library**: It provides React Spectrum Components and uses hooks in React Binder module to add state to those components.

<!-- **View Library (UI Layer)**: A custom form application built in a front-end language. You can use react, Angular, Flutter, NPM, Vue.js, Ionic, BootStrap, or any other language to built front end. You can also use the Headless Adaptive Forms Super Component, provided out-of-the-box, inside a react application to render a headless adaptive form. Headless adaptive forms super component makes use of OOTB react spectrum -based form components to render the Headless adaptive form. 

Core-Components: It enables use to render an Adaptive Form using JSON representation. It uses rule grammar to help create dynamic field interactions. The rule grammar is based on [JSON formula](http://github.com/adobe/json-formula/). You can develop your own renderer or embed the React based Adaptive Forms renderer, provided OOTB, in your front-end app to render the form. -->

**JSON Formula**: It is an implementation of form expression grammar. The grammar is a mashup of spreadsheet-like functions and operators and [JMESPath](https://jmespath.org/) a JSON query language.  It helps you query JSON representation and create rules for headless adaptive forms.  You can also use the [playground](https://opensource.adobe.com/json-formula/dist/index.html) to explore JSON formula syntax and capabilities.


## Artifacts available in beta release

In the journey to bring Adobe Experience Manager Headless Adaptive Forms to you, the following artifacts are available in the beta release:

<!-- ### React Renderer component -->


### AEM Forms as a Cloud Service Sandbox​

AEM Forms as a Cloud Service instance to help you create, store, and fetch Headless Adaptive Forms. It also helps provide prefill, server-side rule validation, and submit services for Headless adaptive forms.

### Forms Web SDK

Forms Web SDK provides the APIs to validate constraints applied to various fields of a form and hooks to connect JSON representation of form to the UI framework. It also provides     React Renderer​ for Headless Adaptive Forms to help integrate a Headless Adaptive Form to your application. The following components of Web SDK are available:

* **[@aemforms/forms-super-component](https://www.npmjs.com/package/@aemforms/forms-super-component)** 
* **[@aemforms/forms-react-core-components](https://www.npmjs.com/package/@aemforms/forms-react-core-components)**
* **[@aemforms/forms-core](https://www.npmjs.com/package/@aemforms/forms-core)**


#### Storybook

[Storybook](https://opensource.adobe.com/aem-forms-af-runtime/storybook/) provides an overview of different components of Headless Adaptive Forms. It also provides a list of all the supported components, their corresponding properties, and constraints.

### Forms Core Component  

<!-- Forms components are the structural elements that constitute the content of the form being authored. These components provide various form fields and ability to customize those fields. -->

Core Components are a set of standardized Web Content Management (WCM) components to help you speed up development time and reduce maintenance cost of your forms. The Forms Container component is a core component. It helps you embed and render a JSON Representation of Headless Adaptive Form on AEM Forms as a Clodu Service editor.  

### Adaptive Forms V2 Specifications

Headless Adaptive Forms specification provides a detailed information on all the components, constraints, and methods available for Headless Adaptive Forms. The specification is available in [PDF](/help/assets/Headless-Adaptive-Form-Specification.pdf) formats.

### HTTP and JS API

[HTTP APIs](https://opensource.adobe.com/aem-forms-af-runtime/api/) allow you to list, fetch, validate, submit, track submission status of headless forms.

[JS APIs](https://opensource.adobe.com/aem-forms-af-runtime/jsdocs/) helps you use Headless Adaptive Forms with any JavaScript based UI framework. 

### Visual Studio Code Plugin

[Visual Studio Code extension](/help/assets/adaptive-form-builder-0.10.0.vsix) to help create a valid JSON representation. It provides IntelliSense support and validation for JSON representation of forms.  

![JSON Form Model And Rendition](/help/assets/rendered-headless-form.png)