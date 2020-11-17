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

**Requirements**

* Katalon Studio 7.0.1
* An active Katalon Studio Enterprise license

## Install the qTest Integration plugin

Please visit our [Katalon Store](https://store.katalon.com/product/136/qTest-Integration) to download this plugin. For further details on how to install and reload this plugin with a Katalon Studio Enterprise license, please see [this document](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#use-plugins-offline).

After reloading plugins successfully to activate the qTest plugin, you can start configuring the integration between Katalon Studio and qTest.

## Enable qTest Integration

1. Open the qTest integration settings

* In version **7.5.5+**: Go to **Project/Settings/Plugins/qTest**
* In **prior to 7.5.5** versions: Go to **Project/Settings/Integration/qTest**

2. Check the **Enable integration** checkbox. Next, you can either use the wizard setup or set up the qTest integration manually.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/enable-wizard.png">

### qTest - Katalon Studio Parity Report

> From version 7.8 onwards, Katalon supports generating a qTest-Katalon Studio Parity Report after a test execution.

Go to **Project Settings/Plugins/qTest**, enable Parity Report by checking the option **Generate the parity report after test execution**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/parity-report.png">

When you turn on this setting, Katalon Studio will generate a report for Test Suite and Test Suite Collection execution. This parity report is to provide a quick check of version and test step contents of your integrated test cases between two systems. In a test execution, only test cases with unique ID are included in this report (two or more duplicate Test Cases are counted as one).

To view the generated parity report, open the Report folder.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/parity-report-html.png" width=420>

## Wizard Setup

Click **Yes** in the above pop-up window after checking "Enable Integration" or click on the **Quick Setup...** link to open the Wizard.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-6-29-163A493A31.png)

In the displayed Setup Wizard, complete all items to finish the setup.

1. Enter authentication information and select your **qTest version**. Once your qTest account is connected successfully, proceed to step 2.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-1-183A263A14.png)

2. Select your **qTest project**.
    
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-1-183A263A32.png)

3. In the Test Structure Mapping section, you need to map the tests between the two systems.

   3.1. **qTest module**: select one of the qTest modules fetched from your account to store the uploaded Katalon test cases.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-4-103A13A24.png)

   3.2. **Katalon Test Case folder**: select one test case folder to be integrated with the chosen **qTest module** above.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-4-103A23A46.png)

   3.3. **Katalon Test Suite folder**: select one test suite folder to be integrated with the selected **qTest module** above.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-4-103A23A19.png)

4. Optional settings when uploading to qTest. Please refer to [Manual Setup](#EnableqTestIntegration-ManualSetup) for more details of each option.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-1-183A283A21.png)

5. Complete all previous steps to finish the qTest setup wizard.

## Manual Setup

1. **qTest Version**: On Authentication form, select the version of your qTest. (_The **7 or higher** option is recommended because APIs of earlier versions might be deprecated soon_).

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-143A493A1.png)

2. To **generate token** for Authentication, you can choose either way (2.1 or 2.2)

   2.1 Log in with username and password: 
   
   Click on the **Generate** button to create the token to be used during the integration session.
    
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-143A503A18.png)
   
   Fill in valid information on the **Generate new token** dialog. For example:
   
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-143A483A8.png)

   Once Katalon Studio successfully connects to your qTest using the provided information, the token will be generated.

   2.2 Log in with SSO token:
   
   If you are using SSO (Single Sign-On) to log into qTest, ignore the **Generate** button, copy and paste the following token format in the **Token** text field:
   
   `{"access_token":"<bearer_token_value>","token_type":"bearer","scope":"read write create delete administration execute import export share baseline"}`
   
   Fill <bearer_token_value> with **Bearer Token**. To find it, you need to access qTest Manager and sign in with your SSO account. Then navigate to the **Download qTest Resources** page, under the **API & SDK** section, you can see **Bearer Token**. 
   
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/bearer-token-sso.png)

3. Select other submitting options as following:

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-8-1-173A33A41.png)

    Where:

    | Field | Description |
    | --- | --- |
    | Automatically submit test run result | Results of executed test cases will be uploaded automatically to qTest. |
    | Submit test run result to latest approved version | Test run result will be submitted to latest **approved** version of mapped qTest test case. |
    | Report format | Additional attachments for reports to be upload to qTest. |

4. **Test Case Mapping**:
   
   Select **Test Case Repositories** setting (in Plugins/qTest). You can create mappings between **qTest modules** and **Katalon Test Case folders** here.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-6-29-163A473A10.png)
   
   Click on the **Add** command. The **Create Test Case Repository** dialog will be displayed. Click **OK** when you are done with the settings.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-153A253A8.png)

