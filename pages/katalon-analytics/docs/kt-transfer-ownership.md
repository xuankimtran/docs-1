---
title: "Transfer Ownership"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt_transfer_ownership.html
description:
---

> Requirements:
>
> You must be the Owner of your Organization.

You may want to transfer ownership in the following circumstances:

* When you want to change your current email address.
* When you want to transfer your Organization to another member.

## Transfer ownership to an existing member

> Requirements:
>
> You have invited the user to join your Organization. See: [Invite users to join an Organization](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html#invite-users-to-join-an-organization).

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login).

2. Go to **Settings** > **User Management**.

    The **User Management** page appears. You can see a list of active members in the **Active Users** section.

3. Mouse over the member you want to select, then click on the *Extension* icon at the end of the row.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-nov-release-transfer-ownership/image-20211110-045945.png" width=100% alt="extension icon click">

4. Select **Transfer Ownership**.

    The **Transfer Ownership** box pops up as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-nov-release-transfer-ownership/image-20211110-045956.png" width=100% alt="transfer ownership popup">

5. Check the email address you want to transfer ownership to.

6. Enter your account's password for authentication.

7. Click **Transfer Ownership**.

    > Notice:
    >
    > You cannot undo this action.

You have transferred the Organization to the selected email address/member.

That member is now the Owner of your Organization. The new Owner has all privileges (including ownership transfering) in the Organization. See: [Roles and permissions](https://docs.katalon.com/katalon-analytics/docs/testops-roles-privileges.html).

After transfering ownership, your role has automatically become the **Admin** role.

> Notes:
>
> * Transferring Organization ownership does not affect Team ownership. The previous Organization Owner maintains Owner permissions for the Teams they have created.

## Transfer ownership to a new email address

As an Owner of an Organization, the email address you have registered with Katalon TestOps is bound to your TestOps Organization and becomes a unique ID. You cannot change this unique ID.

If you want to change your email address, follow these steps:

1. Create a new account using your new email address.
2. Send an invitation to join the Organization to the new email address. See: [Invite users to join an Organization](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html#invite-users-to-join-an-organization).
3. Join the Organization as a new user. See: [Join TestOps Organizations](https://docs.katalon.com/katalon-analytics/docs/kt_users_joining_org.html).
4. Transfer ownership to the new email address. See: [Transfer Ownership](katalon-analytics/docs/kt_transfer_ownership.html#transfer-ownership-to-an-existing-member).
5. Delete the old account. See: [Remove existing users](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html#remove-existing-users).
