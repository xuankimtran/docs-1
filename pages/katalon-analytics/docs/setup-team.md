---
title: "Set up TestOps Team"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/setup-team.html
redirect_from:
    - "/katalon-analytics/docs/setup-team/"
---

A team is a group of users working on same projects. A team is created by either the Owner or Admin of an organization. 

Only the team members can view and access the team's projects.

## Roles and permission at team level

* **Owner**

You become the Owner by default if you create a new team.

As an owner, you have full permission to transfer the Owner role to another team member.

* **Admin**

This role is granted by the Owner.

An admin has similar privileges as the Owner but cannot transfer the team ownership to an existing team member.

* **User**

This role is automatically assigned to any person accepting the invitation to join the team.

A user can only monitor project progress.

## Creating a team

Follow these steps:

1. Click on the **Settings** icon at the top right corner of TestOps homepage and choose **Team Management**.

    The **Manage Teams** page appears.

2. Enter the team name and click **Create**

    You're the Team Owner by default.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/create-team.png" width="" height="">

### Adding Users to Team

1. Go to **Settings** > **Team Management**.

    The **Manage Teams** page appears.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-setup-team/kt-june-create-team-2.png" width="" height="">

2. Choose the team (e.g., Katalon TestOps).
    
    The team page appears.

3. Click **Users** on the left bar of the team page.

    The **Manage Users** page appeas.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-setup-team/kt-june-create-team-3.png" width="" height="">

4. Select users in **Add User to Team** section. Click **Add**.

> You have to [invite a User into an Organization](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html) first.
>
> Only users in the organization can be added to the team. 

### Removing existing Users

In the **Manage Users** page, click on the *Trash bin* icon (next to the *Pencil* icon) to remove a user.

A popup box appears. Confirm your action by clicking **Remove**.

## Transferting team ownership

The Owner can reassign **Owner** and lower roles to existing members.
The Admin can reassign **Admin** and lower roles to existing members.

In the **Manage Users** page, click on the *Pencil* icon to edit the user's role.

The **Edit Current User** box pops up. Select the new role in the dropdown list. Click **Save**.

A user can have different roles in different teams.

See also:

* [Create Organization and Projects](https://docs.katalon.com/katalon-analytics/docs/kt-create-org.html)
* [Integration of Katalon Studio with Katalon TestOps](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html)
