---
title: Headless adaptive forms architecture
description: Headless adaptive forms architecture
keywords: headless, adaptive form, architecture
hide: yes
exl-id: ee7096d8-89e2-41e0-85e7-b26457df96fb
---

# How Headless adaptive form works?

A Headless adaptive form is essentially a JSON structure (schema) consisting form fields (Text box, choices, and many more fields) and corresponding rules (conditional logic) to add interactive behavior to the form. You can use REST APIs in your application or website to request the hosted JSON structure and natively render the JSON structure as a form in your app or website. A single Headless adaptive form can serve multiple webpages and applications without making any app or website-specific changes to it.

![How Headless adaptive form works](/help/assets/how-headless-adaprive-forms-work.png)

## Architecture {#architecture}

A typical Headless adaptive forms architecture constitutes an Adobe Experience Manager Forms Server, Headless adaptive forms hosted on Adobe Experience Manager Forms Server, and your frontend apps (Website, mobile application, JavaScript apps, chat applications, and more) for channel-specific form renditions.

Typical architecture of a Headless adaptive forms deployment looks like the following:

![Architecture](/help/assets/headless-af-architecture.png)

<!-- 

You can use the React renderer component shipped with Headless adaptive forms to render an Adaptive Form or build your own custom component to natively render a Headless Form in a website or an application or use any UI framework or programming language to build your own components to render your forms.

A typical Headless adaptive forms architecture constitutes an Adobe Experience Manager Server, JSON structure of forms, various frontend apps for channel-specific form renditions.

![Architecture](/help/assets/headless-af-architecture.png) -->

### Component of a Headless adaptive forms implementation

**Adobe Experience Manager Server**: Along with serving as host for Headless adaptive forms, Adobe Experience Manager provides the following backend capabilities:  

* RESTful APIs to list, fetch, pre-fill, validate, submit, track submission status of headless forms.
* Visual editor to easily develop a Headless adaptive forms.
* Forms Data Model to receive or send data to disparate data sources.
* Workflow engine to automate complex tasks.

**Headless adaptive forms**: A Headless adaptive form is represented as a .json file. The JSON structure defines components, constraints, and structure of a form.

**Front-end Apps**: Front-end apps like, SPA (Single Page Applications), Mobile Apps, JavaScript Apps, consume Headless adaptive forms (the JSON Form Representation) and render the form on a client. You can use the React renderer component shipped with Headless adaptive forms to render an Adaptive Form or build your own custom component to natively render Headless adaptive forms.

<!-- ### Understanding Headless adaptive forms definition --> 



### Developer tools

In a typical development cycle, you start with creating and hosting Headless adaptive forms on Adobe Experience Manager Forms Server. In the second step, you map your UI components or use a public UI components library, such as Google Material UI or Chakra UI to style your forms. In the last step, you fetch and display Headless adaptive forms in your application (Website, mobile application, JavaScript apps, chat applications, or many other surfaces).  

The following tools help you create and integrate Headless adaptive forms to your applications:

**Forms Web SDK (Client-Side Runtime)**: Forms Web SDK is a client-side JavaScript library. It allows you to apply client-side validations on form fields, maintain state of the form, and provides hooks to connect form with UI layer or adaptive forms rendered component. It allows customers to validate constrains applied to various fields of a form and hooks to connect JSON structure of form to the UI framework. The Forms Web SDK has the following components:

* **Business rule processor**: The business rule processor accepts the forms JSON structure as input, manages the state of the form fields, executes rules, and event handlers present in the JSON.
* **React binder**: Provides hooks over controller to add state to Form Components. It is also helpful in pre-filling a form.
* **Components library**: It provides React Spectrum Components and uses hooks in React Binder module to add state to those components.

Along with providing the APIs to validate constraints applied to various fields of a form, Forms Web SDK provides hooks to connect Headless adaptive forms to the UI framework. It also provides React Renderer​ for Headless adaptive forms to help integrate a Headless adaptive form to your application. The following components of Web SDK are available:

* **[@aemforms/af-react-components](https://www.npmjs.com/package/@aemforms/af-react-components)** 
* **[@aemforms/af-react-renderer](https://www.npmjs.com/package/@aemforms/af-react-renderer)**
* **[@aemforms/af-core](https://www.npmjs.com/package/@aemforms/af-core)**

All of these components are included in AEM Archetype. When you create an AEM Archetype 37 or later project for Headless adaptive forms, the latest version of above listed libraries is included in the project.

**Started Application**: Adobe has also released a started application to help you start quickly with Headless adaptive forms.

<!-- **View Library (UI Layer)**: A custom form application built in a front-end language. You can use react, Angular, Flutter, NPM, Vue.js, Ionic, BootStrap, or any other language to built front end. You can also use the Headless adaptive forms Super Component, provided out-of-the-box, inside a react application to render a Headless adaptive form. Headless adaptive forms super component makes use of OOTB react spectrum -based form components to render the Headless adaptive form. 

Core-Components: It enables use to render an Adaptive Form using JSON structure. It uses rule grammar to help create dynamic field interactions. The rule grammar is based on [JSON formula](http://github.com/adobe/json-formula/). You can develop your own renderer or embed the React based Adaptive Forms renderer, provided OOTB, in your front-end app to render the form. -->

**Storybook**: [Storybook](https://opensource.adobe.com/aem-forms-af-runtime/storybook/) provides an overview of different components of Headless adaptive forms. It also provides a list of all the supported components, their corresponding properties, and constraints.

**Visual Studio Code Extension**: [Visual Studio Code extension](visual-studio-code-extension-for-headless-adaptive-forms.md) to help create a valid JSON structure. It provides IntelliSense support and validation for JSON structure of forms along with common functions like add, delete, or rename components of a JSON structure.

**Adaptive Forms version 2.0 specifications**: Adaptive Forms version 2.0 specification provides a detailed information on all the components, constraints, and methods available to define Headless adaptive forms. The specification is available in [PDF](/help/assets/Headless-Adaptive-Form-Specification.pdf) format.

**HTTP and JavaScript APIs**: [HTTP APIs](https://opensource.adobe.com/aem-forms-af-runtime/api/) allow you to list, fetch, validate, submit, track submission status of headless forms. [JS APIs](https://opensource.adobe.com/aem-forms-af-runtime/jsdocs/) helps you use Headless adaptive forms with any JavaScript based UI framework. 

**JSON Formula**: It is an implementation of forms expression grammar to helps you query JSON structure and create rules for Headless adaptive forms. The grammar is a mashup of spreadsheet-like functions and operators and [JMESPath](https://jmespath.org/) a JSON query language. You can use the [playground](https://opensource.adobe.com/json-formula/dist/index.html) to explore JSON formula syntax and capabilities.