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

## Invite a user to the organization

* Only the organization **Owner** or **Admin** can invite a user to the organization.
* From Katalon TestOps dashboard, select an organization.
* From **Users** tab, select **Invitations** tab.
* Enter an email address and click **Invite**.
* Copy the activation link and send it to that person.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/user-management/KT-user-mgt-invitation.png)

The invited person accepts the invitation by clicking the activation link directing to Katalon TestOps and then clicking the name of the organization.
Before that person accepts the invitation, their email address will be listed in **PENDING INVITATIONS**. Once the person joins the organization, their name and email address will be shown below the **Users** tab with the default User role. 

The new user can only access projects when added by the team Owner or Admin to a team.

> Notes: The Owner/Admin can withdraw the invitation by removing it from **PENDING INVITATIONS**.

## Remove an existing user

Select your organization > from **Users** tab, click the remove icon in the last column and confirm your action in the pop-up.

## Assign Admin or User role

The Admin and Owner can reassign the existing Admin and User to a new role. Select your organization/team > from **Users** Tab, click the pencil icon in the last column and then select **Admin** or **User** role in the drop-down list. A user can have different roles in different teams.

## Assign Billing Manager role

**Billing Manager** role is only available at the organization level and granted by the organization Owner or Admin. Select your organization > from **Users** Tab, click the pencil icon in the last column and then select **Billing Manager** role in the drop-down list.

## Transfer organization ownership

The Owner and Admin of an organization can transfer the ownership of an Owner to another existing team member. 

* Select an organization > select **Users** tab > search for the target user to assign the **Owner** role.

* Click the pencil icon in the last column and then select **Owner** in the drop-down list.

* Click **Save**.

> Note: Transferring Organization ownership does NOT affect Team ownership. The previous Owner still has full permission as a Team Owner to those teams having been created by them before.

## Rename an Organization

> Only **Owner** can access this feature.

To rename an Organization, go to your Organization and click on **Organization Settings**. You can edit the name in the **Organization profile** section.

Remember to click on **Update** to save your changes.

## Delete an Organization

> Only **Owner** can access this feature.

To delete an Organization, click on **Organization Settings**.

In the **Settings** page, you will see **Delete this orgainzation** option. Click on the button and complete confirmation steps.

> This action cannot be undone. This will permanently delete your organization, projects, licenses, and remove all team associations.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/setup-org-team-project/delete-org.png" width="" height="">