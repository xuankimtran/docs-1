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

> To learn more about user management in TestOps, refer to this guide: [TestOps User Management](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html).

### For a new User

To enable SSO for a new User, follow these steps:

1. Go to **Settings** > **User Management**.

    The **User Management** page appears.

2. On the top-right corner of the **User Management** page, click on the **Invite User** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-User-Management-Active-User.png" width=100% alt="User Invitation Window"> 

3. In the displayed **User Invitation** window, insert the new User's email address.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-User-Invitation-Window.png" width=100% alt="User Invitation Window"> 

4. In the **Login Settings** section, toggle on the **Log in to [custom.katalon.io] by Single Sign-On** option.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-User-Management-Toggle-SSO.png" width=70% alt="User Invitation Window">

    > **Notes**:
    >
    > You can choose to select or deselect both options.

5. Click **Next** to continue the User invitation process as usual.

Once the User invitation process is completed, an email is sent to the User asking them to join the Organization. After the User joins the Organization, they will receive a request email to enable SSO.

### For an existing User

To enable SSO for an existing User, follow these steps:

1. Go to **Settings** > **User Management**.

    The **User Management** page appears.

2. In the **Active Users** tab, nagivate to a User's row, click on the <em>more options</em> icon, and select **Edit Login Options**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-User-Management-Active-Users-tab-more-options.png" width=100% alt="More options icon">

3. In the new **Login Settings** pop-up, toggle on the **Log in to [custom.katalon.io] by Single Sign-On** option.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-Log-Settings-Username_Password-enabled.png" width=70% alt="SSO toggle turned on">

    > **Notes**:
    >
    > You can choose to select or deselect both options.
    
    If the selected User already has a pending SSO invitation, the pop-up will display the invitation link. You can copy this link to send to the User.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-Login-Settings-Pending-Invitation-Link.png" width=70% alt="SSO toggle turned on">

4. Click **Save** to complete the configuration.

    A request email is then sent to the selected User.

> **Notes:**
>
> Users must join the Organization to log in to the custom domain by either SSO or username and password.

## View Pending SSO invitations

To view the pending invitations and SSO requests, in the **User Management** page, switch to the **Pending Invitation** tab.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-Pending-Invitations.png" width=100% alt="SSO toggle turned on">

Users with pending SSO invitations are tagged with the *SSO* icon.

## Revoke pending SSO invitations

As an Owner or Admin, you can revoke pending SSO invitations.

### For existing Users

To revoke pending SSO invitation for Users who join the Organization, follow these steps:

1. In the **User Management** page, switch to the **Active Users** tab.

2. In the **Active Users** tab, nagivate to the desired User's row, click on the <em>more options</em> icon, and select **Edit Login Options**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-User-Management-Active-Users-tab-more-options.png" width=100% alt="More options icon">

3. In the new **Login Settings** pop-up, toggle off the **Log in to [custom.katalon.io] by Single Sign-On** option.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-Log-Settings-Username_Password-enabled.png" width=70% alt="SSO toggle turned on">

### For new Users

To revoke pending SSO invitations for Users who have not joined the Organization, follow these steps:

1. In the **User Management** page, switch to the **Pending Invitation** tab.

2. Select the Users with SSO invitations that you want to revoke, then click on the **Revoke SSO** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-Revoke-SSO-button.png" width=100% alt="SSO toggle turned on">

3. In the **Revoke Single Sign-On Invitation** pop-up, verify the list of selected Users and click on the **Revoke SSO** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-SSO-Revoke-Popup.png" width=70% alt="Revoke SSO pop-up">

The SSO invitation links sent to the selected Users will be revoked.

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

> **Notes**:
>
> If you are a new User, you must first accept the invitation to join an Organization. Then you will receive the SSO request email.

To enable SSO, follow these steps:

1. Go to your email and find the *[Katalon TestOps] Verify Single Sign-On (SSO) authentication* email, then click **Click here to confirm** in the email.

    You will be directed to Katalon TestOps and see the below message.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/K1-Accept-SSO-request.png" width=100% alt="user accept sso">

2. Check the information, then click **Yes, enable SSO** to confirm.

    After accepting the SSO request, you are automatically navigated to the Subdomain.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-sso-settings/subdomain-signin-using-sso-blurred.png" width=100% alt="subdomain sign in using SSO">

3. Click **Sign in using SSO**.
