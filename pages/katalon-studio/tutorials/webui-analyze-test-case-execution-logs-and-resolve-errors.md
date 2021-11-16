---
title: "[WebUI] Analyze Test Case Execution Logs and Resolve Errors"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/webui-analyze-test-case-execution-logs-and-resolve-errors.html
description: 
---

After executing a Test Case, Katalon Studio provides users with comprehensive execution logs in the **Log Viewer**. Users can investigate the logs to troubleshoot and pinpoint the root causes of any issue quickly.

This tutorial shows you how to analyze execution logs of a failed Test Case in the **Log Viewer** and resolve the error.

Here we reuse the Test Case ("Sign in the shopping page to purchase a tank top") from the tutorial [[WebUI] Create and Run Web UI Test Case using Record and Playback](https://docs.katalon.com/katalon-studio/tutorials/webui-create-test-case.html).

In our example, the Test Case fails to find a Web element due to an unexpected change in the application under test (AUT). We look for the failed steps in the execution logs, find the root cause, and correct the step.

The execution logs are as follows:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/analyze-test-execution-logs-and-resolve-errors/KS-Test-Execution-overview.png" width=70% alt="Test Execution logs">

## Analyze Test execution logs in Log Viewer

Here we use the **Tree View** mode of the **Log Viewer** to analyze the logs. This view presents the logs in a structural way that helps users trace the Test execution and locate the failed steps.

Follow these steps to analyze the logs:

1. Switch to the **Tree View**. Toggle on the **Tree View** button on the top-right corner of the **Log Viewer**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/analyze-test-execution-logs-and-resolve-errors/KS-Log-Viewer-Tree-View-button.png" width=30% alt="Tree View button">

    The **Tree View** displays the execution logs in a tree-like structure on the left pane and the log message on the right. Each node in the tree corresponds to a step in the Test Case, and failed steps are marked in red.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/analyze-test-execution-logs-and-resolve-errors/KS-Log-Viewer-Tree-View.png" width=70% alt="Tree View">

2. To view warning messages of the failed step, click on the *expand* icon on the left of the step.

    Here the warnings indicate that the Test Case fails to find a Test Object with a specific XPath.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/analyze-test-execution-logs-and-resolve-errors/KS-Log-Viewer-Expanded-warnings.png" width=70% alt="Failed Step warnings">

3. To view the detailed log message, click on the step. The log message is displayed on the right pane.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/analyze-test-execution-logs-and-resolve-errors/KS-Log-Viewer-Log-Message.png" width=70% alt="Log message pane">

    In our example, the log message shows that Katalon Studio cannot locate the sign-in button with the id `'Object Repository/Page_Zack Market/input_Password_button_btn__2lzmo'` and the locator `'//*[@value = 'Signing_in']'`. The error is caused by a UI change in the AUT.

    > Learn more about common exceptions in Web tests here: [Troubleshoot common exceptions when executing web tests](https://docs.katalon.com/katalon-studio/docs/troubleshoot-common-execution-exceptions-web-test.html).

> **Notes**:
>
> * Execution logs of Test Cases are preserved only in the running session of Katalon Studio. Once you reload Katalon Studio, the logs will disappear.

## Resolve the error in the Test Case

After finding the root cause, we navigate the Test Object with incorrect XPath and update the Object Locator.

Follow these steps:

1. Navigate to the Test Object. In the log message of the failed step, click on the displayed Object ID.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/analyze-test-execution-logs-and-resolve-errors/KS-Log-Viewer-click-on-object.png" width=70% alt="Log message pane">

    Katalon Studio will navigate to the selected Test Object.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/analyze-test-execution-logs-and-resolve-errors/KS-Failed-Test-Object.png" width=70% alt="Log message pane">

2. Update the Object Locator.

    Because a change in the AUT causes the error, we can update the Object Locator by re-recording the Test Case with the **Web Recorder**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/analyze-test-execution-logs-and-resolve-errors/KS-Web-Recorder.png" width=70% alt="Log message pane">

3. After re-recording the Test Case, verify that the Test Object is updated.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/analyze-test-execution-logs-and-resolve-errors/KS-Updated-Object.png" width=70% alt="Updated Object">

4. Run the Test Case and verify the results in the **Log Viewer**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/analyze-test-execution-logs-and-resolve-errors/KS-Updated-Test-case.png" width=70% alt="Log message pane">


> **See also**:
>
> * [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html).