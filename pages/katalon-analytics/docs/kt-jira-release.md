---
title: "Manage Test Runs by Release" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-jira-release.html
redirect_from:
    - "/katalon-analytics/docs/release.html"
---

With the Releases feature in **Katalon TestOps**, you can populate releases from Jira or create a new one and link your Test Runs to it.

## Create a new Release

To create a new Release, in your project, go to Test Planning and select *Releases* tab > click *"Create Release"* button.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/release-list.png" width="" height="">

Enter the required information and click *Create* to finish.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/create-release.png" width="" height="">

- *Name*: your Release name
- *Start Date*: by when you want your Release to be started
- *Release date*: by when you want your Release to be ended
- *Jira Project*: can be found once you have configured Jira integration. [Learn more](https://docs.katalon.com/katalon-analytics/docs/kt-jira-config.html)
- *Jira Release*: can be found in your Jira Project

## Populate a Jira Release

You can either create Release directly in **Katalon TestOps** or populate existing releases from Jira using the "*Create Release*", or "*Populate Jira Releases*" button respectively.

To populate a Jira Release, go to Test Planning and select *Releases* tab > click "*Populate Jira Releases*" to get all the existing Releases from Jira, then follow the above section to link your Test Run with the populated release. The test run results that you already linked will be shown under the **Release** section in Jira.

## Link Test Runs to a Release

You can link Test Runs to a Release that you have created.

In your project, go to **Reports & Analytics** and select *Test Runs* > Select a Test Run ID that you want to link to a Release > Click on "*Link to a Release*" and select a release from the drop-down list.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/link-test-run.png" width="" height="">


## View Release Readiness by Test Case status

You can view what Test Cases passed or failed in their most recent Test Runs by going to Release details page.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/test-case-status.png)

A Test Case is shown as passed if and only if all of its Test Runs pass in its most recent execution. A Test Case can run multiple times in an execution (for example, with multiple data rows).

To view details, click on the *Passed/Failed* labels.

> If you have linked a TestOps Release to a Jira Release, you can also view Test Case status directly in Jira.
>
> ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jira-ka-configure/jira-release-result-example.JPG)


## View Release Readiness by Test Runs history

You can view a list of Test Run within each Release by access the Release details page > Select *"Test Runs"* tab.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/test-run-status.png" width="" height="">


> **Quick tips**: You can also view your releases in Katalon Studio’s Test Explorer.
>
> To view releases, in Test Explorer, go to **TestOps** > **Releases**.
> <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/view-release-ks.png" width="" height="">

## Related topics

- [Link Test Cases to Jira Requirements](https://docs.katalon.com/katalon-analytics/docs/ka-integration-jira.html)

- [Link Test Runs to Jira Defects](https://docs.katalon.com/katalon-analytics/docs/ka-defects.html)