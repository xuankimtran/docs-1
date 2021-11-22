---
title: "[WebUI] Analyze Test Case Execution Logs and Resolve Errors"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/webui-analyze-test-case-execution-logs-and-resolve-errors.html
description: 
---

After executing a Test Case, Katalon Studio provides users with comprehensive execution logs in the **Log Viewer**. Users can investigate the logs to troubleshoot and pinpoint the root causes of any issue quickly.

This tutorial shows you how to analyze execution logs of a failed Test Case in the **Log Viewer** and resolve the error.

Here we reuse the Test Case ("Sign in the shopping page to purchase a tank top") from the tutorial [[WebUI] Create and Run Web UI Test Case using Record and Playback](https://docs.katalon.com/katalon-studio/tutorials/webui-create-test-case.html).

> You can download the sample project here: [Shopping Cart Tests](https://github.com/katalon-studio-samples/shopping-cart-tests).

In our example, the Test Case fails to find a Web element due to an unexpected change in the application under test (AUT). We look for the failed steps in the execution logs, find the root cause, and correct the step.
## Analyze Test execution logs in Log Viewer

After executing the Test Case, Katalon Studio displays the results in the **Log Viewer** as follows:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Execution-Results.png" width=70% alt="Test Execution overview">

Here we use the **Tree View** mode of the **Log Viewer** to analyze the logs. This mode displays execution logs in a structural way that helps users trace the Test execution and locate failed steps quickly.

Follow these steps to analyze the logs:

1. Switch to the **Tree View**. Toggle on the **Tree View** button on the top-right corner of the **Log Viewer**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Tree-View-Button.png" width=30% alt="Tree View button">

    The **Tree View** displays the execution logs in a tree-like structure on the left pane. Each node in the tree corresponds to a step in the Test Case, and failed steps are marked in red.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Log-Viewer-Tree-View.png" width=70% alt="Tree View Structure">

    On the right pane, the view displays detailed log messages of each step.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Log-Viewer-Log-Message-Overview.png" width=70% alt="Log Message Pane">

2. To view warning messages of the failed step, click on the *expand* icon on the left of the step.
 
    Here the warnings indicate that Katalon Studio fails to find a Test Object with a specific XPath.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Log-Viewer-Warnings.png" width=70% alt="Log Message Pane">

3. To view the detailed log message, click on the step. The log message is displayed on the right pane.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Log-Viewer-Click-on-step.png" width=70% alt="Tree View Click on step">

    In the root cause section, the message shows an exception: `com.kms.katalon.core.webui.exception.WebElementNotFoundException: Web element with id ... not found.`

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Log-Viewer-Root-cause-section.png" width=70% alt="Root cause section">

    > To learn how to troubleshoot common exceptions in Web tests, you can refer to this document: [Troubleshoot common exceptions when executing web tests](https://docs.katalon.com/katalon-studio/docs/troubleshoot-common-execution-exceptions-web-test.html).

    Below the root cause section, the message displays the failed step in the form of Test Script.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Log-Viewer-Error-Script.png" width=70% alt="Error Script">

    From the details provided, we know that Katalon Studio cannot locate the sign-in button with the id `'Object Repository/Page_Zack Market/input_Password_button_btn__2lzmo'` and the Object Locator `//*[@value = 'Signing_in']`.

> **Notes**:
>
> * Execution logs of Test Cases are preserved only in the running session of Katalon Studio. Once you reload Katalon Studio, the logs will disappear.

## Resolve the error in the Test Case

After finding the root cause, we navigate the Test Object with incorrect XPath and update the Object Locator.

Follow these steps:

1. Navigate to the Test Object. In the log message of the failed step, click on the displayed Object ID.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Log-Viewer-Click-on-Object.png" width=70% alt="Click on Object in Log Message pane">

    Here Katalon Studio navigates to the Test Object with the deprecated Object Locator.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Log-Viewer-Navigated-Object.png" width=70% alt="Navgiated Object with incorrect locator">

2. Update the Object Locator.

    Because a change in the AUT causes the error, we can update the Object Locator by re-recording the Test Case with the **Web Recorder**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Recording-Test-Case.png" width=70% alt="Navgiated Object with incorrect locator">

3. After re-recording the Test Case, verify that the Test Object is updated.

    Here the Object Locator is updated with new properties and XPath.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Updated-Object.png" width=70% alt="Updated Object locator">

4. Run the Test Case and verify the successful Test execution in the **Log Viewer**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-test-executions-and-resolve-errors/KS-Successful-Test-Execution.png" width=70% alt="Successful Test Execution">

> **See also**:
>
> * [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html).