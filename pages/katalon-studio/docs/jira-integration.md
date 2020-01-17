---
title: "Jira Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/jira-integration.html
redirect_from:
    - "/katalon-studio/docs/BDD-field-jira-cloud/"
    - "/katalon-studio/docs/install-and-use-katalons-jira-add-on/"
    - "/katalon-studio/docs/configure-jira-integration/"
    - "/katalon-studio/docs/working-with-jira/"

description:
----
## Configure Jira integration

Install [Jira integration plugin](https://store.katalon.com/product/3/Jira-Integration) from Katalon Store to use this feature.

Learn how to install and use the plugin [here](https://docs.katalon.com/katalon-studio/docs/jira-plugin-integration.html).

## Install and Use Katalon's Jira add-on from Atlassian Marketplace

Katalon Studio provides a free Jira add-on to help create a seamless integration. This add-on gives you several benefits:

* Adding a Gherkin custom field to help you design your test case in a consistent and concise way. The content will be populated right into your Katalon Studio automation scripts automatically.
* Presenting the latest execution result and artifacts right inside the issue page.
* Looking up Katalon Studio execution result status using Jira's JQL syntax.

### Installation

> Install Katalon BDD - Test Automation for Jira [here](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira?hosting=cloud&tab=overview).

Currently, we only support Jira server. To install the add-on, please follow [Atlassian's instruction](https://marketplace.atlassian.com/plugins/com.katalon.katalon-jira-plugin/server/installation).

### Gherkin custom field


> Only availabe for Jira Server Version

This add-on adds a custom field type to Jira called Katalon Gherkin. This custom field lets you write descriptions for your test cases and stories in Gherkin syntax. Gherkin keywords such as _Given_, _When_, _Then_ will be highlighted automatically. Once imported to Katalon Studio, the content of Katalon Gherkin field will be populated into test cases description.  

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-and-use-katalons-jira-add-on/katalon-jira-plugin-1-field-marked.png)  

  

To create Katalon Gherkin custom field, please follow [Atlassian's instruction](https://confluence.atlassian.com/adminjiraserver071/project-screens-schemes-and-fields-802592517.html).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-and-use-katalons-jira-add-on/field-config-marked.png)  

Katalon Studio Test Execution Status
------------------------------------

Once integrated, Katalon Studio BDD's will present the latest execution result inside the issue page. The result includes the status (PASSED, FAILED, INCOMPLETE, ERROR) and links to the associated artifacts (e.g. logs, screenshots etc.).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-and-use-katalons-jira-add-on/katalon-jira-plugin-1-status-marked.png)  

JQL Syntax
----------

Katalon Studio test execution status can be queried via [JQL](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html). The syntax is as following:

```groovy
"Katalon Status"=<status>
```

Where Status value can be one of the following:

| Status | Description |
| --- | --- |
| PASSED | The automation tests that executed successfully. |
| FAILED | The automation tests that failed to execute at certain steps. |
| INCOMPLETE | The automation tests that did not finish running all the steps due to other factors such as wrong syntax, power shortage, disconnected network, etc. |
| ERROR | The automation tests that have some errors occurred. |

For example, to search for all issues that have failed in Katalon Studio test execution_:_

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-and-use-katalons-jira-add-on/katalon-jira-plugin-2.png)


## Install and Use Katalon BDD custom field in Jira Cloud

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

### View Katalon Studio Test Execution Result right on Jira

Once Jira is integrated with Katalon Studio and the add-on is enabled in Jira Cloud, a panel called TEST RESULT inside the issue page enables users to directly view the test result. In the new view of the issue page, just click **Test Result**. The result includes the execution status (PASSED, FAILED, INCOMPLETE, ERROR) and test artifact attachments (e.g. logs, screenshots, etc.).

> Note: In Katalon Studio, the test case imported from Jira should be executed in Test Suite to view the test result.



### Use JQL Syntax to query all issues with a particular execution status

Katalon Studio's test execution status can be queried via [JQL](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html). The syntax is as follows:

`"Katalon Status"="STATUS"`

For example, to search for the issues with *PASSED* status:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/passed.png)

