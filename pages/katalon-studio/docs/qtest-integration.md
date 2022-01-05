---
title: "qTest Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/qtest-integration.html
redirect_from:
    - "/katalon-studio/docs/enable-qtest-integration.html"
    - "/display/KD/Enable+qTest+Integration/"
    - "/display/KD/Enable%20qTest%20Integration/"
    - "/x/m4Ew/"
    - "/katalon-studio/docs/enable-qtest-integration/"
    - "/display/KD/qTest+Integration/"
    - "/katalon-studio/docs/integrate-test-case.html"
    - "/display/KD/Integrate+test+case/"
    - "/display/KD/Integrate%20test%20case/"
    - "/x/ooEw/"
    - "/katalon-studio/docs/integrate-test-case/"
    - "/katalon-studio/docs/integrate-test-suite.html"
    - "/display/KD/Integrate+test+suite/"
    - "/display/KD/Integrate%20test%20suite/"
    - "/x/x4Ew/"
    - "/katalon-studio/docs/integrate-test-suite/"
    - "/katalon-studio/docs/upload-test-execution.html"
    - "/display/KD/Upload+test+execution/"
    - "/display/KD/Upload%20test%20execution/"
    - "/x/5YEw/"
    - "/katalon-studio/docs/upload-test-execution/"
description:
---

