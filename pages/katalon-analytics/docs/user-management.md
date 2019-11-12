---
title: "User Management" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/user-management.html 
redirect_from:
    - "/display/KA/User+Management/"
    - "/display/KA/User%20Management/"
    - "/x/lQjR/"
    - "/katalon-analytics/docs/user-management/"
description: 
---

In Katalon Analytics, each user is identified with the same account registered for Katalon Studio. User Management is only available for the *Owner* and *Admins* in an organization.  

## Default Roles

**In organizational level** 

* Users are the _Owners_ of their own organizations by default.
* An _Admin_ is granted by the _Owner_.
* A _User_ is automatically assigned when a person is first invited to collaborate in an organization.
* A _Billing Manager_ is granted by the _Owner_ to manage the subscription.

**In team level**

* Organizational admins are the _Owners_ of those teams created by them.
* A Team _Admin_ is granted by the team _Owner_.
* A _User_ is automatically assigned when a person is first invited to collaborate in a team.

## Roles and default permissions

**Owner**

* Create new organization.
* Create and manage teams.
* Create and delete projects.
* Invite new users to your organization and to collaborate on your projects.
* Assign *Admin* or *User* or *Billing Manager* roles to new or existing team members.
* Transfer organization or team ownership to existing team member.
* Remove existing *Admins* or *Users* from your organization and projects.
* Monitor project progress.
* Upload test results.
* Manage KSE, RE and TestOps On-Premise License.
* Search and Download Plugins.
* Subscribe KSE, RE and TestOps On-Premise license.

**Admin**

* Create new organization.
* Create and manage teams.
* Create and delete projects.
* Invite new users to collaborate on your projects.
* Assign *Admin* or *User* or *Billing Manager* roles to new or existing team members.
* Transfer organization and team ownership to existing team member.
* Remove existing *Admins* or *Users* from your organization or projects.
* Monitor project progress.
* Upload test results.
* Manage KSE, RE and TestOps On-Premise License.
* Search and Download Plugins.

**Billing Manager**

* Create new organization.
* Monitor project progress.
* Upload test results.
* View number of subscribed license for KSE, RE and TestOps On-Premise
* Search and Download Plugins.
* Subscribe KSE, RE and TestOps On-Premise license.

**Users**

* Create and delete projects.
* Invite new users to collaborate on your projects.
* Monitor project progress.
* Upload test results.
* Search and Download Plugins.

## User-related permissions

**Invite a new user**

Before joining a project, a user is required to join the organization that hosts the project. The invited person is required to have a Katalon account. If the person invited to collaborate on Katalon Analytics projects doesn't have one, an email will be sent to help that person create one.

_Invite a person to your organization:_

* From Katalon Analytics home page, select the organization
* From __Users Tab__, click __Invitations__
* Enter an email address and click __Invite__
* Copy the activation link and send to that person

![User Tab](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/user-management/KT-user-mgt-invitation.png)

The invited person accepts the invitation by clicking the activation link directing to Katalon Analytics and then clicking the name of the organization.

Before that person accepts the invitation, their email address will be listed in __PENDING INVITATIONS__. Once the person joins the organization, their name and email address will be listed below __Users__. The new user is only able to access the projects when added by the Owner or the Admin to a team.
> Notes: The owner can withdraw the invitation by removing it from __PENDING INVITATIONS__.

_Invite a user to your team:_

Only users in an organization can be invited to a team in that organization. Select a team, from __Users Tab__ in a team, select that person's email in drop-down list and then click __Add__ to add a user to a team.

**Remove existing users**

From __Users__ Tab, click the remove icon in the last column and confirm your action in the pop-up. The removed user can be re-added to the project if necessary (refer to *Invite a user to a team*)

**Assign Admin or User roles to new or existing team members**

The *Admin* and *Owner* can reassign the existing *Admin* or *User* to a new role. From __Users__ Tab, click the pencil icon in the last column and then select a new role in the drop-down list.
A user can have different roles in different teams.

**Transfer Ownership of Organization or Team to new or existing team members**

The *Owner* and *Admin* can transfer the organization or team ownership to the existing *Admin* or *User*. From __Users__ Tab, click the pencil icon in the last column and then select *Owner* role in the drop-down list.

## Project-related permissions

**[Upload test results from Katalon Studio](https://docs.katalon.com/katalon-analytics/docs/katalon-analytics/docs/project-management-import-KS.html)**

**[Upload test results using Command Line](https://docs.katalon.com/katalon-analytics/docs/katalon-analytics/docs/project-management-import-cli.html)**

**[Monitor project progress](https://docs.katalon.com/katalon-analytics/docs/project-management-view-reports.html)**

**[Delete projects](https://docs.katalon.com/katalon-analytics/docs/project-management-delete.html)**

## Subscription-related permissions

**[Katalon License Subscription](https://docs.katalon.com/katalon-studio/docs/license-subscription.html)**
