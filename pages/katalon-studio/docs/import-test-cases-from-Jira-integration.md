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

In this article, we demonstrate how to import test cases from Jira, then view the test results in the linked Jira ticket after the test suite execution. 
## Import Test Cases from Jira

Katalon Studio allows you to import test cases from Jira and link Jira issues to Katalon. Follow these steps:

1. From the Katalon toolbar, select **Jira Integration <img src="url" width=70% alt="Jira Intergration icon"> > Import Test Case from JIRA JQL**. A **Import Test Case from JIRA** dialog opens.

    <img src="url" width=70% alt="Import test case from Jira">

2. In the opened dialog:

   - Fill the JQL query of the desired test case in the **Jira JQL** box. To find out JQL query of your test case, you can refer to the Atlassian document here: [Search for issues using JQL](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html)

        For example: We want to import test case TDAP-46 from the Jira board. After searching for the Jira ticket using JOL query, copy and paste the JOL query into the **Jira JQL** box:
            <img src="url" width=70% alt="JOL query from Jira">  
            <img src="url" width=70% alt="Copy and paste JOL query into the Jira JQL">


   - By default, the **Import BDD feature files** box is selected. This option allows you to import BDD feature files to run BDD tests from Jira. 

3. In the displayed **Test Case Folder Selection** window, select the destination to store the issues. Click **OK**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/save_test_cases.png" width=70% alt="Choose the destination for Jiratest cases">

4. In the **Linked Jira Issues** window, click **OK**. If your test cases have already been linked to a JIRA ticket, you can not sync them again.

    <img src="url" width=70% alt="Link the Jira issue">

Katalon opens a new test case with:

- Test case name: The Jira ticket summary/subject
- Test Decription: The Jira ticket content
- With the selected **Import BDD feature files** box, Katalon creates a new feature file with the same name as the test case. Its content is from Jira BDD. A **Run Feature File** step is also added in the test script.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/bdd2.png" width=70% alt="Link the Jira issue">

## Import BDD custom field from Jira Cloud

When importing Jira tickets with BDD feature files from Jira Cloud, you can also import the Jira custom field to Katalon Studio. To learn more about the custom field in Jira, you can refer to the Atlassian document here: [Adding custom fields](https://confluence.atlassian.com/adminjiraserver/adding-custom-fields-1047552713.html).

Follow these steps:

1. Go to **Project > Settings > Plugins > Jira**.
2. In the **Fetch Options** section, select **Enable retrieving content of the specified custom field**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/jira-bdd-78.png" width=70%>

3. Select a custom field from the list. Click **Fetch Custom Fields** to fetch the list from the connected Jira Cloud Server.

> Note: Only existing custom field ID is valid for this configuration.

4. Click **OK** to apply your settings. The custom field’s content will be displayed in **Include\Feature**. 

## View Test Results in Jira

> Katalon can only upload test results after a test suite execution.


After a test suite execution, Katalon Studio automatically uploads a test result to the integrated Jira issue. You can view the test result and its attachments (if you have predefined in Project Settings) in Jira.

<img src="url" width=70% alt="Link the Jira issue">

> Note
>
> Katalon Studio test execution status can be queried via [JQL](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html). The syntax is as following:
>
>```groovy
>"Katalon Status"=<status>
>```
> For example, to search for all issues that have failed in Katalon Studio test execution, type `"Katalon Status"=FAIL` in the search bar. Katalon Studio supports five test status: **Passed**, **Failed**, **Incomplete**, **Error** and **Skip**.
