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

* Submit Bugs to Jira.
* Link a Katalon Studio project with a Jira project.
* Import Test Cases from Jira to Katalon Studio for creating test cases, and run BDD tests.
* Automatically submit test results and test reports to the linked Jira issue.

> Prerequisites:
>
> * An active Katalon Studio Enterprise license.
> * Install the **Jira Integration** plugin for Katalon Studio. You can download the plugin from Katalon Store at: [Jira Intergration](https://store.katalon.com/product/3/Jira-Integration).
> * Install the **Katalon Studio and TestOps integration** plugin for Atlassian site. You can download the plugin from the Atlassian Marketplace website at: [Katalon Studio and TestOps integration](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira).

In this article, we show you how to configure Jira intergration in Katalon Studio, then submit a ticket to Jira from Katalon. 

## Configure Jira integration 

To enable Jira Integration, follow these steps:

1. Go to **Project > Settings > Plugins > JIRA**.

<img src="url" width=70% alt="Jira Configuration in Katalon">

2. Select **Enable integration** option to enable to integration settings.

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
<div>For <strong>Jira Server</strong>: the URL form is <code>http(s)://domain</code> without any trailing parts , for example, <code>/secure</code>.</div>
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

- Hit **Connect** to start the authentication process. A pop-up dialog indicates that the Atlassian account connects successfully.

4. After successfully authenticating with JIRA, all relevant **JIRA Projects** and **Issue Types** will be retrieved and displayed under the **Submit Options** section. You can specify the default project and the default issue type for submission here.

| Field | Description |
| --- | --- |
| Default JIRA Project | The default JIRA project to submit tickets. |
| Default JIRA Issue Type | The default JIRA Issue type to create when submitting tickets. |
| Use Test Case name as Summary for JIRA ticket | To use the test case name as a summary for submitted tickets. |
| Attach Screenshot to JIRA ticket | To include taken screenshots during test execution in submitted tickets. |
| Attach Log to JIRA ticket | To include the execution log in submitted tickets. |


<img src="url" width=70% alt="Submit Options">


5.  Click **Apply and Close** to complete the Jira integration.

> Notes
> 
> If you want to enable Jira integration with Katalon TestOps, you can refer to this document: [TestOps - Jira Integration](https://docs.katalon.com/katalon-analytics/docs/kt-jira-config.html).

## Submit an issue to Jira

After sucessfully configuring Jira Integration, you can submit a ticket to Jira from Katalon. 

> Note:
> 
> You can only submit Jira tickets from test reports, which are automatically generated after executing a test suite.

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

## See also
- [Automation testing with Jira integration]()


