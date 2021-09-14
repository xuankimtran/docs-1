---
title: "Manage Katalon Licenses"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license-management.html
redirect_from:
    - "/katalon-studio/docs/transfer-license.html"
description:
---

After subscribing to the Katalon Licenses, you can start managing your licenses in [Katalon TestOps](https://testops.katalon.io/login).

> Requirements:
>
> You must be the Owner or Admins of your Organization to manage the licenses on the **Licenses** page. For further details on roles and user management, see: [TestOps User Management](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html).

## View the license information

You can verify the subscription information and view all license information by following these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login).

2. Go to **Settings** > **License Management**.

   The **Licenses** page appears.

3. Select the Katalon product whose licenses you want to check. For example, **Katalon Studio Enterprise (Node-locked)**.

   The **Licenses** page displays as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/license.png"  width=100% alt="licenses page">

   * In the **Subscription** section, you can see the following information:
      * **Subscribed Licenses**: the license quota that you have purchased.
      *  **Available Licenses**: the remaining licenses you can use.

         > Notes:
         > 
         > Available Licenses = Subscribed Licenses – (Offline Licenses + Online Licenses).

      * **Machine Quota**: equal to the license quota.

   * In the **Licensed Users** section, you can add users for license usage. You can also view a list of users you have added for license usage.

   * In the **Online Licenses** section, you can see a list of active machine IDs (users who are currently using the licenses online).

   * In the **Offline Licenses** section, you can see a list of machine IDs to which the offline licenses are bound.

   * In the **Registered Machines** section, you can see a list of all machine IDs using either online or offline licenses.

> Notes:
>
> Contact us at license@katalon.com if you need further help with your licenses.

## Grant a license

You can assign licenses to users. See [Grant Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html).

Once being assigned, users can activate and use licenses. See: [Activation doc](link).

## Revoke and transfer a license

### Revoke a license

> Notes:
>
> * You cannot remove an offline license from a machine until the license is expired.
>
> * You can revoke Katalon Studio Enterprise's (KSE) **Online Licenses** only. For Katalon Runtime Engine (KRE), see: [Manage Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/license-management.html#transfer-a-license).

Follow these steps:

1. Go to the **Licenses** page.

2. In the **Online Licenses** section, click on the *Trash bin* icon of the machine ID you want to revoke.

   The **Remove license** box appears as below.

3. Click **Remove** to confirm your action.

   > Notice:
   >
   > By clicking **Remove**, you immediately terminate the current session that machine ID is working on in Katalon Studio. You should revoke a license with caution.

### Transfer a license

> Notes:
>
> Only **Online Licenses** are transferable among the organization's registered users as long as the active licenses do not exceed the license quota.
>
> **Offline Licenses** cannot be transferred until their expiry dates.

> Requirements:
>
> You have already verified that your machine does not have an offline license.

After activation, the KSE/KRE node-locked licenses are bound to the machine IDs until the expiry dates. You need to remove the licenses or transfer them manually.

For KSE, once you have revoked a license, you can transfer the license to another User by adding that User in the **Online Licenses** section. See: [Grant Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html).

For KRE, as one session accounts for one license, you must deactivate the machine ID using that license first, then transfer the license to the on-demand User.

For example, if the KRE license is bound to your machine ID because you have run KSE using KRE. You must deactivate your machine ID so that the other member in your organization can use the KRE node-locked license.

### Deactivate a machine ID

Follow these steps:

1. Go to the **Licenses** page.

2. Scroll down to the **Registered Machines** section.

3. Click on the *Trash bin* icon of the machine ID you want to deactivate.

   The **Deactivate Machine** box appears as below.

4. Click **Remove** to confirm your action.

> Notes:
>
> After deactivating a machine ID, you have removed the machine ID from Katalon TestOps. This also means that the license in that machine is deactivated in Katalon Studio.

### Transfer the KRE license to another machine

All members of an organization can use the KRE licenses by default once the organization has purchased the KRE licenses.

You activate the KRE license by running KSE with KRE. After activating, your machine ID is then added to the **Online Licenses** section.

Therefore, if your machine ID is deactivated, the other member can start running the KSE with KRE to activate the license. The User's machine ID is then added to the **Online Linceses** section.

Repeat the steps to deactivate the machine ID if you want to transfer the KRE license to another machine.
