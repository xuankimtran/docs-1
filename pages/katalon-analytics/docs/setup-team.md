---
title: "Set up TestOps Team"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/setup-team.html
redirect_from:
    - "/katalon-analytics/docs/setup-team/"
---

A Team is a group of Users working on same projects. A Team is created by either the Owner or Admins of an Organization.

Only the team members can view and access the Team's projects.

## Roles and permission at the Team level

* **Owner**

You become the Owner by default if you create a new Team.

As an Owner, you have full permission to transfer the Owner role to another team member.

* **Admin**

This role is granted by the Owner.

The Admin has similar privileges as the Owner but cannot transfer the Team ownership to an existing team member.

* **User**

This role is automatically assigned to any person accepting the invitation to join the Team.

Users can only monitor project progress.

## Create a Team

Follow these steps:

1. Click on the **Settings** icon at the top right corner of TestOps homepage and choose **Team Management**.

    The **Manage Teams** page appears.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-setup-team/kt-june-create-team-2.png" width="" height="">
2. Enter the Team name and click **Create**.

    You are the Owner of your Team.

### Add Users to a Team

1. Go to **Settings** and choose **Team Management**.

    The **Manage Teams** page appears.


2. Choose the Team (e.g., Katalon TestOps).
    
    The Team page appears.

3. Click **Users** on the left bar of the Team page.

    The **Manage Users** page appears.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-setup-team/kt-june-create-team-3.png" width="" height="">

4. Select team members in **Add User to Team** section. Click **Add**.

> Notes:
>
> You have to [invite a User into an Organization](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html) first. Only Users in the Organization can be added to the Team.

### Remove existing Users

In the **Manage Users** page, click on the *Trash bin* icon (next to the *Pencil* icon) to remove a User.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-setup-team/kt-june-create-team-4.png" width="" height="">

A popup box appears. Confirm your action by clicking **Remove**.

## Transfer Team ownership

The Owner can reassign **Owner** and lower roles to existing members.

The Admin can reassign **Admin** and lower roles to existing members.

In the **Manage Users** page, click on the *Pencil* icon to edit the user's role.

The **Edit Current User** box pops up. Select the new role in the dropdown list. Click **Save**.

> Notes:
>
> Users can have different roles in different teams.

See also:

* [Integration of Katalon Studio with Katalon TestOps](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html)
