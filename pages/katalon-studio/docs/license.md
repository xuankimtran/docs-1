---
title: "Katalon Studio Licensing"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license.html
description:
---

> Starting from **version 7.0.0**, you need a license to activate and use one of the Katalon Studio products, including Katalon Studio Enterprise (KSE), Katalon Studio (KS), and Runtime Engine (RE). To obtain a license, click [here](https://www.katalon.com/pricing).

This section provides details on license types, license subscription, and license management. Learn more about KS, KSE, and RE [here](https://www.katalon.com/pricing).

## Katalon Studio License Types

There are three types of Katalon Studio licenses: trial, paid, and free licenses.

### Trial License

A valid email registration is eligible for a 30-day trial of both KSE and RE. The KSE and RE trial licenses are automatically generated and activated when you first log in to the Katalon Studio application.

Each trial license can be activated on only one machine at a time. When your trial period expires, you need to subscribe to the paid license of each product to continue using it. Otherwise, the Katalon Studio free license will be automatically activated.

> Notes: KSE and RE trial licenses can only be registered with business emails. Trial licenses do not support KSE offline activation, KSE features, or offline RE.

### Paid License

#### For Katalon Studio Enterprise

KSE license is named license, meaning:

* One license is exclusively assigned to one Katalon account/user.
* One account can be activated/used on one machine at a time.
* Licenses are transferable.
* License activation and validation require an internet connection.

For offline environments, any license of the KSE **annual** subscription can be converted to a node-locked offline license. A computer ID is required to convert an annual license into an offline license. Once converted, the license will be removed from the KSE subscription and cannot be transferred to another machine or account until it is expired.

#### For Runtime Engine

RE license is a node-locked license. When running from the command-line interface (CLI), one working session accounts for one license equals to a conducted process.

* One license is tied to one registered machine.
* A machine can be mapped to multiple licenses if needed.
* RE licenses are transferable to a new machine for online environments and are non-transferable for offline environments.

#### Online License vs. Offline License

KSE and RE **online** licenses are transferable among the organization's registered users as long as the active licenses do not exceed the license quota.

**Offline** licenses are for using KSE and RE without the internet. Once generated, the offline license will be irrevocable and cannot be terminated. Also, the expiration dates of offline licenses cannot be modified.

> Notes: Offline license is only available for the annual subscription model.

### Free License

The free license granted for each Katalon account only includes the standard Katalon Studio with basic features. Currently, the free license for RE is not available. If you wish to execute Katalon Studio in console mode, you need to subscribe to an RE license. You can upgrade the free KS to KSE with a paid license without having to re-download.

## Subscribe to KSE/RE Licenses

You can purchase a Katalon license via Katalon TestOps.

* Log in to [Katalon TestOps](https://analytics.katalon.com/home).
* Go to Organization > Subscriptions.
* Choose your desired product and subscription model.
* Make payment.

## Manage KSE/RE Licenses

You can access [Katalon TestOps](https://analytics.katalon.com/) to subscribe, create, and distribute licenses. Only an organizational Owner or Admin can access the License tab of the organization. For more details about roles and default permissions, please view [this document](https://docs.katalon.com/katalon-analytics/docs/user-management.html).

### Create an Online KSE/RE License

#### KSE

1. In [Katalon TestOps](https://analytics.katalon.com/home), go to **Organization > License**.
2. Register the on-demand users by adding them to the **Registered Users** list.

> Notes: The number of registered users cannot exceed the license quota.

When the registered users activate KSE, their machine IDs are added to the **Online Licenses** in Katalon TestOps.

#### RE

Any members of an organization can use the RE online licenses that the organization has purchased. To run KS/KSE from the CLI, you need to add API keys to the command.

### Create an Offline RE/KSE License

Offline licenses, once generated, cannot be revoked or terminated. The valid period for each offline license is 60 days. The available licenses for online usage equal the license quota subtracting the number of created offline licenses.

You need a machine ID to generate an offline license for both KSE and RE.

To view a machine ID:

1. Open **Katalon Studio**
2. In the **Katalon Studio Activation** window, click **Offline Activation** to view and copy the machine ID.

To generate a license:

1. Go to [Katalon TestOps](https://analytics.katalon.com/home).
2. Select **Organization > License**.
3. In the KSE or RE view, select **Create Offline License**.
4. Enter a machine ID.
5. Click **Create**. The newly created offline license is added to the **Offline Licenses** list.

### Assign a License

Before assigning a license, the organization owner/admin must [add the team member(s)  to the organization in the Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/user-management.html#user-related-permissions). Once added, the admin can assign a Katalon license to any team member, or withdraw a license if no longer needed.

An organizational owner or admin must add the team member to the organization before assigning a license on the Katalon TestOps account. Once added, you can grant the Katalon license to any team members or withdraw a license if no longer needed.

The available licenses are the remaining licenses after the license quota subtracts the total number of offline licenses created and currently active online licenses.

>   *Available licenses = License quota – (Offline licenses + Active online licenses)*

### View License Details

From the main menu of Katalon Studio:

* macOS: **Katalon Studio > About Katalon Studio**

* Windows/Linux: **Help > About**

## How to use Katalon Studio licenses

* [Activate Katalon Studio](/katalon-studio/docs/katalon-studio-activation-since-70.html)
* [Activate Katalon Studio Enterprise](/katalon-studio/docs/activate-KSE.html)
* [Activate Katalon Studio or Katalon Studio with Runtime Engine](/katalon-studio/docs/activate-RE.html)
