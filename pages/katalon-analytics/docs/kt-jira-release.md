---
title: "Manage Releases" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-jira-release.html
redirect_from:
    - "/katalon-analytics/docs/release.html"
---

With the Releases feature in **Katalon TestOps**, you can populate releases from Jira or create a new one and link your Test Runs to it.

## Create a new Release

1. Under **Test Planning**, select **Releases** tab. 
2. Click **Create Release** button.

<img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-list.png" width="" height="">

3. Enter the required information: 

<img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-create.png" width="" height="">

- *Name*: your Release name
- *Start Date*: by when you want your Release to be started
- *Release date*: by when you want your Release to be ended
- *Jira Project*: can be found once you have configured Jira integration. [Learn more](https://docs.katalon.com/katalon-analytics/docs/kt-jira-config.html)
- *Jira Release*: can be found in your Jira Project

4. Click **Create** to finish.

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


## View Release Readiness by Test Case status

1. Under **Test Planning**, select **Release** tab.
2. Click on a release name to view its detailed page. 

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-detail.png)

A **Test Case** is shown as passed only if all of its **Test Runs** are marked as passed in its most recent execution. A **Test Case** can run multiple times in an execution (for example, with multiple data rows).

To view details, click on the *Passed/Failed* labels.

> If you have linked a TestOps Release to a Jira Release, you can also view Test Case status directly in Jira.
>
> ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jira-ka-configure/jira-release-result-example.JPG)


## View Release Readiness by Test Runs history

On a release detailed page, select **Test Runs** tab.

<img src="https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/release/release-test-run-history.png" width="" height="">


> **Quick tips**: You can also view your releases in Katalon Studio’s Test Explorer.
>
> To view releases, in Test Explorer, go to **TestOps** > **Releases**.
> <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/view-release-ks.png" width="" height="">

## Next steps

- [Create and manage Builds](/katalon-analytics/docs/kt-build.html)

## Related topics

- [Link Test Cases to Jira Requirements](https://docs.katalon.com/katalon-analytics/docs/ka-integration-jira.html)

- [Link Test Runs to Jira Defects](https://docs.katalon.com/katalon-analytics/docs/ka-defects.html)
