---
title: "Manage Katalon Licenses"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license-management.html
description:
---

After successfully subscribing to Katalon licenses, the Organization Owner and Admins can immediately begin granting licenses to your users. For more details about roles and default permission, see [TestOps User Management](https://docs.katalon.com/katalon-analytics/docs/kt-user-role-permission.html).

> **Important**:
>
> * The **Licenses** view of your Organization on Katalon Admin is the workspace to manage Katalon licenses.
> * Only Organization Owner and Admins can view, create, assign, revoke, and transfer licenses.

## Verify and View Licenses Information

Follow these steps to verify the information of your subscribed licenses and contact us via license@katalon.com if you need help. You can also view the number of available licenses and machines.

1. Log into [Katalon TestOps](https://admin.katalon.com/).
2. Select your **Organization > Licenses**.
3. Select a Katalon product to open its view.
4. The product view displays the following information:
* **Subscribed Licenses**- the license quota that you have purchased.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/manage-subscription.png" width=100% alt="manage subscription">
* **Available Licenses**- the remaining licenses after the subscribed license quota subtract the total number of offline licenses created and currently active online licenses.
  > *Available licenses = Subscribed licenses quota – (Offline licenses + Active online licenses)*
* **Machine Quota** is equal to the license quota.
* **Registered Users**- the users are allowed to use Katalon Studio Enterprise licenses. (This list only displays in the **Katalon Studio Enterprise** view.)
* **Online Licenses**- active machines that are using online licenses.
* **Offline Licenses**- machines to which an offline license binds.
* **Registered Machines** display a list of  machines that have used either online or offline licenses.

## Manage and Assign Licenses

We provide different tutorials on how to grant and use different licenses:

* [Grant Online Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html) describes how to grant permission of using the subscribed licenses of both Katalon Studio Enterprise and Katalon Runtime Engine.
* Katalon Studio Enterprise: [How to grant and use an Offline License](https://docs.katalon.com/katalon-studio/docs/how-to-create-kse-offline-license.html)
* Katalon Runtime Engine: [How to grant and use an Offline License](https://docs.katalon.com/katalon-studio/docs/how-to-create-kse-offline-license.html)

## Revoke and Transfer Licenses

Only **online** licenses of Katalon Studio Enterprise and Katalon Runtime Engine are transferable among the organization's registered users as long as the active licenses do not exceed the license quota.

You can revoke a Katalon Studio Enterprise license from a user by removing the user from the **Registered Users** list. You can do the same for a registered machine.

## How to View License Details

Users can view the license details that they are using. From the main menu of Katalon Studio:

* macOS: **Katalon Studio > About Katalon Studio**
* Windows/Linux: **Help > About**

## Configure Idle Timeout

> Introduced in version 7.8.0 and applicable to the **online** Katalon Studio Enterprise (KSE) license only.

With this function, you can optimize the usage of KSE licenses by setting a time restriction for users to have no interactions with Katalon Studio. This setting impacts all KSE users in this organization, which means KSE users will automatically sign out when they take no actions in the app.

**On Katalon Admin**:

To enable timeout setting for license usage, please do as follows:

1. Log into [Katalon TestOps](https://admin.katalon.com/).
2. Select your **Organization** > select **Timeout**
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/manage-idle-timeout.png" width=60% alt="manage idle timeout">
3. In the displayed **Idle Timeout Settings** screen, Katalon turns off the idle timeout by default, click on the switch button to enable the setting.
4. Specify the desired timeout (in minutes). By default, Katalon sets 120 minutes as the timeout period.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/manage-enabling-timeout.png" alt="set timeout" width=60%>

5. Click **Update** to save your setting.

**In Katalon Studio**:

When this setting is applied, if the users in that organization have been idle for the specified minutes, they will log out automatically. Katalon Studio will send a notification to the user before the automatic sign-out.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-mgt/noti.png" width=60%>