> Requirements:
> * Katalon Studio version 7.0.1 onwards.
> * An active Katalon Studio Enterprise license. To learn more about activating your Katalon Studio license, you can refer to this document: [Activate Katalon license](https://docs.katalon.com/katalon-studio/docs/activate-license.html#activate-a-license-with-internet-access).

## Install the qTest Integration plugin

To download and install the **qTest Integration** plugin, you can go to the Katalon Store here: [qTest Integration](https://store.katalon.com/product/136/qTest-Integration). 

To activate the installed plugin, navigate to Account Settings in Katalon Studio and click **Reload Plugin**.
If you want to use the plugin in console mode, refer to this document: [Use Plugins in Console Mode](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#use-plugins-in-console-mode).

## Enable qTest integration

1. Open the qTest integration settings:

* For Katalon version 7.5.5 onwards: Go to **Project > Settings > Plugins > qTest**
* For versions older than 7.5.5: Go to **Project > Settings > Integration > qTest**

2. Check the **Enable integration** checkbox. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-QTEST-Enable-qTest-integration.png" width=85% alt="Enable qTest integration">

## Configure qTest integration

> Notes:
> * From version 7.9.0 onwards, Katalon Studio supports pushing screenshots (PNG files) to qTest to generate reports.

You can configure qTest integration manually or with the Setup Wizard as follows:

<details><summary>Setup Wizard</summary>

To open the setup wizard, after checking the **Enable Integration** box, click **Yes** in the pop-up window. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-QTEST-Wizard-tour.png" width=85% alt="The Wizard Setup box">

Alternatively, you can also click on the **Quick Setup...** hyperlink.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-6-29-163A493A31.png" width=70% alt="The Wizard Setup hyperlink">

In the displayed **qTest Integration Setup Wizard** dialog, complete all items to finish the setup.

1. Select your **qTest version** and enter you qTest account for authentication information. Once your qTest account is connected successfully, proceed to step 2.

   > Notes:
   > * In the version options, we recommend selecting 7 or higher. This is because earlier versions might be deprecated soon.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-1-183A263A14.png" width=70% alt="Choose qTest version in the Wizard Setup box">

2. Select your qTest project.
    
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-1-183A263A32.png" width=70% alt="Select qTest project in the Wizard Setup box">

3. In the **Test Structure Mapping** section, you need to map the tests between the two systems.

   3.1. In the **qTest module** section: select one of the qTest modules fetched from your account to store the uploaded Katalon test cases.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-4-103A13A24.png" width=80% alt="Choose qTest module in the Wizard Setup box">

   3.2. In the **Katalon Test Case folder** section: select a test case folder to integrate with the qTest module from step 3.1.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-4-103A23A46.png" width=80% alt="Choose test case folder in the Wizard Setup box">


   3.3. In the **Katalon Test Suite folder** section: select a test suite folder to integrate with the qTest module from step 3.1.
      
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-4-103A23A19.png" width=80% alt="Choose test suite folder in the Wizard Setup box">

4. In the **Execution Options** section, choose the settings for uploading results to qTest.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-QTEST-configured-qTest.png" width=80% alt="Execution Options">

   <table>
   <thead>
   <tr>
      <th>Field</th>
      <th>Description</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Automatically submit test run result</td>
      <td>Results of executed test cases are uploaded automatically to qTest.</td>
   </tr>
   <tr>
      <td>Submit test run result to the latest approved version</td>
      <td>Test run results are submitted to the latest approved version of the mapped qTest test case.</td>
   </tr>
   <tr>
      <td>Report format</td>
      <td>Additional attachments for reports to be upload to qTest.</td>
   </tr>
   </tbody>
   </table>

   > Notes:
   > * To upload the HTML report to qTest, make sure to enable the HTML reports generation in **Project > Settings > Plugins > Reports**.
      ><img alt="Enable HTML reports" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-qTest-HTML-report-generator.png" width=85%>

5. Click **Finish**.

</details>

<details><summary>Manual Setup</summary>

1. In the **Authentication** section, select your qTest version.

   > Notes:
   > * In the version options, we recommend selecting 7 or higher. This is because earlier versions might be deprecated soon.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-143A493A1.png" width=30% alt="Authentication in the Manual Septup">

2. To generate a token for authentication, you can choose either log in with username and password or with an SSO token.

   <details><summary>Log in with username and password</summary>
   
      - Click **Generate**. The **Generate new token** dialog opens.
      
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-143A503A18.png" width=80% alt="Generate new token dialog">

      - Fill in your qTest account information. Then click **Generate**.
      
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-143A483A8.png" width=80% alt="Fill in account information">

      - KS connects to qTest using the provided information. The token is generated.
   
   </details>

   <details><summary>Log in with SSO token</summary>
   
      - If you are using Single Sign-On (SSO) to log in to qTest, ignore the **Generate** button, copy and paste the following token format in the **Token** text field:
      
      `{"access_token":"<bearer_token_value>","token_type":"bearer","scope":"read write create delete administration execute import export share baseline"}`
      
      - To find the `<bearer_token_value>`, access qTest Manager. Sign in with your SSO account. Navigate to the **Download qTest Resources** page. In the **API & SDK** section, you can see the **Bearer Token** value. 
      
      <img alt="Bearer token" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/bearer-token.png" width=85%>
   
   </details>

3. Select your preferred test submission method from the following options:

    <img alt="Submitting options" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/submitting-options.png" width=85% alt="Execution Options">

   <table>
   <thead>
   <tr>
      <th>Field</th>
      <th>Description</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Automatically submit test run result</td>
      <td>Results of executed test cases are uploaded automatically to qTest.</td>
   </tr>
   <tr>
      <td>Submit test run result to the latest approved version</td>
      <td>Test run results are submitted to the latest approved version of the mapped qTest test case.</td>
   </tr>
   <tr>
      <td>Report format</td>
      <td>Additional attachments for reports to be upload to qTest.</td>
   </tr>
   </tbody>
   </table>

   > Notes:
   > * To upload the HTML report to qTest, make sure to enable the HTML reports generation in **Project > Settings > Plugins > Reports**.
      > <img alt="Enable HTML reports" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-qTest-HTML-report-generator.png" width=85%>

4. Conduct test case mapping.
   
   - To create mappings between qTest modules and Katalon Test Case folders, go to **Project > Settings > Plugins > qTest > Test Case Repositories**.

   <img alt="Test case mapping" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-6-29-163A473A10.png" width=85%>
   
   - Click **Add**. The **Create Test Case Repository** dialog opens. 
   - Choose your qTest project, qTest module and browse the Katalon folder for the test case you wish to map with. 
   - Click **OK** when you are done.

      <img alt="Browse mapping test cases" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-153A253A8.png" width=85%>

5. Conduct test suite mapping.

   - To create mappings between qTest projects and Katalon Test Suite folders, go to **Project > Settings > Plugins > qTest > Test Suite Repositories**.
   
      <img alt="Enable HTML reports" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-6-29-163A483A33.png" width=85%>

   - Click **Add**. The **Create Test Suite Repository** dialog opens. 
   - Choose your qTest Project, and browse the Katalon folder for the test suite you wish to map with.
   - Click **OK** when you are done.

      <img alt="Enable HTML reports" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-153A373A55.png" width=85%>

      > Notes:
      > * You should select test suites that contain test cases defined in the **Test Case Repositories** settings.

</details>

## qTest - Katalon Studio parity report

> Requirements:
> * Katalon Studio version 7.8.0 onwards.

To enable parity reports generation, go to **Project Settings > Plugins > qTest**, check the **Generate the parity report after test execution** box.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-QTEST-Parity-report.png" width=100% alt="Parity reports">

Katalon Studio will generate test suite and test suite collection reports when you turn on this setting. This parity report provides a quick check of the version and test step contents of your integrated test cases between two systems. 

> Notes:
> * Only test cases with a unique ID are counted. Duplicate test cases are counted as one.

To view the generated parity report, open the `<your-project-folder>/Reports` folder.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/parity-report-html.png" width=70% alt="Open the parity report in the project folder">

## Execution Status Mapping

> Requirements:
> * Katalon Studio version 7.9.0 onwards.

1. To submit execution results from Katalon Studio to qTest Manager, activate the Automation Integration settings and map the automation status to the test run status in qTest. You can learn more about activating the Automation Integration settings in the Tricentis document here: [Activate Automation Integrations](https://documentation.tricentis.com/qtest/1001/en/content/qtest_manager/project_settings/activate_automation_integrations.htm).

   <a class="pop">
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/qtest_map_status.png" width=100% alt="Map test status in qTest">
   </a>
   <p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

   <a class="pop">
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-QTEST-Automation-status.png" width=100% alt="Map test status in Katalon Studio">
   </a>
   <p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

2. Map the Katalon Studio test status to the qTest test status.

   To do so, in Katalon Studio, go to **Project > Settings > Plugins > qTest > Execution Status Mapping**. 
   In the **qTest API's status** column, input the value that matches the Automation Status you configured earlier from step 1.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-QTEST-Execution-mapping.png" width=70% alt="Map test status in Katalon Studio">

## Upload test cases to qTest

Katalon allows you to upload a test case or all test cases in a test case folder to qTest. 
### Upload a test case to qTest

> Requirements:
> * The test case you wish to upload must be located in the integrated test case folder with qTest. To learn more about integrating a test case folder with qTest, refer to step 4 in Manual Setup. See above: [Manual Setup](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#configure-qtest-integration).

To upload a test case to an integrated qTest module, do as follows:

- In the **Tests Explorer** panel, right-click on the test case to trigger its context menu. Select **qTest > Upload**.  

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A293A21.png" width=70% alt="Upload a test case">

- Alternatively, you can also navigate to the **Integration** tab of the test case. Click **Upload**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-QTEST-Upload-a-test-case.png" width=100% alt="Upload a test case">

- Uploaded test cases have a qTest icon at the bottom right of the icon as shown below:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A303A1.png" width=70% alt="Upload a test case">

- You can also go to qTest to verify whether the Katalon Studio test case is successfully uploaded to the integrated qTest module. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A353A44.png" width=70% alt="Upload a test case">

- You can also see the following information in the **Integration** tab of the integrated test case.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-Test-case-integrated-information.png" width=100% alt="Test case information"> 
   
   <table>
   <thead>
   <tr>
      <th>Field</th>
      <th>Description</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Test Case ID</td>
      <td>The ID of the integrated qTest test case.</td>
   </tr>
   <tr>
      <td>Alias</td>
      <td>The alias of the integrated qTest test case.</td>
   </tr>
   <tr>
      <td>Parent ID</td>
      <td>The ID of the integrated qTest module.</td>
   </tr>
   <tr>
      <td>Version</td>
      <td>The qTest test case version.</td>
   </tr>
   </tbody>
   </table>

   > Tips:
   > * You can quickly open the integrated test case in qTest by clicking **Navigate**.

### Upload a test case folder to qTest

> Requirements:
> * The test case folders you wish to upload should be added in **Project > Settings > Plugins > qTest > Test Case Repositories**. To learn more about adding a test case folder in the **Test Case Repositories**, refer to step 4 in Manual Setup. See above: [Manual Setup](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#configure-qtest-integration).

- In the **Tests Explorer** panel, right-click on the test case folder to trigger its context menu. Select **qTest > Upload**.  

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-9-163A343A22.png" width=70% alt="Upload test case folder">

- The uploaded test case folder and test cases have a qTest icon at the bottom right of the icon as shown below:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-9-163A413A46.png" width=70% alt="Upload test case folder">

- Alternatively, you can go to qTest to verify whether the Katalon test cases within the selected folder are successfully uploaded to the integrated qTest module.  

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-9-163A453A32.png" width=70% alt="Upload test case folder">

## Download qTest test cases to Katalon

1. In qTest, switch to the **Test Design** tab. Move the test cases you wish to download into the qTest module that is integrated with Katalon Studio. 

   For example, we want to download the **Login_myAccount** test case to Katalon Studio. We move it to the **Login** qTest module, which we have integrated with Katalon Studio beforehand.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-qTest-Download-test-case-from-qTest.png" width=70% alt="Move test case to the integrated folder in qTest">

2. Switch to Katalon Studio. In the **Tests Explorer** panel, right-click the test case folder that is integrated with the above qTest module. Select **qTest > Download**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A513A18.png" width=70% alt="Download qTest test case">

3. The **Downloaded test case preview** dialog opens. You can see all test cases in the integrated qTest module that are available for download. Select the test case you want to download. Click **OK** to continue.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A523A29.png" width=70% alt="Downloaded test case preview">
   
   > Notes:
   > * Test cases that are downloaded will not be displayed again.

4. Once the downloading process is finished, you can view the downloaded test cases in the integrated test case folder.  

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A563A37.png" width=70% alt="View downloaded test cases">

## Disintegrate test cases from qTest

Katalon allows you to disintegrate a test case or all test cases in a test case folder from qTest.
### Disintegrate a test case from qTest

You can break the connection between a Katalon Studio test case and qTest by following the steps below:

1. To disintegrate a test case from qTest, navigate to the **Integration** tab of the test case. Click **Disintegrate**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-QTEST-Disintegrate-test-case.png" width=70% alt="Disintegrate a test case from qTest">

   Alternatively, you can right-click the test case you wish to disintegrate, select **qTest > Disintegrate**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-QTEST-Disintegrate-test-case-2.png" width=70% alt="Disintegrate a test case from qTest">

2. In the **Confirmation** dialog, click **OK**. The connection between the test case and qTest is removed.  

### Disintegrate a test case folder from qTest

You can break the connection between a Katalon Studio test case folder and qTest by following the steps below.

> Notes:
> * Disintegrate a test case folder from qTest will also disintegrate all test cases in the folder from qTest.

1. To disintegrate a test case folder from qTest, in the **Tests Explorer** view, right-click the test case folder you wish to disintegrate. Select **qTest > Disintegrate**.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-173A23A57.png" width=70% alt="Disintegrate a test case folder from qTest">

2. In the **Confirmation** dialog, click **OK**. The connection between the test case folder and qTest is removed.

## Upload test suites to qTest

> Requirements:
> * The test suite you wish to upload to qTest should be located in the integrated test suite folder with qTest. To learn more about integrating a test suite folder with qTest, refer to step 5 in Manual Setup. See above: [Manual Setup](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#configure-qtest-integration).
### Register a qTest location for a test suite

1. Navigate to the **Integration** tab of the test suite. Click on the **New parent** button.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2017-8-6-153A193A52.png" width=70% alt="Register a qTest location for a test suite">

2. The **Create Test Suite's parent** dialog opens. Select a **Parent** folder, then choose the location to integrate with the Katalon test suite.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-21-153A233A4.png" width=70% alt="Choose the parent folder">

3. In the **Creation Options** section, you can decide the integration behavior with the following options:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-QTEST-Creation-option.png" width=70% alt="Creation options">

   <table>
   <thead>
   <tr>
      <th>Option</th>
      <th>Description</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Create only</td>
      <td>- Create an association between the Katalon test suite and the selected qTest location. <br>- With this option, if you want to upload the Katalon test suite to the selected qTest location, you need to do it manually. See below: <a href="https://docs.katalon.com/katalon-studio/docs/qtest-integration.htm#upload-test-suites-manually" target="_blank" rel="noopener noreferrer">Upload a test suite manually</a></td>
   </tr>
   <tr>
      <td>Create and upload</td>
      <td>- Create an association between the Katalon test suite and the selected qTest location.<br>- Upload the Katalon test suite to the selected qTest location.</td>
   </tr>
   <tr>
      <td>Create, upload, and set as default</td>
      <td>- Create an association between the Katalon test suite and the selected qTest location.<br>- Upload the Katalon test suite to the selected qTest location.<br>- Set the qTest location as default for uploading the execution result of the Katalon test suite.</td>
   </tr>
   </tbody>
   </table>

   > Notes: 
   > * A test suite can be registered in many qTest locations, but only one qTest location can be set as default.

4. Click **OK** to continue. 
   Once integrated, you can see the location and the name of the parent folder on qTest.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-21-153A503A3.png" width=70% alt="Register a qTest location for a test suite">
    
    | Icon | Description |
    | --- | --- |
    | <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/84.png" alt="Successfully integrated icon"> | The Katalon test suite is integrated with the qTest location. |
    | <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/85.png" alt="Unsuccessfully integrated icon"> | The Katalon test suite is not integrated with the qTest location. |
    
    You can also view the integration information, including **Parent ID**, **Test Suite ID**, and **Alias**, as shown below:

    | Field | Description |
    | --- | --- |
    | Test Suite ID | The ID of the integrated qTest test suite. |
    | Alias | The alias of the integrated qTest test suite. |
    | Parent ID | The ID of the integrated qTest location. |
    
   > Tips:
   > * You can quickly open the uploaded test suite in qTest by clicking **Navigate**.
      > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-21-183A123A57.png" width=70% alt="Quickly navigate to qTest">

### Upload test suites manually

> Notes:
> * Suppose you choose the **Create and upload** or the **Create, upload and set as default** option while registering a qTest location for a test suite. In that case, your test suite is automatically uploaded to the registered qTest location. You can skip this part.

Katalon allows you to upload a test suite or all test suites in a test suite folder to qTest.

1. Upload a test suite manually:

   > Requirements:
   > * Make sure all test suites have at least one registered qTest location.
   > * The selected test suites have not been uploaded yet.

   - To upload a test suite manually to the predefined qTest location, navigate to the **Integration** tab of the test suite. In the **List of test suite's parents**, select a qTest location, then click **Upload**.  

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-143A103A48.png" width=70% alt="Upload test suites manually">

   - Alternatively, you can also right-click on the test suite to trigger its context menu. Select **qTest > Upload**.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-143A193A18.png" width=70% alt="Upload test suites manually">

   - Once the uploading process finishes, you can go to qTest to verify whether the Katalon test suite is successfully uploaded to the registered qTest location.  

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-143A343A18.png" width=70% alt="Upload test suites manually">

2. Upload a test suite folder manually:

   > Requirements:
   > * Make sure all test suites in the test suite folder have at least one registered qTest location.
   > * At least one test suite in the selected test suites folder has not been uploaded yet.

   - In the **Tests Explorer** panel, right-click on the test suite folder to trigger its context menu. Select **qTest > Upload**.
    
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-143A573A33.png" width=70% alt="Upload test suites folder manually">
    
   - Once the uploading process finishes, you can go to qTest to verify whether the Katalon test suites in the selected folder are uploaded to the registered qTest locations.
      
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-173A493A23.png" width=70% alt="Upload test suites folder manually">

## Disintegrate test suites from qTest

Katalon allows you to disintegrate a test suite or all test suites in a folder from qTest.
### Disintegrate a test suite from qTest

You can remove the integration between the Katalon test suite and the registered qTest location by following the steps below:

1. To remove the connection between a test suite and the registered qTest location, navigate to the **Integration** tab of the test suite. Select a qTest location, click **Disintegrate**.
      
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-173A573A5.png" width=70% alt="Disintegrate a test suite from qTest">

   Alternatively, you can also right-click on the test suite you wish to disintegrate. Select **qTest > Disintegrate**. 

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-183A33A20.png" width=70% alt="Disintegrate a test suite from qTest">

2. Click **OK** on the **Confirmation** dialog. The integration between the test suite and the registered qTest location is removed.
### Disintegrate a test suite folder from qTest

You can break the connection between a Katalon Studio test suite folder and qTest by following the steps below:

> Notes:
> * Disintegrate a test suite folder from qTest will also disintegrate all test suites in the folder from qTest.

1. In the **Tests Explorer** view, right-click on the test suite folder you wish to disintegrate. Select **qTest > Disintegrate**.  
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-183A133A46.png" width=70% alt="Disintegrate a test suite from qTest">

2. Click **OK** on the **Confirmation** dialog. The integration between the test suite folder and qTest is removed.

## Upload test execution results

> Requirements:
> * The associated test case is uploaded to qTest. For further instructions, see above [Upload test cases to qTest](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#upload-test-cases-to-qtest).
> * The associated test suite is uploaded to qTest. For further instructions, see above [Upload test suites to qTest](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#upload-test-suites-to-qtest).
> * A registered qTest location for the associated test suite is set as default.
> * The qTest test case version is at least 1.0. 
### Upload test results automatically

1. To automatically upload the test execution results, check the **Automatically submit test run results** option in **Project > Settings > Plugins > qTest**.
2. Add an integrated test case to an integrated test suite.
3. Execute an integrated Katalon test suite.
4. Open the generated test execution report.
5. In the **Test Cases Table** section, the status of all test execution is displayed with the following information.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-153A423A26.png" width=70% alt="the Test Cases Table section">
    
   <table>
   <thead>
   <tr>
      <th>Icon</th>
      <th>Description</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-2-28-163A323A19.png" alt="Successfully uploaded icon"></td>
      <td>The execution result of the test case is uploaded to qTest.</td>
   </tr>
   <tr>
      <td><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-2-28-163A293A39.png" alt="Unsuccessfully uploaded icon"></td>
      <td>The execution result of the test case is not uploaded to qTest.</td>
   </tr>
   </tbody>
   </table>
    
5. To find the qTest information, click **Show Test Case Details**. In the **Test Case's Log** table, go to the **Integration** tab.
    
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-153A453A53.png" width=70% alt="Show test case details">

   You can view the following information:
    
   <table>
   <thead>
   <tr>
      <th>Field</th>
      <th>Description</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Test Run Alias</td>
      <td>The alias of the integrated qTest test run.</td>
   </tr>
   <tr>
      <td>Test Log ID</td>
      <td>The ID of the test log created in qTest, for example, execution history record.</td>
   </tr>
   <tr>
      <td>Attachment</td>
      <td>This lets users know whether all the execution logs and reports are sent to qTest as an attachment. (i.e., Yes or No)<br>If yes, you can go to qTest and find them under the related execution history record, as illustrated below:<br><p style="text-align: center;"><a class="pop"><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-153A503A43.png"></a><em>Click the image to enlarge it.</em></p></td>
   </tr>
   </tbody>
   </table>

### Upload test case results manually

1. Add an integrated test case to an integrated test suite.
2. Execute the integrated Katalon test suite.
2. Open the generated test execution report.
3. In the **Test Cases Table** section, right-click the test case you wish to upload the test result. Select **qTest > Upload**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-163A33A27.png" width=70% alt="Upload test case results manually">

4. Once the uploading process is finished, you can go to qTest to verify whether the test execution is uploaded successfully to qTest test run.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-163A103A23.png" width=100% alt="Upload test case results manually">

### Upload test suite results manually

1. In the **Tests Explorer** panel, open the **Reports** folder. Right-click the test execution result you wish to upload. Select **qTest > Upload**. 

   To upload all test executions, you can right-click the **Report** folder, select **qTest > Upload**. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-163A113A37.png" width=366 alt="Upload test suite results manually">

2. Once the uploading process is finished, you can go to qTest to verify whether the test execution is uploaded successfully to the qTest test run.
## qTest Test Cases Version Control and Synchronization

> Requirements:
> * Katalon Studio version 7.8.0 onwards.
> * The qTest integration enabled.
> * The associated test case is uploaded to qTest. For further instructions, see above [Upload test cases to qTest](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#upload-test-cases-to-qtest).

Katalon allows you to check which Katalon Studio test cases need updating when the integrated qTest test cases change the test step content.
You can do so with one or many test cases. In each Katalon test case, you can also retrieve the latest content of the integrated qTest test case.
### Check for version updates in bulk

1. Click on the qTest icon on the menu bar.
2. Select **Check for updates**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/qtest-check-for-update.png" width=366 alt="Upload test suite result manually">

3. In the **Check for updates** dialog, select test cases you wish to check for update. Click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/tc-browser.png" width=391 alt="The check for update dialog">

   Wait for the test engine to retrieve information from the qTest server.

   <a class="pop">
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-qTest-Check-update-in-bulk.gif" width=100% alt="Check for version updates">
   </a>
   <p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>

### Check for version updates in a test case

In a test case editor, open the **Integration** tab, click **Check for updates** to fetch the latest qTest test case version and test steps content. Wait for the test engine to retrieve information from the qTest server.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/test-case-version.png" width=420 alt="Check for version updates in a test case">

Wait for the test engine to retrieve information from the qTest server.
If you wish to save the latest content of test steps and test case version, in the pop-up **qTest Integration Update** dialog, click **Sync up**.

<a class="pop">
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/KS-qTest-Check-update-in-a-test-case.gif" width=100% alt="Check for version updates">
</a>
<p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>

## Map a Katalon test case to a qTest test case by database ID

> Requirements:
> * Katalon Studio version 7.9.0 onwards.
> * qTest integration enabled.
> * The Katalon test case must be located in the integrated test case folder with qTest. To learn more about integrating a test case folder with qTest, refer to step 4 in Manual Setup. See above: [Manual Setup](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#configure-qtest-integration).

Katalon Studio provides an easy way to map a Katalon test case to an existing qTest test case. Follow these steps:

1. In qTest, you can get a qTest test case database ID in the test case URL. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/id.png" width=70% alt="Get qTest test case database ID in qTest">  

2. In Katalon Studio, select a test case you want to link to the above qTest test case. Add the copied value to its name in the following format: `<qTest Database ID> <Katalon test case name>`.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/renamed.png" width=80% alt="Copy ID database in the test case">

3. Open the test case editor, select the **Integration** tab. 
4. Click **Link qTest Test Case**.  

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/link.png" width=50% alt="Link qTest Test case">

5. Save your change when the test case is linked to qTest successfully. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/linked.png" width=70% alt="Link qTest Test case successfully">







