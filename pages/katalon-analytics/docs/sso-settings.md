---
title: "Enable Single Sign-On (SSO) for an Organization"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/sso-settings.html
redirect_from:
    - "/katalon-analytics/docs/accept-sso/"
---

> Notes:
>
> This feature is only available in Katalon TestOps Enterprise.
>
> You can request a trial of Katalon TestOps Enterprise. See: [TestOps Trial Plans](https://docs.katalon.com/katalon-analytics/docs/trial-plans.html).

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

### For a new User

To enable SSO for a new member, follow these steps:

1. Invite a User to your Organization. See [TestOps User Management](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html#invite-a-user-to-join-an-organization).

2. Enable the SSO option on the **Invite User** page, then click **Invite**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/invite-sso.png" width=100% alt="enable SSO in Invite user page">

    An invitation is then sent to the User.

### For an existing User

To enable SSO for an existing memeber, follow these steps:

1. Go to **Settings** > **User Management**.

    The **Manage Users** page appears.

2. Edit a User's account by clicking on the *Pencil* icon.

    The **User's detail** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/invite-sso.png" width=100% alt="user's detail page">

3. Enable the SSO option on the page.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/update-sso.png" width=100% alt="user's detail page highlight SSO option">

    A request to enable SSO is then sent to the existing User.

> Notes:
>
> * The action is pending until new members accept the invitations and existing members accept the requests.

### As an User

If you are not an Owner or Admin or an Organization, you will receive the invitation or SSO request via email.

As a new User, accept the invitation to join the Organization first. See: [TestOps User Management](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html#as-a-user).

As an existing User, you see a screen with the message *The Organization Admin [...] has requested to enable Single Sign-On (SSO) for your account. Please check your inbox and confirm the request*.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/accept-sso/join-organization-sso.png" width=100% alt="sso request message from user's side">

Continue with the following steps:

1. Go to your email and find the *Verify Single Sign-On authentication* email, then click on the URL in the email.

    You will be directed to Katalon TestOps.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/accept-sso/accept-sso.png" width=100% alt="user accept sso">

    > Notes:
    >
    > If you are a new User, you must accept the invitation to join an Organization first. Then you will receive the authentication email.

2. Check the information, then click **Allow this account to access Organization [...] via SSO**”*** to confirm.

    After accepting the SSO request, you are automatically navigated to the Subdomain.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/accept-sso/signin-sso.png" width=100% alt="subdomain highlight">

3. Click **Sign in using SSO**.

## View and manage User Authentication

### View pending SSO requests

You can view the pending invitations and SSO requests on the **Manage Users** page.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/manage-sso.png" width=100% alt="pending SSO invitations">

You can withdraw an invitation and request by clicking on the *Trash bin* icon. After confirming your action, the member will no longer be able to access to the URLs.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/delete-sso-request.png" width=100% alt="pending SSO delete box">

### Update authentication methods

There are two login options: **Enable SSO** and **Access Katalon TestOps with username & password**.

You can always switch back to **Access Katalon TestOps with username & password** to change the authentication method.

To update the authentication method for Users, go to the **User's detail** page and update the login option.

## Activate SSO in Katalon Studio

After configuring SSO in Katalon TestOps, you can activate SSO in Katalon Studio by following these steps:

1. Open Katalon Studio.

2. Go to Katalon Studio Activation log.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/activate-ks.png" width=100% alt="ks activation box">

3. Fill in the below information.

    * **Server URL**: enter the Subdomain you have configured (e.g., https://techwrite.katalon.io).

    * **Email**: enter your registered Katalon account.

    * **Password**: enter an API key generated in Katalon TestOps. See: [API Keys](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html).