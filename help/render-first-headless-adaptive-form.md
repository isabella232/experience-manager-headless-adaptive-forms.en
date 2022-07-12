---
title: Create first headless adaptive form
description: Create first headless adaptive form
keywords: headless, adaptive form
hide: yes
---

# Create your first headless adaptive form

You can use Adobe Experience Manager Headless Adaptive Forms to build forms applications using front-end UI like React, Angular, Flutter, NPM, Vue.js, Ionic, Chakra UI, Bootstrap, and more and use  Forms Web SDK for capabilities like state management, validation, and integrations with various other touchpoints.

For example, an organization We.Org is looking to digitize their customer enrollment journey. Their developers are well versed at using Angular to build frontend solutions. They are looking to build a custom front end while offloading form validation and electronic signatures to specialized solutions.

Adobe Experience Manager Headless Adaptive Forms provides such organizations freedom to build forms using their existing expertise in frontend languages while providing support to use back-end capabilities to create enterprise class forms experience.

<!-- >>[!VIDEO](https://video.tv.adobe.com/v/341011/) -->

![Create a Headless Adaptive Form](/help/assets/headless-forms.png)

## Prerequisites

* Set up the [development environment](setup-development-environment.md)
* [JSON representation](https://opensource.adobe.com/aem-forms-af-runtime/storybook/) of your headless adaptive forms.

## Use the archetype project to create a headless adaptive form

The archetype project is a maven-based template. It creates a miminal, best-practice based project to get started with headless adaptive forms. It includes Adaptive Form template, a sample headless adaptive form JSON, Adaptive Forms Container core component, react components (Client library), Web SDK (Client library) for headless adaptive forms to Forms as a Cloud Service and local development environments.

It is mandatory to create and deploy the archetype 37 based project during the beta phase. Post-beta the project would be required only for customizations. To create and deploy the project:  

1. Open the command prompt and run the below command to create an Experience Manager Forms as a Cloud Service project. Use archetype version 37 or later. If you are on Windows, run the following command with Administrative privileges (Run command prompt or bash shell as an administrator):   

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
        * A blank template with [core components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=en). It is based on template type Adaptive Form V2.
        * A frontend react module, `ui.frontend.react.forms.af`. It helps you render headless adaptive form in a react app.  

1. Deploy the project to your local development environment to locally create headless adaptive forms. <!-- or deploy directly to your Forms as a Cloud Service environment. !--> To deploy to your local development environment, use the following command: 

        `mvn -PautoInstallPackage clean install`

    If you are on Windows, run the following command with Administrative privileges (Run command prompt or [bash shell as an administrator](https://khushwantsehgal.wordpress.com/2022/06/29/check-if-git-bash-is-running-in-administrator-mode/)). For the complete list of commands, see [Building and Installing](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html?lang=en#building-and-installing).
    
    <!-- *  To learn how to deploy code to AEM as a Cloud Service, see the video in [Deploying to AEM as a Cloud Service]https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/overview.html?lang=en#coding-against-the-right-aem-version) article : -->

    <br>It deploys the blank template and other resources included in the project to your development environment.

1. To create a Headless Adaptive Form:

    1. Log in to your [local](http://localhost:4502/) <!-- or Forms as a Cloud Service --> development environment.

    1. After you are logged in, in the upper-left corner, tap Adobe Experience Manager > Forms > Forms & Documents.  

    1. Create a folder and upload JSON representation(schema.json) of your headless adaptive form to it.

    1. Tap Create and select Adaptive Form. Select the Blank template and tap Create.

    1. An option to Add Properties appears. Specify the values for following property fields. The Title and Name fields are mandatory:

        * **Title**: Specifies the display name of the form. The title helps you identify the form in the Experience Manager Forms user interface.
        * **Name**: Specifies the name of the form. A node with the specified name is created in the repository. As you start typing a title, value for the name field is automatically generated. You can change the suggested value. The name field can include only alphanumeric characters, hyphens, and underscores. All the invalid inputs are replaced with a hyphen.

    1. Tap Create. An Adaptive Form is created.

    1. The form opens for editing and displays the contents available in the template. It also displays the sidebar to customize the newly created form according to the needs.

    1. Tap the Adaptive Forms Container component and Tap Properties. It displays properties explorer in the sidebar.

    1. In the properties explorer, expand the BASIC accordion, and specify path of the JSON representation uploaded in a previous step for the Forms Runtime Document Path option. The container component displays a rendition of the form.

    1. In the properties explorer, expand the SUBMISSION accordion and set a Submit Action for the adaptive form. Your form is ready to be used in a react app.

    1. To render the form, hosted on your local development machine:
    
          1. Open the `[Archetype project]\ui.frontend.react.forms.af\.env` file and set the path of form. For example, /content/forms/af/contact

          1. Open the command prompt and navigate to the ui.frontend.react.forms.af project and run the following command:

            `npm run start`
        
    It opens the rendered headless adaptive form in your browser Window. To test the submission functionality, login to your AEM Forms server, and open the form in preview mode. 

    You can take a look at [Storybook](https://opensource.adobe.com/aem-forms-af-runtime/storybook/) to learn about the various components and rules that can be set on various Headless Adaptive Forms along with some example of JSON representation of Headless Adaptive Forms. You can also take a look at [specifications](/help/assets/Headless-Adaptive-Form-Specification.pdf) document to learn about various rules and properties related to Headless Adaptive Forms.
