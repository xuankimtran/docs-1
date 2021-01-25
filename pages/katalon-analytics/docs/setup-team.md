---
title: "How to set up Katalon TestOps Team and Project"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/setup-team.html
redirect_from:
    - "/katalon-analytics/docs/setup-team/"
---

## Create a Team

Teams are groups of users that reflect the company's structures. A team is created by either Owner or Admin in an organization. Only members of a team can view and access the projects within that team.

In the top right corner, click icon **Settings**, and then click **Team Management**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/ka_set_team_manage.png)

In the **Manage Teams** view, select **Teams** on the left side-bar > give a name to your team and click **Create**. You're the team Owner by default.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/create-team.png" width="" height="">

## Add users to Team

In the top right corner, click icon **Settings**, and then click **Team Management**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/ka_set_user_mange.png)

Select **Users** on the left sidebar. The lists of **Users** and **Pending Invitations** display. Only the user, who you have just invited to the Organization, can be added to this team. Add your members to the team one by one by selecting **Invite user** on the top right corner.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/ka_manager_user_invite.png)

**Manage User** displays with the list of **Users** and **Pending Invitations**. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/add-users-team.png" width="" height=""> 

## **Team-level roles and permissions**

* **Owner** - is granted by default when creating new a team or transferred by other users, who has full permission related to the team, including users and projects of their team.
* **Admin** - is granted by the Owner, who has the privileges of the Owner but cannot transfer the team ownership to an existing team member.
* **User** - is automatically assigned when a person is first invited to collaborate in a team. Users can only monitor project progress.

## Invite a user to the team

* Only the team **Owner** or **Admin** can invite a user to the team.

> Note: Only the user in an organization can be invited to a team in that organization. 

* In the **Manage Teams** view, choose a team in the list **Teams**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_manage_team.png)

* The **Dashboard** displays. Click **Users** on the left sidebar. At the **Add User to Team** choose the users in the drop-down list. Then click **Add** to add users to the team.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_manage_user_add_user.png)

* In the **Users** of **Manage Users**, the users and owner display. The default role for the invited person is **User**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_manage_user_new_user.png)

## Remove an existing user

Select your team in **Manage Teams**, choose **Users** in the left sidebar, click the icon **Remove user** ( ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_remove_icon.png) ) in the last column and confirm your action in the pop-up.

## Transfer team ownership

The Admin and Owner can reassign the existing Admin and User to a new role. In the **Users** of **Manage Users**, click the pencil icon in the last column and then select **Admin**, **User** or **Owner** role in the drop-down list and click **Save**. A user can have different roles in different teams.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_edit_role_user.png)

## Create Projects

A Katalon TestOps project is a handful of reports generated based on a dataset of automation test results which are imported by users. It would typically represent the development of automation testing work. A project is created only by Admins of a team with a particular name and automatically generated ID. There are many projects in a team.

* On the top right corner, click icon **Settings**.
* Click **Project Management**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_setting_project_manage.png)

* On the top right corner, click the button **Create Project**, select the team in **Choose Team**, and click the button **Next**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_creat_new_team.png)

Select **Projects** (on the left sidebar), give a name to your project and click **Create**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/create-project.png" width="" height="">

You have had your organization, team, and project. You can start working with Katalon TestOps now.

* [Integration of Katalon Studio with Katalon TestOps](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html)
