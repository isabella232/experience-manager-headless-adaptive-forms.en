---
title: AEM Headless Adaptive Forms Overview
description: Overview for AEM Headless Adaptive Forms.
hide: yes
exl-id: 3b5b955b-d59c-43d9-9cc4-3244a08f80dc
---
# Headless Adaptive Forms Overview

Adobe Experience Manager Headless Adaptive Forms is an API-first form builder platform for developers and business users. You can use Headless Adaptive Forms to build and natively render a form in any website or application. <!-- You can also use Headless Adaptive Forms to build custom data capture experiences for voice based or non-visual interactions. --> Headless Adaptive Forms provide the flexibility to render the forms for any channel in an optimal way. For example, a React app, any  SPA (Single Page Application), or a native mobile app. It helps improve the enrolment experience for customers leading to better conversion. Headless Adaptive Forms includes:

* Omni-channel forms with a single source of truth to easily manage and update forms
* Channel agnostic JSON structure of forms for easy consumption in any application
* RESTful APIs to list, fetch, validate, submit, track submission status of headless forms
* Web SDK to natively render a headless adaptive form in a website or web application
* Rule grammar to build dynamic forms and validations
* Adaptive Forms Visual Studio Code extension to help create a valid JSON structure

<!-- ![Build and natively render a form in any website, an application, or non-visual inteactions](/help/assets/headless-forms-for-any-device.jpg) -->

At the beta stage, we expect front end developers familiar with modern JavaScript frameworks to use the Headless Adaptive Forms. Developers can leverage their existing expertise in frontend languages like React to create build beautiful enterprise class data capture experiences.

## Why use Adobe Experience Manager Headless Adaptive Forms?

Headless Adaptive Forms are based on an [Adaptive Forms V2 specification](/help/assets/Headless-Adaptive-Form-Specification.pdf) (JSON structure of form and Rules grammar) developed by Adobe and provide native SDKs to manage form state, validate form content, and connect a form to a UI framework of your choice, providing you freedom to concentrate on building great user experiences while leaving complex backend tasks to Adobe. You have the freedom to develop your own components to render a form using any UI framework or programming language or use OOTB react components to render a form. Along with the specification, Headless Adaptive Forms would add the following user-friendly backend tools and services for complex tasks as beta progresses:

* Visual editor to easily develop a Headless Adaptive Forms.
* Workflow engine to automate complex tasks.
* Support to generate Document of Record automatically and on-demand.
* HTTP APIs to invoke a business logic.
* Forms Data Model to receive or send data to disparate data sources.
* Pre-filling a form based on user-profile or available data.

![JSON Form Model And Rendition](/help/assets/rendered-headless-form.png)

## How Headless Adaptive Form works?

A Headless Adaptive Form is essentially a JSON structure (schema) consisting form fields (Text box, choices, and many more fields) and corresponding rules (conditional logic) to add interactive behaviour to the form. You can use REST APIs in your application or website to request the hosted JSON structure and natively render the JSON structure as a form in your app or website. A single headless adapive form can serve multiple webpages and applications without making any app or website specific changes to it.

![How Headless Adaptive Form works](/help/assets/how-headless-adaprive-forms-work.png)

You can use forms react renderer component shipped with Headless Adaptive Forms to render an Adaptive Form or build your own custom component to natively render a Headless Form in a website or an application or use any UI framework or programming language to build your own components to render your forms.

The following diagram describes the typical workflow of creating, deploying, and using Headless Adaptive Form components in your application or website:

![How Headless Adaptive Form works](/help/assets/artifacts.png)

## How to join the beta program?

You can send an email to afforms-headless_beta@adobe.com from your official email ID to join the beta program.
