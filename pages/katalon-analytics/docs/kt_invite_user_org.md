---
title: "TestOps User Management"
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

You can invite your team members into your Organization to work on projects.

> Requirements:
>
> You need a Katalon account. Register [Katalon account](https://www.katalon.com/sign-up/) if you don't have one.

## Roles and permissions at the Organization level

* **Owner**

By default, you become the Owner of the Organization you have created.

The Owner can also transfer ownership to another member.

* **Admin**

This role is granted by the Owner.

The Admin has similar privileges as the Owner but cannot manage the subscriptions.

* **User**

This role is automatically assigned to a person who joins an Organization.

Users can only monitor the project's progress.

* **Billing Manager**

This role is granted by the Owner or Admins.

The Billing Manager has similar privileges as the User and can also manage subscriptions.

## Invite a User to join an Organization

> Notes:
>
> Only the Owner or Admins of an Organization can do this.

Follow these steps:

1. Click on the **Settings** icon at the top right corner of the TestOps homepage and choose **User Management**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/kt-june-invite-user-org-1.png" width=100%>

    The **Manage Users** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/kt-june-invite-user-org-2.png" width=100%>
 
    You can see **Users** and **Pending Invitations** here.

2. Click on the **Invite user** button at the top right corner.

3. Enter valid email addresses, choose Katalon TestOps in **Product Access**, then click **Invite**.

> Notes:
>
> You can enter multiple email addresses at the same time.

Your team members will receive the invitation emails. Once they accept the invitation emails, they become Users in your Organization.

Alternatively, you can copy the activation link and send it to them.

> Notes:
>
> After joining your Organization, the new users are not yet part of a team. You have to add them to a team so that they can gain access to a project.

### As a User

If you are not the Owner nor Admin, you will receive an invitation to join the Organization via email.

1. Accept the invitation in the email.

     You will be directed to [Katalon TestOps](https://testops.katalon.io/login).

2. Sign in on the TestOps page.
 
    The invitation page appears.

3. Click on the blue button to join the Organization.

## Manage Users

> Only the Owner or Admins of an Organization can do this.

### View pending invitations

You can check all pending invitations on the **Manage Users** page.

> Notes:
>
> You can withdraw pending invitations by removing the email address in the **Pending Invitations** section.

### View the member list

On the **Manage Users** page, you can also view the list of all existing members.

Once your team members have accepted the invitations, the **Users** section will display their names, email addresses, and roles.

> Notes:
>
> The default role for team members is User. You can update their permissions on the **User's detail** page.

### Remove an existing User

In the **Manager Users** page, click on the *Trash bin* icon (next to the *Pencil* icon).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/kt-june-invite-user-org-3.png" width=100%>

A confirmation popup box appears. Click **Remove** to confirm.

### Change a User's permission

As an Owner or Admin, you can change the permissions of an existing member by following these steps:

1. Go to the **Manage Users** page.

2. Click on the *Pencil* icon.

    The **User's detail** page appears as below.
 
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/kt-june-invite-user-org-4.png" width=100%>

3. Select a new role in the dropdown list of the **Role** section, then click **Update**.

    > Notes:
    >
    > * Organization members can have different roles in different teams.
    > * The **Owner** role only appears in the dropdown list if you are the Owner of your Organization.
    > * The **Billing Manager** role is only available at the Organization level.

## Transfer Organization

> Notes:
>
> Only the Owner of an Organization can transfer the ownership to an existing team member.

In the **User's detail** page, click on the dropdown button. In the **Role** section, select **Owner**. Click **Update**.

This User is now the Owner of your Organization.

> Notes:
>
> Transferring Organization ownership does not affect Team ownership. The previous Organization Owner maintains Owner permissions for the Teams they have created.
