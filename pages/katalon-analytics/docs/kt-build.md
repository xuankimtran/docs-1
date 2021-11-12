---
title: "Create and manage Builds" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-build.html

---

During the release cycle, you commonly need to test different builds to easily track production issues. In TestOps, the Build function allows you to associate and orchestrate the test runs relevant to each build.

## Create a build

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

2. Go to **Planning** > **Releases**.

3. Select a Release (e.g., **7.3.7**).

    The **Test Cases** page of the **7.3.7** Release appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/builds/create-build.png" width="" height="" alt="create build button">

4. Click on the **Create Build** button at the top right corner.
    
    The **Create Build** page appears.

5. Fill in the required information.

    * **Name**: enter the Build's name.
    * **Description**: add a note about your Build.
    * **Date**: enter the date you create this Build.

6. Click **Create**.

You have created a new Build. This Build now appears in the **Builds** section of the **7.3.7** Release.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/builds/build-list.png" width="" height="" alt="builds section">

### Link Test Runs to a build

You can link a Test Run to a Build (or a Release). See: [Link Test Runs to a Release](https://docs.katalon.com/katalon-analytics/docs/kt-release.html#link-test-runs-to-a-release).

> Notes:
>
> You can link multiple Test Runs to a Build.

After linking, you can view the linked Test Runs on the Build page.

## Manage a build

### View a build  

1. Go to **Planning** > **Releases**.

2. Select a Release.

3. Scroll down to view a list of Builds in the **Builds** section.

4. Select a Build.

    The Build page appears.

    You can view a list of Test Runs you have linked to this Build. 
    
    You can also see all Test Cases associated with this Build.

###  Update a build

1. Go to **Planning** > **Releases**.

2. Select a Release.

3. Scroll down to view a list of Builds in the **Builds** section.

4. Click on the *Extension* icon of the Build you want to update.

    <img src="https://raw.githubusercontent.com/katalon-studio/docs-images/testops-new/katalon-analytics/docs/build/build-edit-delete.png" width="" height="" alt="edit build">

5. Click **Edit**.

6. Update the Build's information.

7. Click **Save**.

You have updated a Build.

### Delete a build

1. Go to **Planning** > **Releases**.

2. Select a Release.

3. Scroll down to view a list of Builds in the **Builds** section.

4. Click on the *Extension* icon of the Build you want to delete.

5. Click **Delete**.

    The **Delete Build** box pops up as below.

    <img src="https://raw.githubusercontent.com/katalon-studio/docs-images/testops-new/katalon-analytics/docs/build/build-delete.png" width="" height="" alt="edit build">

6. Click **Delete** to confirm your action.

> Notice:
>
> You cannot undo this action.
    
See also: [Manage Test Runs by Release](https://docs.katalon.com/katalon-analytics/docs/kt-jira-release.html).
