---
title: "Test Suite" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/create-test-suite.html 
redirect_from:
    - "/katalon-studio/docs/create-test-suite/"
    - "/katalon-studio/docs/design-a-test-suite.html"
    - "/display/KD/Design+a+Test+Suite/"
    - "/display/KD/Design%20a%20Test%20Suite/"
    - "/x/mAvR/"
    - "/katalon-studio/docs/design-a-test-suite/"
    - "/katalon-studio/docs/dynamic-test-suite.html"
    - "/katalon-studio/docs/dynamic-querying-test-suite/"
    - "/katalon-studio/docs/dynamic+querying+test+suite/"
    - "/katalon-studio/docs/dynamic%20querying%20test%20suite/"
    - "/katalon-studio/docs/test-suite.html/"
    
description:
---
A Test Suite is a collection of multiple different or duplicate test cases.

## Create a new Test Suite

To create a new Test Suite, do as follows:

1. From the menu bar, select **File > New > Test Suite**

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/test-suite-1.png)

2. Fill in the name of the test suite and the description (optional).

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/New-test-suite-window.png)

3. Click **OK** when you are done.

Alternatively, you can create a new Test Suite after creating a Test Case. In a Test Case, click the **Add to test suite** button.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/Test-suite-2.png)

You can choose to add that test case to an **existing** or a **new** test suite.

## Modify Execution Information

You can specify additional configurations for test suite execution by expanding the **Execution Information** section, as below:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-2-15-143A493A29.png)

## Implicit timeout

In **Implicit timeout**, you can decide the timeout period that Katalon Studio waits for a page to be loaded by choosing one of the following options:
<ul>
   <li><strong>Use default</strong>: Use the predefined default value</li>
   <li><strong>User define (in seconds)</strong>: Set a custom waiting time. Input a value in seconds.</li>
</ul>

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-2-15-143A563A48.png">

## Retry

Using the **Retry** feature, you can configure when and how many times Katalon retries an execution of a Test Suite before the Test Suite finishes executing.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/retry.png" alt="retry after executing all" width=60%>

### Retry Failed Execution Immediately

By default, each Test Case is run only one time in a Test Suite execution. Suppose you want to rerun a failed Test Case several times to identify flaky before executing the next ones. You can set the desired number of retry times in **Retry Failed Execution Immediately**. The failed test case will be rerun immediately until they pass or all retries are used up. If all rerun attempts fail, Katalon Studio marks that Test Case as **Failed** and proceeds with the rests in the Test Suite.

   >**Requirements**
   >
   > - An active Katalon Studio Enterprise license
   > - A Test Suite

   **Usage example**
   
   In this example, we have a Test Suite with five Test Cases. We set **Retry Failed Execution Immediately** for one time. When we run the Test Suite, and a test fails, Katalon Studio immediately reruns the problematic test case until it passes or a one-time retry is reached.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/ts-with-5-tc-and-retry-fail-1.png" width=70%>

   You can see the Test Suite status once the Test Suite finishes executing. Because Test Case 3 fails, we open the **Result** tab and collapse Test Case 3 for investigating. It fails two times with 1 is the main run and 2 is the retry time that has been used up (one time). Since the test result pattern in Test Case 3 fails intermittently, it is likely to be flaky. At this point, Katalon Studio logs its final result as Failed and continues to execute Test Case 4 and 5 with the same logic.

   You can get how many Test Cases in the Test Suite were executed and their final status in the **Summary** tab. In this use case, the Test Suite has five total Test Cases, three of them pass and two fail.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/retry-usage-example-result.png" width=85%>
   
   **Consolidate Reports**

   > **Requirements**
   >
   > - Katalon Studio version 8.1.0 onwards
   > 
   > - Only applicable to the **Retry Failed Execution Immediately** functionality

   From version 8.1.0 onwards, Katalon Studio automatically consolidates reports in JUnit, HTML, PDF, and CSV format with one final test result for a Test Case. Browser-based or window-based videos are recorded for runs and reruns of a Test Case.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/reports.png" width=80%>

### Retry After Executing All

   In **Retry after executing all**:

   * **Retry All executions**: Retry all executions when the Test Suite fails.
   * **Retry Failed executions only**: Retry only failed executions when the Test Suite fails.

### Mail Recipients

You can add a list of recipients who will receive execution reports via email once the test suite finishes its execution.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/email.png" alt="email recipients" width=70%>

There's also another list of recipients who will receive all the reports from Katalon by default. Refer to [Emails Settings](https://docs.katalon.com/katalon-studio/docs/execution-settings.html#emails-settings) for more details.

## Manage Test Case List

There are several ways to add Test Cases into Test Suites. You can drag and drop the Test Case into Test Suites or using the Test Suite editor to manually add the test case.

