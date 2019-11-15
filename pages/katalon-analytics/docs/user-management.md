---
title: "User Management" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/user-management.html 
redirect_from:
    - "/display/KA/User+Management/"
    - "/display/KA/User%20Management/"
    - "/x/lQjR/"
    - "/katalon-analytics/docs/user-management/"
description: How to manage Users at organization and team level
---
Each role will have permission at the organization or team level exclusively. 

## Invite a user to the organization

* Available for Organization **Owner** or **Admin** user role.
* From Katalon TestOps dashboard, select an organization.
* From **Users Tab**, select **Invitations** tab.
* Enter an email address and click **Invite**.
* Copy the activation link and send to that person.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/user-management/KT-user-mgt-invitation.png)

The invited person accepts the invitation by clicking the activation link directing to Katalon Analytics and then clicking the name of the organization.
Before that person accepts the invitation, their email address will be listed in **PENDING INVITATIONS**. Once the person joins the organization, their name and email address will be shown below Users tab with the default role is User. 

The new user is only able to access the projects when added by the Owner or the Admin to a team.

> Notes: The owner can withdraw the invitation by removing it from **PENDING INVITATIONS**.

## Invite a user to the team

* Available for Team **Owner** and **Admin** user role.

> Note: Only user is already in an organization can be invited to a team in that organization. 

* Select a team, from **Users** Tab in a team, select that person's email in drop-down list and then click Add to add a user to a team. 
* The default role for invited person is **User**.

## Remove existing users from organization or team

From **Users** Tab, click the remove icon in the last column and confirm your action in the pop-up. 

* User is removed from Organization can be re-invited by Organization Owner or Admin. Refer to *Invite a user to the organization*.
* User is removed from Team can be re-added to work on projects, Refer to *Invite a user to the Team*

## Assign Admin or User roles to new and existing team members

The Admin and Owner can reassign the existing Admin and User to a new role. From **Users** Tab, click the pencil icon in the last column and then select a new role in the drop-down list. A user can have different roles in different teams.

## Transfer organization ownership to existing team member


