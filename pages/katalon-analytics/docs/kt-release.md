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

1. Sign in [Katalon TestOps](https://testops.katalon.io/login?redirect=%252F%253F) and go to your Project.

    The Project's **Dashboard** page appears.

2. Select the **Test Planning** tab, then the **Releases** tab.

    The **Releases** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/create-release-in-test-planning-testops.png" width="" height="">

3. Click on the **Create Release** button on the top right corner.

    The **Create Release** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/create-release-page-fill-in-info.png" width="" height="">

4. Fill in the required information.
    * **Name**: your Release Name (e.g., Release 01).
    * **Start Date**: when you want your Release to start.
    * **Release Date**: when you want your Release to end.

5. Click **Create**.

    A new Release now displays in the **Releases** page.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/release-created-appears-on-test-planning.png" width="" height="">

## Populate a Jira Release

> Notes:
>
> You must enable Jira integration in Katalon TestOps first.

There are two ways to populate Releases from Jira:

* You create a new Release.

OR

* You populate a Jira Release.

### Create Release

Once you enable Jira integration in Katalon TestOps, the **Jira Project** and **Jira Release** sections are added in the **Create Release** page.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/create-release-page-once-jira-integrated.png" width="" height="">

Select your Jira Project and Jira Release in the dropdown menu, then click **Create**.

### Populate Jira Releases

Once you enable Jira integration in Katalon TestOps, the **Populate Jira Releases** button appears next to the **Create Release** button in the **Releases** page.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/populate-jira-release-button.png" width="" height="">

Click on the **Populate Jira Releases** button. The **Populate Jira Releases** box displays as below.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/populate-jira-release-box-popup.png" width="" height="">

Choose your Jira Release in the dropdown menu, then click **OK**.

## Link Test Runs to a Release

Follow these steps:

1. Go to your Project.

    The Project's **Dashboard** page appears.

2. Select the **Reports & Analytics** tab.

    The **Test Runs** page appears.

3. Scroll down the **Test Runs** page to see the list of all Test Runs and their IDs.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/scroll-down-for-test-run-id-list.png" width="" height="">

4. Click on the ID number in the **ID** column (e.g., click **21**).

    The page of that Test Run ID appears (e.g., **Test Run: #21**).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/test-run-id-21-page.png" width="" height="">

3. Click on the **Link to a release** button at the top right corner.

    The dropdown menu appears.

4. Select a Release in the dropdown menu.

> Notes:
>
> After linking the Test Runs to a Release, the Test Runs are shown under the **Release** section on your Jira page.

If a Test Run has already been linked before, click on the button (as shown below) at the top right corner and select a Release.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/kt_test_run_link_release1.png" width="" height="">
