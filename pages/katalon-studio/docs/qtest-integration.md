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
> * An active Katalon Studio Enterprise license. To learn more about activating Katalon Studio license, you can refer to this document: [Activate Katalon license](https://docs.katalon.com/katalon-studio/docs/activate-license.html#activate-a-license-with-internet-access).

## Install the qTest Integration plugin

To download and install the **qTest Integration** plugin, you can go to the Katalon Store here: [qTest Integration](https://store.katalon.com/product/136/qTest-Integration). 

To activate the installed plugin, navigate to Account Settings in Katalon Studio and click **Reload Plugin**.
If you want to use the plugin in console mode, you can refer to this document: [Use Plugins in Console Mode](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#use-plugins-in-console-mode).

After reloading plugins successfully to activate the qTest plugin, you can start configuring the integration between Katalon Studio and qTest.

## Enable qTest integration

1. Open the qTest integration settings

* For Katalon version 7.5.5 onwards: Go to **Project > Settings > Plugins > qTest**
* For versions older than 7.5.5: Go to **Project > Settings > Integration > qTest**

2. Check the **Enable integration** checkbox. Next, you can either use the wizard setup or set up the qTest integration manually.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/enable-wizard.png" width=85%>

## Configure qTest integration

> Notes:
> * From version 7.9.0 onwards, Katalon Studio supports pushing screenshots (PNG files) along with other existing submitting options to qTest to generate reports.

You can configure qTest integration manually or with Wizard Setup as follows:

<details><summary>Wizard Setup</summary>

To open the **Wizard Setup**, click **Yes** in the above pop-up window after checking **Enable Integration** or click on the **Quick Setup...** hyperlink.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-6-29-163A493A31.png" width=70%>

In the displayed **qTest Integration Setup Wizard** dialog, complete all items to finish the setup.

1. Enter authentication information and select your **qTest version**. Once your qTest account is connected successfully, proceed to step 2.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-1-183A263A14.png" width=70%>

2. Select your **qTest project**.
    
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-1-183A263A32.png" width=70%>

3. In the Test Structure Mapping section, you need to map the tests between the two systems.

   3.1. **qTest module**: select one of the qTest modules fetched from your account to store the uploaded Katalon test cases.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-4-103A13A24.png" width=80%>

   3.2. **Katalon Test Case folder**: select one test case folder to be integrated with the chosen **qTest module** above.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-4-103A23A46.png" width=80%>


   3.3. **Katalon Test Suite folder**: select one test suite folder to be integrated with the selected **qTest module** above.
      
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-4-103A23A19.png" width=80%>

4. Optional settings when uploading to qTest.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-1-183A283A21.png" width=80%>

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
      <td>Submit test run result to latest approved version</td>
      <td>Test run results are submitted to latest approved version of mapped qTest test case.</td>
   </tr>
   <tr>
      <td>Report format</td>
      <td>Additional attachments for reports to be upload to qTest.</td>
   </tr>
   </tbody>
   </table>

   > Notes:
   > * To upload the HTML report to qTest, make sure to enable the HTML reports generation in **Project > Settings > Plugins > Reports**.
      > <img alt="Enable HTML reports" src="url" width=85%>

5. Recheck setup information, then click **Finish**.

</details>

<details><summary>Manual Setup</summary>

1. **qTest Version**: On Authentication form, select the version of your qTest.

   > Notes:
   > * The **7 or higher** option is recommended because APIs of earlier versions might be deprecated soon.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-143A493A1.png" width=30%>

2. To **generate token** for Authentication, you can choose either logging in with username and password or logging in with SSO token.

   <details><summary>Log in with username and password</summary>
   
      Click on the **Generate** button to create the token to be used during the integration session.
      
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-143A503A18.png" width=80%>

      Fill in valid information on the **Generate new token** dialog. For example:
      
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-143A483A8.png" width=80%>

      Once Katalon Studio successfully connects to your qTest using the provided information, the token will be generated.
   
   </details>

   <details><summary>Log in with SSO token</summary>
   
      If you are using SSO (Single Sign-On) to log into qTest, ignore the **Generate** button, copy and paste the following token format in the **Token** text field:
      
      `{"access_token":"<bearer_token_value>","token_type":"bearer","scope":"read write create delete administration execute import export share baseline"}`
      
      Fill <bearer_token_value> with **Bearer Token**. To find it, you need to access qTest Manager and sign in with your SSO account. Then navigate to the **Download qTest Resources** page, under the **API & SDK** section, you can see **Bearer Token**. 
      
      <img alt="Bearer token" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/bearer-token.png" width=85%>
   
   </details>

3. Select other submitting options as following:

    <img alt="Submitting options" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/submitting-options.png" width=85%>

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
      <td>Submit test run result to latest approved version</td>
      <td>Test run results are submitted to latest approved version of mapped qTest test case.</td>
   </tr>
   <tr>
      <td>Report format</td>
      <td>Additional attachments for reports to be upload to qTest.</td>
   </tr>
   </tbody>
   </table>

   > Notes:
   > * To upload the HTML report to qTest, make sure to enable the HTML reports generation in **Project > Settings > Plugins > Reports**.
      > <img alt="Enable HTML reports" src="url" width=85%>

4. **Test Case Mapping**:
   
   To create mappings between **qTest modules** and **Katalon Test Case folders**, go to **Project > Settings > Plugins > qTest > Test Case Repositories**.

   <img alt="Test case mapping" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-6-29-163A473A10.png" width=85%>
   
   Click **Add**. The **Create Test Case Repository** dialog opens. 
   Choose the **qTest Project**, **qTest Module** and browse the **Katalon Folder** for the test case you wish to map with. Click **OK** when you are done.

   <img alt="Browse mapping test cases" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-153A253A8.png" width=85%>

5. **Test Suite Mapping**:

   To create mappings between **qTest projects** and **Katalon Test Suite folders**, go to **Project > Settings > Plugins > qTest > Test Suite Repositories**.
   
      <img alt="Enable HTML reports" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-6-29-163A483A33.png" width=85%>

   Click **Add**. The **Create Test Suite Repository** dialog opens. 
   Choose the **qTest Project**, and browse the **Katalon Folder** for the test suite you wish to map with.
   Click **OK** when you are done.

      <img alt="Enable HTML reports" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-153A373A55.png" width=85%>

   > Notes:
   > * You should select test suites that contain test cases defined in **Test Case Repositories** settings.

</details>

## Execution Status Mapping

> Requirements:
> * Katalon Studio version 7.9.0 onwards.

1. To submit execution results from Katalon Studio to qTest Manager, activate the Automation Integration and mapped Automation Status to Test Run Status in qTest. You can learn more about activating Automation Integration, you can refer to the Tricentis document here: [Activate Automation Integrations](https://documentation.tricentis.com/qtest/1001/en/content/qtest_manager/project_settings/activate_automation_integrations.htm).

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/qtest_map_status.png" width=70% alt="Map test status in qTest">

2. Map Katalon Studio test status to the Automation Status you have configured earlier from step 1. 

   To do so, in Katalon Studio, go to **Project > Settings > Plugins > qTest > Execution Status Mapping** and specify the submitted value of each test status.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/status-map-ks.png" width=60% alt="Map test status in Katalon Studio">

## qTest - Katalon Studio Parity Report

> From version 7.8.0 onwards, Katalon supports generating a qTest-Katalon Studio Parity Report after a test execution.

To enable parity reports generation, go to **Project Settings > Plugins > qTest**, check the **Generate the parity report after test execution** box.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/parity-report.png">

When you turn on this setting, Katalon Studio will generate a report for Test Suite and Test Suite Collection execution. This parity report is to provide a quick check of version and test step contents of your integrated test cases between two systems. In a test execution, only test cases with unique ID are included in this report (two or more duplicate Test Cases are counted as one).

To view the generated parity report, open the Report folder.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/parity-report-html.png" width=70%>

## Upload test cases/test case folders to qTest

### Upload a test case

> Requirements:
> * The test case you wish to upload must locate in the integrated test case folder with qTest. To learn more about integrating a test case folder with qTest, see above: [Manual Setup - Test Case Mapping](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#configure-qtest-integration).

To upload a test case to an integrated qTest Module, do as follows:

- In the **Tests Explorer** panel, right-click on the test case to trigger its context menu. Select **qTest > Upload**.  

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A293A21.png" width=70%>

- Alternatively, you can also navigate to the **Integration** tab of the test case. Click **Upload**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2016-11-18-143A193A2.png" width=70%>

- Uploaded test cases have qTest icon at the bottom right of the icon as shown below:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A303A1.png" width=70%>

- You can also go to qTest to verify whether the Katalon Studio test case is successfully uploaded to the integrated qTest module. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A353A44.png" width=70%>

- You can also see the following information in the **Integration** tab of the integrated test case.

    <table><thead><tr><th>Field</th><th>Description</th></tr></thead><tbody><tr><td>Test Case ID</td><td>The ID of the integrated qTest test case.</td></tr><tr><td>Alias</td><td>The alias of the integrated qTest test case.</td></tr><tr><td>Parent ID</td><td><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-9-163A273A25.png"></p><p>The ID of the integrated qTest module.</p></td></tr></tbody></table>

   > Tips:
   > * You can quickly open the integrated test case in qTest by clicking **Navigate**.

### Upload test case folder

> Requirements:
> * The test case folders you wish to upload should be added in **Project > Settings > Plugins > qTest > Test Case Repositories**. To learn more about adding a test case folder in the **Test Case Repositories**, see above: [Manual Setup](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#configure-qtest-integration).

- In the **Tests Explorer** panel, right-click on the test case folder to trigger its context menu. Select **qTest > Upload**.  

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-9-163A343A22.png" width=70%>

- The uploaded test case folder and test cases have qTest icon at the bottom right of the icon as shown below:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-9-163A413A46.png" width=70%>

- Alternatively, you can go to qTest to verify whether the Katalon test cases within the selected folder are successfully uploaded to the integrated qTest module.  

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-9-163A453A32.png" width=70%>

## Download qTest test cases

1. In qTest, switch to the **Test Design** tab. Move the test cases you wish to download into the qTest module that is integrated with Katalon Studio. 

   For example, we want to download the **Login_myAccount** test case to Katalon Studio, we move it to the **Login** qTest module, which we have integrated with Katalon Studio beforehand.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A483A50.png" width=70%>

2. Go to Katalon Studio, in the **Tests Explorer** panel, right-click the test case folder that is integrated with the above qTest module. Select **qTest > Download**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A513A18.png" width=70%>

3. The **Downloaded test case preview** dialog opens. You can see all test cases in the integrated qTest module are available for download. Select the test case you want to download. Click **OK** to continue.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A523A29.png" width=70%>
   
   > Notes:
   > * Test cases that are downloaded will not be displayed again.

4. Once the downloading process finished, you can view the downloaded test cases in the integrated test case folder.  

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A563A37.png" width=70%>

## Disintegrate test cases/test case folders from qTest
### Disintegrate a test case from qTest

You can break the connection between a Katalon Studio test case and qTest by following the steps below:

1. To disintegrate a test case from qTest, navigate to the **Integration** tab of the test case. Click **Disintegrate**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2016-11-18-163A453A57.png" width=70%>

   Alternatively, you can right-click the test case you wish to disintegrate, select **qTest > Disintegrate**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A593A5.png" width=70%>

2. Click **OK** on the **Confirmation** dialog. The connection between the test case and qTest will be removed.  

### Disintegrate a test case folder from qTest

You can break the connection between a Katalon Studio test case folder and qTest by following the steps below.

> Disintegrate a test case folder from qTest will also disintegrate all test cases in the folder from qTest.

1. To disintegrate a test case folder from qTest, in the **Tests Explorer** view, right-click the test case folder you wish to disintegrate. Select **qTest > Disintegrate**.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-173A23A57.png" width=70%>

2. Click **OK** on the **Confirmation** dialog. The connection between the test case folder and qTest will be removed.

## Upload test suites to qTest
## Register qTest location for a test suite

> Requirements:
> * The test suite you wish to upload to qTest should be in the integrated test suite folder with qTest. To learn more about integrating a test suite folder with qTest, see above: [Manual Setup - Test Suite Mapping](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#configure-qtest-integration).

1. Navigate to the **Integration** tab of the test suite. Click on the **New parent** button.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2017-8-6-153A193A52.png" width=70%>

2. The **Create Test Suite's parent** dialog opens. Select a **Parent** folder, then choose the location to integrate with the Katalon test suite.

3. You can also decide the integration behaviour in the **Creation Options** with the following options:

    <table><thead><tr><th>Option</th><th>Description</th></tr></thead><tbody><tr><td>Create only</td><td><ul><li>Create an association between the Katalon test suite and the selected qTest location.</li></ul></td></tr><tr><td>Create and upload</td><td><ul><li>Create an association between the Katalon test suite and the selected qTest location.</li><li>Upload the Katalon test suite to the selected qTest location.</li></ul></td></tr><tr><td>Create, upload and set as default</td><td><ul><li>Create an association between the Katalon test suite and the selected qTest location.</li><li>Upload the Katalon test suite to the selected qTest location.</li><li>Set the qTest location as default for uploading the execution result of the Katalon test suite.</li></ul></td></tr></tbody></table>

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-21-153A233A4.png" width=70%>

4. Click **OK** to continue. 
   Once integrated, you can see the location and the name of the parent folder on qTest:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-21-153A503A3.png" width=70%>
    
    | Icon | Description |
    | --- | --- |
    | <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/84.png"> | The Katalon test suite is integrated into the qTest location. |
    | <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/85.png"> | The Katalon test suite is not integrated into the qTest location. |
    
    You can also view the integration informationm including **Parent ID**, **Test Suite ID**, and **Alias** as shown below:

    | Field | Description |
    | --- | --- |
    | Test Suite ID | The ID of the integrated qTest test suite. |
    | Alias | The alias of the integrated qTest test suite. |
    | Parent ID | The ID of the integrated qTest location. |
    
   > Tips:
   > * You can quickly open the qTest parent folder where the test suites are uploaded in qTest by clicking **Navigate**.
      > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-21-183A123A57.png" width=70%>

### Upload a test suite/test suite folder automatically

While registering qTest location for a test suite, select the **Create and upload** or **Create, upload and set as default** options. Click **OK**. 
The test suite/test suite folder will be uploaded to qTest automatically. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-21-153A233A4.png" width=70%>

### Upload a test suite manually

1. To upload a test suite to the predefined qTest location:
      
    1.1 Navigate to the **Integration** tab of the test suite. Select a **qTest location** that is yet to be integrated from the **List of test suite's parents** and click on the **Upload** button.  

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-143A103A48.png" width=70%>

    1.2. In the Tests Explorer view, right-click on the test suite to trigger its context menu. Select the **qTest > Upload** option.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-143A193A18.png" width=70%>

    > The **Upload** option is available only when:
    > * The test suite is **NOT** uploaded yet.

2.  Once the uploading process finishes, you can go to qTest to verify that the **Katalon test suite** is uploaded to the registered **qTest location**.  
      
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-143A343A18.png)

### Upload test suite folder manually

1.  In the **Tests Explorer** view, right-click on the test suite folder to trigger its context menu. Select the **qTest > Upload** option.
    
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-143A573A33.png" width=70%>
    
    > The **Upload** option is available only when:
    > * The test suite is **NOT** uploaded yet.
    
2.  Once the uploading process finishes, you can go to qTest to verify that the **Katalon test suites** within the selected folder are uploaded to the registered **qTest locations**.
      
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-173A493A23.png" width=70%>

## Disintegrate a test suite/test suite folder from qTest
### Disintegrate a test suite from qTest

Remove the integration between **Katalon test suites** and its registered **qTest locations**.

1. You have two methods to remove the connection between a test suite and registered qTest locations:

    1.1 Navigate to the **Integration** tab of the test suite. Select a **qTest location** and click on the **Disintegrate** button.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-173A573A5.png)

    1.2 In the Tests Explorer view, right-click on the **test suite** to trigger its context menu. Select the **qTest > Disintegrate** option.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-183A33A20.png)  

2. Click **OK** on the Confirmation dialog. The integration between this test suite and all registered qTest locations will be removed.
### Disintegrate a test suite folder from qTest

You can remove the integration between a test suite folder (together with all its test suites) and all registered qTest locations by following the steps below:

1. In the **Tests Explorer** view, right-click on the **test suite folder** to trigger its context menu. Select the **qTest > Disintegrate** option.  
   
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-183A133A46.png)

2. Click **OK** on the Confirmation dialog. The integration between this folder (as well as all of its test suites) and qTest will be removed.

## Upload test execution results

In order for a test execution to be uploaded to qTest, the following conditions need to be fulfilled:

* The associated **test case** is integrated to qTest. Refer to [Integrate test case](/display/KD/Integrate+test+case) for more details.
* The associated **test suite** is integrated to qTest. Refer to [Integrate test suite](/display/KD/Integrate+test+suite) for more details.
* The integrated **qTest location** is set as **default**. Refer to [Integrate test suite](/display/KD/Integrate+test+suite) for more details.
* The version of **qTest test case** needs to be at least **1.0**. For example:

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-163A153A25.png)

### Upload test results automatically

> The test result from Katalon Studio will be upload to qTest automatically in case the **Automatically submit test run result** option is **checked** in [qTest Integration settings](/display/KD/qTest+Integration).

1. Execute an integrated Katalon test suite.
2. Open the generated test execution report.
3. In the **Test Cases Table**, the status of all test execution will be displayed accordingly.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-153A423A26.png)  
    Where:
    
    <table><thead><tr><th>Icon</th><th>Description</th></tr></thead><tbody><tr><td><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-2-28-163A323A19.png"></p></td><td>The execution result of the test case is integrated to qTest.</td></tr><tr><td><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-2-28-163A293A39.png"></p></td><td>The execution result of the test case is <strong>not</strong> integrated to qTest.</td></tr></tbody></table>
    
4. Select an integrated execution from **Test Cases Table** and you can find the related information of qTest in **Integration** tab of **Test Case's Log.** (You need to select **Show Test Case Details** to access this section)
    
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-153A453A53.png)  

    where:
    
    <table><thead><tr><th>Field</th><th>Description</th></tr></thead><tbody><tr><td>Test Run Alias</td><td>The alias of the integrated qTest test run.</td></tr><tr><td>Test Log ID</td><td>The ID of the test log (i.e., execution history record) created in qTest.</td></tr><tr><td>Attachment</td><td><p>This is to let users know whether all the execution logs and reports are sent to qTest as an attachment. (i.e., Yes or No)</p><p>If yes, you can go to qTest and find them under the related execution history record, as illustrated below:</p><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-153A503A43.png"></p></td></tr></tbody></table>

