---
title: "Use and Maintain Katalon Licenses"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license-management.html
description:
---

After successfully subscribing to Katalon licenses, the **Organization Owner and Admins** can start granting licenses to your users immediately. For more details about roles and default permission, please view [this document](hhttps://docs.katalon.com/katalon-analytics/docs/kt-user-role-permission.html).

> **Important**:
>
> * The **Licenses** view of your Organization on Katalon TestOps is the workspace to manage Katalon licenses.
> * Only **Organization Owner and Admins** can view, create, assign, revoke, and transfer licenses.

## Manage and Assign Licenses

We provide different tutorials of how to grant and use different licenses:

* [Grant Online Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html) describes how to grant permission of using the subscribed licenses of both Katalon Studio Enterprise and Katalon Runtime Engine
* Katalon Studio Enterprise: [How to grant and use an Offline License](https://docs.katalon.com/katalon-studio/docs/how-to-create-kse-offline-license.html)
* Katalon Runtime Engine: [How to grant and use an Offline License](https://docs.katalon.com/katalon-studio/docs/how-to-create-kse-offline-license.html)

## View Available Licenses and Machines

1. Log into [Katalon TestOps](https://analytics.katalon.com/home)
2. Select your **Organization > Licenses**
3. Select a Katalon product to open its view
4. The product view display the following information:

* **Subscribed Licenses**- license quota that you have purchase.
* **Available Licenses**- the remaining licenses after the subscribed license quota subtracts the total number of offline licenses created and currently active online licenses.

  > *Available licenses = Subscribed licenses quota – (Offline licenses + Active online licenses)*

* **Machine Quota** is equal to the license quota.
* **Registered Users**- the users are allowed to use Katalon Studio Enterprise licenses.
* **Online Licenses**- active machines that are using online licenses.
* **Offline Licenses**- machines to which an offline license binds.
* **Registered Machines**: machines that have used either online or offline license.

## Revoke and Transfer Licenses

Only **online** licenses of Katalon Studio Enterprise and Katalon Runtime Engine are transferable among the organization's registered users as long as the active licenses do not exceed the license quota.

You can revoke a Katalon Studio Enterprise license from a user by remove the user from the **Registered Users** list. You can do the same for a registered machine.

## How to View License Details

Users can view the license's details that they are using. From the main menu of Katalon Studio:

* macOS: **Katalon Studio > About Katalon Studio**
* Windows/Linux: **Help > About**
