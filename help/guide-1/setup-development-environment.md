---
title: Setup development environment for AEM Headless Adaptive Forms
description: Setup development environment for AEM Headless Adaptive Forms
---

# Setup development environment

You can setup development environment to create, test, and deploy headless forms. After a Headless Adaptive Form or related assets are ready on the local development environment, you can deploy the Headless Adaptive Form application to your publishing environment.

## Prerequisites

You require knowledge to build application using react and the following software to set up a development environment.

<table>
    <tbody>
        <tr>
            <td style="width: 99.3pt;border: 1pt solid windowtext;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;text-align:center;'><strong>Software</strong></p>
            </td>
            <td style="width: 156.05pt;border-color: windowtext windowtext windowtext currentcolor;border-style: solid solid solid none;border-width: 1pt 1pt 1pt medium;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;text-align:center;'><strong>Description</strong></p>
            </td>
            <td style="width: 131.35pt;border-color: windowtext windowtext windowtext currentcolor;border-style: solid solid solid none;border-width: 1pt 1pt 1pt medium;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;text-align:center;'><strong>Supported Version</strong></p>
            </td>
            <td style="width: 152.8pt;border-color: windowtext windowtext windowtext currentcolor;border-style: solid solid solid none;border-width: 1pt 1pt 1pt medium;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;text-align:center;'><strong>Download links</strong></p>
            </td>
        </tr>
        <tr>
            <td style="width: 99.3pt;border-color: currentcolor windowtext windowtext;border-style: none solid solid;border-width: medium 1pt 1pt;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>Node.js</p>
            </td>
            <td style="width: 156.05pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>Forms Web SDK required node.js to run</p>
            </td>
            <td style="width: 131.35pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'><span style="color:#24292F;background:white;">16.13.0 or later</span></p>
            </td>
            <td style="width: 152.8pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>Download from <a href="https://nodejs.org/en/">Node.js (nodejs.org)</a></p>
            </td>
        </tr>
        <tr>
            <td style="width: 99.3pt;border-color: currentcolor windowtext windowtext;border-style: none solid solid;border-width: medium 1pt 1pt;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>NPM (Node package manager)</p>
            </td>
            <td style="width: 156.05pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>NPM is required to install Forms Web SDK packages</p>
            </td>
            <td style="width: 131.35pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'><span style="color:#24292F;background:white;">8.x.x or later</span></p>
            </td>
            <td style="width: 152.8pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>Installed along Node.js. No separate installation is required<span style="color:blue;text-decoration:underline;">.</span></p>
            </td>
        </tr>
        <tr>
            <td style="width: 99.3pt;border-color: currentcolor windowtext windowtext;border-style: none solid solid;border-width: medium 1pt 1pt;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>IDE (Integrated Development environment)</p>
            </td>
            <td style="width: 156.05pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>You can use any IDE. Microsoft Visual Studio Code was used for examples in this document.</p>
            </td>
            <td style="width: 131.35pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>NA</p>
            </td>
            <td style="width: 152.8pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'><a href="https://code.visualstudio.com/">Visual Studio Code - Code Editing. Redefined</a></p>
            </td>
        </tr>
        <tr>
            <td style="width: 99.3pt;border-color: currentcolor windowtext windowtext;border-style: none solid solid;border-width: medium 1pt 1pt;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>Adaptive forms builder extension for Visual Studio Code</p>
            </td>
            <td style="width: 156.05pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>&nbsp;</p>
            </td>
            <td style="width: 131.35pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>1.62.0 or later</p>
            </td>
            <td style="width: 152.8pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'><a href="/help/assets/adaptive-form-builder-0.11.0.vsix">Adaptive forms builder extension</a></p>
            </td>
        </tr>
                <tr>
            <td style="width: 99.3pt;border-color: currentcolor windowtext windowtext;border-style: none solid solid;border-width: medium 1pt 1pt;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>Local Developement environment for AEM Forms as a Cloud Service</p>
            </td>
            <td style="width: 156.05pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'>&nbsp;</p>
            </td>
            <td style="width: 131.35pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'></p>
            </td>
            <td style="width: 152.8pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin:0in;font-size:16px;font-family:"Adobe Clean",sans-serif;'><a href="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-environment/setup-local-development-environment.html?lang=en">Set up a local development environment and initial development project</a></p>
            </td>
        </tr>
    </tbody>
</table>

## Install Visual Studio Code extension for headless adaptive forms {#Install-Visual-Studio-Code-extension-for-headless-adaptive-forms}

