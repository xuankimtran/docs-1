---
title: "Configure Jira BDD Settings"
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-studio/docs/bdd-settings.html
redirect_from:
    - "katalon-studio/docs/install-and-use-katalons-jira-add-on.html"
    - "katalon-studio/docs/BDD-field-jira-cloud.html"
    - "katalon-analytics/docs/bdd-settings.html"
---
Katalon Studio provides a free Jira add-on to help create a seamless integration. This add-on gives you several benefits:

* Sync test cases written in Gherkin and test execution results; and query issues based on testing status.
* Dynamic perspectives and an insightful look at your automation testing data.
* Progress tracking for better test management.

> Requirements:
> * The **Katalon Studio and TestOps integration** plugin installed in Jira. You can download the plugin from the Atlassian Marketplace website here: [Katalon Studio and TestOps integration](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira?hosting=cloud&tab=overview).
> * Jira Integration with Katalon TestOps enabled. To enable Jira Integration with Katalon TestOps, follow the steps in this document: [TestOps - Jira Integration](https://docs.katalon.com/katalon-analytics/docs/kt-jira-config.html).

## Jira Server

> Only availabe for Jira Server Version

This add-on adds a custom field type to Jira called the **Katalon Gherkin** custom field. This custom field lets you write descriptions for your test cases and stories in Gherkin syntax. Gherkin keywords such as _Given_, _When_, _Then_ will be highlighted automatically. 

To create the Katalon Gherkin custom field, please follow the instructions from the Atlassian document here: [Project screens, schemes and fields](https://confluence.atlassian.com/adminjiraserver071/project-screens-schemes-and-fields-802592517.html).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-and-use-katalons-jira-add-on/field-config-marked.png" width=50% alt="Create the Katalon Gherkin">

Once imported to Katalon Studio, the content of the Katalon Gherkin field is in the test cases description.  

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/TO-JIRA-View-results-on-Jira-Gherkin.png" width=70% alt="Results after linking the Katalon Gherkin">

## Jira Cloud

You can also add a Katalon BDD custom field into your ticket with Jira Cloud Intergration. Follow these steps:
### Create the Katalon BDD custom field

1. From **Jira settings** -> Select **Issues** ->in the **FIELDS** tab, select **Custom fields -> Add custom field**.
2. Select a Field Type: **_Text Field (multi-line)._** Remember to associate it with the issue types you want.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/3-field-type.png" width=50% alt="Add the BDD custom field">


3. In the new custom field window, provide a name and description -> Click **Create**.
4. Associate the custom field to multiple screens by checkbox.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/4-screens.png" width=50% alt="Choose screens for the BDD custom fields">

### Enable the Katalon add-on and custom field

In **Project settings** -> Scroll down to the bottom then select **Katalon BDD** -> Select the field you’ve created, then Click **Add** -> Select issue types to show this field with BDD editor -> Click **Save**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/5-enable.png" width=50% alt="Choose the BDD custom fields for Katalon BDD">

### Try the BDD editor

In the selected issue, you need to enable the **Katalon BDD Fields**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/6-KBDD.png" width=50% alt="Enable the Katalon BDD field">


To edit content in Katalon BDD  Field, click the pencil icon and write a Gherkin content, then click the check icon. Make sure the content starts with `Feature`.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/7-gherkin.png" width=50% alt="Edit the BDD field">


## View Katalon Studio Test Execution Result on Jira

Once Jira is integrated with Katalon Studio and the add-on is enabled in Jira Cloud, a panel called TEST RESULT inside the issue page enables users to directly view the test result. In the new view of the issue page, just click **Test Result**. The result includes the execution status (PASSED, FAILED, INCOMPLETE, ERROR) and test artifact attachments (e.g. logs, screenshots, etc.).

> Note: In Katalon Studio, the test case imported from Jira should be executed in Test Suite to view the test result.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Open-test-results-2.png" width=70% alt="Click on the Open test results in the Jira issue">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-View-results-on-Jira.png" width=70% alt="See results of test case in the Jira issue">

## Related topics

- [View BDD Test Results in Katalon TestOps](/katalon-analytics/docs/bdd-test-results.html)