5. **Test Suite Mapping**:
   
   Select the **Test Suite Repositories** setting (in Plugins/qTest). You can create mappings between **qTest projects** and **Katalon Test Suite folders** here.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2017-6-29-163A483A33.png)

   Click on the **Add** command. The **Create Test Suite Repository** dialog will be displayed. Click **OK** when you are done with the settings.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/image2016-11-15-153A373A55.png)

   > You should select test suites that contain those test cases defined in **Test Case Repositories** settings.

## Upload test cases to qTest

> **Test cases folder** must be registered in [**Test Case Repositories**](/display/KD/qTest+Integration) before you can upload test cases to qTest.

### Upload a single test case

1. You have two methods to upload a test case to a predefined qTest Module

    1.1 Navigate to the **Integration** tab of the test case. Click on the **Upload** button.
       ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2016-11-18-143A193A2.png)  

    1.2 In the Tests Explorer view, right-click on the test case to trigger its context menu. Select the **qTest > Upload** option.  
       ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A293A21.png)  

2. Uploaded Test Case will have qTest icon at the bottom right of the icon as shown below
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A303A1.png)  

3. You can also go to qTest to verify that the **Katalon Studio test case** is uploaded to the integrated **qTest module**. Refer to [Enable qTest Integration](/display/KD/Enable+qTest+Integration) for details about setting up an integrated qTest module.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A353A44.png)  

4. Katalon Studio will also retrieve the information regarding the above **qTest test case** and display them in the **Integration** tab of the Katalon test case.

    Where:
    
    <table><thead><tr><th>Field</th><th>Description</th></tr></thead><tbody><tr><td>Test Case ID</td><td>The ID of the integrated qTest test case.</td></tr><tr><td>Alias</td><td>The alias of the integrated qTest test case.</td></tr><tr><td>Parent ID</td><td><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-9-163A273A25.png"></p><p>The ID of the integrated qTest module.</p></td></tr></tbody></table>

5. Click the **Navigate** button to quickly open the integrated **qTest test case** from Katalon Studio.  

### Upload test case folder

> **Test cases folder** must be registered in [**Test Case Repositories**](/display/KD/qTest+Integration) before you can upload test cases to qTest.

1. In the **Tests Explorer** view, right-click on the test case folder to trigger its context menu. Select the **qTest > Upload** option.  
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-9-163A343A22.png)  

2.  Once the uploading process finished, you can verify by qTest icon at the bottom right of test case icon as shown below  

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-9-163A413A46.png)  

    Or you can go to qTest to verify that the **Katalon test cases** within the selected folder are uploaded to the integrated **qTest module**.  

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-9-163A453A32.png)

## Download qTest test case

1. Select Test Design in qTest, move any **test cases** to be downloaded into the integrated **qTest module**. Refer to [Enable qTest Integration](/display/KD/Enable+qTest+Integration) for details about setting up an integrated qTest Module in Katalon Studio.  
   
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A483A50.png)  

2. In Tests Explorer of Katalon Studio, right-click on the **test case folder** which is integrated with the **qTest module** above (Refer to [Enable qTest Integration](/display/KD/Enable+qTest+Integration) for more details).
   
   Right-click > **qTest > Download** option from the context menu.
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A513A18.png)  

3. The **Downloaded test case preview** dialog is displayed. All test cases within the integrated **qTest module** that are available for download are listed. Click **OK** to continue.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A523A29.png)
   
   > **Test cases** that are already integrated will **not** be displayed again.

4. Once the downloading process finished, you can view new integrated test cases in Tests Explorer of Katalon Studio.  

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A563A37.png)

## Disintegrate a test case from qTest

Remove the connection between **Katalon test cases** and **qTest test cases**.

1. You have two methods to break the connection between a test case and qTest:

    1.1 Navigate to the **Integration** tab of the test case. Click on the **Disintegrate** button.
       ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2016-11-18-163A453A57.png)  

    1.2 In the Tests Explorer view, **Right-click > qTest > Disintegrate**.
       ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-163A593A5.png)  

2. Click **OK** on the Confirmation dialog. The connection from this test case to qTest will be removed.  

## Disintegrate a test case folder from qTest

You can break the connection between a Katalon Studio test case folder (together with **all** its **test cases**) and qTest system by following the steps below:

1. In the **Tests Explorer** view, right-click on the test case folder. Select the **qTest > Disintegrate**.
   
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-case/image2017-8-5-173A23A57.png)  

2. Click **OK** on the Confirmation dialog. The connection from this folder (and all its test cases) to qTest will be removed.

## Register qTest location for a test suite

The selected **Katalon test suites folder** must be registered in [**Test Suite Repositories** settings](/display/KD/qTest+Integration) before you can upload the test suites within to qTest.

