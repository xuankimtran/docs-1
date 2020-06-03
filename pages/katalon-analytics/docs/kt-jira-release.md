---
title: "Releases" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-jira-release.html
redirect_from:
    - "/katalon-analytics/docs/release.html"
---

With the Releases feature in Katalon TestOps, you can [populate releases from Jira](https://docs.katalon.com/katalon-analytics/docs/kt-jira-release.html) or create a new one and map your executions to it.

## Create a new release

To create a new release, in your project, go to **Releases** > **Create Release**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/release-list.png" width="" height="">

Enter the required information and click **Create** to finish.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/create-release.png" width="" height="">

Now your release has been created.

## Map executions to a release

You can map executions to the release you have created.

In your project, go to **Executions** > Click on Release icon and select the release from the drop-down list.


<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/map-release.png" width="" height="">

Your execution is now mapped to the release.

You can view what test cases passed or failed in their most recent executions by going to Release details page.

> A test case is shown as passed if and only if all of its test runs pass in its most recent execution. A test case can run multiple times in an execution (for example, with multiple data rows).

To view details, click on the **Passed/Failed** labels.


<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/release-details.png" width="" height="">

## Link a TestOps release to a Jira release

You can either create release directly in Katalon TestOps or populate existing releases from Jira using the **Create Release**, or **Populate Jira Releases** button respectively.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jira-ka-configure/ka-create-release.JPG)

In Katalon TestOps, click **Populate Jira Releases** to get all the existing releases from Jira, then link your test run with the populated release. The test run results that you already linked will be shown under the **Release** section in Jira.

Alternatively, in Katalon TestOps, click **Create Release**, select a Jira Project and Jira Release to associate the Katalon’s release with existing Jira’s one, then link your test run with the newly created release so that you can also view the test run results in Jira **Release** section.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jira-ka-configure/ka-create-release-2.JPG)

Example of viewing release status in **Jira Cloud**:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jira-ka-configure/jira-release-result-example.JPG)
