---
title: "[WebUI] View and Analyze Test Case Execution Logs"
sidebar: katalon_studio_docs_sidebar
permalink: 
description: 
---

The **Log Viewer** in Katalon Studio provides users with comprehensive reports of Test runs to quickly troubleshoot and pinpoint root causes of any issue.

This tutorial shows you how to view and analyze logs of Test Case execution using the **Log Viewer**.

## Analyze Test execution logs in Log Viewer

You can use the **Log Viewer** in two modes: **Tabular View** and **Tree View**.

To switch between the two modes, in the top-right corner of the **Log Viewer**, toggle the **Tree View** button.

[image]

### Using Tabular View

The **Tabular View** displays execution logs in the form of rows with different statuses. 

Follow these steps to analyze the Test execution logs: 

1. Filter the logs in the Test excution. In the **Execution Filter** section, select the filter options of your choice.

    In our example, we filter the failure logs by selecting the **Failed** option.

    [image]

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

    [image]

### Using Tree View

The **Tree View** displays execution reports in the form of nodes on the left pane, and log messages on the right pane. Each node corresponds to a step in a Test Case.

    [image]

1. To view the log message of a step, click on the coressponding node. The detailed message is displayed on the right pane.

    In our example, the failure log message indicates a specific root cause.

    [image]

2. To navigate to a specific step in the **Script** View, right-click on a node and select **Go to this step in Script View**. 

    [image]

> **Notes**:
>
> * Test execution logs of Test Cases are preserved only in the running session of Katalon Studio. Once Katalon Studio is reloaded, the execution logs  will disappear.

> **See also**:
>
> * [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html).