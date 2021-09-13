---
title: "Manage Katalon Licenses"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license-management.html
description:
---

After subscribing to the Katalon Licenses, you can start managing your licenses in [Katalon TestOps](https://testops.katalon.io/login).

> Requirements:
>
> You must be the Owner or Admins of your Organization to manage the licenses on the **Licenses** page. For further details on roles and user management, see: [TestOps User Management](https://docs.katalon.com/katalon-analytics/docs/kt_invite_user_org.html).

## Find your machine ID

It's important to know your machine ID. You know your machine ID to verify if your local machine is currently using an offline license.

Users must know their machine IDs to send IDs to you, so that you can grant offline licenses to Users.

Follow these steps:

1. Open Katalon Studio in your local machine.

2. Click on the *Profile* icon at the top right corner and select **Deactivate**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/transfer-license/1-deactivate.png" width=300 alt="ks profile settings">

   The **Katalon Studio Activation** log appears as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/transfer-license/2-machine-id.png" width="400">

   You can see your machine ID here.

3. Select the **Offline Activation** tab on the **Katalon Studio Activation** log.

   The **Katalon Studio Enterprise Activation** log appears as below. 
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/transfer-license/3-license-file.png" width="400">

   You can click on the **Copy** button to copy your machine ID to a clipboard.

4. Paste your machine ID into a note to store it.

5. Click **Back** and enter your email and password, then click **Activate** to reactivate Katalon Studio.

## Verify and view the license information

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
> You can revoke KSE's **Online Licenses** only. 

Follow these steps:

1. Go to the **Licenses** page.

2. In the **Online Licenses** section, click on the *Trash bin* icon of the machine ID you want to revoke.

   The **Remove license** box appears as below.

3. Click **Remove** to confirm your action.

   > Notice:
   >
   > By clicking **Remove**, you immediately terminate the current session that machine ID is working on in Katalon Studio. You should revoke a license with caution.

If a User is leaving your Organization, you can also end that User's license usage by deactivating that User's machine ID.

Follow these steps:

1. Go to the **Licenses** page.

2. Scroll down to the **Registered Machines** section.

3. Click on the *Trash bin* icon of the machine ID you want to deactivate.

   The **Deactivate Machine** box appears as below.

4. Click **Remove** to confirm your action.

### Transfer a license

> Notes:
>
> Only **Online Licenses** are transferable among the organization's registered users as long as the active licenses do not exceed the license quota.



An online Node-locked Runtime Engine license, when activated, binds to a machine until expired or manually removed from that machine. For other members in your organization to use an online Node-locked Runtime Engine, you must remove it from your machine.

> Only **online licenses** are transferable.
>
> **Offline licenses** cannot be transferred until expired (60 days).

## Verify that the machine does not have an offline license

Visit **Katalon TestOps** > **Organization** > **License**, navigate to tab **Runtime Engine**. You should not see your Machine ID in step 1 listed under **Offline Licenses**. 


If you do see it, then it means this machine already has an offline license. You won’t be able to remove an offline license from the machine until the license is expired or 60 days have passed. In this case, this guide is not for you. 

If you do not see your **Machine ID** listed there, then please continue.


## Remove an online Node-locked Runtime Engine license from a machine

At the bottom of the same page, you should see under Registered Machines, the **Machine ID** (step 1) There is a button to remove it from the list.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/transfer-license/4-delete-machine-id.png)


You will be asked to provide confirmation.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/transfer-license/5-confirm.png)

Once you confirm, the **Machine ID** will be removed from the Registered Machines.

> As soon as you remove the **Machine ID** from **Katalon TestOps**, the online license in that machine will be deactivated in **Katalon Studio**.


## Use the online Node-locked Runtime Engine license on another machine

Now you can use the license for Runtime Engine on another machine.
## How to View License Details

Users can view the license's details that they are using. From the main menu of Katalon Studio:

* macOS: **Katalon Studio > About Katalon Studio**
* Windows/Linux: **Help > About**

## Configure Idle Timeout

> Introduced in version 7.8 and applicable to the **online** Katalon Studio Enterprise (KSE) license only.

With this function, you can optimize the usage of KSE licenses by setting a time restriction for users to have no interactions with Katalon Studio. This setting impacts all KSE users in this organization, which means a KSE user will sign out automatically when they take no actions in the app. 

**On Katalon Admin**: 

To enable timeout setting for license usage, please do as follows:

1. Log into [Katalon Admin](https://admin.katalon.com/) 
2. Select your **Organization** > select **Timeout**
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/turn-off.png" width=60%>
3. In the displayed **Idle Timeout Settings** screen, Katalon turns off the idle timeout by default, click on the switch button to enable the setting.
4. Specify the desired timeout (in minutes). By default, Katalon sets 120 minutes as the timeout period.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/turn-on.png" width=60%>
5. Click **Update** to save your setting.

**In Katalon Studio**: 

When this setting is applied, if the users in that organization have been idle for the specified minutes, they will log out automatically. Katalon Studio will send a notification to the user before the automatic signout.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/noti.png" width=60%>
