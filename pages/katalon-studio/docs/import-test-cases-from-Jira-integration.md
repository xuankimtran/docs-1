---
title: "Execute test cases with Jira Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/execute-test-cases-with-jira-integration.html
redirect_from:
description:
---

With Jira intergration, you can import test cases from both Jira Cloud and Jira Server to Katalon Studio for creating test cases, and run BDD tests. After the test suite execution, Katalon automatically submit test results and test reports to the linked Jira issue.

> Prerequisites:
>
> * An active Katalon Studio Enterprise license.
> * Install the Jira Integration plugin. You can download the plugin from Katalon Store here: [Jira Intergration](https://store.katalon.com/product/3/Jira-Integration) 
> * Install the Katalon Studio and TestOps integration plugin. You can download the plugin from the Atlassian Marketplace website: [Katalon Studio and TestOps integration](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira) for Jira from Atlassian Marketplace.

In this article, we demonstrate how to execute test cases imported from Jira, then view the test results in the linked Jira ticket after the test suite execution. 

## Execute Test Cases with Jira Intergration
### Import Test Cases from Jira

Katalon Studio allows you to import test cases from Jira and link Jira issues to Katalon. Follow these steps:

1. From the Katalon toolbar, select **Jira Integration <img src="url" width=70% alt="Jira Intergration icon"> > Import Test Case from JIRA JQL**. A **Import Test Case from JIRA** dialog opens.

    <img src="url" width=70% alt="Import test case from Jira">

2. In the opened dialog:

   - Fill the JQL query of the desired test case in the **Jira JQL** box. To find out JQL query of your test case, you can refer to the Atlassian document here: [Search for issues using JQL](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html)

        For example: We want to import test case TDAP-46 from the Jira board. After searching for the Jira ticket using JOL query, copy and paste the JOL query into the **Jira JQL** box:
            <img src="url" width=70% alt="JOL query from Jira">  
            <img src="url" width=70% alt="Copy and paste JOL query into the Jira JQL">


   - By default, the **Import BDD feature files** box is selected. This option allows you to import BDD feature files to run BDD tests. To learn more about BDD testing, you can refer to this document here: [BDD Testing Framework (Cucumber Intergration)](https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html#set-default-package-for-step-definitions.)

3. In the displayed **Test Case Folder Selection** window, select the destination to store the issues. Click **OK**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/save_test_cases.png" width=50% alt="Choose the destination for Jira test cases">

4. In the **Linked Jira Issues** window, click **OK**. If your test cases have already been linked to a JIRA ticket, you can not sync them again.

    <img src="url" width=70% alt="Link the Jira issue">

Katalon opens a new test case with:

- The Test Case name is the Jira ticket's summary/subject.
- The Test Decription is the Jira ticket's content.
- With the selected **Import BDD feature files** box, Katalon creates a new feature file in **Include\Feature** with the same name as the test case. Its content is from Jira BDD. A **Run Feature File** step is also added in the test script.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/bdd2.png" width=70% alt="Link the Jira issue">

### Import BDD custom field from Jira Cloud

For Jira Cloud intergration, besides from importing BDD feature files, you can also import the Jira custom fields to Katalon Studio. To learn more about the custom field in Jira, you can refer to the Atlassian document here: [Adding a custom field](https://confluence.atlassian.com/adminjiraserver071/adding-a-custom-field-802592519.html).

Follow these steps:

1. Go to **Project > Settings > Plugins > Jira**.
2. In the **Fetch Options** section, select **Enable retrieving content of the specified custom field**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/jira-bdd-78.png" width=70%>

3. Select a custom field from the list. Click **Fetch Custom Fields** to fetch the list from the connected Jira Cloud Server.

> Note: Only existing custom field ID is valid for this configuration.

4. Click **Apply and Close** to apply your settings. The custom field’s content is displayed in **Include\Feature**. 

### Run Test Cases 

After importing the test case from Jira, hit **Run** to run the test case.
## View Test Results in Jira

To view test results in Jira, follow these steps:
1. Add the associated test cases to a test suite. 
2. After a test suite execution, open the linked Jira ticket, click **Open Test Results** in the **Details** group.

<img src="url" width=70% alt="Click on the Open test results in the Jira issue">

Katalon Studio automatically uploads a test result to the integrated Jira issue. You can view the test result and its attachments you have predefined in **Project > Settings > Jira**.

<img src="url" width=70% alt="See results of test case in the Jira issue">

> Note
>
> Katalon Studio test execution status can be queried via [JQL](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html). The syntax is as following:
>
>```groovy
>"Katalon Status"=<status>
>```
> For example, to search for all issues that have failed in Katalon Studio test execution, type `"Katalon Status"=FAIL` in the search bar. Katalon Studio supports five test status: **Passed**, **Failed**, **Incomplete**, **Error** and **Skip**.

## Submit an issue to Jira

After executing a test suite, you can submit a ticket to Jira from Katalon. 

> Note:
> 
> You can only submit Jira tickets from test reports.

Follow these steps:

1. In the **Test Explorer** panel, go to **Reports**, double-click to open the test reports you want to review for issues. 
2. In the opened test report, click **Bug** <img src="url" width=70% alt="Bug icon">. A **Linked Jira issues** dialog opens.

    <img src="url" width=70% alt="Jira intergration in test cases table">

3. In the opened dialog, click **Add** to choose your submit options.

    <img src="url" width=70% alt="Choose your submit options">

The ticket submission options include:

<table>
<thead>
<tr>
<th>Option</th>
<th>Description</th>
<th>Steps to take&nbsp;</th>
</tr>
</thead>
<tbody>
<tr>
<td>Create as New</td>
<td>To create a new ticket on Jira.</td>
<td>
<p>After choosing this option:</p>
<p>1. A&nbsp;<strong>JIRA native submission form </strong>opens in the pop-up browser<strong>.&nbsp;</strong>You might be prompt to sign in to your Atlassian account. You only have to do this once.</p>
<p>2 After signing in, fill in the&nbsp;<strong>JIRA native submission form&nbsp;</strong>to submit the ticket.</p>
</td>
</tr>
<tr>
<td>Create as Sub Issue</td>
<td>To create a sub-task for an existing Jira issue.</td>
<td>
<p>After choosing this option:</p>
<p>1. A <strong>Create as JIRA Sub Task </strong>dialogopens. Fill in the&nbsp;<strong>ID</strong>&nbsp;of an existing Jira issue to create a sub-task within. Click&nbsp;<strong>OK&nbsp;</strong>to open&nbsp;<strong>JIRA native submission form.</strong></p>
<p>2. You might be prompt to sign in to your Atlassian account. You only have to do this once.</p>
<p>- After signing in, fill in the&nbsp;<strong>JIRA native submission form&nbsp;</strong>to submit the ticket.</p>
</td>
</tr>
<tr>
<td>Link to existing Issue</td>
<td>This option will add the execution details of the test to an existing JIRA issue. You will be asked to provide the <strong>ID</strong> of the existing JIRA issue for this.</td>
<td>
<p>After choosing this option:&nbsp;</p>
<p>- A <strong>Link to JIRA Issue</strong> dialog opens. Fill in the&nbsp;<strong>ID</strong>&nbsp;of an existing Jira issue. Click&nbsp;<strong>OK.&nbsp;</strong>The test case execution .zip files&nbsp;will be attached to the linked JIRA Issue.</p>
</td>
</tr>
</tbody>
</table>

> Note:
> 
> * The default **JIRA native submission form** might include the **Summary**, **Screenshots**, **Logs**, **Reports**, and **Description** of the test case. You can configure the default submission form from the **Submit Options** section in the Jira integration settings.
> * To quickly navigate to a linked JIRA issue, click the hyperlink embbeded in the ticket's ID. 
> 
> <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/katalon_studio_integration_with_jira_overview/Linked-JIRA-issues1.png" width=70% alt="Jira Issues Hyperlink">
