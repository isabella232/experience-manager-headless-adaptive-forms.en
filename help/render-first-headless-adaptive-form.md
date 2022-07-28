---
title: Create first headless adaptive form
description: Create first headless adaptive form
keywords: headless, adaptive form
hide: yes
exl-id: 99985fed-4a34-47d6-bb6f-79f81e1cd71b
---
# Create your first headless adaptive form

You can use Adobe Experience Manager Headless Adaptive Forms to build forms applications using front-end UI like React, Angular, Flutter, NPM, Vue.js, Ionic, Chakra UI, Bootstrap, and more and use  Forms Web SDK for capabilities like state management, validation, and integrations with various other touchpoints.

For example, an organization We.Org is looking to digitize their customer enrollment journey. Their developers are well versed at using Angular to build frontend solutions. They are looking to build a custom front end while offloading form validation and electronic signatures to specialized solutions.

Adobe Experience Manager Headless Adaptive Forms provides such organizations freedom to build forms using their existing expertise in frontend languages while providing support to use back-end capabilities to create enterprise class forms experience.

<!-- >>[!VIDEO](https://video.tv.adobe.com/v/341011/) -->

![Create a Headless Adaptive Form](/help/assets/headless-forms.png)

## Prerequisites

* Set up the [development environment](setup-development-environment.md) to enable you to create and test a Headless Adaptive Form.

## Use the archetype project to create a headless adaptive form

The archetype project is a maven-based template. It creates a minimal, best-practice based project to get started with headless adaptive forms. It includes Adaptive Form template, a sample-headless adaptive form JSON, Adaptive Forms Container core component, react components (Client library), Web SDK (Client library) for Headless Adaptive Forms to Forms as a Cloud Service and local development environments. It is mandatory to create and deploy the archetype 37 based project during the beta phase. Post-beta the project would be required only for customizations. 

Perform the following steps to create and render your first Headless Adaptive Form: 

1. [Create an AEM Archetype based project](#create-an-archetype-based-project)
1. [Create JSON representation of Headless Adaptive Form](#create-add-json-representation-of-headless-adaptive-forms)
1. [Add JSON representation to your AEM Archetype based project](#create-add-json-representation-of-headless-adaptive-forms)  
1. [Deploy the project to a local development environment](#deploy-the-project-to-a-local-development-environment)
1. [Use the Blank with core components template to create the Adaptive Form](#create-adaptive-form-with-blank-with-core-components-template)
1. [Configure the Adaptive Form to use the JSON representation](configure-adaptive-form-to-use-the-JSON-representation)

### Create an AEM Archetype based project {#create-an-archetype-based-project}  

Open the command prompt and run the below command to create an Experience Manager Forms as a Cloud Service project. Use archetype version 37 or later. If you are on Windows, run the following command with Administrative privileges (Run command prompt or bash shell as an administrator):   

    ```

    mvn -B org.apache.maven.plugins:maven-archetype-plugin:3.2.1:generate \
    -D archetypeGroupId=com.adobe.aem \
    -D archetypeArtifactId=aem-project-archetype \
    -D archetypeVersion=37 \
    -D appTitle=myheadlessform \
    -D appId=myheadlessform \
    -D groupId=com.myheadlessform \
    -D includeFormsheadless="y"  

    ```

Change the `appTitle`, `appId`, and `groupId` in the above command to reflect your environment.

* Use the `includeFormsenrollment=y` option to include Forms specific configurations, themes, templates, Core Components, and dependencies required to create Adaptive Forms. If you use Forms Portal, set the `includeExamples=y` option. It adds Forms Portal core components to the project.

* Use the `includeFormsheadless=y` option includes Forms Core Components and dependencies required to include Headless Adaptive Forms functionality. On enabling this option, the following are included:  
    * A template type Adaptive Form V2.
    * The **Blank with core components** template with [core components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=en). It is based on template type Adaptive Form V2.
    * A frontend react module, `ui.frontend.react.forms.af`. It helps you render headless adaptive form in a react app.  

### Create or add JSON representation of Headless Adaptive Form to your AEM Archetype based project {#create-add-json-representation-of-headless-adaptive-forms}

You can use **[Adaptive Forms builder extension for Visual Studio Code]** to build a JSON representation of your headless adaptive forms. You can see [Storybook](https://opensource.adobe.com/aem-forms-af-runtime/storybook/?path=/story/reference-examples--introduction) for sample JSON representations and list of components, attributes, and properties. You can also see the [specifications document](/help/assets/Headless-Adaptive-Form-Specification.pdf) for detailed information on all the components, constraints, and methods available to define Headless Adaptive Forms.

File extension of a JSON representation of Headless Adaptive Forms is schema.json. For example, formname.schema.json. Create or add the file to your AEM Archetype based project. For example, `\myheadlessform\ui.content\src\main\content\jcr_root\content\dam\myheadlessform\home-loan.schema.json`

### Deploy the project to a local development environment {#deploy-the-project-to-a-local-development-environment}

You can deploy the project to local development environment. It adds headless adaptive forms functionality, the **Blank with core components** template, JSON representation of form, and other resources included in the project to your development environment. <!-- Deploy the project to your local development environment to locally create headless adaptive forms. or deploy directly to your Forms as a Cloud Service environment. !--> To deploy to your local development environment, use the following command: 

    `mvn -PautoInstallPackage clean install`

If you are on Windows, run the above with Administrative privileges (Run command prompt or [bash shell as an administrator](https://khushwantsehgal.wordpress.com/2022/06/29/check-if-git-bash-is-running-in-administrator-mode/)). For the complete list of commands, see [Building and Installing](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html?lang=en#building-and-installing).
    
<!-- *  To learn how to deploy code to AEM as a Cloud Service, see the video in [Deploying to AEM as a Cloud Service]https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/overview.html?lang=en#coding-against-the-right-aem-version) article : -->

### Create an Adaptive Form based on the Blank with core components template {#create-adaptive-form-with-blank-with-core-components-template}

1. Log in to your [local](http://localhost:4502/) <!-- or Forms as a Cloud Service --> development environment.

1. After you are logged in, in the upper-left corner, tap Adobe Experience Manager > Forms > Forms & Documents.  

1. Create a folder and upload JSON representation of your headless adaptive form to it.

    >[!NOTE]
    >
    >File extension of a JSON representation of Headless Adaptive Forms is schema.json. For example, formname.schema.json

1. Tap Create and select Adaptive Form. Select the **Blank with core components** template and tap Create.

1. An option to Add Properties appears. Specify the values for following property fields. The Title and Name fields are mandatory:

   * **Title**: Specifies the display name of the form. The title helps you identify the form in the Experience Manager Forms user interface.
   * **Name**: Specifies the name of the form. A node with the specified name is created in the repository. As you start typing a title, value for the name field is automatically generated. You can change the suggested value. The name field can include only alphanumeric characters, hyphens, and underscores. All the invalid inputs are replaced with a hyphen.

1. Tap Create. An Adaptive Form is created.

### Configure the Adaptive Form to use the JSON representation {#configure-adaptive-form-to-use-the-JSON-representation}

Open the form created in the previous section for editing. When you open the form for editing, it  displays the sidebar to customize the newly created form. To configure the Adaptive Form to use the JSON representation:

1. Tap the Adaptive Forms Container component and Tap Properties. It displays properties explorer in the sidebar.

1. In the properties explorer, expand the BASIC accordion, and specify path of the JSON representation uploaded in a previous step for the Forms Runtime Document Path option. The container component displays a rendition of the form.

1. In the properties explorer, expand the SUBMISSION accordion and set a Submit Action for the adaptive form. Your form is ready to be used in a react app.

1. To render the form, hosted on your local development machine:

    1. Open the `[Archetype project]\ui.frontend.react.forms.af\.env` file and set the path of form. For example, /content/forms/af/contact

    1. Open the command prompt and navigate to the ui.frontend.react.forms.af project and run the following command:

        `npm run start`

    1. After the completion, open the localhost:3000 in your browser window to view rendered Headless Adaptive Form. 
    1. To test the submission functionality, login to your AEM Forms Server, and use the **Preview the form in HTML** option to open the form in preview mode. 

The [Storybook provides  a list of components and rules that can be set on various Headless Adaptive Forms along with some example of JSON representation of Headless Adaptive Forms. You can also look at [specifications](/help/assets/Headless-Adaptive-Form-Specification.pdf) document to learn about various rules and properties related to Headless Adaptive Forms.
