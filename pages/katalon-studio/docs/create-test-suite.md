---
title: "Test Suite" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/create-test-suite.html 
redirect_from:
    - "/katalon-studio/docs/design-a-test-suite.html"
    - "/display/KD/Design+a+Test+Suite/"
    - "/display/KD/Design%20a%20Test%20Suite/"
    - "/x/mAvR/"
    - "/katalon-studio/docs/design-a-test-suite/"
    - "/katalon-studio/docs/test-suite.html/"
    
description:
---
A Test Suite is a collection of multiple different or duplicate test cases.

This guide shows you how to configure and create a Test Suite.

## Create a new Test Suite

To create a new Test Suite, do as follows:

1. From the menu bar, select **File > New > Test Suite**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/file-new-test-suite.png" alt="create new test suite" width="100%">

2. Fill in the **Name** of the test suite and the **Description** (optional).

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/new-test-suite.png" alt="add test suite name" width="70%">

3. Click **OK** when you are done.

   Alternatively, you can create a new Test Suite after creating a Test Case. In a Test Case, click the **Add to test suite** button.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/add-to-test-suite.png" alt="add to test suite" width="100%">

You can choose to add that test case to an **existing** or a **new** test suite.

## Modify Execution Information

You can specify additional configurations for test suite execution by expanding the **Execution Information** section, as below:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/execution-information.png" alt="execution information" width="50%">

## Implicit timeout

In **Implicit timeout**, you can decide the timeout period that Katalon Studio waits for a page to be loaded by choosing one of the following options:
<ul>
   <li><strong>Use default</strong>: Use the predefined default value</li>
   <li><strong>User define (in seconds)</strong>: Set a custom waiting time. Input a value in seconds.</li>
</ul>

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/implicit-timeout.png" alt="implicit timeout" width="60%">

## Retry

Using the **Retry** feature, you can configure when and how many times Katalon retries an execution of a Test Suite before the Test Suite finishes executing.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/retry.png" alt="retry after executing all" width=65%>

### Retry Failed Execution Immediately

By default, each Test Case is run only one time in a Test Suite execution. Suppose you want to rerun failed Test Cases several times to identify flaky tests before executing the next ones. You can set the desired number of retry times in **Retry Failed Execution Immediately**. The failed test case will be rerun immediately until they pass or all retries are used up. If all rerun attempts fail, Katalon Studio marks that Test Case as **Failed** and proceeds with the rest in the Test Suite.

   >**Requirement**
   >
   > - An active Katalon Studio Enterprise license

**Consolidate Reports**

   From version 8.1.0 onwards, Katalon Studio automatically consolidates reports in JUnit, HTML, PDF, and CSV format with one final test result for a Test Case. Browser-based or window-based videos are recorded for runs and reruns of a Test Case.

**Usage example**
   
   In this example, we have a Test Suite with five Test Cases. We set **Retry Failed Execution Immediately** for one and two times. When we run the Test Suite and a test fails, Katalon Studio immediately reruns the problematic test case until it passes or the maximum number of retries is reached.

- **Example 1**: Execute the Test Suite with a Retry limit of 1:

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/ts-with-5-tc-and-retry-fail-1.png" width=65%>

   You can see the Test Suite status once the Test Suite finishes executing. Because Test Case 3 is marked as **Failed**, we open the **Result** tab and expand Test Case 3 to investigate. 
      
   Test Case 3 failed twice, once during the main run and once as a retried run. Only one retried run was allowed. 
      
   At this point, Katalon Studio logged its final result as **Failed** and continued to execute Test Case 4 and 5 with the same logic.

   You can view how many Test Cases in the Test Suite were executed and their final status in the **Summary** tab. In this use case, the Test Suite has five total Test Cases; Test Cases 1, 2, and 4 pass while 3 and 5 fail.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/retry-usage-example-result.png" width=85%>

 - **Example 2**: Execute the Test Suite with a Retry limit of 2:

   When we set the retry limit to 2, five Test Cases passed. Test Cases 3 and 5 failed at the main run and first rerun but passed at the second try. 

   Since Test Cases 3 and 5 did not succeed on the first try but still succeed after two tries, their result pattern is intermittent. This is a clear sign of test flakiness and can be further investigated.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/retry-2-times-result.png" width=85%>

### Retry After Executing All

   In **Retry after executing all**:

   * **Retry All executions**: Retry all executions when the Test Suite fails.
   * **Retry Failed executions only**: Retry only failed executions when the Test Suite fails.

### Mail Recipients

To send test summary reports via email, first you need to configure the [Email Settings](https://docs.katalon.com/katalon-studio/docs/execution-settings.html#emails-settings). You need to set up a mail server, an email template, and a default recipient list.

Once configured, you can add an additional list of recipients for a specific Test Suite report.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/email.png" alt="email recipients" width=70%>

> Notes:
>
> The default recipient list in Email settings and the additional list in a Test Suite can receive the same test reports after the Test Suite execution.  

## Manage Test Case List

There are several ways to add Test Cases into Test Suites. You can drag and drop the Test Case into Test Suites or use the Test Suite editor to manually add the test case.

> Test Cases can be duplicated in the same Test Suite.

Open a test suite, then select the option to add **Add Test Case** from the command toolbar.  

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/add-test-case.png" alt="add test case" width="70%">

All test cases in Katalon Studio are displayed in the **Test Case Browser** dialog for you to select your preferred options. The selected test cases are added to the test case list accordingly.  

> The checkbox at the end of the test case row is checked by default. It means that the test case is executed when you run a test suite.
## Execute a Test Suite

Open a test case/test suite, then select an environment to run the test case from **Run** command of the main toolbar.

> If you click on the **Run** button, the test case is executed using the default browser defined in [Execution Settings](/display/KD/Execution+Settings).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/run-option.png" width=50% alt="run option">

* **Browsers**: Select one of the supported browsers, including Chrome, Firefox, IE (for Windows only), Safari, or Edge Chromium, Chrome (headless), and Firefox (headless).
* **Mobile Devices**: Select one of the listed devices (Android or iOS).

  Before executing your test, check if you have set up the environment for mobile testing for <a href="/display/KD/Mobile+on+Windows">Windows</a> or for <a href="/display/KD/Mobile+on+macOS">macOS</a>.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android/device.png" alt="mobile device" width="70%">

  > Troubleshooting
  >
  > If there is no device listed, please make sure the Developer Mode on the phone is turned on, try to unplug, and reconnect several times until you are prompted to accept/trust this device.
  >
  > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/device-troubleshoot.png" alt="troubleshooting" width="70%">

* **Windows**: Select this option if you are executing tests on a desktop application.
* **Remote**: Make sure you have set up the default configuration for the remote environment in project settings. Refer to&nbsp;<a href="/display/KD/Introduction+to+Desired+Capabilities">Introduction to Desired Capabilities</a>&nbsp;for more details.
* **Custom**: Make sure you have set up the default configuration for the remote environment in project settings. Refer to&nbsp;<a class="external-link" href="/x/cgFO#ExecutionSettings-CustomExecution" rel="nofollow">Custom Execution</a>&nbsp;for more details. When you have set up your custom environment, select it from the drop-down list.

The Job Progress is triggered automatically to show the progress while your test case/test suite is being executed.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/job-progress.png" alt="job progress" width="100%">

> See also [Execute the test case using console mode](/display/KD/Console+Mode+Execution).

## Submit and view test results on Katalon TestOps

You can centralize test results including logs and attachments on [Katalon TestOps](/katalon-studio/docs/katalon-analytics-beta-integration.html). Besides test results management, Katalon TestOps will also provide analytics to improve the quality of your test cases.
