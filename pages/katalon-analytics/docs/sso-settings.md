---
title: "Enable Single Sign-On (SSO) for an Organization to access Katalon TestOps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/sso-settings.html
redirect_from:
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

## Configure Single Sign-On

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login).

2. Go to **Settings** > **Organization Management**.

3. Select **Settings** on the left bar, and scroll down to the **Single Sign-On (SSO) Settings** section.

4. Switch **Enable SSO** to **Active**.

    You then can enter your Metadata.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/enable-sso.png" width=100% alt="SSO section input metadata">

5. Click **Update**.

## Enable SSO for new members and existing members

After configuring SSO, you can enable SSO for new members by inviting them to your Organization.

You can also enable SSO for the existing members of your Organization.

### For a new user

1. Learn how to invite users to an organization [here](https://docs.katalon.com/katalon-analytics/docs/setup-org-team-project.html#invite-a-user-to-the-organization).

2. In the **Login Options** section in the **Invite users** page, enable the SSO option and click on **Invite** to finish.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/invite-sso.png)

3. A request to enable SSO will be sent to invited users. 

This action will be *pending* until your member [accepts the request](https://docs.katalon.com/katalon-analytics/docs/setup-org-team-project.html#invite-a-user-to-the-organization).

> Note: The *“Verify Single Sign-On authentication"* email will be sent to invited users once they have accepted the invitation to join the organization.

### Enable SSO for an existing member

1. To enable SSO for an existing member in an organization, in **Katalon Admin** page, go to **Users** and select an account you want to enable SSO. 

2. Click on the pencil icon to go to the details page.

3. In the **Login Options** section in the user's details page, enable the SSO option. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/update-sso.png)

4. A request to enable SSO will be sent to invited users. 

This action will be pending until your member [accepts the request](https://docs.katalon.com/katalon-analytics/docs/setup-org-team-project.html#invite-a-user-to-the-organization).

> You need to enable SSO for your own account in order to login via SSO.

## View and Manage User Authentication

### View Pending SSO Requests

After enabling SSO for your member, the pending request will be displayed in the **Users** page.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/manage-sso.png)

Before the member have accepted the request, you can withdraw it by removing the URL from the pending list. Once you have confirmed your action, the member will no longer be able to access your request URL.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/delete-sso-request.png)

### Update Authentication Methods

Once users have accepted the request to enable SSO, their accounts will be displayed in the user list with details of login options. 

To update authentication methods, in the **Katalon Admin** page, go to **Users** and click on the pencil icon to view user's details.

You can update the login options (SSO and/or Username & Password) for members in the **Login Settings** section.

## Activate Katalon Studio

After you have finished the SSO configurations, open the activation log of Katalon Studio and fill in the below information to get started. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/activate-ks.png)

- Server URL: your subdomain that you have already configured. (E.g.: https://beo.katalon.io)
- Email: your registered Katalon account
- Password: an API key generated from Katalon TestOps. [Learn more](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html)