The extension adds adaptive forms related IntelliSense capabilities to provide suggestions and auto-complete headless adaptive forms JSON syntax and also adds a panel to help navigate JSON representation of form. The navigation panel, titled Forms Tree, is helpful in navigating large JSON representations. To install the extension:

1. Download the [Adaptive forms builder extension](/help/assets/adaptive-form-builder-0.11.0.vsix).

1. Navigate the directory containing the *adaptive-form-builder-[version].vsix* file.

1. Run the following command:
*code –install-extension adaptive-form-builder-[version].vsix*

    Replace the [version] with actual version of the extension. For example, adaptive-form-builder-1.0.0.vsix

    ![Installing extension](/help/assets/install-extension.png)

<!-- ## Create and setup a react app

Adaptive forms renderer component is a react based component. It requires a react app to run and render a headless adaptive form. To create and setup react app:

1. Open terminal in Visual Studio code and run the following command to create a react app and installs all related dependencies:

    ```shell
    npx create-react-app [react-app-name] --scripts-version 4.0.3 --template typescript
    ```

    Where [react-app-name] represents name of the project, script version is 4.0.3, and template of type typescript. For example, the following command creates a react app named *headless-forms-demo*.

    ```shell
    npx create-react-app headless-forms-demo --scripts-version 4.0.3 --template typescript
    ```

    It may take some time to create the react app and install all the dependencies. The command creates an empty react app with latest version of react and react-dom dependencies. It does not have any artifacts related to adaptive forms renderer component.

1. Adaptive forms renderer component is based on react spectrum and requires react 16.0.0 and react-dom 16.0.0. To install react 16.0.0 and related dependencies:
    1. Open the Visual Studio code terminal Window or command prompt.
    1. Navigate to the directory of react project.  
    1. Run the following command:

        ```shell
        npm install --save react@16.0.0 react-dom@16.14.0 -force
        ```

1. Run the following command to install adaptive forms renderer component related dependencies:

    ```shell
    npm i --save @aemforms/forms-super-component @aemforms/forms-react-core-components @aemforms/forms-super-component @adobe/react-spectrum @react/react-spectrum
    ```


<!-- 1. Install dependencies for adaptive forms renderer component. Packages for these dependencies are available in Adobe Artifactory. To authenticate with Adobe Artifactory and install dependencies for adaptive forms renderer component:

    1. Create environment variables ARTIFACTORY_USER and ARTIFACTORY_API_TOKEN. The ARTIFACTORY_USER stores Adobe LDAP username and ARTIFACTORY_API_TOKEN stores your [Adobe Artifactory token](https://wiki.corp.adobe.com/display/Artifactory/API+Keys)

    1. Run the following command to set NPM_TOKEN and NPM_EMAIL tokens:

        ```shell

        auth=$(curl -s -u${ARTIFACTORY_USER}:${ARTIFACTORY_API_TOKEN} https://artifactory.corp.adobe.com/artifactory/api/npm/auth)
        export NPM_TOKEN=$(echo "${auth}" | grep "_auth" | awk -F " " '{ print $3 }')
        export NPM_EMAIL=$(echo "${auth}" | grep "email" | awk -F " " '{ print $3 }')
        ```

        These tokens are required to communicated with Adobe Artifactory.

    1. Create a .npmrc file in the react project.

        ![.npmrc file](/help/assets/npmrc.png)

    1. Add the following code to the file:

        ```shell
        @aemforms:registry=https://artifactory.corp.adobe.com/artifactory/api/npm/npm-aem-release/
        @react:registry=https://artifactory.corp.adobe.com/artifactory/api/npm/npm-react-release/
        @quarry:registry=https://artifactory.corp.adobe.com/artifactory/api/npm/npm-adobe-release-local/
        //artifactory.corp.adobe.com/artifactory/api/npm/npm-adobe-release-loca/:_auth=${NPM_TOKEN}
        //artifactory.corp.adobe.com/artifactory/api/npm/npm-aem-release/:_auth=${NPM_TOKEN}
        //artifactory.corp.adobe.com/artifactory/api/npm/npm-react-release/:_auth=${NPM_TOKEN}
        _auth=${NPM_TOKEN}
        email=${NPM_EMAIL}
        always-auth=true
        ```

        It defines the antifactory repositories to use for Headless Adaptive Forms, react, and quarry related scope.
    1. Run the following command to install adaptive forms renderer component related dependencies:

    ```shell
    npm i --save @aemforms/crispr-react-bindings @aemforms/crispr-react-core-components @adobe/react-spectrum @react/react-spectrum
    ``` 

 Your environment is ready. --> You can use the react app to embed and render an adaptive form.
