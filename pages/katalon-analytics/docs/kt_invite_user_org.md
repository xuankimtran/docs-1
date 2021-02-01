---
title: "How to invite a user into an Organization"
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

This tutorial shows you how to create teams and projects.

> You need a Katalon account. Register [here](https://www.katalon.com/sign-up/) if you don't have one.

## **Organization-level roles and permissions** 

* **Owner** - is granted by default when creating a new organization or transferred by the other users, who have full permission related to the organization, including teams, users, projects, licenses, plugins, and subscriptions.
* **Admin** - is granted by the Owner, who has the Owner's privileges but cannot manage the subscriptions.
* **User** - is automatically assigned when a person joins an organization. Users can only monitor project progress.
* **Billing Manager** - is granted by the Owner or Admin, who has the User's privileges with additional permission to manage subscriptions.

## Invite a user to join organization

### As an Owner/Admin

> This feature is accesible to the organization **Owner** and **Admin** only.

* In **Katalon Administrantion** page, on the top right corner, click the symbol **Setting**. Click **User Management**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_set_org_user_manage.png)

* The **Manager User** displays with **Users** and **Pending Invitations**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_manager_user.png)

* Go to **Users** > Click on the **Invite user** button on the top right corner.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_user_manage_invite.png)

* Enter valid email addresses and click **Invite**. *Note: You can enter multiple accounts at the same time.*

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_invite_user.png)

* An invitation email will be sent to the invited members, or you can copy the activation link and send it to them to confirm and join your organization.

> After joining the organization, the new user can only access projects after being added to a team.

### As a User

After being invited to join organization, you will recieve an email with the subject *"Invitation to join Katalon Organization"*.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_mail_invite.png)

Accept the invitation by clicking the activation link in the email.

Sign in to the Katalons TestOps.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/login_kat_testops.png)

You will be navigated to the below page. Click on the blue button to join your organzation.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_invitation_org.png)

## Manage users

> This feature is accesible to the organization **Owner** and **Admin** only.

### View pending invitations

After inviting users to your organization, you can view the list of pending invitations in **Users** page.

Before users accept the invitation, their email address will display in the list with activation links. 

> You can withdraw the invitation by removing it from **PENDING INVITATIONS**.

### View a list of members in your organization

You can view the list of existing members in **Users** page once they have accepted the invitation to join your organization.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_manager_user.png)

> After joining the organization, their name and email address will display in the **Users** section with the default **User** role. You can update their permission by editing information on the User's details page.

### Remove an existing user

On the left sidebar, click **Users**. On the **Manager Users** click the remove icon in the last column and confirm your action in the pop-up.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_manage_user_remove_icon.png)

### Update user permission

**Assign Admin or User role**

The Admin and Owner can reassign the existing Admin and User to a new role. Select your organization/team > from **Users** Tab, click the pencil icon in the last column.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_manager_user_change_user.png)

On page **detail**, show **Role** select **Admin**, **User**, **Billing Manager** or **Owner** role in the drop-down list. A user can have different roles in different teams.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_change_role_user.png)

**Assign Billing Manager role**

**Billing Manager** role is only available at the organization level and granted by the organization Owner or Admin. Select your organization > from **Users** Tab, click the pencil icon in the last column and then select **Billing Manager** role in the drop-down list.

## Transfer organization ownership

The Owner and Admin of an organization can transfer the ownership of an Owner to another existing team member. 

* Select an organization, go to **Manage Users** page, go to the user's details page by clicking on the pencil icon.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_change_role_user.png)

* Select **Owner** in the drop-down list.

* Click **Update**.

> Note: Transferring Organization ownership does NOT affect Team ownership. The previous Owner still has full permission as a Team Owner to these teams, which have been created by them before.

## Rename an Organization

> This feature is accesible to the organization **Owner** and **Admin** only.

To rename an Organization, go to your Organization and click **Settings**, choose **Organization Management**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_set_org_management.png)

You can edit the name in the **Organization profile** section.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_org_profile.png)

Click **Update** to save your changes.

## Delete an Organization

> This feature is accesible to the organization **Owner** only.

To delete an Organization, click **Settings**, choose **Organization Management**, the **Settings** page displays. In the **Settings** page, you will see **Delete this organization** option. Click the button **I understand the consequences, delete this organization**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_set_delete_org.png)

Type the organization's name and click the button **I understand the consequences, delete this organization**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/kt_confirm_del_org.png)

> You cannot undo this action. You will permanently delete your organization, projects, licenses and remove all associated teams.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/delete-org.png" width="" height="">