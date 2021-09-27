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
* Import Test Cases from Jira to Katalon Studio for creating test cases and running BDD tests.
* Automatically submit test results and test reports to the linked Jira issue.
* Submit Bugs to Jira.
  
> Prerequisites:
>
> * An active Katalon Studio Enterprise license.
> * Install the **Jira Integration** plugin for Katalon Studio. You can download the plugin from Katalon Store here: [Jira Integration](https://store.katalon.com/product/3/Jira-Integration).
> * Install the **Katalon Studio and TestOps integration** plugin for the Atlassian site. You can download the plugin from the Atlassian Marketplace website here: [Katalon Studio and TestOps integration](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira).
## Configure Jira Integration 

To enable Jira Integration, follow these steps:

1. Go to **Project > Settings > Plugins > JIRA**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Jira%20Configuration-in-Katalon.png" width=50% alt="Jira Configuration in Katalon">

2. Select **Enable integration** option to enable Jira Integration settings.

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
    <div>For <strong>Jira Cloud</strong>: <code>https://&lt;site_name&gt;.atlassian.net</code></div>
    <div>For <strong>Jira Server</strong>: <code>http(s)://domain</code> without any trailing parts, for example, <code>/secure</code>.</div>
    </div>
    </div>
    </div>
    </div>
    </div>
    </td>
    </tr>
    <tr>
    <td><strong>Username</strong></td>
    <td>&nbsp;Your username or the registered email of the Atlassian account.</td>
    </tr>
    <tr>
    <td><strong>Password/API Token</strong></td>
    <td>
    <div>
    <div>The Atlassian Cloud's API token. To learn more about generating API in Atlassian, you can refer to the Atlassian document: <a href="https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account/">Manage Atlassian token for your Atlassian account</a>.</div>
    </div>
    </td>
    </tr>
    </tbody>
    </table>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Enable-JIRA-intergration.png" width=50% alt="Enable Jira Configuration in Katalon">

   - Hit **Connect** to start the authentication process. A pop-up dialog indicates that the Atlassian account connects successfully.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Connect-JIRA-successfully.png" width=50% alt="Connect Jira Configuration successfully in Katalon">

4. After successfully authenticating with JIRA, all relevant **JIRA Projects** and **Issue Types** will be retrieved and displayed under the **Submit Options** section. You can specify the default project and the default issue type for submission here.

    | Field | Description |
    | --- | --- |
    | Default JIRA Project | The default JIRA project to submit tickets. |
    | Default JIRA Issue Type | The default JIRA Issue type to create when submitting tickets. |
    | Use Test Case name as Summary for JIRA ticket | To use the test case name as a summary for submitted tickets. |
    | Attach Screenshot to JIRA ticket | To include taken screenshots during test execution in submitted tickets. |
    | Attach Log to JIRA ticket | To include the execution log in submitted tickets. |


    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Submit-Options.png" width=50% alt="Submit Options">

5.  Click **Apply and Close** to complete the Jira integration.

    > Notes
    > 
    > If you want to enable Jira integration with Katalon TestOps, you can refer to this document: [TestOps - Jira Integration](https://docs.katalon.com/katalon-analytics/docs/kt-jira-config.html).

## Execute Test Cases with Jira Integration

There are three main steps to execute test cases imported from Jira in Katalon. However, if you don't want to run BDD tests or you are intergrating Jira Server with Katalon, you can skip Step 1.
### Step 1: Import BDD custom fields (Applicable to Jira Cloud Intergration)

From Katalon Studio version 7.8.0 onwards, for Jira Cloud integration, you can also import the BDD custom fields to Katalon Studio when importing BDD feature files. To learn more about adding BDD custom fields in Jira via Katlon BDD, you can refer to this document here: [Install and Use Katalon BDD custom field in Jira Cloud](https://docs.katalon.com/katalon-studio/docs/BDD-field-jira-cloud.html#prerequisites).

Follow these steps:

1. Go to **Project > Settings > Plugins > Jira**.
2. In the **Fetch Options** section, check the **Enable retrieving content of the specified custom field** box.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Enable-BDD-custom-files-2.png" width=50% alt="Enable the BDD custom field in Jira Cloud">

3. Select a custom field from the drop-down list. 

    > Note:
    >
    > Only existing custom field ID is valid for this configuration.
    > In case you can not find the custom field in the drop-down list, click **Fetch Custom Fields** to fetch the latest list from the connected Jira Cloud. 

4. Click **Apply and Close** to apply your settings. 
### Step 2: Import Test Cases from Jira

Katalon Studio allows you to pull test cases from Jira and link Jira issues to Katalon. Follow these steps:

1. From the Katalon toolbar, select **Jira Integration <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Jira-icon.png" width=3% alt="Jira Intergration icon"> > Import Test Case from JIRA JQL**. An **Import Test Case from JIRA JQL** dialog opens.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Click-the-JIRA-icon.png" width=50% alt="Import test case from Jira">

2. In the opened dialog:

   - Fill the JIRA Query Language (JQL) script of the desired test case in the **Jira JQL** box. To find out the JQL script of your test case, you can refer to the Atlassian document here: [Search for issues using JQL](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html)

        For example: We want to import test case TDAP-46 from the Jira board. After searching for the Jira ticket using the JQL query, copy and paste the JOL script into the **Jira JQL** box:

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-JQL-query-from-Jira.png" width=90% alt="JQL query from Jira">  

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Copy-JQL-syntax-to-Katalon.png" width=50% alt="Copy and paste JQL script into the Jira JQL">


   - By default, the **Import BDD feature files** box is selected. This option allows you to import BDD feature files to run BDD tests. In case you don't want to run BDD tests, uncheck this option. To learn more about BDD testing, you can refer to this document here: [BDD Testing Framework (Cucumber Integration)](https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html#set-default-package-for-step-definitions.)

        <img src="https://github.com/katalon-studio/docs-images/raw/de6b6cc7920a9776a331e2e44b4bb30f90344653/katalon-studio/docs/configure-jira-integration/KS-JIRA-Import-BDD-feature-file.png" width=50% alt="Import the BDD feature files">

3. In the **Test Case Folder Selection** dialog, select the destination to store the issues. Click **OK**. A **Jira Issues** dialog opens.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Choose-the-des-for-Jira-test-cases.png" width=40% alt="Choose the destination for Jira test cases">

4. In the **Jira Issues** dialog, click **OK**. 

    > Notice:
    >
    > If your test cases have already been linked to a JIRA ticket, you can not sync them again.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Link-the-JIRA-issue.png" width=40% alt="Link the Jira issue">

    Katalon opens a new test case with:

    <table width="886">
    <tbody>
    <tr>
    <td>Test Case Name</td>
    <td>
    <div>
    <div>Jira ticket's summary/subject</div>
    </div>
    </td>
    </tr>
    <tr>
    <td>
    <div>
    <div>Test Description</div>
    </div>
    </td>
    <td>
    <div>
    <div>Jira ticket's content</div>
    </div>
    </td>
    </tr>
    <tr>
    <td>
    <div>
    <div>
    <div>
    <div>With the selected <strong>Import BDD feature files</strong> box from Step 2</div>
    </div>
    </div>
    </div>
    </td>
    <td>
    <p>&nbsp;Katalon creates a&nbsp;new feature file in <strong>Include\Feature&nbsp;</strong>with:</p>
    <p>- The feature file's name is the same as the test case's name.</p>
    <p>- The feature file's content is the BDD content from Jira. For Jira Cloud integration, if the&nbsp;<strong>Enable retrieving content of the specified custom field&nbsp;</strong>option in <b>Project Settings</b> is enabled, it also displays the BDD custom field in the content.</div>
    </div>
    <p>&nbsp;- A <strong>Run Feature File</strong> step is also added in the test script.</p>
    </td>
    </tr>
    </tbody>
    </table>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Final-results-after-importing-test-cases.png" width=70% alt="Final results after importing test cases">

### Step 3: Run the test case

After importing the test case from Jira, you can continue to add additional steps in the test case for your purpose. Then hit **Run** to run the test case.

## View Test Results in Jira

To view test results in Jira, follow these steps:
1. Add the associated test cases to a test suite. 
After a test suite execution, Katalon Studio automatically uploads the latest test result and attaches a `.zip` file that contains test reports to the linked Jira issue. 
2. To view the test results, open the linked Jira ticket, click **Open Test Results** in the **Details** group.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Click-Open-test-results-in-the-Jira-issue.png" width=70% alt="Click on the Open test results in the Jira issue">

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-see-results-of-test-case-in-the-Jira-issue.png" width=70% alt="See results of test case in the Jira issue">

    > Note
    >
    > You can quickly find the test execution status via JQL. The syntax is as follows:
    >```groovy
    >"Katalon Status"=<status>
    >```
    > For example, to search for all issues that have failed in the Katalon Studio test execution, type `"Katalon Status"=FAIL` in the search bar. Katalon Studio supports five test statuses: **Passed**, **Failed**, **Incomplete**, **Error**, and **Skipped**.

## Submit an issue to Jira

After executing a test suite, you can submit a ticket to Jira from its test reports. 

Follow these steps:

1. Go to **Reports** in the **Test Explorer** panel and double-click to open the test reports you want to review for issues. 
2. In the opened test report, click **Bug** <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Bug-icon.png" width=3% alt="Bug icon">. A **Linked Jira issues** dialog opens.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Click-the-Bug-icon.png" width=50% alt="Click the Bug icon">

3. In the opened dialog, click **Add** to choose your submit options.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Choose-your-submit-options.png" width=50% alt="Choose your submit options">

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
    <p>1. A&nbsp;<strong>JIRA native submission form </strong>opens in the pop-up browser<strong>.&nbsp;</strong>You might be prompted to sign in to your Atlassian account. You only have to do this once.</p>
    <p>2 After signing in, fill in the&nbsp;<strong>JIRA native submission form&nbsp;</strong>to submit the ticket.</p>
    </td>
    </tr>
    <tr>
    <td>Create as Sub Issue</td>
    <td>To create a sub-task for an existing Jira issue.</td>
    <td>
    <p>After choosing this option:</p>
    <p>1. A <strong>Create as JIRA Sub Task </strong>dialog opens. Fill in the&nbsp;<strong>ID</strong>&nbsp;of an existing Jira issue to create a sub-task within. Click&nbsp;<strong>OK&nbsp;</strong>to open&nbsp;<strong>JIRA native submission form.</strong></p>
    <p><strong><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Create-as-sub-task.png" alt="Create a sub ticket" /></strong></p>
    <p>2. You might be prompted to sign in to your Atlassian account. You only have to do this once.</p>
    <p>- After signing in, fill in the&nbsp;<strong>JIRA native submission form&nbsp;</strong>to submit the ticket.</p>
    </td>
    </tr>
    <tr>
    <td>Link to existing Issue</td>
    <td>This option adds the execution details of the test to an existing JIRA issue. You need to provide the <strong>ID</strong> of the existing JIRA issue for this.</td>
    <td>
    <p>After choosing this option:&nbsp;</p>
    <p>- A <strong>Link to JIRA Issue</strong> dialog opens. Fill in the&nbsp;<strong>ID</strong>&nbsp;of an existing Jira issue. Click&nbsp;<strong>OK.&nbsp;</strong>The test case execution .zip files&nbsp;will be attached to the linked JIRA Issue.</p>
    <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/configure-jira-integration/KS-JIRA-Create-a-linked-ticket.png" alt="Create a linked ticket" /></p>
    </td>
    </tr>
    </tbody>
    </table>

    > Note:
    > 
    > * The default **JIRA native submission form** might include the **Summary**, **Screenshots**, **Logs**, **Reports**, and **Description** of the test case. You can configure the default submission form from the **Submit Options** section in the Jira integration settings.
    > * To quickly navigate to a linked JIRA issue, click the hyperlink embedded in the ticket's ID. 
    > 
    > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/katalon_studio_integration_with_jira_overview/Linked-JIRA-issues1.png" width=40% alt="Jira Issues Hyperlink">






