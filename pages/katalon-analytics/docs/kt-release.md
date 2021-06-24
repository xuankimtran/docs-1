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

3. Click on the **Create Release** button at the top right corner.

    The **Create Release** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/create-release-page-appears.png" width="" height="">

4. Fill in the required information.
    * **Name**: your Release version (e.g., Release **8.0**).
    * **Start Date**: when you want to start your Release.
    * **Release Date**: when you want to end your Release.

5. Click **Create**.

## Populate a Jira Release

> Notes:
>
> You must enable Jira integration in Katalon TestOps first.

There are two ways to populate Releases from Jira:

* You create a new Release.

OR

* You populate a Jira Release.

### Create Releases

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

4. Click on the ID number a the Test Run.

    The **Test Run: #** page appears, and **#** represents the ID number (e.g., **Test Run: #21**).

3. Click on the **Link to a release** button at the top right corner.

    The dropdown menu appears.

4. Select a Release in the dropdown menu.

> Notes:
>
> After linking the Test Runs to a Release, these Test Runs are shown under the **Release** section on your Jira page.

### Link Test Runs to a different Release

If you have already linked a Test Run to a Release, the **Test Run: #** page displays as below.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/test-run-already-linked-to-a-release.png" width="" height="">

For example, **Test Run: #1234** has already been linked to Release **8.0**.

You can link this Test Run to a different Release by clicking on the button next to the current Release (next to **8.0**).

The scrolldown menu appears as below.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/test-run-already-linked-scrolldown-menu.png" width="" height="">

Select the new Release you want to link.

> Notes:
>
> You can also unlink a Test Run by selecting the **Clear this release** option.
