---
title: "[WebUI] Analyze Test Case Execution Logs and Resolve Errors"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/webui-view-test-case-execution-logs.html
description: 
---

After Test execution, Katalon Studio provides users with comprehensive execution logs in the **Log Viewer**. Users can investigate the logs to quickly troubleshoot and pinpoint root causes of any issue.

This tutorial shows you how to analyze execution logs of a failed Test Case in the **Log Viewer**, and resolve the failure.

Here we reuse the Test Case from the tutorial [[WebUI] Create and Run Web UI Test Case using Record and Playback](https://docs.katalon.com/katalon-studio/tutorials/webui-create-test-case.html).

In our example, the Test Case fails to find a Web element due to an unexpected change of the application under test (AUT). We look for the failed steps in the execution logs, find the root cause, and resolve the failure.

In our example, the log is as follows:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/analyze-test-execution-logs-and-resolve-errors/KS-Log-Viewer-overview.png" width=70% alt="Test Case and test execution">

## Analyze Test execution logs in Log Viewer

Here we use the **Tree View** mode to analyze the logs. This view presents the logs in a structural way that helps users to trace the Test execution and locate the failed steps.

Follow these steps to analyze the logs:

1. Switch to the **Tree View**. Toggle on the **Tree View** button on the top-right corner of the **Log Viewer**.

    The **Tree View** displays the execution logs in a tree-like structure on the left pane and log message of the right pane. Each node in the tree corresponds to a step in the Test Case, and failed steps are highlighted in red.

    [image]

2. To view warning message of the failed step, click on the *expand* icon on the left of the step.

    [image-step-expanded]

3. To view the detailed log message, click on the step. The log message is displayed on the right pane.  

    In our example, the log message shows the root cause of the failed step. The root cause indicates that Katalon Studio cannot locate a Web element using the XPath `'//*[@value = 'Signing_in']'`.

    [image-log-message-failed-steps]

> **Notes**:
>
> * Execution logs of Test Cases are preserved only in the running session of Katalon Studio. Once Katalon Studio is reloaded, the logs will disappear.

## Resovle the failure in the Test Case

After finding the root cause, we navigate to the Test Object containing incorrect XPath and resolve the failure.

Follow these steps:

1. 

> **See also**:
>
> * [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html).