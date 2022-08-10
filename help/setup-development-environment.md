---
title: Set up development environment for AEM Headless Adaptive Forms
description: Set up development environment for AEM Headless Adaptive Forms
hide: yes
exl-id: fd92f057-1217-42f8-a454-1bc7e3827e01
---
# Setup development environment

You can set up development environment to create, test, and deploy headless forms. <!-- After a Headless Adaptive Form or related assets are ready on the local development environment, you can deploy the Headless Adaptive Form application to your publishing environment. -->

## Pre-requisites

You require knowledge to build application using react and the following software to set up a development environment. Download and configure these before starting to set up the local development environment:

<table>
    <tbody>
        <tr>
            <td>
                <p><strong>Software</strong></p>
            </td>
            <td>
                <p><strong>Description</strong></p>
            </td>
            <td>
                <p><strong>Supported Version</strong></p>
            </td>
            <td>
                <p><strong>Download links</strong></p>
            </td>
        </tr>
        <tr>
            <td>
                <p>Node.js</p>
            </td>
            <td>
                <p>Forms Web SDK required node.js to run</p>
            </td>
            <td>
                <p><span>16.13.0 or later</span></p>
            </td>
            <td>
                <p>Download from <a href="https://nodejs.org/">Node.js (nodejs.org)</a></p>
            </td>
        </tr>
        <tr>
            <td>
                <p>NPM (Node Package Manager)</p>
            </td>
            <td>
                <p>NPM is required to install Forms Web SDK packages</p>
            </td>
            <td>
                <p>8.x.x or later</span></p>
            </td>
            <td>
                <p>Installed along Node.js. No separate installation is required<span>.</span></p>
            </td>
        </tr>
        <tr>
            <td>
                <p>IDE (Integrated Development environment)</p>
            </td>
            <td>
                <p>You can use any IDE. Microsoft® Visual Studio Code was used for examples in this document.</p>
            </td>
            <td>
                <p>Visual Studio Code 1.62.0 or later</p>
            </td>
            <td>
                <p>Download and configure for your operating system: <a href="https://code.visualstudio.com/docs/setup/linux"> Linux®</a>, <a href="https://code.visualstudio.com/docs/setup/mac"> macOS </a>, or <a href="https://code.visualstudio.com/docs/setup/windows"> Windows.</a> </br></br>Note: To use Visual Studio from command line on macOS, see <a href="https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line"> Launching from the command line </a></p>
            </td>
        </tr>
        <tr>
            <td>
                <p>Adaptive forms builder extension for Visual Studio Code</p>
            </td>
            <td>  Provides IntelliSense and forms structure navigation capabilities to easily build and navigate JSON representation of a Headless Adaptive Form.
                <p> </p>
            </td>
            <td>
                <p></p>
            </td>
            <td>
                <p><a href="/help/assets/adaptive-form-builder-0.11.0.vsix">Adaptive forms builder extension</a></p>
            </td>
        </tr>
                <tr>
            <td>
                <p>Adobe Experience Manager as a Cloud Service SDK</p>
            </td>
            <td>
                <p>SDK includes [!DNL Adobe Experience Manager] QuickStart and Dispatcher tools</p>
            </td>
            <td> 2022.7.8005.20220711T194049Z-220600 or later
                <p></p>
            </td>
            <td> Download the SDK from <p><a href="https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-sdk-2022.7.8005.20220711T194049Z-220600.zip">Software Distribution</a></p>
            </td>
        </tr>
        <tr>
            <td>
                <p>Adobe Experience Manager Forms feature archive (AEM Forms add-on)</p>
            </td>
            <td >
                <p >Tools to create, style, and optimize Adaptive Forms and other Adobe Experience Manager Forms features</p>
            </td>
            <td >
                <p> aem-forms-addon-2022.07.06.02-220600 or later</p>
            </td>
            <td> Download from  <a href="https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-forms-addon-2022.07.06.02-220600.zip">Software Distribution</a> </p>
            </td>
        </tr>
        <tr>
            <td>
                <p>Apache Maven</p>
            </td>
            <td >
                <p >Open-source Java command-line tool used to build AEM Projects generated from the AEM Project Maven Archetype</p>
            </td>
            <td >
                <p>3.6 or later </p>
            </td>
            <td> See <a href="https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/development-tools.html?lang=en#install-maven">Set up development tools article</a> for instructions to download and install Maven</p>
            </td>
        </tr>
        <tr>
            <td>
                <p>Git </p>
            </td>
            <td >
                <p >Git is the source control management system used by Adobe Cloud Manager</p>
            </td>
            <td >
                <p></p>
            </td>
            <td> See <a href="https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/development-tools.html?lang=en#install-git">Set up development tools article</a> for instructions to download and install Git</p>
            </td>
        </tr>
    </tbody>
</table>

### Download the latest version of AEM as a Cloud Service SDK or Forms feature archive (AEM Forms add-on) from Software Distribution {#software-distribution}

