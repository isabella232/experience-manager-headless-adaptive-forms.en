---
title: Create first headless adaptive form
description: Create first headless adaptive form
keywords: headless, adaptive form
---

# Render your first headless adaptive form

You can use Adobe Experience Manager Headless Adaptive Forms to build forms applications using front-end UI like React, Angular, Flutter, NPM, Vue.js, Ionic, Chakra UI, BootStrap, and more and use  Forms Web SDK for capabilities like state management, validation and integrations with various other touchpoints.

For example, an organization We.Org is looking to digitize their customer enrollment journey. Their developers are well versed at using Angular to build frontend solutions. They are looking to build a custom front-end while offloading form validation and electronic signatures to specialized solutions.

Adobe Experience Manager Headless Adaptive Forms provides such organizations freedom to build forms using their existing expertise in frontend languages while providing support to use back-end capabilities to create enterprise class forms experience.

>[!VIDEO](https://adobe-my.sharepoint.com/personal/macman_adobe_com/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fmacman%5Fadobe%5Fcom%2FDocuments%2FRecordings%2FDemo%20recording%20for%20Headless%20AF%2D20220309%5F150858%2DMeeting%20Recording%2Emp4&parent=%2Fpersonal%2Fmacman%5Fadobe%5Fcom%2FDocuments%2FRecordings)

## Prerequisites

* Setup the [development environment](setup-development-environment.md)

* [JSON representation](https://git.corp.adobe.com/pages/livecycle/af2-web-runtime/story/?path=/story/crispr-introduction--page) of the headless adaptive form.

## Render a headless adaptive form

To create a headless adaptive form:

1. Open the react project in your IDE. This procedure assumes you are using Visual Studio code.

1. Create a file with .form.json extension and add the JSON representation code to it. For example, demo.form.json

1. Open the boilerplate, the App.tsx file, in the react app.

1. Remove the `<header>` tag and code in it.

1. Add the `<Spectrum3Provider>` and adaptive form mappings to the App.tsx file. For the [contact us](https://git.corp.adobe.com/pages/livecycle/af2-web-runtime/story/?path=/story/crispr-introduction--page) form example in storybook, the code look like the following:

    ```JavaScript  

    import React from 'react';
    import logo from './logo.svg';
    import './App.css';
    import { Provider as Spectrum3Provider, defaultTheme } from '@adobe/react-spectrum'
    import {mappings} from '@aemforms/forms-react-components'
    import {AdaptiveForm} from '@aemforms/forms-super-component';

    function App() {
    return (
        <div className="App">
        <Spectrum3Provider theme={defaultTheme}>
            <AdaptiveForm mappings={mappings} formJson={json}
        </Spectrum3Provider>

        </div>
    );
    }

    export default App;
    ```

1. To run the react application and render the form, run the following command:

    ```Shell
    
    npm run start

    ```

The adaptive form opens in a new browser window. For examples of headless adaptive forms, see:

* [Storybook](https://git.corp.adobe.com/pages/livecycle/af2-web-runtime/story/?path=/story/crispr-introduction--page).

* [API Specifications](https://git.corp.adobe.com/pages/livecycle/af2-docs/spec/latest/internal/#_appendix_b_implementation_and_examples)