> Test Cases can be duplicated in the same Test Suite.

Open a test suite, then select the option to add **Add Test Case** from the command toolbar.  
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-2-15-143A333A40.png)

All test cases in Katalon Studio are displayed in the **Test Case Browser** dialog for you to select your preferred options. The selected test cases are added to the test case list accordingly.  

> The checkbox at the end of the test case row is checked by default. It means that the test case is executed when you run a test suite.

## Dynamic Test Suite (Dynamic Test Cases List)

**Dynamic Test Suite** is a test suite in which a collection of multiple test cases are added to NOT in a manual way but via a [search query](https://docs.katalon.com/katalon-studio/docs/search.html). This feature only works when you have already installed the plugin that defines the querying syntax. In case there is no installed plugin, the Query Provider is set to “No query provider available.” by default.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-querying-test-suite/dynamic-ts.png" width="100%" alt="dynamic test suite">

Currently, there are three plugins from Katalon Store, which enable this feature by providing query search function and returning any matched test cases or test suites of the query statement.

* [Basic Search For Dynamic Test Suite](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite).
* [Test Case Management with Tags](https://store.katalon.com/product/6/Test-Case-Management-with-Tags). [Learn more](https://store.katalon.com/product/13/TestRail-Integration).
* [TestRail Integration](https://store.katalon.com/product/13/TestRail-Integration). [Learn more](https://docs.katalon.com/katalon-studio/docs/testrail-integration.html).

After installing one of those plugins, go to Katalon Studio and click **Reload Plugins**. [Learn more about how to reload plugins](https://docs.katalon.com/katalon-store/docs/user/access-store-in-KS.html#reload-plugins).

**Query Provider**: The query syntax standard of a plugin that is currently applied. For example, when you successfully install the *Basic Search For Dynamic Test Suite* plugin, the query syntax standard becomes "Built-in".

**Query**: This search box allows you to input the query syntax manually. For example,
`id=(Test Cases/Simple Examples/Katalon Shop/Custom-keyword samples/Order and check out a single product)`.

**Query Builder** provides a convenient way to create and run a query in Katalon Studio.

- **Id**: to search by the exact IDs of a test artifact.
- **Name**: to search by the name of a test artifact.
- **Tag**: to search by the tag linked to test artifacts.
- **Comment**: to search by the comments attached to test artifacts.
- **Description**: to search by the description associated with test artifacts.

*Note*: Search criteria are applied to all test artifacts, including test case, test suite, folder, and etc.

**Preview**: View the results after having the searching query.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-querying-test-suite/result.png" width="100%" alt="search querry">

## Execute a Test Suite

Open a test case/test suite, then select an environment to run the test case from **Run** command of the main toolbar.

> If you click on the **Run** button, the test case is executed using the default browser defined in [Execution Settings](/display/KD/Execution+Settings).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/environment.png" width=310>

* **Browsers**: Select one of the supported browsers, including Chrome, Firefox, IE (for Windows only), Safari, or Edge Chromium, Chrome (headless), and Firefox (headless).
* **Mobile Devices**: Select one of the listed devices (Android or iOS).

  Before executing your test, check if you have set up the environment for mobile testing for <a href="/display/KD/Mobile+on+Windows">Windows</a> or for <a href="/display/KD/Mobile+on+macOS">macOS</a>.

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2018-1-26-183A543A41.png">

  > Troubleshooting
  >
  > If there is no device listed, please make sure the Developer Mode on the phone is turned on, try to unplug, and reconnect several times until you are prompted to accept/trust this device.
  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2018-8-2-153A313A52.png">

* **Windows**: Select this option if you are executing tests on a desktop application.
* **Remote**: Make sure you have set up the default configuration for the remote environment in project settings. Refer to&nbsp;<a href="/display/KD/Introduction+to+Desired+Capabilities">Introduction to Desired Capabilities</a>&nbsp;for more details.
* **Custom**: Make sure you have set up the default configuration for the remote environment in project settings. Refer to&nbsp;<a class="external-link" href="/x/cgFO#ExecutionSettings-CustomExecution" rel="nofollow">Custom Execution</a>&nbsp;for more details. When you have set up your custom environment, select it from the drop-down list.

The Job Progress is triggered automatically to show the progress while your test case/test suite is being executed.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2017-6-30-203A543A25.png)

> See also [Execute the test case using console mode](/display/KD/Console+Mode+Execution).

## Submit and view test results on Katalon TestOps

You can centralize test results including logs and attachments on [Katalon TestOps](/katalon-studio/docs/katalon-analytics-beta-integration.html). Besides test results management, Katalon TestOps will also provide analytics to improve the quality of your test cases.