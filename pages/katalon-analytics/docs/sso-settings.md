---
title: "[Admin] Enable Single Sign-On (SSO) for an Organization to access Katalon TestOps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/sso-settings.html
redirect_from:
---
> This feature is accesible to the organization **Owner** and **Admin** only.

## Prerequisites

- You have configured a subdomain for your Organization. [Learn more](https://docs.katalon.com/katalon-analytics/docs/subdomain.html)
- You have configured Identity Provider and have your metadata (this will be automatically encrypted in Katalon's database).

## Configure Single Sign-On

1. Access https://testops.katalon.io.

2. In the **Katalon Admin** page, go to **Settings** > **Single Sign-On (SSO) Settings** > **Enable SSO** and enter your metadata.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/sso-settings/enable-sso.png)

3. Click on **Update** to finish.

## Invite and enable SSO for Organization members

After you have configured SSO for your Organization, you can invite and enable SSO for each member.

### Invite and enable SSO for a new user

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
