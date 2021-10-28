---
title: "Delete data" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/project-management-delete.html 
redirect_from:
    - "/display/KA/Project+and+Execution+Deletion/"
    - "/display/KA/Project%20and%20Execution%20Deletion/"
    - "/x/pwbR/"
    - "/katalon-analytics/docs/project-management-delete/"
description: 
---

> Notice:
>
> You cannot recover the deleted projects and executions. Delete them with caution.

## Delete a Project

> Requirements:
>
> You must be the Owner or Admin of a Team.

Follow these steps:

1. Go to **Settings** > **Team Management**.

    The **Manage Teams** page appears.

2. Choose your Team in the **Teams** section.

    The Team's **Dashboard** page appears.

3. Select **Projects** on the left bar to view all Projects your Team has.

    The **Manage Projects** page appears.

4. Click on the *Settings* icon of the Project you want to delete.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-delete-data/manage-project-page-settings-icon.png"  width=100% alt="manage project page">

    The **Project Settings** page appears.

5. Scroll down to the **Danger zone** section, and click **Delete this project**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-delete-data/project-settings-page-danger-zone-section.png" width=100% alt="delete this project button">

6. Enter the Project's name, then click **I understand the consequences, delete this project** to confirm your action.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-delete-data/delete-project-popup-confirm-action.png" width=100% alt="delete this project button">

## Delete an Execution

> Requirements:
>
> You must be the Owner or Admin of an Organization.

1. Go to your Project > **Reports & Analytics** > **Test Runs**.

2. Click on the *Extension* icon of the Test Run you want to delete and choose **Delete**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-delete-data/extension-icon-delete-button.png"  width=100% alt="extension icon for deletion">

    The **Delete Execution** box then pops up.

3. Click **Delete** to confirm your action.

> Notes:
> 
> After deleting, it might take a while for the Execution to disappear from the Test Runs list.

### Delete multiple Executions

In Katalon TestOps, you can also delete multiple Executions at the same time by using the bulk selection feature.

1. Go to your Project > **Reports & Analytics** > **Test Runs**.

2. Check the boxes (as shown below) to select the Executions you want to delete.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-delete-data/bulk-selection-for-execution-delete.png"  width=100% alt="test runs page bulk delete appears">

    A new command row appears at the top of the **Test Runs** page after you check the boxes.

3. Select **Delete**.

4. Confirm your action in the **Delete Execution** popup box.

You have deleted your Executions.