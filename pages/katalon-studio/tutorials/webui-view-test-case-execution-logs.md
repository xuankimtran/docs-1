---
title: "[WebUI] View Test Case Execution Logs"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/webui-view-test-case-execution-logs.html
description: 
---

The **Log Viewer** in Katalon Studio provides users with comprehensive reports of Test runs to quickly troubleshoot and pinpoint root causes of any issue.

This tutorial shows you how to view logs of Test Case execution using the **Log Viewer**.

## View Test execution logs in Log Viewer

You can use the **Log Viewer** in two modes: **Tabular View** and **Tree View**.

To switch between the two modes, in the top-right corner of the **Log Viewer**, toggle the **Tree View** button.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-test-case-execution-logs/KS-Log-Viewer-Tabular-View-toggle-button.png" width=70% alt="Log Viewer Toggle button">

### Using Tabular View

The **Tabular View** displays execution logs in the form of rows with different statuses. 

Follow these steps to view the Test execution logs: 

1. Filter the logs in the test execution. In the **Execution Filter** section, select the filter options of your choice.

    In our example, we filter the failure logs by selecting the **Failed** option.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-test-case-execution-logs/KS-WebUI-Log-Viewer-Tabular-View-filter.png" width=70% alt="Log Viewer Tabular View filtered results">

    Using the filter options, you can specify what type of logs to be displayed.

    <table>
    <thead>
    <tr>
    <th>Filter</th>
    <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>All</td>
    <td>Show all the log messages.</td>
    </tr>
    <tr>
    <td>Info</td>
    <td>Show only the log messages for information/reference.</td>
    </tr>
    <tr>
    <td>Passed</td>
    <td>Show only the log messages indicating that a step is successfully executed.</td>
    </tr>
    <tr>
    <td>Failed</td>
    <td>Show only the log messages indicating that a test step fails to execute.</td>
    </tr>
    <tr>
    <td>Error</td>
    <td>Show only the log messages indicating that some error has occurred at a given step.</td>
    </tr>
    <tr>
    <td>Warning</td>
    <td>Show only the log messages indicating that a test step is failed but accepted as a warning.</td>
    </tr>
    <tr>
    <td>Not Run</td>
    <td>Show only the log messages indicating that a test step is skipped.</td>
    </tr>
    </tbody>
    </table>

2. To view a log message, double-click on the log. The message is displayed in the **Log's Properties** dialog.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-test-case-execution-logs/KS-Log-Viewer-Log-Properties-dialog.png" width=70% alt="Log Viewer Tabular View filtered results">

### Using Tree View

The **Tree View** displays execution reports in the form of a tree on the left pane and detailed log messages on the right pane. Each node in the tree corresponds to a step in a Test Case.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-test-case-execution-logs/KS-Log-Viewer-Tree-View-overview.png" width=70% alt="Log Viewer Tree View results">

1. To view the log message of a step, click on the corresponding node. The detailed message is displayed on the right pane.

    In our example, the failure log message indicates a specific root cause.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-test-case-execution-logs/KS-Log-Viewer-Tree-View-failed-step.png" width=70% alt="Log Viewer Tree View log message">

2. To navigate from a node to a specific step in the **Script** View, right-click on the node and select **Go to this step in Script View**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-test-case-execution-logs/KS-Log-Viewer-Tree-View-right-click.png" width=70% alt="Log Viewer Tree View log message">

> **Notes**:
>
> * Test execution logs of Test Cases are preserved only in the running session of Katalon Studio. Once Katalon Studio is reloaded, the execution logs will disappear.

> **See also**:
>
> * [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html).