---
title: "Katalon License Management"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license-management.html
description:
---

You can access [Katalon TestOps](https://analytics.katalon.com/) to subscribe, create, and distribute licenses. Only an organization Owner or Admin can access the License tab of the organization. For more details about roles and default permissions, please view [this document](https://docs.katalon.com/katalon-analytics/docs/user-management.html).

Before assigning a license, the organization owner/admin must [add the team member(s)  to the organization in the Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/user-management.html#user-related-permissions). Once added, the admin can assign a Katalon license to any team member, or withdraw a license if no longer needed.

The available licenses are the remaining licenses after the license quota subtracts the total number of offline licenses created and currently active online licenses.

>   *Available licenses = License quota – (Offline licenses + Active online licenses)*

## Create and Assign an Online KSE/RE License

### KSE

1. In [Katalon TestOps](https://analytics.katalon.com/home), go to **Organization > License**.
2. Register the on-demand users by adding them to the **Registered Users** list.

> Notes: The number of registered users cannot exceed the license quota.

When the registered users activate KSE, their machine IDs are added to the **Online Licenses** in Katalon TestOps.

### RE

Any members of an organization can use the RE online licenses that the organization has purchased. To run KS/KSE from the CLI, you need to add API keys to the command.

## Create and Assign an Offline RE/KSE License

Offline licenses, once generated, cannot be revoked or terminated. The valid period for each offline license is 60 days. The available licenses for online usage equal the license quota subtracting the number of created offline licenses.

You need a machine ID to generate an offline license for both KSE and RE.

### View a machine ID

1. Open **Katalon Studio**
2. In the **Katalon Studio Activation** window, click **Offline Activation** to view and copy the machine ID.

> **Important**: Due to the irrevocable offline license, you can create a testing license to verify if your entered machine ID is correct in version 7.1 and later.

### Create a testing license

1. Go to [Katalon TestOps](https://analytics.katalon.com/home).
2. Select **Organization > License**.
3. In the KSE or RE view, select **Create Offline License**.
4. Enter a machine ID.
5. Click **Create Testing License**. The newly created testing license is automatically downloaded.
6. For Runtime Engine, the testing license must be stored in the **license** folder.

* Windows: C:\Users<user_name>.katalon\license
* Linux: /home/<user_name>/.katalon/license
* macOS: /Users/<user_name>/.katalon/license

> Note: **.katalon** is a hidden folder.

### Create an offline license

1. Go to [Katalon TestOps](https://analytics.katalon.com/home).
2. Select **Organization > License**.
3. In the KSE or RE view, select **Create Offline License**.
4. Enter a machine ID.
5. Click **Create**. The newly created offline license is added to the **Offline Licenses** list.

## View License Details

From the main menu of Katalon Studio:

* macOS: **Katalon Studio > About Katalon Studio**

* Windows/Linux: **Help > About**

## How to Use Katalon Licenses

* [Activate Katalon Studio](/katalon-studio/docs/katalon-studio-activation-since-70.html)
* [Activate Katalon Studio Enterprise](/katalon-studio/docs/activate-KSE.html)
* [Activate Katalon Studio or Katalon Studio with Runtime Engine](/katalon-studio/docs/activate-RE.html)