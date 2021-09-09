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

> Notes:
>
> An **Online License** of KSE and KRE is transferable among registered users of an organization as long as the number of active licenses does not exceed the license quota. See: [Manage Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/license-management.html).

> Requirements:
>
> You must add team members to your Organization. See: [TestOps User Management](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html#invite-a-user-to-join-an-organization).
>
> The Owner or Admin of an Organization can grant licenses to any team member. The Owner or Admin can also revoke this action anytime. See: [Manage Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/license-management.html).

Follow these steps to grant a KSE license:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login), then go to **Settings** > **License Management**.

    The **Licenses** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/licenses-page-blurred.png" width=100% alt="license page licensed users section highlighted">

2. Choose between KSE (Node-locked) and KSE (Floating).

  > Notes:
  >
  > See [new doc](link) for detailed information on the differences between a node-locked license and a floating license.

3. Add users to the **Licensed Users** section.

   Once the licensed users activate KSE, their machine IDs are added in the **Online Licenses** section.

   > Notes:
   >
   > The number of licensed users cannot exceed the license quota.

For KRE, all Users of an Organization can use the KRE licenses by default once the Organization has purchased the KRE licenses.

However, to optimize license usage and avoid session termination, the Owner and Admin must remember the following rules:

* Each session accounts for one license.
* The number of parallel sessions cannot exceed the license quota.
* The number of registered machine IDs cannot exceed the license quota.
* Users need [API Keys](https://docs.katalon.com/katalon-studio/docs/katalon-apikey-70.html) to activate a KRE online license.

  > Notes:
  >
  > If you are a user, see [Activate Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/license_activation.html) for instructions on activating the Katalon licenses.

### Create an offline license

An **Offline License** allows you to use KSE and KRE without internet. Once an offline license is activated, you cannot revoke or transfer it to a different machine.

An offline license expires at the end of your subscription period. It can also be expired earlier than its actual date if you make changes in the offline license file.

When an offline license expires, you can generate a new offline license file to continue using KSE/KRE offline, or you can switch to an online license instead.

As a machine ID is required to create an offline license, Katalon generates a machine ID based on the hardware specifications and the user's account logging in to that machine at the generation time.

For example, if User A logs in to Machine A, Katalon generates a machine ID X. At the same time, if User B logs in to Machine A, Katalon generates a machine ID Y. This means that you need two offline licenses for User A and User B.

> Notice:
>
> A KSE/KRE license, once being converted to an offline license, is bound to a machine until its expiry date (in **60 days**). You should generate an offline license with cautions as you cannot undo this action.

> Requirements:
>
> An **annual** node-locked license.
>
> You must be the Owner or Admin of your Organization.

Follow these steps:

1. Receive the User's machine ID.

  > Notes:
  >
  > If you are a user, see [Activate Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/license_activation.html) for instructions on finding your machine ID and using Katalon licenses.

2. Sign in to [Katalon TestOps](https://testops.katalon.io/login).

3. Go to **Settings** > **License Management**.

    The **Licenses** page appears.

4. Choose between KSE (Node-locked) and KRE (Node-locked).

5. Click on the **Create Offline License** button at the top right corner.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/create-offline-license-button.png" width="1424" height="" alt="create offline license button">

6. Enter the User's machine ID and input the expiry date, then click **Create**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/create-offline-license-page.png" width="1424" height="" alt="create offline license page">

  > Notes:
  >
  > You should double check the machine IDs to make sure you distribute offline licenses to the right users.

6. Confirm your action.

    For KSE, the newly-created offline license file is named `KSE_<machineID>.lic` and added in the **Offline Licenses** section.

    For KRE, the newly-created offline license file is named `KRE_<machineID>.lic` and added in the **Offline Licenses** section.

See also:
* [Manage Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/license-utilization-dashboard.html#license-usage-visualization).
* [License Utilization Dashboard](https://docs.katalon.com/katalon-studio/docs/license-utilization-dashboard.html#license-usage-visualization).