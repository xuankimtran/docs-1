---
title: "Manage Test Runs by Release" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-release.html
redirect_from:
    - "/katalon-analytics/docs/release.html"
---

With the Releases feature in **Katalon TestOps**, you can populate releases from Jira or create a new one and link your Test Runs to it.

## Create a new Release

To create a new Release in your project, go to **Test Planning** and select **Releases** tab > click **Create Release** button.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_plan_release_tab.png)

Enter the required information and click **Create** to finish.
- **Name**: your Release name.
- **Start Date**: by when you want your Release to be started.
- **Release Date**: by when you want your Release to be ended.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_create_release.png)

A new Release displays in **Test Planning**. If you want to create a new Release, you will click the **Create Release** button.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_plan_release_list_create.png)

## Link Test Runs to a Release

You can link Test Runs to a Release that you have created. In your project, go to **Reports & Analytics** and select **Test Runs**, then click a Test Run ID that you want to link to a Release.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_click_id_test_run.png)

Click on **Link to a Release** and select a release from the drop-down list.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_run_link_release.png)

If a Test Run has been linked before, you will click a button (next to the name of Release) on the top right corner and select a Release.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_run_link_release1.png)

## View Release Readiness by Test Case status

You can view what Test Cases passed or failed in their most recent Test Runs by going to Test Plan details page. On the sidebar **Test Planning**, click on **Releases**, the list of Releases displays. You choose a Release that you want to see in detail.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_plan_choose_release.png)

Then you can see all the Test Cases passed or failed in the Release.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_sample_release_detail.png)

A Test Case is shown as passed if and only if all of its Test Runs pass in its most recent execution. A Test Case can run multiple times in an execution (for example, with multiple data rows).

## View Release Readiness by Test Runs history

You can view a list of Test Run within each Release by access the Release details page > Select **Test Runs** tab.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/test-run-status.png" width="" height="">

> **Quick tips**: You can also view your releases in Katalon Studio’s Test Explorer.
>
> To view releases, in Test Explorerss, go to **TestOps** > **Releases**.
>
> <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/view-release-ks.png" width="" height="">

## Related topics

- [Link Test Cases to Jira Requirements](https://docs.katalon.com/katalon-analytics/docs/ka-integration-jira.html)

- [Link Test Runs to Jira Defects](https://docs.katalon.com/katalon-analytics/docs/ka-defects.html)