1. Navigate to the **Integration** tab of the test suite. Click on the **New parent** button.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2017-8-6-153A193A52.png)  

2. The **Create Test Suite's parent** dialog is displayed where you can select a **Parent** folder.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-21-153A233A4.png)

    From the test structure, select the location to be integrated with the Katalon test suite then click **OK** to continue. Further options are as following:

    <table><thead><tr><th>Option</th><th>Description</th></tr></thead><tbody><tr><td>Create only</td><td><ul><li>Create an association between the Katalon test suite and the selected qTest location.</li></ul></td></tr><tr><td>Create and upload</td><td><ul><li>Create an association between the Katalon test suite and the selected qTest location.</li><li>Upload the Katalon test suite to the selected qTest location.</li></ul></td></tr><tr><td>Create, upload and set as default</td><td><ul><li>Create an association between the Katalon test suite and the selected qTest location.</li><li>Upload the Katalon test suite to the selected qTest location.</li><li>Set the qTest location as default for uploading the execution result of the Katalon test suite.</li></ul></td></tr></tbody></table>

3. Once integrated, Katalon Studio will provide details information such as location and name of the parent folder on qTest, integration information (Parent IID, Test Suite ID, and Alias) as shown below:

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-21-153A503A3.png)
    
    Where:
    
    | Icon | Description |
    | --- | --- |
    | ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/84.png) | The Katalon test suite is integrated into the qTest location. |
    | ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/85.png) | The Katalon test suite is not integrated into the qTest location. |
    
    If the selected **qTest location** is integrated, then the related information can be viewed in the **Integration Information** section where:
    
    | Field | Description |
    | --- | --- |
    | Test Suite ID | The ID of the integrated qTest test suite. |
    | Alias | The alias of the integrated qTest test suite. |
    | Parent ID | The ID of the integrated qTest location. |
    
4.  You can also quickly navigate to the **qTest parent** folder where the test suite(s) is uploaded by clicking on the **Navigate** button.  

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-21-183A123A57.png)

## Upload test suites to qTest

Katalon Studio test suites are usually uploaded automatically by selected options in **Creation Option** when registering. There is a way to upload Katalon Studio test suite manually. Below instruction shows how to do it for a single test suite or test suite folder:

### Upload a single test suite

1. You have two methods to upload a **test suite** to the predefined **qTest location**:
      
    1.1 Navigate to the **Integration** tab of the test suite. Select a **qTest location** that is yet to be integrated from the **List of test suite's parents** and click on the **Upload** button.  

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-143A103A48.png)  

    1.2. In the Tests Explorer view, right-click on the test suite to trigger its context menu. Select the **qTest > Upload** option.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-143A193A18.png)

    > The **Upload** option is available only when:
    > 
    > \+ There must be **at least one** **registered** qTest location as a **Parent** of Katalon Studio's test suite
    > 
    > \+ Selected qTest location is **NOT** integrated yet.
    > 
    > _Please be cautious_: **Katalon test suite** will be uploaded to all **qTest locations** that meet the above criteria accordingly.

2.  Once the uploading process finishes, you can go to qTest to verify that the **Katalon test suite** is uploaded to the registered **qTest location**.  
      
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-143A343A18.png)

### Upload test suite folder

1.  In the **Tests Explorer** view, right-click on the test suite folder to trigger its context menu. Select the **qTest > Upload** option.
    
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-143A573A33.png)
    
    > The **Upload** option is available only when:
    > 
    > \+ There must be **at least one** **registered** qTest location as a **Parent** of Katalon Studio's test suite
    > 
    > \+ Selected qTest location is **NOT** integrated yet.
    > 
    > _Please be cautious_: **Katalon test suite folder** will be uploaded to all **qTest locations** that meet the above criteria accordingly.
    
2.  Once the uploading process finishes, you can go to qTest to verify that the **Katalon test suites** within the selected folder are uploaded to the registered **qTest locations**.
      
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-173A493A23.png)

## Disintegrate a test suite from qTest

Remove the integration between **Katalon test suites** and its registered **qTest locations**.

1. You have two methods to remove the connection between a test suite and registered qTest locations:

    1.1 Navigate to the **Integration** tab of the test suite. Select a **qTest location** and click on the **Disintegrate** button.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-173A573A5.png)

    1.2 In the Tests Explorer view, right-click on the **test suite** to trigger its context menu. Select the **qTest > Disintegrate** option.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/integrate-test-suite/image2016-11-22-183A33A20.png)  

2. Click **OK** on the Confirmation dialog. The integration between this test suite and all registered qTest locations will be removed.

## Disintegrate a test suite folder from qTest

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
