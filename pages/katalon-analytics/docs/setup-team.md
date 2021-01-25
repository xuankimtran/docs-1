---
title: "How to set up Katalon TestOps Team and Project"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/setup-team.html
redirect_from:
    - "/katalon-analytics/docs/setup-team/"
---

## Create a Team

Teams are groups of users that reflect the company's structures. A team is created by either Owner or Admin in an organization. Only members of a team can view and access the projects within that team.

In the top right corner, click **Setting**, and then click **Team Management**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/ka_set_team_manage.png)

In the **Manage Teams** view, select **Teams** on the left side-bar > give a name to your team and click **Create**. You're the team Owner by default.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/create-team.png" width="" height="">

## Add users to Team

In the top right corner, click **Setting**, and then click **Team Management**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/ka_set_user_mange.png)

Select the **Users** on the left side-bar. The lists of **Users** and **Pending Invitations** are on. Only the user, who you have just invited to the Organization, can be added to this team. Add your members to the team one by one by selecting **Invite user** on the top right corner.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/ka_manager_user_invite.png)

**Manage User** is on with the list of **Users** and **Pending Invitations**. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/add-users-team.png" width="" height=""> 

## **Team-level roles and permissions**

* **Owner** - is granted by default when creating new a team or transferred by other users, who has full permission related to the team, including users and projects of their team.
* **Admin** - is granted by the Owner, who has the privileges of the Owner but cannot transfer the team ownership to an existing team member.
* **User** - is automatically assigned when a person is first invited to collaborate in a team. Users can only monitor project progress.

## Invite a user to the team

* Only the team **Owner** or **Admin** can invite a user to the team.

> Note: Only the user in an organization can be invited to a team in that organization. 

* In the **Manage Teams** view, chose a team at the list **Teams**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_manage_team.png)

* The **Dashboard** is on. Click to the **Users** on the left sidebar. At the **Add User to Team** chose the users in the drop-down list. Then click **Add** to add users to the team..

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_manage_user_add_user.png)

* In the **Users** of **Manage Users**, the users and the owner are on. The default role for the invited person is **User**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_manage_user_new_user.png)

## Remove an existing user

Select your team in **Manage Teams**, chose **Users** on the left sidebar, click the icon **Remove user** ( ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_remove_icon.png) ) in the last column and confirm your action in the pop-up.

## Assign Admin or User role

The Admin and Owner can reassign the existing Admin and User to a new role. Select your organization/team > from **Users** Tab, click the pencil icon in the last column and then select **Admin** or **User** role in the drop-down list. A user can have different roles in different teams.

## Transfer team ownership

The Owner of a team can transfer the ownership to another existing team member. 

* Select a team > under **Users** tab, search for the target user to assign the **Owner** role.

* Click the pencil icon in the last column and then select **Owner** in the drop-down list.

* Click **Save**.

## Create Projects

A Katalon TestOps project is a handful of reports generated based on a dataset of automation test results which are imported by users. It would typically represent the development of automation testing work. A project is created only by Admins of a team with a particular name and automatically generated ID. There are many projects in a team.

Select **Projects** > give a name to your project and click **Create**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/create-project.png" width="" height="">

You have had your organization, team, and project. You can start working with Katalon TestOps now.

* [Integration of Katalon Studio with Katalon TestOps](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html)
