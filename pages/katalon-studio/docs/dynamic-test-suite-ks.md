---
title: "Dynamic test suite in Katalon Studio" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/dynamic-test-suite-ks.html 
redirect_from:
description:
---

A dynamic test suite is a test suite with multiple test cases added via a search query. You can dynamically add additional test cases while running the test suite. 
This article shows you how to configure and create a dynamic test suite.

## Create a dynamic test suite

To create a new Test Suite, do as follows:

1. From the menu bar, select **File > New > Dynamic Test Suite**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Create-a-new-dynamic-test-suite.png" width="70%" alt="Create a dynamic test suite">

2. Fill in the name and the description (optional). Here, we name it **Dynamic Test Suite 1** and leave the description blank.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Name-the-test-suite.png" width="70%" alt="Create a dynamic test suite">

3. Click **OK**.

## Modify Execution Information

You can specify additional configurations for test suite execution by expanding the **Execution Information** section.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Open-execute-information.png" width="45%" alt="Open the execution information"> 

### Implicit timeout

In the **Implicit timeout** section, you can decide the timeout period that Katalon Studio waits for a page to be loaded by choosing one of the following options:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Implicit-timeout.png" alt="Set implicit timeout">

<table>
<thead>
  <tr>
    <th>Options</th>
    <th>Description</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Use default</td>
    <td>Use the predefined value set in <strong>Project &gt; Settings &gt; Execution &gt; Default wait for element timeout (in seconds)</strong>.</td>
  </tr>
  <tr>
    <td>User define (in seconds)</td>
    <td>Set a custom waiting time. Input a value in seconds.</td>
  </tr>
</tbody>
</table>

### Retry after executing all

Katalon allows you to rerun test cases in a failed test suite execution to identify flaky tests.

To do so, in the **Retry after executing all** text field, set the desired number of retry times. By default, this is set to `0`.

Choose one of the following options:

   * **Retry all executions**: Retry all test cases when the test suite fails.
   * **Retry failed executions only**: Retry only failed test cases when the test suite fails.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Retry-options.png" alt="retry after executing all" width=50%>

For example, when a test suite execution fails, we want to rerun failed test cases in that test suite two times.

In the **Retry after executing all** checkbox, we input `2` in the text field, then we choose the **Retry failed executions only** option.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Set-up-retry-2-times.png" alt="retry after executing all" width=50%>

In this case, the test suite is executed three times in total. The first one is the main execution; the latter two are the retried executions when the first execution fails. 

<a class="pop">
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Retry-2-times.png" alt="retry after executing all" width=100%>
</a>
<p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

Katalon automatically generates reports after each test execution. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Reports-retry-2-times.png" alt="retry after executing all" width=60%>

### Mail Recipients

> Requirements:
> * You have configured a mail server, an email template, and a default recipient list in **Project > Settings > Email**. To learn more about configuring email settings, you can refer to this document: [Email settings](https://docs.katalon.com/katalon-studio/docs/execution-settings.html#emails-settings). 

Katalon allows you to add an additional list of recipients to receive reports in a specific dynamic test suite.
To do so, in the **Mail Recipients** text field, input the email that you want to send the reports to.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/email.png" alt="email recipients" width=70%>

> Notes:
>
> The default recipient list in email settings and the additional list in a dynamic test suite can receive the same test reports after the test suite execution.  

## Manage test case list

### Enable the query provider

When you implement the dynamic test suite for the first time, the **Query Provider** is set to **No query provider available** by default.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-querying-test-suite/dynamic-ts.png" width="100%" alt="dynamic test suite">

To enable the query provider for the dynamic test suite, install one of the following plugins from the Katalon Store:

* [Basic search for dynamic test suite](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite)
* [Test case management with tags](https://store.katalon.com/product/6/Test-Case-Management-with-Tags)
* [TestRail integration](https://store.katalon.com/product/13/TestRail-Integration)

To activate the installed plugin, navigate to Account Settings in Katalon Studio and click **Reload Plugin**.

After you successfully activate the plugin, the **Query Provider** automatically applies the query syntax of the installed plugin. For example, after activating the **Basic search for dynamic test suite** plugin, the **Query Provider** is set to **Built-in**. You can now add test cases for dynamic test suite execution.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Query-provider-after-installing-plugin.png" width="100%" alt="Results after installing plugins">

### Add test cases to a dynamic test suite

There are two main ways to add test cases into a dynamic test suite. You can add test cases via a search query or the **Query Builder** function.

1. Add test cases via the search query.

To add test cases via the search query, manually input the search condition into the **Query** box. Then hit **Preview** to query out the matching test cases.
For example, to add the **DDT at TC level** test case into this dynamic test suite, you can input `id=(Test Cases/DDT at TC level)` into the **Query** box. The matched test case appears in the test suite.

To learn more about the search query syntax, you can refer to this document: [Search test cases](https://docs.katalon.com/katalon-studio/docs/search.html).

<a class="pop">
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Dynamic-Test-suite.png" width="100%" alt="Results after searching query">
</a>
<p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

2. Add test cases via the **Query Builder** function.

**Query Builder** provides a convenient way to create and run a query in Katalon Studio.
To open the **Query Builder** function, in the dynamic test suite view, click **Query Builder**. The **Query Builder** dialog appears. Input your search criteria, then click **Search**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/search/query-builder-dialog.png" alt="query dialog" width="70%">

The **Query Builder** dialog includes:

- **Id**: to search by the exact IDs of a test artifact.
- **Name**: to search by the name of a test artifact.
- **Tag**: to search by the tag linked to test artifacts.
- **Comment**: to search by the comments attached to test artifacts.
- **Description**: to search by the description associated with test artifacts.


> Notes: 
> * Every field in this Query Builder mode can be applied to search for all types of test artifacts such as test cases, test suites, folders, etc.
> * You can only search for one keyword at a time when searching by tag, description, or comment.

For example, we want to add all test cases whose name contains `Chrome` into the dynamic test suite. 
After opening the **Query Builder** dialog, input `Chrome` into the **Name** text field. Then hit **Search**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Find-test-cases-named-chrome.png" width="70%" alt="Input Chrome into the Query Builder dialog">

Katalon finds three test cases in the current project whose name contains `Chrome`.

<a class="pop">
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-test-cases-named-chrome.png" width="100%" alt="search query">
</a>
<p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

## Execute a dynamic test suite

After adding test cases to the dynamic test suite, from the main toolbar, click **Run**. The test case is executed with the default browser defined in **Project > Settings > Execution > Default execution**. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Click-run.png" alt="The Run dropdown list">

Alternatively, you can choose the environment in the dropdown list next to **Run**. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Run-dropdown-list.png" alt="The Run dropdown list">

The **Job Progress** bar is triggered automatically to show the progress while your test case/test suite is being executed.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-progress-bar.png" alt="The Run dropdown list">

You can also run the dynamic test suite in console mode. For detailed instructions on running a test execution in console mode, you can refer to this document: [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).

## Test Reports

After the test suite execution, to view your test reports, go to the **Reports** folder in the **Test Explorer** panel. 

<a class="pop">
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Open-built-in-report.png" width="100%" alt="Reports">
</a>
<p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

Alternatively, you can also view your reports and details in `<your-project-folder>/Reports`. Katalon Studio supports exporting test reports into different formats, such as HTML, CSV, PDF, and JUnit. You can learn more about exporting reports here: [Generate reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html#automatically-generate-reports).

> Notes:
> * For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

**See also**

* [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html#view-execution-log)