To download the supported version of Adobe Experience Manager as a Cloud Service SDK or Forms feature archive (AEM Forms add-on):

1. Log in to [Software Distribution](https://experience.adobe.com/#/downloads) portal with your Adobe ID.

    >[!NOTE]
    >
    > Your Adobe Organization must be provisioned for AEM as a Cloud Service to download the AEM as a Cloud Service SDK.

1. Navigate to the **[!UICONTROL AEM as a Cloud Service]** tab.
1. Sort by published date in descending order.
1. Click on the latest Adobe Experience Manager as a Cloud Service SDK or Forms feature archive (AEM Forms add-on).
1. Review and accept the EULA. Tap the **[!UICONTROL Download]** button.

## Set up a local development environment and initial development project {#local-development-environment}

To set up a new local development environment and use it to develop Headless Adaptive Forms, [Setup local Author and Publish instances](#set-up-local-experience-manager-environment-for-development)

### Set up local Experience Manager environment for development

The Cloud Service SDK provides a QuickStart file. It runs a local version of Experience Manager. You can run both the Author and Publish instances locally.

<!-- While the QuickStart provides a local development experience, it does not have all features available in [!DNL Adobe Experience Manager] as a Cloud Service. So, always test your features and code with [!DNL Adobe Experience Manager] as a Cloud Service development environment before moving the features to stage or production. -->

To install and configure local Experience Manager environment, perform the following steps:

* [Download and extract](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html) the [!DNL Adobe Experience Manager] as a Cloud Service SDK
* [Set up an Author instance](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/aem-runtime.html?lang=en#set-up-local-aem-author-service).  When launching the SDK Quickstart, include the argument -r prerelease.
* [Set up a Publish instance](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/aem-runtime.html?lang=en#set-up-local-aem-publish-service). When launching the SDK Quickstart, include the argument -r prerelease.

### Add Forms archive to local Author and Publish instances and configure Forms-specific users {#add-forms-archive-configure-users}

Perform the following steps in the listed order to add Forms archive to Experience Manager instances and configure forms-specific users:

#### Install the latest Forms add-on feature archive {#add-forms-archive}

Adobe Experience Manager Forms as a Cloud Service feature archive provides tools to create Headless Adaptive Forms on the local development environment. To install the feature archive:

1. Download and extract the latest [!DNL AEM Forms] feature archive (AEM Forms add-on) from [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?fulltext=AEM*+Forms*+add*+on*&orderby=%40jcr%3Acontent%2Fjcr%3AlastModified&orderby.sort=desc&layout=list&p.offset=0&p.limit=20).

1. Navigate to the crx-quickstart/install directory. If the folder does not exist, create it.

1. Stop your AEM instance, place the [!DNL AEM Forms] add-on feature archive, `aem-forms-addon-<version>.far`,  in the install folder, and restart the instance.

#### Configure users and permissions {#configure-users-and-permissions}

Create users like Form Developer and Form Practitioner and [add these users to pre-defined forms groups](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/accessing/aem-users-groups-and-permissions.html?lang=en#accessing) to provide them required permissions. The table below lists all types of users and pre-defined groups for each type of forms users:
  
| User Type | AEM Group |
|---|---|
| Form developer | [!DNL forms-users] (AEM Forms Users), [!DNL template-authors], [!DNL workflow-users], [!DNL workflow-editors], and [!DNL fdm-authors]  |
| Customer Experience Lead or UX Designer| [!DNL forms-users], [!DNL template-authors]|
| AEM administrator | [!DNL aem-administrators], [!DNL fd-administrators] |
| End user| When a user must log in to view and submit an Adaptive Form, add such users to [!DNL forms-users] group. </br> When no user authentication is required to access Adaptive Forms, do not assign any group to such users.|

## Install Visual Studio Code extension for headless adaptive forms {#Install-Visual-Studio-Code-extension-for-headless-adaptive-forms}

The extension adds adaptive forms related IntelliSense capabilities to provide suggestions and auto-complete headless adaptive forms JSON syntax and also adds a panel to help navigate JSON representation of form. The navigation panel, titled Forms Tree, is helpful in navigating large JSON representations. To install the extension:

1. Download the [Adaptive forms builder extension](/help/assets/adaptive-form-builder-0.11.0.vsix).

1. Navigate the directory containing the *adaptive-form-builder-[version].vsix* file.

1. Run the following command or see [Install from a VSIX](https://code.visualstudio.com/docs/editor/extension-marketplace#_install-from-a-vsix) for detailed instructions to install a Visual Studio Code extension from a VSIX file:

    *code -–install-extension adaptive-form-builder-[version].vsix*

    </br> Replace the [version] with actual version of the extension. For example, adaptive-form-builder-1.0.0.vsix 

    </br> 

    ![Installing extension](/help/assets/install-extension.png)

, 
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
--> 
 Your environment is ready. You can proceed to create a Headless Adaptive Form.
