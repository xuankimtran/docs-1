---
title: "[WebUI] View and Analyze Test Case Execution Logs"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/webui-view-test-case-execution-logs.html
description: 
---

During Test execution, Katalon Studio provides users with comprehensive execution logs in the **Log Viewer**. Users can investigate the logs to quickly troubleshoot and pinpoint root causes of any issue.

This tutorial shows you how to view execution logs of a Test Case, analyze the logs, and resolve the failed steps using the **Log Viewer**.

## View Test execution logs in Log Viewer

The **Log Viewer** offers two view modes: **Tabular View** and **Tree View**.

The **Tree View** presents the Test execution logs in a structural way that illustrates to how a Test Case is organized, which helps users to trace the Test execution and locate the errors.

In our example, we use the **Tree View** to view the logs.

Follow these steps:

1. Switch to the **Tree View**. Toggle on the **Tree View** button on the top-right corner of the **Log Viewer**.

    Here the **Tree View** displays the execution logs in the form of a tree on the left pane, and detailed log message of the right pane. Each node in the tree corresponds to a step in the Test Case, and failed steps are highlighted in red.

    [image]

2. To view details of a step, click on the *carat* icon on the left.

    Here **Tree View** displays relevant warnings of the failed steps.

    [image-step-expanded]

3. To view log message of a step, click on the step. 

    In our example, the log message shows the root cause of the failed step.

    [image-log-message-failed-steps]

## Resovle errors in Test Cases

From the 

The **Tree View** displays execution logs in the form of a tree on the left pane and detailed log messages on the right pane. Each node in the tree corresponds to a step in a Test Case.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-test-case-execution-logs/KS-Log-Viewer-Tree-View-overview.png" width=70% alt="Log Viewer Tree View results">

1. To view the log message of a step, click on the corresponding node. The detailed message is displayed on the right pane.

    In our example, the failure log message indicates a specific root cause. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-test-case-execution-logs/KS-Log-Viewer-Tree-View-failed-step.png" width=70% alt="Log Viewer Tree View log message">

2. To navigate from a node to a specific step in the **Script** View, right-click on the node and select **Go to this step in Script View**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-test-case-execution-logs/KS-Log-Viewer-Tree-View-right-click.png" width=70% alt="Log Viewer Tree View log message">

> **Notes**:
>
> * Execution logs of Test Cases are preserved only in the running session of Katalon Studio. Once Katalon Studio is reloaded, the logs will disappear.

> **See also**:
>
> * [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html).