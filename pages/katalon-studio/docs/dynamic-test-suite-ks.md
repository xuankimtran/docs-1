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

    <img src="url" width="70%" alt="Create a dynamic test suite">

2. Fill in the name and the description (optional). Here, we name it **Dynamic Test Suite 1**.

    <img src="url" width="70%" alt="Create a dynamic test suite">

3. Click **OK** when you are done.

## Modify Execution Information

You can specify additional configurations for test suite execution by expanding the **Execution Information** section, as below:

<img src="url" alt="Open the execution information"> 

### Implicit timeout

In the **Implicit timeout** section, you can decide the timeout period that Katalon Studio waits for a page to be loaded by choosing one of the following options:

<img src="url" alt="Set implicit timeout">

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

   <img src="url" alt="retry after executing all" width=60%>

For example, when a test suite execution fails, we want to rerun failed test cases in that test suite two times.

In the **Retry after executing all** checkbox, we input `2` in the text field, then we choose the **Retry failed executions only** option.

You can see in the following picture, the test suite is executed 3 times in total. The first one is the main execution, the later two are the retried executions when the first execution fails. 

<img src="url" alt="retry after executing all" width=60%>

Katalon automatically generates reports after each test execution. 

<img src="url" alt="retry after executing all" width=60%>

### Mail Recipients

> Requirements:
> * You have configured a mail server, an email template, and a default recipient list in **Project > Settings > Email**. To learn more about configuring email settings, you can refer to this document: [Email settings](https://docs.katalon.com/katalon-studio/docs/execution-settings.html#emails-settings). 

Katalon allows you to add an additional list of recipients to recieve reports in a specific dynamic test suite.
To do so, in the **Mail Recipients** text field, input the email that you want to send the reports to.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/email.png" alt="email recipients" width=70%>

> Notes:
>
> The default recipient list in email settings and the additional list in a dynamic test suite can receive the same test reports after the test suite execution.  

## Manage test case list

### Enable the query provider

When you implement the dynamic test suite for the first time, the **Query Provider** is set to **No query provider available** by default.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-querying-test-suite/dynamic-ts.png" width="100%" alt="dynamic test suite">

To enable the query provider for the dynamic test suite, install one of the plugins from the Katalon Store:

* [Basic search for dynamic test suite](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite)
* [Test case management with tags](https://store.katalon.com/product/6/Test-Case-Management-with-Tags)
* [TestRail integration](https://store.katalon.com/product/13/TestRail-Integration)

To activate the installed plugin, navigate to Account Settings in Katalon Studio and click **Reload Plugin**.

After successfully activating the plugin, the **Query Provider** automatically applies the query syntax of the installed plugin. For example, after activting the **Basic search for dynamic test suite** plugin, the **Query Provider** is set to **Built-in**. You can now add test cases for dynamic test suite execution.

### Add test cases to a dynamic test suite

There are 2 main ways to add test cases into a dynamic test suite. You can add test cases via search query or use the **Query Builder** function.

1. Add test cases via search query.

To add test cases via search query, manually input the search condition into the **Query** box. Then hit **Preview** to query out the matching test cases.
For example: To add the **DDT at TC level** test case into this dynamic test suite, you can input `id=(Test Cases/DDT at TC level)` into the **Query** box. The matched test case appears in the test suite.

To learn more about the search query syntax, you can refer to this document: [Search test cases](https://docs.katalon.com/katalon-studio/docs/search.html).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Dynamic-Test-suite.png" width="100%" alt="Results after searching query">

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

For example, we want to add all test cases that name contains `Chrome` into the dynamic test suite. 
After opening the **Query Builder** dialog, input `Chrome` into the **Name** test field. Then hit **Search**.

<img src="url" width="100%" alt="Input Chrome into the Query Builder dialog">

Katalon finds three test cases in the current project that name contains `Chrome`.

<img src="url" width="100%" alt="search query">