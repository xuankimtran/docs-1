---
title: "Jira Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/jira-integration.html
redirect_from:
    - "/katalon-studio/docs/configure-jira-integration/"
    - "/katalon-studio/docs/BDD-field-jira-cloud/"
    - "/katalon-studio/docs/install-and-use-katalons-jira-add-on/"
    - "/display/KD/Install+and+Use+Katalon%27s+JIRA+add-on/"
    - "/display/KD/Install%20and%20Use%20Katalon%27s%20JIRA%20add-on/"
    - "/x/TBBO/"
    - "/katalon-studio/docs/working-with-jira/"
    - "/display/KD/Configure+JIRA+Integration/"
    - "/display/KD/Configure%20JIRA%20Integration/"
    - "/x/7oEw/"
    - "/display/KD/JIRA%20Integration/"
    - "/display/KD/Working+with+JIRA/"
    - "/display/KD/Working%20with%20JIRA/"
    - "/x/MhBO/"
    - "/katalon-studio/docs/jira-plugin-integration.html"
    - "/katalon-studio/tutorials/katalon_studio_integration_with_jira_overview.html"
description:
---

Katalon Studio can integrate with both Jira Cloud and Jira Server. This integration helps you:

* Link a Katalon Studio project with a Jira project.
* Import Test Cases from Jira to Studio for creating test cases, and BDD tests.
* Automatically submit test results and test reports to the linked Jira issue.
* Submit Bugs to Jira.

> Prerequisites:
>
> * An active Katalon Studio Enterprise license.
> * Install the Jira Integration plugin. You can download the plugin from Katalon Store here: [Jira Intergration](https://store.katalon.com/product/3/Jira-Integration) 
> * Install the Katalon Studio and TestOps integration plugin. You can download the plugin from the Atlassian Marketplace website: [Katalon Studio and TestOps integration](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira) for Jira from Atlassian Marketplace.

In this article, we show you how to configure Katalon Studio for Jira intergration . Follow these steps:
## Configure Jira integration 


1. To enable JIRA Integration in order to submit issues to JIRA. Go to **Project > Settings > Plugins > JIRA**.

<img src="url" width=70% alt="Jira Configuration in Katalon">


2. Select **Enable integration** option. The setting is available for configuration.

3. In the **Authentication** section, fill in the criteria as shown below: 

<table width="842">
<tbody>
<tr>
<td><strong>Server URL</strong></td>
<td>
<div>
<div>
<div>
<div>
<div>
<div>For <strong>Jira Cloud</strong>: the URL form is <code>https://&lt;site_name&gt;.atlassian.net</code></div>
<div>For <strong>Jira Server</strong>: the URL form is <code>http(s)://domain</code> without any trailing parts , for example, <code>/secure</code>,<code>/about</code>.</div>
</div>
</div>
</div>
</div>
</div>
</td>
</tr>
<tr>
<td><strong>Username</strong></td>
<td>&nbsp;Your username or the registered email for Atlassian account.</td>
</tr>
<tr>
<td><strong>Password/API Token</strong></td>
<td>
<div>
<div>The Atlassian Cloud's API token. To learn more about generating API in Atlassian, you can refer to the Atlassian document here: <a href="https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account/">Manage Atlassian token for your Atlassian account</a>.</div>
</div>
</td>
</tr>
</tbody>
</table>

<img src="url" width=70% alt="Jira Configuration in Katalon">

- Hit **Connect** to start the authentication process. A pop-up dialog indicates the Atlassian account connects successfully.

4. After successfully authenticating with JIRA, all relevant **JIRA Projects** and **Issue Types** will be retrieved and displayed under the **Submit Options** section. You can specify the default project and issue type for submission here.

The fields for setting include:

| Field | Description |
| --- | --- |
| Default JIRA Project | The default JIRA project to submit tickets. |
| Default JIRA Issue Type | The default JIRA Issue type to create when submitting tickets. |
| Use Test Case name as Summary for JIRA ticket | The Katalon Test Case Name will be used as a summary for submitted tickets. |
| Attach Screenshot to JIRA ticket | Any taken screenshot during execution will be included in submitted tickets. |
| Attach Log to JIRA ticket | The execution log will be included in submitted tickets. |


<img src="url" width=70% alt="Submit Options">


4.  Click **Apply and Close** to complete the JIRA Integration setup.


## Import Test Cases from Jira

1. Prepare [Jira JQL Script](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html)

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/image2017-8-2-113A393A33.png)

2. Select the **Jira Integration** icon > select **Import Test Case from JIRA JQL**
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/image2017-8-2-113A233A49.png)

3. Enter the Jira JQL and click **OK**.
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/image2017-8-2-113A413A34.png)

4. In the displayed **Test Case Folder Selection** window, select the destination to store the issues. Click **OK**.
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/save_test_cases.png)

5. In the **Linked Jira Issues** window, click **OK**.
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/image2016-11-3-143A413A132.png)

If your test cases have already been linked to a JIRA ticket, Katalon Studio will not sync them again.

## Import BDD Feature Files

### Jira Server Integration

Once you have enabled the integration with Jira Server, you can import Jira BDD Feature Files to Katalon Studio. When importing test cases from Jira, please check **Link to BDD Feature File** &gt; **OK** &gt; Choose the destination to store the issues.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/sample.png)

A new Feature File (with the same name as the test case) will be created with the content from Jira BDD. Moreover, a RunFeature step will be created in the linked test case to Jira.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/bdd2.png)

### Jira Cloud Integration

> Introduced in version 7.8

When importing Jira tickets with BDD feature file from Jira Cloud, you can import the BDD field to Katalon Studio as well by turning on this setting in Project Settings.

1. Go to **Project/Settings/Plugins/Jira**.
2. In the **Fetch Options** section, select **Enable retrieving content of the specified custom field**.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/jira-bdd-78.png" width=100%>
3. Select a custom field from the list. Click **Fetch Custom Fields** to fetch the list from the connected Jira Cloud Server.

> Note: Only existing custom field ID is valid for this configuration.

4. Click **OK** to apply your settings. 

Once this setting is configured successfully in Project Settings, the custom field’s content will be retrieved like in Jira Server integration. 

## View Test Results in Jira

After a test suite execution finishes, Katalon Studio automatically uploads a test result to the integrated Jira issue. You can view the test result and its attachments (if you have predefined in Project Settings) in Jira.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jira-plugin-integration/image2017-8-2-173A563A40.png)

> Note
>
> Katalon Studio test execution status can be queried via [JQL](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html). The syntax is as following:
>
>```groovy
>"Katalon Status"=<status>
>```
> For example, to search for all issues that have failed in Katalon Studio test execution, type `"Katalon Status"=FAIL` in the search bar. Katalon Studio supports five test status: **Passed**, **Failed**, **Incomplete**, **Error** and **Skip**.

## Submit an Issue to Jira

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





> Notes
> 
> If you need to enable Jira integration with [Katalon TestOps](https://analytics.katalon.com) to have an insightful look at your testing data and better test management. Refer to [TestOps - Jira Integration](https://docs.katalon.com/katalon-analytics/docs/kt-jira-config.html) to learn how to configure the integration.