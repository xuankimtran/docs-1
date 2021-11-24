---
title: "[WebUI] Analyze Test Execution Logs and Debug the Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/webui-analyze-test-case-execution-logs-and-resolve-errors.html
description: 
---

After executing a Test Case, Katalon Studio provides users with comprehensive execution logs in the **Log Viewer**. Users can quickly investigate the logs to pinpoint the root causes of any issue and correct the Test execution with Debug utilities in Katalon Studio.

This tutorial shows you how to analyze execution logs of a failed Test Case in the **Log Viewer** and debug the Test Case.

Here we reuse the Test Case ("Sign in the shopping page to purchase a tank top") from the tutorial [[WebUI] Create and Run Web UI Test Case using Record and Playback](https://docs.katalon.com/katalon-studio/tutorials/webui-create-test-case.html).

> You can download the sample project here: [Shopping Cart Tests](https://github.com/katalon-studio-samples/shopping-cart-tests).

In our example, the Test Case fails to find a Web element due to an unexpected change in the application under test (AUT). We look for the failed steps in the execution logs, find the root cause, correct the step, and resume execution using the **Run from here** Debug utility.

> **Notes**:
>
> To use the Debug utility, you need to configure Katalon Studio to NOT terminate browser session when execution finishes. For detailed instructions, refer to this guide: [Execute and Debug a Test Case](https://docs.katalon.com/katalon-studio/docs/execute-a-test-case-or-a-test-suite.html#debug-run-from-here).
## Analyze Test execution logs in Log Viewer

After executing the Test Case, Katalon Studio displays the results in the **Log Viewer** as follows:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Execution-Results.png" width=70% alt="Test Execution overview">

Here we use the **Tree View** mode of the **Log Viewer** to analyze the logs. This mode displays execution logs in a structural way that helps users trace the Test execution and locate failed steps quickly.

Follow these steps to analyze the logs:

1. Switch to the **Tree View**. Toggle on the **Tree View** button on the top-right corner of the **Log Viewer**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Tree-View-Button.png" width=30% alt="Tree View button">

    The **Tree View** displays the execution logs in a tree-like structure on the left pane. Each node in the tree corresponds to a step in the Test Case, and failed steps are marked in red.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Log-Viewer-Tree-View.png" width=70% alt="Tree View Structure">

    On the right pane, the view displays detailed log messages of each step.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Log-Viewer-Log-Message-Overview.png" width=70% alt="Log Message Pane">

2. To view warning messages of the failed step, click on the *expand* icon on the left of the step.

    Here the warnings indicate that Katalon Studio fails to find a Test Object with a specific XPath.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Log-Viewer-Warnings.png" width=70% alt="Log Message Pane">

3. To view the detailed log message, click on the step. The log message is displayed on the right pane.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Log-Viewer-Click-on-step.png" width=70% alt="Tree View Click on step">

    In the root cause section, the message shows an exception: `com.kms.katalon.core.webui.exception.WebElementNotFoundException: Web element with id ... not found.`

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Log-Viewer-Root-cause-section.png" width=70% alt="Root cause section">

    > To learn how to troubleshoot common exceptions in Web tests, you can refer to this document: [Troubleshoot common exceptions when executing web tests](https://docs.katalon.com/katalon-studio/docs/troubleshoot-common-execution-exceptions-web-test.html).

    Below the root cause section, the message displays the failed step in the form of Test Script.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Log-Viewer-Error-Script.png" width=70% alt="Error Script">

    From the details provided, we know that Katalon Studio cannot locate the sign-in button with the id `'Object Repository/Page_Zack Market/input_Password_button_btn__2lzmo'` and the Object Locator `//*[@value = 'Signing_in']`.

> **Notes**:
>
> * Execution logs of Test Cases are preserved only in the running session of Katalon Studio. Once you reload Katalon Studio, the logs will disappear.

## Debug the Test Case

After finding the root cause, we navigate the Test Object with incorrect XPath, update the Object with a new XPath, and use the **Run from here** Debug utility to resume the Test execution.
### Update the Object Locator using the Browser Inspector

Because a deprecated Object Locator causes the error, we can get a new Object Locator using the browser's **Inspector** tool.

In our example, we use the **Inspector** tool to get the XPath of the corresponding Web element.

Follow these steps:

1. To get the new XPath, in the running browser instance, right-click on the target web element, and select **Inspect**.

    Here we right-click on the Sign-in button that causes the error.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Browser-right-click-on-element.png" width=70% alt="Error Script">

2. In the inspector window, the selected element is highlighted, indicating the target element's location in the HTML DOM. Right-click on the highlighted line and select **Copy > Copy XPath**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Copy-XPath.png" width=70% alt="Error Script">

3. Add the new XPath to the Test Object. Open the Test Object, in the Test Object view, specify **XPath** as the **Selection Method** and paste the copied XPath from step 2 in the **Selected Locator** editor.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Add-new-XPath.png" width=70% alt="Error Script">
### Resume the Test execution

After adding the new XPath to the Test Object, we use the **Run from here** Debug utility to resume Test execution without re-executing the entire Test Case.

Follow these steps to resume the Test execution:

1. Resume executing from the failed step. Open the Test Case, right-click on the failed step, and select **Run from here** > *The running browser session*.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Run-from-here.png" width=70% alt="Error Script">

2. After the Test execution is completed, verify the results in the Log Viewer.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-analyze-execution-logs-and-debug/KS-Successful-Test-Execution.png" width=70% alt="Error Script">

> **See also**:
>
> * [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html).