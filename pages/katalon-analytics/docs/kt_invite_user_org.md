---
title: "Invite a User into TestOps Organization"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt_invite_user_org.html
redirect_from:
 - "/katalon-analytics/docs/kt-user-role-permission.html"
 - "/display/KA/User+Management/"
 - "/display/KA/User%20Management/"
 - "/x/lQjR/"
 - "/katalon-analytics/docs/user-management/"
 - "/katalon-analytics/docs/setup-org-team-project/"
---

You can invite your team members into your organization to work on projects.

> You need a Katalon account. Register [here](https://www.katalon.com/sign-up/) if you don't have one.

## Roles and permissions at organization level

* **Owner**

By default, you become the Owner of the organization you have created.

You can also become the Owner of an organization through ownership transferring.

* **Admin**

This role is granted by the Owner. 

An admin has similar privileges as the Owner but cannot manage the subscriptions.

* **User**

This role is automatically assigned to a person who joins an organization.

A user can only monitor the project's progress.

* **Billing Manager**

This role is granted by the Owner or admins.

A billing manager has similar privileges as a user and can also manage subscriptions.

## Inviting a user to join an organization

> Only the Owner or Admins of an organization can do this.

Follow these steps:

1. Click on the **Settings** icon at the top right corner of the TestOps homepage and choose **User Management**.

 <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/kt-june-invite-user-org-1.png" width=100%>

 The **Manage Users** page appears as below.

 <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/kt-june-invite-user-org-2.png" width=100%>
 
 You can see **Users** and **Pending Invitations** here.

2. Click on the **Invite user** button at the top right corner.

3. Enter valid email addresses, choose Katalon TestOps in **Product Access**, then click **Invite**.

> You can enter multiple email addresses at the same time.

Your team members will receive the invitation emails. Once they accept the invitation emails, they become users in your organization.

Alternatively, you can copy the activation link and send it to them.

> After joining your organization, the new users are not yet part of a team. You have to add them to a team so that they can gain access to the projects.

### As a user

If you are not the Owner nor Admin, you will receive an invitation to join the organization via email.

1. Accept the invitation in the email.

 You will be directed to [Katalon TestOps](https://testops.katalon.io/login).
2. Sign in TestOps page. 
 
 The invitation page appears. 
3. Click on the blue button to join the organization.

## Managing users

> Only the Owner or Admins of an organization can do this.

### Viewing pending invitations

Unless your team members accept the invitations, you can check all pending invitations on the **Manage Users** page.

> You can withdraw the invitation by removing the email address in the **Pending Invitations** section.

### Viewing the member list

On the **Manage Users** page, you can also view the list of all existing members.

Once your team members have accepted the invitations, the **Users** section will display their names, email addresses, and roles.

> After joining your organization, their roles are users by default. You can update their permission on the User's detail page.

### Removing an existing user

In the **Manager Users** page, click on the *Trash bin* icon (next to the *Pencil* icon).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/kt-june-invite-user-org-3.png" width=100%>

The pop-up box appears. Confirm your action by clicking **Remove**.

### Updating a user's permission

The Owner and Admin can reassign a role to the existing member by following these steps:

1. Go to the **Manage Users** page.

2. Click on the *Pencil* icon.

 The User's detail page appears as below.

 <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/kt-june-invite-user-org-4.png" width=100%>

3. Select a new role in the drop-down list of the **Role** section, then click **Update**.

 You can choose between **Admin**, **User**, **Billing Manager** or **Owner** role. 
 
 A user can have different roles in different teams.

> The **Owner** role only appears in the drop-down list if you are the Owner of your organization.
>
>The **Billing Manager** role is only available at the organization level.

## Transferring organization ownership

> Only the Owner of an organization can transfer the ownership to an existing team member.

In the User's detail page, choose **Owner** in the drop-down list of the **Role** section and click **Update**.

The User now becomes the Owner of your organization.

>Transferring the organization ownership does NOT affect the team ownership. The previous Owner still has full permission as Team Owner if the previous Owner has created that team before.

