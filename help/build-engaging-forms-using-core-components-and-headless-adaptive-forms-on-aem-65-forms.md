---
title: Build Engaging Forms Using Core Components and Headless
seo-title: Build Engaging Forms Using Core Components and Headless
description: Build Engaging Forms Using Core Components and Headless
seo-description: Build Engaging Forms Using Core Components and Headless
topic-tags: develop
hide: yes
---

# Build Engaging Forms Using Core Components and Headless Adaptive Forms on AEM 6.5 Forms {#build-engaging-forms-using-core-components-and-headless}

## Lab Overview {#lab-overview}

In this hands-on lab, you learn:

How to use AEM Forms to easily create Adaptive Forms using the latest Core Components which are consistent with AEM Sites, enable omnichannel data capture experiences by delivering the Adaptive Forms as headless forms to web, mobile, and chat. You also learn best practices around styling, customizations, and front-end development.

## Key takeaways {#key-takeaways}

*   **Business Agility**: As a business user, I can author Form experience for multiple channels easily.

*   **Power to frontend developer**: As a frontend developer, I can control the end-user experience using headless forms.

*   **Developer Velocity**: As a developer, I can easily and consistently customize Sites and Forms components.

## Before you start {#pre-requisites}

To use this hands on lab:

*   Install the [latest release of Git](https://git-scm.com/downloads). If you are new to Git, see [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

*   Install [Node.js 16.13.0 or later](https://nodejs.org/en/download/). If you are new to Node.js, see [How to install Node.js](https://nodejs.dev/en/learn/how-to-install-nodejs).

*   [Enable Headless Adaptive Forms](enable-headless-adaptive-forms-and-core-components.md) on your AEM 6.5 Forms environment.

*   Install [Microsoft Visual Studio Code](https://code.visualstudio.com/download) or any plain text editor. Examples in document make use of Microsoft Visual Studio Code. 

## Lesson 1 {#lesson-1}

### Objective {#lesson-1-objectives}

Familiarize yourself with AEM 6.5 Forms environment.

### Lesson context {#lesson-1-context}

In this lesson, you familiarize yourself with AEM 6.5 Forms by navigating the user interface.

### Exercise {#lesson-1-excercise}

1.  Open your browser and enter the URL of the author environment. For example:
    [https://localhost:4502](https://localhost:4502).

1.  After you are logged in, navigate to the AEM Forms UI. Click **Forms**.

    ![](/help/assets/screenshot2028113829.png){width="50%" align="left"}

1.  Click **Forms & Documents**. Dismiss any pop-ups related to preferences or information.

    ![](/help/assets/screenshot2028113929.png){width="50%" align="left"}

    All the available forms are displayed.
    
    ![](/help/assets/screenshot2028114029.png){width="50%" align="left"}

## Lesson 2

### Objective

Author an Adaptive Form using the latest Core Components, configure, and submit the form.

### Lesson context

In this lesson, as a business user, you author an Adaptive Form for multiple channels like web, mobile, and chat using Adaptive Forms editor with standardized Out-of-the-box Core Components to capture data.

### Exercise

1.  Create a submission endpoint for the form:

    1.  Open <https://requestbin.com/> in a new browser tab.
        ![](/help/assets/screenshot2028114329.png){width="50%" align="left"}

    1.  Click **Create a public bin** and copy the endpoint URL.
        ![](/help/assets/screenshot202023-03-0120at206.10.0020pm.png){width="50%" align="left"}

    This example endpoint is to demonstrate the process of data submission. In an actual production environment, it is recommended that you use your own endpoint or submission method.
    
    This particular endpoint serves as an example for submitting and viewing data. In actual production, you use your own endpoint or data sources to store the captured data.  

1.  Author an Adaptive Form:

    1.  In the browser tab used in Lesson 1, navigate to AEM Forms web interface and navigate to **Forms** > **Forms and Documents**.

    1.  Click **Create** and select Adaptive Form.
        ![](/help/assets/creating-adaptive-form-6-5.png){width="50%" align="left"}

    1.  Select the **Blank with Core Components** template from the template selection screen as shown below and click **Next**.
    ![](/help/assets/creating-adaptive-form-6-5-select-blank-template.png){width="50%" align="left"}

    1.  Specify `Contact us` as the **Title** of the form. Ensure that the **Name** of the form is `contact-us`.
    ![](/help/assets/creating-adaptive-form-65-specify-title.png){width="50%" align="left"}

    1.  Click **Create**. A dialog box is displayed.
    
    1.  On the dialog box, click **Edit**. The form opens in Adaptive Form editor. Dismiss any pop-ups or dialogs for preferences or information.
   
    1.  Open the Components browser and drag and drop the Panel component to the middle of the screen.

        ![](/help/assets/lab65-add-panel.png){width="50%" align="left"} 

    1.  Drag and drop components from the Components browser to create a form, similar to the following:

        ![](/help/assets/contact-us-headless-adaptive-form.png){width="50%" align="left"}


    1.  Open the Content Browser, click Guide Container properties icon, and open the **Submission** tab. Select the **Submit to REST endpoint** Submit Action, select the **Enable POST request** option, and specify REST endpoint created in lesson 2 in the **URL for POST request** text box, and click the **Done** icon. 

        ![](/help/assets/configure-submit-action.png){width="50%" align="left"}
   
1.  Open AEM UI, navigate to **Forms** > **Forms & Documents**. Select the form created in previous step and click **Publish**. 

1.  On the Publish Assets dialog, click **Publish**. The success message is displayed.

## Lesson 3

### Objective

Update styles using frontend development best practices.

### Lesson context

In this lesson, as a front-end developer, you learn how you can update styling for the previously created Adaptive Form easily.

### Exercise

Set up local repository of the theme:

1.  Open the Command Prompt or shell with administrator rights:

    ![](/help/assets/screenshot2028115829.png){width="50%" align="left"}

1.  On the Command Prompt, use the following command to navigate to `c:\git` folder. 

    ```Shell

    cd git

    ```

    If the folder does not exist, use the `md git` command to create it.

1.  Use the following command to clone the theme frontend code:
    
    ```Shell
    
    git clone -b WKND https://github.com/adobe/aem-forms-theme-canvas

    ```

1.  Use the following command in the listed order to navigate to the **aem-forms-theme-canvas** directory and open Visual Studio Code.
    
    ```Shell
    
    cd aem-forms-theme-canvas
    code .

    ```
    
    ![](/help/assets/screenshot2028126029.png){width="50%" align="left"}

1.  Select **Trust the authors of all files in the parent folder** and click **Yes, I trust the authors**.

    ![](/help/assets/screenshot2028116229.png){width="50%" align="left"}

1.  Rename the `env_template` file to .env.  To rename the file, right click the **env_template** file and select the **Rename** option.

    ![](/help/assets/screenshot2028116429.png){width="30%" align="left"}

     </br>

    ![](/help/assets/screenshot2028116529.png){width="50%" align="left"}

1.  Set the following values for the variables in .env file and save the file:

    *   **AEM_URL**: Specify URL of a **publish** instance. For example, `https://localhost:4502/`
    
    *   **AEM_ADAPTIVE_FORM**: Specify the name of the form. For example, `contact-us`.

     </br>

    ![](/help/assets/lab65-theme-environment-variable.png)
    

1.  In the Command Prompt window, run the following command:

    ```Shell

    npm install

    ```

    ![](/help/assets/screenshot2028117029.png)

    >[!NOTE]
    >
    > * If you get a message asking to update npm via the `npm notice Run npm nstall -g npm@9.6.0`command, ignore the message.
    > * Do not run other npm commands unless instructed in the workbook.

1.  Now run the following command to preview the form.
    
    ```Shell
    
    npm run live
    
    ```
    
    ![](/help/assets/screenshot2028117229.png)

    Once the above command is executed, wait for the `webpack compiled` message. The form is displayed in a browser tab.

    >[!NOTE]
    >
    >If you experience a blank screen in browser after executing the `npm run live` command for more than 3-4 minutes, change `localhost` in browser URL to 127.0.0.1 and hit **Enter**. 

    
    ![](/help/assets/contact-us-headless-adaptive-form-with-canvas-theme.png){width="50%" align="left"}


1.  In Visual Studio Code, open the `PROJECT\src\site\_variables.scss` file. Notice the `$error` color is a shade of RED.

    ![](/help/assets/screenshot2028120729.png){width="50%" align="left"}

1.  In the browser, submit the form to see the Red color in the **First Name** field.

    ![](/help/assets/error-color-before.png)

1.  Set the **$error** color to **#5736eb** and save the file. 

1.  Refresh the browser and submit the form. Notice error color on the first name field has changed accordingly.
    
    ![](/help/assets/error-color-after.png)

1.  In the Command Prompt, press **CTRL+C**, enter **Y**, and press **Enter** key to terminate the npm process. It is important to stop the npm server so it does not conflict with the next set of exercises.
1.  Close Visual Studio Code and Command Prompt windows.

## Lesson 4

### Objective

Render the form to web/mobile and other interfaces as a headless form.

### Lesson context

In this lesson, as a frontend developer, you will learn how you can render the Adaptive Form created previously as a headless form using react spectrum design framework.

### Exercise

Setup local repository using react starter project:

1.  Open the Command Prompt using administrator rights.

    ![](/help/assets/screenshot2028115829.png){width="30%" align="left"}

1.  On the Command Prompt, use the following command to navigate to `c:\git` folder. 

    ```Shell

    cd git

    ```

1.  Use the following command to clone the Adaptive Form react starter project:
    
    ```Shell
    
    git clone https://github.com/adobe/react-starter-kit-aem-headless-forms

    ```
    
    ![](/help/assets/screenshot2028117329.png)

1.  Use the following commands in the listed order to navigate to the **react-starter-kit-aem-headless-forms** directory and open Visual Studio Code.

    ```Shell
    
    cd react-starter-kit-aem-headless-forms

    code .

    ```
    
    ![](/help/assets/screenshot2028117529.png)
    

    The Visual Studio Code window opens.

    ![](/help/assets/screenshot2028117429.png){width="50%" align="left"}

To render the form hosted on your publish environment:

1.  Rename the env_template file to .env file. To rename, right-click the **env_template** file and select the **Rename** option. 
    
    ![](/help/assets/screenshot2028117629.png){width="30%" align="left"}
    
    ![](/help/assets/screenshot2028117729.png)

1.  Set the following values for the variables in the .env file. After updating variables, save the file.

    *   **AEM_URL**: Specify the URL of the publish environment. For example, `https://localhost:4503/`

    *   **AEM_FORM_PATH**: Specify the path of the Adaptive Form created in the previous lesson. For example, `/content/forms/af/contact-us/`

    </br>

    ![](/help/assets/lab65-starter-kit-environment-variable.png)

1.  Open the command window, ensure you are at the **react-starter-kit-aem-headless-forms** directory, and run the following command:

    ```Shell
    
    npm install
    
    ```

    ![](/help/assets/screenshot2028118029.png)


1.  In the Command Prompt window, run the following command:
    
    ```Shell

    npm start
    
    ```

    ![](/help/assets/lab65-starter-kit-start.png)

    The above command starts a local development server which would render the form definition fetched from AEM in a headless way using the react-spectrum frontend library.

    >[!NOTE]
    >
    > 
    > If you experience a blank screen in browser after executing the `npm start` command for more than 3-4 minutes, change `localhost` in browser URL to 127.0.0.1 and hit **Enter**. 

    ![](/help/assets/headless-adaptive-form-lab.png)

Let's make changes on the form on the server as a business user and view changes reflected in the headless form automatically.

1.  Open the AEM Forms management interface in the browser. For example, [http://localhost:4502/aem/forms.html/content/dam/formsanddocuments](http://localhost:4502/aem/forms.html/content/dam/formsanddocuments).

1.  Select the **Contact Us** form and click **Edit.** It opens the form in the Adaptive Forms editor.


1.  Select the **Contact number** field and click the **Edit icon (Pencil icon)** in the toolbar. If you are not able to see the pop up toolbar, switch to Edit mode by clicking **Edit** button in top right, left to **Preview** button.

    ![](/help/assets/change-field-title.png){width="50%" align="left"}

1.  Change the label to **Mobile Number**. Click any empty space in the form and the changes made to the form are saved.

Let's publish the updated form to propagate the changes to publish environment.

1.  In the AEM Forms management interface tab, select the contact us form, and click **Unpublish**. If you do not see the **Unpublish** button, skip to step 3 to publish the changes directly.


1.  Click **Unpublish**. Click **Close** in respective dialog.
    
1.  After the browser refreshes, select the contact us form and click **Publish**.


1.  Click **Publish**. Click **Close** in the respective dialog.

1.  Refresh the browser tab with the headless form displayed. Notice, the Contact Number label has changed to Mobile number.

    ![](/help/assets/headless-adaptive-form.png)

1.  Open the Command Prompt window that is used to start the **react-starter-kit-aem-headless-forms** project, press **CTRL+C**, then
    enter **Y** and press Enter key to terminate the npm process. It is important to stop the npm server so it does not conflict with the next set of exercises.

1.  Close Visual Studio Code and Command Prompt windows.


## Lesson 5

### Objective

Render the form as a headless form using Google Material UI

### Lesson context

In this lesson, as a front-end developer, you learn how to render the Adaptive Form created previously as a headless form using Google Material UI.

### Exercise

Setup local repository using Material UI starter project:

1.  Open the Command Prompt using administrator rights.
    
    ![](/help/assets/screenshot2028115829.png){width="30%" align="left"}

1.  On the Command Prompt, use the following command to navigate to `c:\git` folder. 

    ```Shell

    cd git

    ```

1.  Run the following commands in the listed order to create a folder named mui and navigate to the mui folder using following commands: 

    ```Shell

    mkdir mui

    cd mui
    
    ```

1.  Use the following command to clone the Adaptive Form react starter project: 

    ```Shell

    git clone -b mui-lab https://github.com/adobe/react-starter-kit-aem-headless-forms

    ```

    ![](/help/assets/screenshot2028126529.png)

1.  Use the following command in the listed order to navigate to the **react-starter-kit-aem-headless-forms** folder and open the code in Visual Studio Code:

    ```Shell

    cd react-starter-kit-aem-headless-forms

    code .

    ```

    ![](/help/assets/screenshot2028126829.png)

To render the form hosted on your publish environment:

1.  Rename the **env_template** file to **.env** file. To rename, right-click the **env_template** file and select **Rename**.

    ![](/help/assets/screenshot2028126629.png){width="30%" align="left"}

1.  Set the following values for the variables in the .env file. After updating variables, save the file. Use the **CTRL + S** switch combination to save the file. 

    *   **AEM_URL**: Specify the URL of the publish environment. For example, [https://localhost:4503](https://localhost:4503)

    *   **AEM_FORM_PATH**: Specify the path of the Adaptive Form created in the previous lesson. For example, /content/forms/af/contact-us/


1.  Open the command window, ensure you are at the **react-starter-kit-aem-headless-forms** directory, and run the following command:

    ```Shell
    
    npm install
    
    ```

    ![](/help/assets/screenshot2028127029.png)

1.  In the Command Prompt window, run the following command:
    
    ```Shell

    npm start
    
    ```

    ![](/help/assets/lab65-mui-starter-kit-start.png)
    
    The command starts a local development server and renders the form definition fetched from AEM in a headless way using the Google Material UI frontend library.

    >[!NOTE]
    >
    >If you experience a blank screen in browser after executing the `npm start` command for more than 3-4 minutes, change `localhost` in browser URL to 127.0.0.1 and hit **Enter**. 

    ![](/help/assets/google-mui-form.png)

## Lesson 6

### Objective

Create an alternate look and feel of the headless form using Material UI component variations

### Lesson context

In this lesson, as a front-end developer, you learn how to create an alternate representation of different components using Material UI for the Adaptive Form created previously by the business user.

### Exercise

Update the variation of components in the headless project. To change the variant of the material UI text input component to `OutlinedInput`: 

1.  In Visual Code, navigate to the text input component by opening the `index.tsx` file at `src/components/textinput/index.tsx`.

1.  Add `//` at the beginning of the code line 104. It converts the line to a comment. 

    ```Shell

    //const Cmp = \'outlined\' === appliedCssClassNames ? OutlinedInput: Input;

    ```

1.  Add the following at line 105 to use a different variant of component and save the file. Use the **CTRL + S** switch combination to save the file. 

    ```Shell
    
    const Cmp = OutlinedInput;

    ```

    ![](/help/assets/aem65-lab-code-update.png)

    It is essential to use correct capitalization for 'OutlinedInput' variant else compilation would fail. The local development environment compilation begins automatically in Command Prompt. Wait until you see the following message

    `webpack 5.75.0 compiled with 3 warnings in 6659 ms` 
    `inside proxy req`
    `setting new origin header`

1.  Refresh the browser, if it does not refresh automatically, to see text input component use a different variant.

    ![](/help/assets/screenshot2028127729.png){width="50%" align="left"}

    
    This change happens for end users without any change to form definition at AEM Forms Server and is specific for the headless
    channel under consideration. For example, web channel in this lab.
    
    ![](/help/assets/aem65-lab-mui-style-update.png)


1.  Close Visual Studio Code and Command Prompt Windows.

## Frequently Asked Questions (FAQs)

+++ Are Core Components available publicly?  

Yes, Adaptive Forms Core Components are available with AEM 6.5 Forms and Forms as Cloud Service. You require AEM Forms 6.5 Service Pack 16 or later to use Adaptive Forms Core Components. 

+++

+++ Do Headless forms require a separate license?  

No, Headless forms use the same licensing value metric, number of form submissions.

+++




## Next steps

Now that you have learned how to build Adaptive Forms and deliver them to multiple channels using headless forms, you should try to put your new skills in action. Have fun and go ahead by creating and delivering exceptional data capture experiences to your end users, where they are, at scale!

## Resources

*   [Adaptive Form Core Components introduction](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html)

*   [Create Adaptive Form using Core Components](https://experienceleague.corp.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

*   [Update styling for core component-based AF](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html?lang=en)

*   [Headless Adaptive Forms](https://experienceleague.adobe.com/docs/experience-manager-headless-adaptive-forms/using/overview.html?lang=en)

*   [Using Headless React starter kit](https://experienceleague.adobe.com/docs/experience-manager-headless-adaptive-forms/using/get-started/create-and-publish-a-headless-form.html?lang=en)


