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
## Working with Jira

Prerequisites:
* Install [Jira Integration plugin](https://store.katalon.com/product/3/Jira-Integration) for Katalon Studio from Katalon Store.
* Install [Katalon BDD app](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira) for Jira from Atlassian Marketplace.

### Configure Jira integration 

You need to enable JIRA Integration in order to submit issues to JIRA. This setting is available at **Project > Settings > Integration > JIRA**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/config.png)
1.  Select **Enable integration** option. The settings will be available for configuration.

  * Jira Cloud
    * *Server URL* must be in the form *https://<site_name>.atlassian.net*.
    * Use a Atlassian Cloud's API token for *Password*. See instructions [here](https://confluence.atlassian.com/cloud/api-tokens-938839638.html).

  * Jira Server
    * *Server URL* must be in the form *http(s)://domain* without any trailing parts e.g. */secure*.
    * Use username instead of email for *Username*.

2.  Specify information regarding your JIRA Server and login credential then click **Connect** button.


3.  After successfully authenticating with JIRA, all relevant **JIRA Projects** and **Issue Types** will be retrieved and displayed under **Submit Options**. You can specify the default project and issue type for submission here.

The fields for setting include:

| Field | Description |
| --- | --- |
| Default JIRA Project | The default JIRA project to submit tickets. |
| Default JIRA Issue Type | The default JIRA Issue type to create when submitting tickets. |
| Use Test Case name as Summary for JIRA ticket | The Katalon Test Case Name will be used as a summary for submitted tickets. |
| Attach Screenshot to JIRA ticket | Any taken screenshot during execution will be included in submitted tickets. |
| Attach Log to JIRA ticket | The execution log will be included in submitted tickets. |

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/image2016-11-3-133A533A20.png)


4.  Click **OK** button to complete the JIRA Integration setup.

### Integrate Test Case

1. Prepare [ Jira JQL Script]( https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html )
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/image2017-8-2-113A393A33.png)

2. Open **Jira Integration** > click Import Test Case from JIRA JQL
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/image2017-8-2-113A233A49.png)

3. Enter the Jira JQL. Click **OK**.
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/image2017-8-2-113A413A34.png)

4. The **Test Case Folder Selection** window will appear. Choose the destination to store the issues. Click **OK**.
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/save_test_cases.png)

5. The **Jira Issues** window will appear. Click **OK**.
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/image2016-11-3-143A413A132.png)

If your test cases have already been linked to a JIRA ticket, Katalon Studio will not sync them again.

### Import BDD Feature Files

**Jira Integration** also allows you to import Jira BDD Feature Files to Katalon Studio.

When importing test cases from Jira, please check **Link to BDD Feature File** &gt; **OK** &gt; Choose the destination to store the issues.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/sample.png)

A new Feature File (with the same name as the test case) will be created with the content from Jira BDD. Moreover, a RunFeature step will be created in the linked test case to Jira.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/bdd2.png)

### View Test Results on Jira

After you have successfully integrated test cases, test execution results will be automatically created in the associated Jira ticket. Review the status and attachments of Katalon Studio test cases right inside Jira.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/image2017-8-2-173A563A40.png)

### Submit an Issue to Jira

Bug submission options will be available in Test Reports after JIRA Integration setup is successfully configured.

1. Open a test execution in **Reports** that you want to review for issues. In **Test Cases Table**, a dedicated column for JIRA Integration will be enabled.
![Test-Cases-Table](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/katalon_studio_integration_with_jira_overview/Test-Cases-Table.png)

2. Click on the bug icon to display the list of related JIRA issues associated with the selected Test Case. The issues are shown in the following screen.
![JIRA issues associated](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/katalon_studio_integration_with_jira_overview/JIRA-issues.png)

3. Select submit option under the **Add** command.
![Create new Jira ticket](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/katalon_studio_integration_with_jira_overview/Add-command.png)
The bug submission options include:

<table>
    <thead>
        <tr>
            <th>Option</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Create as New</td>
            <td>A new Issue will be submitted to JIRA.</td>
        </tr>
        <tr>
            <td>Create as Sub Issue</td>
            <td>
                A sub-task for an existing JIRA issue will be created. You will be asked to provide the <b>ID</b> of the existing JIRA issue to create a sub-task within.
                <p></p>
                <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/working-with-jira/image2017-8-2-163A123A21.png"></p>
            </td>
        </tr>
        <tr>
            <td>Link to existing Issue</td>
            <td>
                This option will append execution details to an existing JIRA issue. You will be asked to provide the ID of the existing JIRA issue for this.
                <p></p>
                <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/katalon_studio_integration_with_jira_overview/Link-to-existing-Issue.png"></p>
            </td>
        </tr>
    </tbody>
</table>

