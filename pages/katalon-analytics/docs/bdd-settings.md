---
title: "Configure Jira BDD Settings"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/bdd-settings.html
redirect_from:
    - "/katalon-studio/docs/bdd-settings.html"
---
Katalon Studio provides a free Jira add-on to help create a seamless integration. This add-on gives you several benefits:

* Sync test cases written in Gherkin and test execution results; and query issues based on testing status.
* Dynamic perspectives and an insightful look at your automation testing data.
* Progress tracking for better test management.

## Jira Server

### Installation

> Install Katalon BDD - Test Automation for Jira [here](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira?hosting=cloud&tab=overview).

To install the add-on, please follow [Atlassian's instruction](https://marketplace.atlassian.com/plugins/com.katalon.katalon-jira-plugin/server/installation).

### Gherkin custom field

> Only availabe for Jira Server Version

This add-on adds a custom field type to Jira called Katalon Gherkin. This custom field lets you write descriptions for your test cases and stories in Gherkin syntax. Gherkin keywords such as _Given_, _When_, _Then_ will be highlighted automatically. Once imported to Katalon Studio, the content of Katalon Gherkin field will be populated into test cases description.  

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-and-use-katalons-jira-add-on/katalon-jira-plugin-1-field-marked.png)  
 

To create Katalon Gherkin custom field, please follow [Atlassian's instruction](https://confluence.atlassian.com/adminjiraserver071/project-screens-schemes-and-fields-802592517.html).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-and-use-katalons-jira-add-on/field-config-marked.png)

## Jira Cloud

### Install and Use Katalon BDD custom field in Jira Cloud

A new version of the Katalon BDD Add-on for Jira Cloud which supports BDD editor is available [here](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira?hosting=cloud&tab=overview). 

### Install the Katalon BDD add-on

To add the **Katalon BDD** custom field to Jira Cloud, from **Jira settings** -> Select **Apps**-> Select **Find new apps** -> Enter **“BDD Katalon”** in Filter apps-> **Get app**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/1-enter-Katalon-BDD.png)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/2-install.png)

### Create the Katalon BDD custom field

+ From **Jira settings** -> Select **Issues** ->in FIELDS tab, select **Custom fields -> Add custom field**.
+ Select a Field Type: **_Text Field (multi-line)._** Remember to associate it with issue types you want.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/3-field-type.png)

+ Provide a name and its description -> **Create**.
+ Associate the custom field to multiple screens by checkbox.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/4-screens.png)

### Enable the Katalon add-on and custom field

In **Project settings** -> Scroll down to the bottom then select **Katalon BDD** -> Select the field you’ve created, then Click **Add** -> Select issue types to show this field with BDD editor -> Click **Save**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/5-enable.png)

### Try the BDD editor

In the selected issue, you need to enable the **Katalon BDD Fields**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/6-KBDD.png)

To edit content in Katalon BDD  Field, click the pencil icon and write a Gherkin content, then click the check icon. Make sure the content starts with `Feature`.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/7-gherkin.png)

### View Katalon Studio Test Execution Result on Jira

Once Jira is integrated with Katalon Studio and the add-on is enabled in Jira Cloud, a panel called TEST RESULT inside the issue page enables users to directly view the test result. In the new view of the issue page, just click **Test Result**. The result includes the execution status (PASSED, FAILED, INCOMPLETE, ERROR) and test artifact attachments (e.g. logs, screenshots, etc.).

> Note: In Katalon Studio, the test case imported from Jira should be executed in Test Suite to view the test result.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-and-use-katalons-jira-add-on/katalon-jira-plugin-1-status-marked.png) 


## Related topics

- [View BDD Test Results in Katalon TestOps](/katalon-analytics/docs/bdd-test-results.html)