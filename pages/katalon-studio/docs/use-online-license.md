---
title: "Grant Katalon Licenses"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/use-online-license.html
redirect_from:
  - "/katalon-studio/docs/online-offline-licenses.html"
  - "/katalon-studio/docs/re-offline-licenses.html"
  - "/katalon-studio/docs/how-to-create-kse-offline-license.html"
description:
---
In this guide, you will learn to assign Katalon Studio Enterprise (KSE) and Katalon Runtime Engine (KRE) licenses to Users in your Organization.

## Grant a license

> Requirements:
>
> * An internet connection for you and the users you will grant the license to.
>
> * You must be the Owner or Admin of your Organization.
>
> * You have already added team members to your Organization. See: [TestOps User Management](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html#invite-a-user-to-join-an-organization).

Follow these steps to grant KSE licenses:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login), select your Organization, then go to **Settings** > **License Management**.

    The **Licenses** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/licenses-page-blurred.png" width=100% alt="license page licensed users section highlighted">

2. Choose between KSE (Node-locked) and KSE (Floating).

  > Notes:
  >
  > See [Types of Licenses](https://docs.katalon.com/katalon-studio/docs/overview.html#types#of#licenses) to understand the differences between a node-locked license and a floating license.
  
3. Add users to the **Licensed Users** section.

  You have granted the KSE licenses to Users.

For KRE, all Users of an Organization can use the KRE licenses by default once the Organization has purchased the KRE licenses.

However, to optimize license usage and avoid session termination, the Owner and Admin must remember the following rules:

* Each session accounts for one license.
* The number of parallel sessions cannot exceed the license quota.
* The number of registered machine IDs cannot exceed the license quota. You can remove a registered machine ID by following this guide: [Manage Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/license-management.html#revoke-a-license).
* Users need [API Keys](https://docs.katalon.com/katalon-studio/docs/katalon-apikey-70.html) to activate a KRE online license.

Your users can now activate their KSE and KRE licenses. You can refer them to this link for activation: [Activate Katalon License](https://docs.katalon.com/katalon-studio/docs/activate-license.html).

Granting a license this way allows you to transfer a license freely among registered users of an Organization as long as the number of licensed users does not exceed the license quota.

You can revoke these licenses at any time by following this guide: [Manage Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/license-management.html).

If the users you wish to grant a license to are not connected to the internet, you can instead generate an offline license.

### Create an offline license

An **Offline License** allows you to use KSE and KRE without internet. Once an offline license is generated, you cannot revoke or transfer it to a different machine.

By default, an offline license expires at the end of your subscription period. It can also be set to expire earlier by inputting a different expiry date when generating the offline license file.

When an offline license expires, you can generate a new offline license file to continue using KSE/KRE offline, or you can switch to an online license instead.

As a machine ID is required to create an offline license, Katalon generates a machine ID based on the hardware specifications and the user's account logging in to that machine.

For example, if User A logs in to A's account on Machine A, Katalon generates a machine ID X. If User B logs in to B's account on Machine A, Katalon generates a machine ID Y. This means that you need two offline licenses for User A and User B.

> Notice:
>
> Once converted to an offline license, a KSE/KRE license is bound to a machine until it expires. You cannot undo this action.

> Requirements:
>
> * You can only convert an **annual** node-locked license into an offline license.
>
> * You must be the Owner or Admin of your Organization.
>
> * You have already received the User's machine ID. You can send this guide to your users:  [View Machine ID](https://docs.katalon.com/katalon-studio/docs/machine-id.html), for instructions on how to find a machine ID.

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login).

2. Go to **Settings** > **License Management**.

    The **Licenses** page appears.

3. Choose between KSE (Node-locked) and KRE (Node-locked).

4. Click on the **Create Offline License** button at the top right corner.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/create-offline-license-button.png" width="1424" height="" alt="create offline license button">

5. Enter the User's machine ID and input the expiry date, then click **Create**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/create-offline-license-page.png" width="1424" height="" alt="create offline license page">

  > Notes:
  >
  > You should double check the machine IDs to make sure you distribute offline licenses to the right users.

6. Confirm your action.

    For KSE, the newly-created offline license file is named `KSE_<machineID>.lic` and added in the **Offline Licenses** section.

    For KRE, the newly-created offline license file is named `KRE_<machineID>.lic` and added in the **Offline Licenses** section.

7. Download and transfer the offline license files to the User.

8. Send your users this activation guide: [Activate Katalon License](https://docs.katalon.com/katalon-studio/docs/activate-license.html).

See also:
* [Manage Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/license-utilization-dashboard.html#license-usage-visualization).
* [License Utilization Dashboard](https://docs.katalon.com/katalon-studio/docs/license-utilization-dashboard.html#license-usage-visualization).