### Upload test results of a test case manually

1. Execute an integrated Katalon test suite.
2. Open the generated test execution report.
3. In the **Test Cases Table**, right-click on the test case to trigger its context menu. Select the **qTest > Upload** option.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-163A33A27.png)

4. Once the uploading process finished, you can go to qTest to verify that the **test execution** is uploaded to **qTest test run** accordingly.
   
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-163A103A23.png)

### Upload test results of a test suite manually

1. In the **Tests Explorer** view, right-click on the test execution to trigger its context menu. Select the **qTest > Upload** option. (You can select the **Upload** option from **Report folders** to upload multiple test execution if needed)  

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/upload-test-execution/image2017-8-7-163A113A37.png)  

2. Once the uploading process finished, you can go to qTest to verify that all **test execution** are uploaded to **qTest test runs** accordingly.

## qTest Test Cases' Version Control and Synchronization

**Preconditions**

* Katalon Studio version 7.8 onwards
* qTest Integration is enabled.
* There is an integration between a Katalon test case and a qTest test case.

### Version checking in bulk

When you want to check which integrated Katalon Studio Test Cases need updating based on the integrated qTest Test Cases, you can do as follows:

1. Click on the qTest icon on the menu bar
2. Select **Check for updates**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/qtest-check-for-update.png" width=366>

