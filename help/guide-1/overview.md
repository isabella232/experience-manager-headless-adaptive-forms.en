---
title: AEM Headless Adaptive Forms Overview
description: Overview for AEM Headless Adaptive Forms.
---

# Headless Adaptive Forms Overview

Adobe Experience Manager Headless Adaptive Forms is an API-first form builder platform for developers and business users. You can use Headless Adaptive Forms to build and natively render a form in any website, an application, or email. You can also use Headless Adaptive Forms to build custom data capture experiences for voice based or non-visual interactions. Headless Adaptive Forms provide the flexibility to render the forms for any channel in an optimal way. For example, a React app, any  SPA (Single Page Application), or a native mobile app. This helps improve the enrollment experience for customers leading to better conversion. Headless adaptive forms includes:

* Multi-channel forms with a single source of truth to easily manage and update forms.
* Channel agnostic JSON representation of forms for easy consumption in any application.
* RESTful APIs to list, fetch, validate, submit, track submission status of headless forms.
* Web SDK to natively render a headless adaptive form in a website or web application.
* Rule grammer to build dynamic forms and validations.
* Visual Studio Code extension to help create a valid JSON representation.  

![Build and natively render a form in any website, an application, or non-visual inteactions](/help/assets/headless-forms-for-any-device.jpg)

Headless Adaptive Forms are for everyone. However, at the beta stage, we expect developers and designers familiar with modern JavaScript frameworks to use the Headless Adaptive Forms. Developers can leverage their existing expertise in frontend languages like React to build beautiful enterprise class form experiences.

## Why use Adobe Experience Manager Headless Adaptive Forms?

Our headless forms are based on an open-specification (JSON representation of form and Rules grammar) developed by Adobe and provide native SDKs to manage form state, validate form content, and connect a form to a UI framework of your choice, providing you freedom to concentrate on building great user experiences while leaving complex backend tasks on Adobe. You have freedom to develop your own components to render a form using any UI framework or programming language or use OOTB react components to render a form. Along with the specification, Headless Adaptive Forms would add the following user-friendly backend tools and services for complex tasks as beta progresses:

* Visual editor to easily develop a Headless Adaptive Forms.
* Workflow engine to automate complex tasks.
* Support to generate Document of Record automatically and on-demand.
* HTTP APIs to invoke a business logic.
* Forms Data Model to receive or send data to disparate data sources.
* Pre-filling a form based on user-profile or available data.

![JSON Form Model And Rendition](/help/assets/rendered-headless-form.png)

## How Headless Adaptive Form work?

A Headless Adaptive Form is essentially a JSON representation (Schema) complete with fields (Text box, choices, and many more fields) and corresponding rules (Conditional logic) to add dynamism to the form. You can use REST APIs in your application or website to request the hosted schema and natively render the schema as a form in your app or website. A schema can serve multiple webpages and applications without making any app or website specific changes to it.

![How Headless Adaptive Form works](/help/assets/how-headless-adaprive-forms-work.png)

You can use React component shipped with Headless Adaptive Forms to render an Adaptive Form or build your own custom component to natively render a Headless Form in a Website or an application or use any UI framework or programming language to build your own components to render your forms.

## How to join the beta program?

You can send an email to headless-af-beta@adobe.com from your official email ID to join the beta program.



## Frequently asked questions (FAQ) {#headless-adaptive-forms-faq}

**Should I know React.js to use Headless Adaptive Forms?**
You can use any framework, library, or language to render Headless Adaptive Forms and use our REST APIs to validate and submit the forms. Web SDK and React component provided out of the box are for your convenience. You can develop your own components and are not limited to use these.

**Where is captured data stored?**

The data is handed to the configured REST endpoint. You can also configure a Form Data Model (FDM) to receive or send data to disparate data sources (FDM feature would be available in a subsequent beta release.)

**Is Headless Adaptive Forms HIPPA complaint?**