4. In case of creating a new JIRA issue (or Sub-task), a **JIRA native submission form** will be displayed. The following is an example form for creating a new JIRA issue:
![JIRA native submission form](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/katalon_studio_integration_with_jira_overview/JIRA-native-submission-form.png)

5. Based on your preferences in [JIRA Integration settings](/display/KD/JIRA+Integration#JIRAIntegration-Configuration), the **Summary**, **Screenshots**, **Logs, Reporter, and Description** of test cases will be populated and attached accordingly. Once done, click on the **Create** button at bottom of the form.

6. A created **JIRA issue** will have its **ID** recorded in the **Linked JIRA issues** list so that you can quickly navigate there from Katalon Studio. You can also edit linked JIRA issue or remove the linking of the created JIRA issue.![Linked JIRA issues](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/katalon_studio_integration_with_jira_overview/Linked-JIRA-issues1.png)

7. Once clicked on **ID**, you will be taken to **JIRA issues** page accordingly as shown below

![JIRA issues page](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/katalon_studio_integration_with_jira_overview/JIRA-issues-page.png)

## Install and Use Katalon's Jira add-on from Atlassian Marketplace

Katalon Studio provides a free Jira add-on to help create a seamless integration. This add-on gives you several benefits:

* Adding a Gherkin custom field to help you design your test case in a consistent and concise way. The content will be populated right into your Katalon Studio automation scripts automatically.
* Presenting the latest execution result and artifacts right inside the issue page.
* Looking up Katalon Studio execution result status using Jira's JQL syntax.

### Jira Server

#### Installation

> Install Katalon BDD - Test Automation for Jira [here](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira?hosting=cloud&tab=overview).

To install the add-on, please follow [Atlassian's instruction](https://marketplace.atlassian.com/plugins/com.katalon.katalon-jira-plugin/server/installation).

#### Gherkin custom field


> Only availabe for Jira Server Version

This add-on adds a custom field type to Jira called Katalon Gherkin. This custom field lets you write descriptions for your test cases and stories in Gherkin syntax. Gherkin keywords such as _Given_, _When_, _Then_ will be highlighted automatically. Once imported to Katalon Studio, the content of Katalon Gherkin field will be populated into test cases description.  

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-and-use-katalons-jira-add-on/katalon-jira-plugin-1-field-marked.png)  

  

To create Katalon Gherkin custom field, please follow [Atlassian's instruction](https://confluence.atlassian.com/adminjiraserver071/project-screens-schemes-and-fields-802592517.html).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-and-use-katalons-jira-add-on/field-config-marked.png)  

### Jira Cloud

#### Install and Use Katalon BDD custom field in Jira Cloud

A new version of the Katalon BDD Add-on for Jira Cloud which supports BDD editor is available [here](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira?hosting=cloud&tab=overview). 

#### Install the Katalon BDD add-on

To add the **Katalon BDD** custom field to Jira Cloud, from **Jira settings** -> Select **Apps**-> Select **Find new apps** -> Enter **“BDD Katalon”** in Filter apps-> **Get app**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/1-enter-Katalon-BDD.png)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/2-install.png)

#### Create the Katalon BDD custom field

+ From **Jira settings** -> Select **Issues** ->in FIELDS tab, select **Custom fields -> Add custom field**.
+ Select a Field Type: **_Text Field (multi-line)._** Remember to associate it with issue types you want.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/3-field-type.png)

+ Provide a name and its description -> **Create**.
+ Associate the custom field to multiple screens by checkbox.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/4-screens.png)

#### Enable the Katalon add-on and custom field

In **Project settings** -> Scroll down to the bottom then select **Katalon BDD** -> Select the field you’ve created, then Click **Add** -> Select issue types to show this field with BDD editor -> Click **Save**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/5-enable.png)

#### Try the BDD editor

In the selected issue, you need to enable the **Katalon BDD Fields**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/6-KBDD.png)

To edit content in Katalon BDD  Field, click the pencil icon and write a Gherkin content, then click the check icon. Make sure the content starts with `Feature`.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/7-gherkin.png)

#### View Katalon Studio Test Execution Result on Jira

Once Jira is integrated with Katalon Studio and the add-on is enabled in Jira Cloud, a panel called TEST RESULT inside the issue page enables users to directly view the test result. In the new view of the issue page, just click **Test Result**. The result includes the execution status (PASSED, FAILED, INCOMPLETE, ERROR) and test artifact attachments (e.g. logs, screenshots, etc.).

> Note: In Katalon Studio, the test case imported from Jira should be executed in Test Suite to view the test result.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/install-and-use-katalons-jira-add-on/katalon-jira-plugin-1-status-marked.png)  


### JQL Syntax


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



#### Use JQL Syntax to query all issues with a particular execution status

Katalon Studio's test execution status can be queried via [JQL](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html). The syntax is as follows:

`"Katalon Status"="STATUS"`

For example, to search for the issues with *PASSED* status:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/BDD-field-Jira-Cloud/passed.png)

