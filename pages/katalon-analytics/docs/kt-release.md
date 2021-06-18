---
title: "Manage Test Runs by Release" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-release.html
redirect_from:
    - "/katalon-analytics/docs/release.html"
    - "/katalon-analytics/docs/kt-jira-release.html"
---

Using Katalon TestOps's Releases feature, you can populate Jira Releases or create a new Release and link your Test Runs to it.

## Create a new Release

Follow these steps:

1. Go to **Test Planning** and click on the **Releases** tab. Select the **Create Release** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_plan_release_tab.png" width="" height="">

2. Fill in the required information and click **Create**.
    * **Name**: your Release Name.
    * **Start Date**: when you want your Release to be started.
    * **Release Date**: when you want your Release to be ended.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_create_release.png" width="" height="">

    A new Release displays in **Test Planning**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_plan_release_list_create.png" width="" height="">

## Populate a Jira Release

There are two ways to populate Releases from Jira:

* Select a Jira Project and a Jira Release after clicking on the **Create Release** button.

    <img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-create-jira.png" width="" height="">

OR

* Click **Populate Jira Releases**.

    <img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-populate-jira.png" width="" height="">

## Link Test Runs to a Release

> Notes:
>
> After linking, the Test Runs are shown under the **Release** section on Jira.

Follow these steps:

1. Choose **Reports & Analytics** and click **Test Runs**.
2. Select a Test Run ID.

    The **Test Run's detail** page appears.

    <img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-link-test-run.png" width="" height="">

3. Click **Link to a release**.

4. Select a Release from the dropdown list.

    <img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-link-menu.png" width="" height="">

If a Test Run has already been linked before, click on the button (as shown below) at the top right corner and select a Release.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_run_link_release1.png" width="" height="">
