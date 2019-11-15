---
title: "Integration with Jira" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/ka-integration-jira.html 
description: How to integrate Katalon TestOps with Jira
---
## Overview

Katalon TestOps provides seamless integration with Jira that brings several benefits for team collaboration, including:
* Quickly attach Jira issues to Katalon Test Case or Test Run.
* Easily view detail of Jira issue on one click from Katalon TestOps.
* Easily see the test result for each release in Jira.

**Prerequisites:**
* The [Katalon BDD Add-on for Jira](https://docs.katalon.com/katalon-studio/docs/BDD-field-jira-cloud.html#install-and-use-katalon-bdd-custom-field-in-jira-cloud) installed 

## Configuration in Jira

1. Navigate to **Katalon Settings** at the bottom of Project Settings.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jira-ka-configure/1-jira-ka-config.png)

2. Enter the email registered for your Katalon account.

3. Enter an **[API Key](https://docs.katalon.com/katalon-analytics/docs/api-key.html)**.

4. Enter **[Organization ID](https://docs.katalon.com/katalon-analytics/docs/getting-started.html)**.

5. Click **Save**.

## Configuration in Katalon TestOps

1. Navigate to **Jira Settings** located in the toolbar of the project page.

2. Enter Jira URL, Username, and Password.

* Jira Cloud

    a. Jira URL must be in the form of _Https://<site_name>.atlassian.net_.\
    b. Enter the email registered for your Jira Cloud account in *Username*.\
    c. Enter an Atlassian Cloud's API token in *Password*. See the instructions **[here](https://confluence.atlassian.com/cloud/api-tokens-938839638.html)**.

* Jira Server

    a. Jira URL must be in the form of _Http(s)://domain_ without any trailing parts e.g., _/secure_.\
    b. Use your username instead of an email in *Username*.\
    c. Enter Password.

3. Click **Test Connection** to see if the connection is successful.

4. Click **Save**.

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jira-ka-configure/2-jira-ka-config.JPG)

## Work with Jira releases

You can either create release directly in Katalon TestOps or populate existing releases from Jira using the **Create Release**, or **Populate Jira Releases** button respectively.

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jira-ka-configure/ka-create-release.JPG)

In Katalon TestOps, click **Populate Jira Releases** to get all the existing releases from Jira, then link your test run with the populated release. The test run results that you already linked will be shown under the **Release** section in Jira.

Alternatively, in Katalon TestOps, click **Create Release**, select a Jira Project and Jira Release to associate the Katalon’s release with existing Jira’s one, then link your test run with the newly created release so that you can also view the test run results in Jira **Release** section.

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jira-ka-configure/ka-create-release-2.JPG)

Example of viewing release status in **Jira Cloud**:

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jira-ka-configure/jira-release-result-example.JPG)


## Work with Jira issues

You can link existing Jira issues with Test Cases, and Test Runs in Katalon TestOps by following these steps:

1. Go to your project > in **Test Design**, select a Test Case.

2. Click **Link**.

3. Enter a Jira issue key under Properties section.

4. Click **Check** to see the Jira issue is linked with the Test Case.

> Note: You can add more than one issue by typing [issue1,issue2,...].

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jira-ka-configure/ka-link-jira-issue-with-test-case.JPG)

5. In Jira, view the issue details to see if it's linked with any Test Case or Test Run.

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jira-ka-configure/jira-issue-detail-with-linked-test-case.JPG)

You also can directly submit a new Jira issue with Test Run result by using Katalon Plugin installed in your browser.

1. Install the Katalon Integration plugin in your browser. **[Download here](https://chrome.google.com/webstore/detail/katalon-integration/cechonbcopffiimhnkgghckbgipciedg)**.

2. After installation, enable the Katalon Plugin.

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jira-ka-configure/katalon-plugin-installed.JPG)

3. In Katalon TestOps, go to your project > select **Execution** > select **Test Runs** tab.

4. Select a Test Run by clicking its ID.

5. Under the Jira Issue section, click the **Create** button. You will be navigated to **Jira Project Dashboard** where you can create a new Jira issue.

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jira-ka-configure/ka-create-jira-issue.JPG)

6. In the detailed view of the newly created issue, you can see a floating icon on the bottom right corner.

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jira-ka-configure/jira-issue-detail-with-floating-katalon-icon.JPG)

7. Click on the icon to go back to its associated Test Run on Katalon TestOps.

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/jira-ka-configure/ka-linked-jira-issue-with-test-execution.JPG)
