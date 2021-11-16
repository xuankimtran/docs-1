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

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

    The Project's **Dashboard** page appears.

2. Go to **Planning** > **Releases**.

    The **Releases** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/create-release-in-test-planning-testops-2.png" width="" height="" alt="release page">

3. Click on the **Create Release** button at the top right corner.

    The **Create Release** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/create-release-page-appears-2.png" width="" height="" alt="create release page">

4. Fill in the required information.
    * **Name**: your Release version (e.g., Release **8.0**).
    * **Start Date**: when you want to start your Release.
    * **Release Date**: when you want to end your Release.

5. Click **Create**.

## Populate a Jira Release

> Requirements:
>
> You have enabled Jira integration. See: [Jira Settings](https://docs.katalon.com/katalon-analytics/docs/kt-jira-config.html).

There are two ways to populate Releases from Jira:

* You create a new Release.

OR

* You populate a Jira Release.

### Create Releases

Once you have enabled Jira integration in Katalon TestOps, the **Jira Project** and **Jira Release** sections are added in the **Create Release** page.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/create-release-page-once-jira-integrated.png" width="" height="" alt="create release jira integrated page">

Select your Jira Project and Jira Release in the dropdown menu, then click **Create**.

### Populate Jira Releases

Once you have enabled Jira integration in Katalon TestOps, the **Populate Jira Releases** button appears next to the **Create Release** button on the **Releases** page.

Click on the **Populate Jira Releases** button.

The **Populate Jira Releases** box pops up.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/populate-jira-release-box-popup.png" width="" height="" alt="populate jira release popup">

Select your Jira Release in the dropdown menu, then click **OK**.

## Link Test Runs to a Release

Follow these steps:

1. Go to your Project.

    The Project's **Dashboard** page appears.

2. Go to **Reports** > **Test Runs**.

3. Scroll down to see the list of all Test Runs and their IDs.

4. Click on the ID number of a Test Run.

    The **Test Run: #** page appears, and **#** represents the ID number (e.g., **Test Run: #21**).

3. Click on the **Link to a release** button at the top right corner.

    The dropdown menu appears.

4. Select a Release in the dropdown menu.

> Notes:
>
> After linking the Test Runs to a Release, these Test Runs are shown under the **Release** section on your Jira page.

### Link Test Runs to a different Release

If you have already linked a Test Run to a Release, the **Test Run: #** page displays as below.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-releases/test-run-already-linked-to-a-release-2.png" width="" height="" alt="linked release button">

For example, **Test Run: #1234** has already been linked to Release **8.0**.

You can link this Test Run to a different Release by clicking on the icon next to the current Release (next to **8.0**), then select the new Release you want to link.

> Notes:
>
> You can also unlink a Test Run by selecting the **Clear this release** option.
