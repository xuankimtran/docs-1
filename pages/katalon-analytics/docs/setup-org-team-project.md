---
title: "How to set up Katalon TestOps Organization"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/setup-org-team-project.html
redirect_from:
    - "/katalon-analytics/docs/manage-org.html"
    - "/katalon-analytics/docs/kt-user-role-permission.html"
    - "/display/KA/User+Management/"
    - "/display/KA/User%20Management/"
    - "/x/lQjR/"
    - "/katalon-analytics/docs/user-management/"
    - "/katalon-analytics/docs/setup-org-team-project/"
    - "/katalon-analytics/docs/manage-org.html"

---
This tutorial shows you how to set up an Organization properly in Katalon TestOps, and to create teams and projects. One member of the team can complete these steps to invite all the others to an Organization for working on projects.

> You need a Katalon account. Register [here](https://www.katalon.com/sign-up/) if you don't have one.

## Create an Organization

Organizations are shared Katalon TestOps accounts where groups of users can collaborate across several projects at once. A user defaults to owning a personal organization and can belong to many organizations.

1. Log into Katalon TestOps
2. On the home page, click **Create Organization** at the bottom and confirm your action

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/create-org.png" width="" height="">

   You have just created an Organization in which you are the Owner.
3. In the **Organization** View, give a name to your Organization. Here is you can also view your Organization ID.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/org-name.png" width="" height=""> 

## **Organization-level roles and permissions** 

* **Owner** - is granted by default when creating a new organization or transferred by other users, who has full permission related to the organization, including teams, users, projects, licenses, plugins, and subscriptions.
* **Admin** - is granted by the Owner, who has the privileges of the Owner but cannot manage the subscriptions.
* **User** - is automatically assigned when a person is first invited to collaborate in an organization. Users can only monitor project progress.
* **Billing Manager** - is granted by the Owner or Admin, who has the privileges of the User with additional permission to manage subscriptions.

## Invite a user to join organization

### As an Owner/Admin

> This feature is accesible to the organization **Owner** and **Admin** only.

* In [Katalon Admin](https://admin.katalon.com) page, select an organization.
* Go to **Users** > Click on the **Invite user** button.
* Enter valid email addresses and click **Invite**. *Note: You can enter multiple accounts at the same time.*

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/invite-user.png)

* An invitation email will be sent to the invited members, or you can copy the activation link and send it to them to confirm and join your organization.

> After joining the organization, the new user can only access projects after being added to a team.

### As a User

After being invited to join organization, you will recieve an email with the subject *"Invitation to join Katalon Organization"*.

Accept the invitation by clicking the activation link in the email or the one sent by your admin.

You will be navigated to the below page. Click on the blue button to join your organzation.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/accept-invitation.png)

## Manage users

> This feature is accesible to the organization **Owner** and **Admin** only.

### View pending invitations

After inviting users to your organization, you can view the list of pending invitations in **Users** page.

Before users accept the invitation, their email address will be displayed in the list with activation links. 

> You can withdraw the invitation by removing it from **PENDING INVITATIONS**.

### View a list of members in your organization

You can view the list of existing members in **Users** page once they have accepted the invitation to join your organization.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/manage-users.png" width="" height="">

> After joining the organization, their name and email address will be displayed in the **Users** section with the default **User** role. You can update their permission by editing information in the user's details page.

### Remove an existing user

Select your organization > from **Users** tab, click the remove icon in the last column and confirm your action in the pop-up.

### Update user permission

**Assign Admin or User role**

The Admin and Owner can reassign the existing Admin and User to a new role. Select your organization/team > from **Users** Tab, click the pencil icon in the last column and then select **Admin** or **User** role in the drop-down list. A user can have different roles in different teams.

**Assign Billing Manager role**

**Billing Manager** role is only available at the organization level and granted by the organization Owner or Admin. Select your organization > from **Users** Tab, click the pencil icon in the last column and then select **Billing Manager** role in the drop-down list.

## Transfer organization ownership

The Owner and Admin of an organization can transfer the ownership of an Owner to another existing team member. 

* Select an organization > go to **Users** page > go to the user's details page by clicking on the pencil icon.

* Select **Owner** in the drop-down list.

* Click **Save**.

> Note: Transferring Organization ownership does NOT affect Team ownership. The previous Owner still has full permission as a Team Owner to those teams having been created by them before.

## Rename an Organization

> This feature is accesible to the organization **Owner** and **Admin** only.

To rename an Organization, go to your Organization and click on **Organization Settings**. You can edit the name in the **Organization profile** section.

Remember to click on **Update** to save your changes.

## Delete an Organization

> This feature is accesible to the organization **Owner** only.

To delete an Organization, click on **Organization Settings**.

In the **Settings** page, you will see **Delete this orgainzation** option. Click on the button and complete confirmation steps.

> This action cannot be undone. This will permanently delete your organization, projects, licenses, and remove all associated teams.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/delete-org.png" width="" height="">