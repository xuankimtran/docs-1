---
title: "Enable Single Sign-On (SSO) for an Organization"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/sso-settings.html
redirect_from:
    - "/katalon-analytics/docs/accept-sso/"
---

> Requirements:
>
> You need to subscribe to Katalon TestOps Enterprise plan. To request a trial of Katalon TestOps Enterprise, see [TestOps Trial Plans](https://docs.katalon.com/katalon-analytics/docs/trial-plans.html).

## Configure Single Sign-On

> Requirements:
>
> * You must be an **Owner** or **Admin** of an Organization.
>
> * You have configured a Subdomain. See [Configure a Subdomain for an Organization](https://docs.katalon.com/katalon-analytics/docs/subdomain.html).
>
> * You have configured Identity Provider. Your metadata is then automatically encrypted in Katalon's database.

As an Owner or Admin, you can configure SSO by following these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login).

2. Go to **Settings** > **Organization Management**.

3. Select **Settings** on the left bar, and scroll down to the **Single Sign-On (SSO) Settings** section.

4. Switch **Enable SSO** to **Active**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/enter-metadata-for-sso.png" width=100% alt="SSO enabled input metadata">

    You then can enter your Metadata.

5. Click **Update**.

## Enable SSO for new members and existing members

After configuring SSO, you can enable SSO for new members when inviting them to your Organization.

You can also enable SSO for the existing members of your Organization.

> To learn more User Management in TestOps, refer to this guide: [TestOps User Management](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html).

### For a new User

To enable SSO for a new User, follow these steps:

1. Go to **Settings** > **User Management**.

    The **User Management** page appears.

2. On the top-right corner of the **User Management** page, click on the **Invite** button and select the desired invitation method, **By Email** or **Import CSV File**.

    For example, we invite a new User by email as follows:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-User- Management-Click-on-Invite.png" width=100% alt="Invite User By Email">

3. In the displayed *User Invitation* window, insert the new User's email address.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-User-Management-Insert-Email.png" width=100% alt="User Invitation Window">

4. Enable SSO for the User. In the **Login Settings** section, toggle on the **Log in to [custom.katalon.io] by Single Sign-On** option.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-User-Management-Toggle-SSO.png" width=70% alt="User Invitation Window">

    > **Notes**:
    >
    > You can choose to enable both options.

5. Click **Next** to continue the User invitation process as normal.

Once the User invitation process is completed, a request email is sent to the invited User.

### For an existing User

To enable SSO for an existing member, follow these steps:

1. Go to **Settings** > **User Management**.

    The **User Management** page appears.

2. In the **Active Users** tab, nagivate to a User's row, click on the <em>more options</em> icon, and select **Edit Login Options**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-User-Management-Active-Users-tab-more-options.png" width=100% alt="More options icon">

3. Enable SSO for the User. In the new **Login Settings** pop-up, toggle on the **Log in to [custom.katalon.io] by Single Sign-On** option.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-Log-Settings-Username_Password-enabled.png" width=70% alt="SSO toggle turned on">

    > **Notes**:
    >
    > You can choose to enable both options.

4. Click **Save** to complete the configuration.

    A request email is then sent to the selected User.

> **Notes:**
>
> New members must first accept their invitations, and existing members must accept their requests before they are allowed to use SSO.

## View and manage User Authentication

### View pending SSO requests

As an Owner or Admin, you can view the pending invitations and SSO requests on the **Manage Users** page.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/sso-pending-highlight-blurred.png" width=100% alt="pending SSO invitations">

You can withdraw an invitation and request by clicking on the *Trash bin* icon. After confirming your action, the member will no longer be able to access the URLs.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/delete-sso-pop-up-blurred.png" width=100% alt="pending SSO delete box">

### Revoke SSO invitations

To revoke pending SSO invitations, follow these steps:

1. In the **User Management** page, switch to the **Pending Invitation** tab.

    Users with pending SSO invitations are tagged with the *SSO* icon.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-User-Management-Pending-Invitation-SSO.png" width=100% alt="Pending Invitation tab">

2. Select the Users with SSO invitations that you want to revoke, then click on the **Revoke SSO Invitation** button.

    []

3. In the **Revoke Single Sign-On Invitation** pop-up, verify the list of selected Users and click on the **Revoke SSO** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-SSO-Revoke-Popup.png" width=70% alt="Revoke SSO pop-up">

The SSO invitation links sent to the selected Users will be revoked.

### Update authentication methods

There are two login options: **Enable SSO** and **Access Katalon TestOps with username & password**.

You can always switch back to **Access Katalon TestOps with username & password** to change the authentication method.

To update the authentication method for Users, go to the **User's detail** page and update the login option.

## Activate SSO in Katalon Studio

After configuring SSO in Katalon TestOps, you must reactivate Katalon Studio to enable SSO.

Follow these steps:

1. Open Katalon Studio.

2. Click on the *Profile* icon at the top right corner, and select **Deactivate**.

    The **Katalon Studio Activation** box appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/activate-sso-in-studio.png" width=100% alt="ks activation box">

3. Fill in the required information.

    * **Server URL**: enter the Subdomain you have configured (e.g., https://techwrite.katalon.io).

    * **Email**: enter your registered Katalon account.

    * **Password**: enter an API key generated in Katalon TestOps. See: [API Keys](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html).

## Enable SSO as a User

If you are not an Owner or Admin of an Organization, you will receive the invitation or SSO request via email.

As a new User, accept the invitation to join the Organization first. See: [TestOps User Management](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html#as-a-user).

As an existing User, follow these steps:

1. Go to your email and find the *[Katalon TestOps] Verify Single Sign-On (SSO) authentication* email, then click **Click here to confirm** in the email.

    You will be directed to Katalon TestOps and see the below message.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/user-navigate-sso-acceptance-blurred.png" width=100% alt="user accept sso">

    > Notes:
    >
    > If you are a new User, you must accept the invitation to join an Organization first. Then you will receive the authentication email.

2. Check the information, then click **Allow this account to access Organization [...] via SSO** to confirm.

    After accepting the SSO request, you are automatically navigated to the Subdomain.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/subdomain-signin-using-sso-blurred.png" width=100% alt="subdomain sign in using SSO">

3. Click **Sign in using SSO**.
