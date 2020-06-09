---
title: "Install and Use Katalon BDD custom field in Jira Cloud" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/BDD-field-jira-cloud.html 
redirect_from:
    - "/katalon-studio/docs/BDD-field-jira-cloud/"
description: 
---

## Prerequisites

- The [Jira App](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira) has been installed.

## Install the Katalon BDD add-on

To add the **Katalon BDD** custom field to Jira Cloud, from **Jira settings** -> Select **Apps**-> Select **Find new apps** -> Enter **“BDD Katalon”** in Filter apps-> **Get app**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/1-enter-Katalon-BDD.png)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/2-install.png)

## Create the Katalon BDD custom field

+ From **Jira settings** -> Select **Issues** ->in FIELDS tab, select **Custom fields -> Add custom field**.
+ Select a Field Type: **_Text Field (multi-line)._** Remember to associate it with issue types you want.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/3-field-type.png)

+ Provide a name and its description -> **Create**.
+ Associate the custom field to multiple screens by checkbox.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/4-screens.png)

## Enable the Katalon add-on and custom field

In **Project settings** -> Scroll down to the bottom then select **Katalon BDD** -> Select the field you’ve created, then Click **Add** -> Select issue types to show this field with BDD editor -> Click **Save**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/5-enable.png)

## Try the BDD editor

In the selected issue, you need to enable the **Katalon BDD Fields**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/6-KBDD.png)

To edit content in Katalon BDD  Field, click the pencil icon and write a Gherkin content, then click the check icon. Make sure the content starts with `Feature`.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/7-gherkin.png)

## View Katalon Studio Test Execution Result right on Jira

Once Jira is integrated with Katalon Studio and the add-on is enabled in Jira Cloud, a panel called TEST RESULT inside the issue page enables users to directly view the test result. In the new view of the issue page, just click **Test Result**. The result includes the execution status (PASSED, FAILED, INCOMPLETE, ERROR) and test artifact attachments (e.g. logs, screenshots, etc.).

> Note: In Katalon Studio, the test case imported from Jira should be executed in Test Suite to view the test result.



## Use JQL Syntax to query all issues with a particular execution status

Katalon Studio's test execution status can be queried via [JQL](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html). The syntax is as follows:

`"Katalon Status"="STATUS"`

For example, to search for the issues with *PASSED* status

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/passed.png)