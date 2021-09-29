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

> Requirements:
>
> You need a Katalon account. [Sign up to Katalon](https://www.katalon.com/sign-up/).

## Invite Users to join an Organization

> Notes:
>
> Only the Owner or Admins of an Organization can do this.

Follow these steps:

1. Click on the **Settings** icon at the top right corner of the TestOps homepage and choose **User Management**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/k1-user-mgt-settings.png" width=100% alt="kt settings">

    The **User Management** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/k1-user-mgt-page-new-ui.png" width=100% alt="new ui user mgt page">

2. Click **Invite Users** at the top right corner.

    A new window pops up asking you to enter the email and assign the product license to the new User.

3. Fill in the required information, then click **Invite**.

    You can enter multiple email addresses to invite members. Multiple email addresses should be separated by a space or comma, or *Enter*.

Your team members will receive an invitation email containing a link. Once they click on the link and accept the invitation, they become Users in your Organization.

Alternatively, you can copy the activation link in the **Pending Invitation** section and send it to them.

> Notes:
>
> The default role for team members is Member, you can change this role later anytime.

## Manage Users

> Notes:
>
> Only the Owner or Admins of an Organization can do this.

### View the members list

Go to the **User Management** page and click on the **Active Users** tab.

You then can view the list of all existing members.

Once your team members have accepted the invitations to join your organization, you will see their full names, emails, their roles, the dates they have joined your organization, their license access and their most recent access to the organization in the **Active Users** section.

> Notes:
>
> You can update their permissions by changing their roles.

### View pending invitations

Go to the **User Management** page and click on the **Pending Invitation** tab.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/k1-pending-invitation-tab.png" width=100% alt="pending invitation tab">

You can check all pending invitations here.

### View the removed users list

Go to the **User Management** page and click on the **Removed Users** tab.

<img src="https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/k1-removed-users-tab.png" width=100% alt="removed users tab">

You can view a full list of users you have removed from your organization.

### Search Users

In the **Active Users** section, use the search bar if you want to find a specific user.

In the **Pending Invitations** section, use the search bar if you want to find the invitation to a specific user.

In the **Removed Users** section, use the search bar if you want to find the user you have removed.

### Revoke invitations

1. Go to the **User Management** page and click on the **Pending Invitation** tab.

2. Check the box next to the name to select and enable the **Revoke** button.

    You can revoke multiple invitations by selecting multiple checkboxes.

3. Click **Revoke**.

    The **Revoke Invitation** box pops up.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/k1-revoke-invitation-popup.png" width=100% alt="revoke invitation popup">

4. Double check the email addresses, then click **Revoke**.

You have revoked the invitations. The invitation links your team members have received now become invalid.

### Remove existing Users

1. Go to the **User Management** page, and click on the **Active Users** tab.

2. Check the box next to the User's name to select the User and enable the **Remove Users** button.

    You can remove multiple users by selecting multiple checkboxes.

3. Click **Remove**.

    The **Remove Users** box pops up.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/k1-remove-users-popup.png" width=100% alt="remove users popup">

4. Click **Remove** to confirm your action.

You have removed the users.

> Notes:
>
> * The users cannot log in to your organization after being removed.
> * You still keep the data the users have performed in your organization and you can invite them back to your organization anytime.

### Change Users' roles

In an organization, different roles have different permissions. See: [Roles and permissions](https://docs.katalon.com/katalon-analytics/docs/testops-roles-privileges.html).

As an Owner or Admin, you can change the role of an existing member by following these steps:

1. Go to the **User Management** page.

2. Check the box next to the User's name to select the User and enable the **Change Role** button.

    You can check multiple boxes if you want to update the same role for multiple users.

3. Click **Change Role**.

    The **Change User Role** box pops up.
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/k1-change-user-role-popup.png" width=100% alt="change user role popup">

4. Select a new role in the dropdown list, then click **Change Role**.

    > Notes:
    >
    > * Organization members can have different roles in different teams.
    > * The **Billing Manager** role is only available at the Organization level.

### Export Users list

1. Go to the **User Management** page.

2. Click **Export User** at the top right corner.

    The Users list is exported in .csv format.
    
> Notes:
>
> The exported file contains **Active Users** list and **Removed Users** list.
