---
title: "Working with Releases in Katalon TestOps" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/aws-eks.html 
description: 
---
With the Releases feature in Katalon TestOps, you can [populate releases from Jira](https://docs.katalon.com/katalon-analytics/docs/kt-jira-release.html) or create a new one and map your executions to it.

## Create a new release

To create a new release, go to **Releases** > **Create Release**.

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