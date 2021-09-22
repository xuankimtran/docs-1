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
> You need a Katalon account. You can create a Katalon account on our website: [Sign Up to Katalon](https://www.katalon.com/sign-up/).

## Invite a User to join an Organization

> Notes:
>
> Only the Owner or Admins of an Organization can do this.

Follow these steps:

1. Click on the **Settings** icon at the top right corner of the TestOps homepage and choose **User Management**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/kt-june-invite-user-org-1.png" width=100% alt="kt settings">

    The **User Management** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-invite-user-org/kt-june-invite-user-org-2.png" width=100% alt="new user mgt ui">

2. Click on the **Invite User** button at the top right corner, then click **By Email**.

    A new window pops up asking you to enter the email and assign the product license to the new User.

3. Fill in the required information, then click **Invite members**.

    You can enter multiple email addresses to invite members. Multiple email addresses should be separated by a space.
    
Your team members will receive an invitation email containing a link. Once they click on the link, they become Users in your Organization.

Alternatively, you can copy the activation link in the **Pending Invitation** section and send it to them.

> Notes:
>
> After joining your Organization, the new users are not yet part of a team. You have to add them to a team so that they can gain access to a project.

## Manage Users

> Notes:
>
> Only the Owner or Admins of an Organization can do this.

### View the member list

Go to the **User Management** page and click on the **Active Users** tab.

You then can view the list of all existing members.

Once your team members have accepted the invitations to join your organization, you will see their full names, emails, their roles, the dates they have joined your organization, their license access and their most recent access to the organization in the **Active Users** section.

> Notes:
>
> The default role for team members is User. You can update their permissions by changing their roles.

### View pending invitations

Go to the **User Management** page and click on the **Pending Invitation** tab.

You can check all pending invitations here.

### Remove an existing User

1. Go to the **User Management** page.

2. Check the box next to the User's name to select the User and enable the **Remove User** button.

    You can remove multiple users by selecting multiple checkboxes.

3. Click **Remove User**.

4. Confirm your action in the popup screen.

You have removed the User from your Organization.

#### View the Removed Users list

Go to the **User Management** page and click on the **Removed Users** tab.

You can view a full list of users you have removed from your organization.

Use the search bar if you want to find a specific user you have removed.

### Change a User's role

As an Owner or Admin, you can change the role of an existing member by following these steps:

1. Go to the **User Management** page.

2. Check the box next to the User's name to select the User and enable the **Change Role** button.

    You can check multiple boxes if you want to update the same role for multiple users.

3. Select a new role in the dropdown list. then click **Change role**.

    > Notes:
    >
    > * Organization members can have different roles in different teams.
    > * The **Owner** role only appears in the dropdown list if you are the Owner of your Organization.
    > * The **Billing Manager** role is only available at the Organization level.

### Export a User's data

1. Go to the **User Management** page.

2. Check the box to select the User and enable the **Export User** button.

3. Click **Export User**.

    The User's data is exported in .csv format.

4. Download the .csv file.

> Notes:
>
> You can select multiple users to export their data.

## Transfer Organization

> Notes:
>
> Only the Owner of an Organization can transfer the ownership to an existing team member.

In the **User's detail** page, click on the dropdown button. In the **Role** section, select **Owner**. Click **Update**.

This User is now the Owner of your Organization.

> Notes:
>
> Transferring Organization ownership does not affect Team ownership. The previous Organization Owner maintains Owner permissions for the Teams they have created.
