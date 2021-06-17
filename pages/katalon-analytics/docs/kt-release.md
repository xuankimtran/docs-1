---
title: "Manage Test Runs by Release" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-release.html
redirect_from:
    - "/katalon-analytics/docs/release.html"
---

Using the Releases feature, you can populate Jira Releases or create a new Release and link your Test Runs to it in [Katalon TestOps](https://testops.katalon.io/login?redirect=%252F%253F).

## Create a new Release

Follow these steps:

1. Go to **Test Planning** > **Releases** tab > **Create Release** button.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_plan_release_tab.png)

Enter the required information and click **Create** to finish.
- **Name**: your Release name.
- **Start Date**: by when you want your Release to be started.
- **Release Date**: by when you want your Release to be ended.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_create_release.png)

A new Release displays in **Test Planning**. If you want to create a new Release, you will click the **Create Release** button.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_plan_release_list_create.png)

## Populate a Jira Release

There are 2 ways to populate releases from Jira:  
1. Select a Jira Project and a Jira Release after clicking on **Create Release** button 

<img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-create-jira.png" width="" height="">


2. Quickly create by clicking on **Populate Jira Releases** 

<img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-populate-jira.png" width="" height="">

> Follow the below section to link your Test Run with the populated release. The test run results that you already linked will be shown under the **Release** section in Jira.

## Link Test Runs to a Release

1. Under **Reports & Analytics**, select **Test Runs**.
2. Click to select a Test Run ID. 
3. In the detail page of a Test Run, click on **Link to a Release**.

<img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-link-test-run.png" width="" height="">

4. Select a release from the drop-down list.

<img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-link-menu.png" width="" height="">


## Link Test Runs to a Release

You can link Test Runs to a Release that you have created. In your project, go to **Reports & Analytics** and select **Test Runs**, then click a Test Run ID that you want to link to a Release.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_click_id_test_run.png)

Click on **Link to a Release** and select a release from the drop-down list.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_run_link_release.png)

If a Test Run has been linked before, you will click a button (next to the name of Release) on the top right corner and select a Release.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_run_link_release1.png)