3. In the **Check for updates** dialog, select multiple test cases that have been integrated with qTest, click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/tc-browser.png" width=391>

Wait for the test engine to retrieve information from qTest server.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/qtest-version-checking-in-bulk.gif" width=100%>

### Check for version update in a Test Case

In a Test Case editor, open the **Integration** screen, click **Check for updates** to fetch the latest qTest test case's version and test steps' content. Wait for the test engine to retrieve information from qTest server.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/test-case-version.png" width=420>

If you wish to save the latest content of test steps and test case version, click **Sync up** in the pop-up **qTest Integration Update** dialog.

### Map a Katalon test case to a qTest test case by database ID

> Introduced in version 7.9

Katalon Studio provides an easy way to map a Katalon test case to an existing qTest test case.

**Requirements**

* You have enabled the qTest integration. 
* Only applicable to test cases stored in the test case folders that have integrated with a qTest module. (refer to step 4 in [manual setup](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#manual-setup))
* Katalon Studio version 7.9

1. Append the qTest test case's database ID to your Katalon test case's name.

* In qTest, you can get a qTest test case's database ID in the test case URL. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/id.png" width=70%>

* In Katalon Studio, select a test case you want to link to the above qTest test case, append the copied value to its name.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/renamed.png" width=80%>

2. Open its editor, select the **Integration** tab. 
3. Click **Link qTest Test Case**.  

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/link.png" width=50%>

4. Save your change when the test case is linked to qTest successfully. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/linked.png" width=70%>







