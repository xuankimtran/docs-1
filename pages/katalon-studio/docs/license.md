---
title: "Katalon Studio Licensing"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license.html
description:
---

> Starting from **version 7.0.0**, you need a license to activate and use one of the Katalon Studio products, including Katalon Studio Enterprise (KSE), Katalon Studio (KS), and Runtime Engine (RE).

This section provides a comprehensive view of license types, license subscription, and management.

Click [here](refer to the FAQ/comparing table) for a detailed comparison between KS and KSE as well as more information on RE.

## Katalon Studio License Types

There are three types of Katalon Studio licenses, including trial, paid, and free licenses.

### Trial License

With a unique and valid email registration, you are eligible for a 30-day trial for both KSE and RE. The KSE and RE trial license is generated and activated automatically with your first login to the application.

Each trial license can be active on only one machine at a time. When your trial period is expired, you need to subscribe to the paid license of each product to continue using it, or the Katalon Studio free license is automatically activated.

> Notes
>
> * The KSE and RE trial license is only available for business emails.
> * The trial license does not support KSE offline activation and features nor offline RE.

### Paid license

#### For Katalon Studio Enterprise

Katalon Studio Enterprise license is named license.

* 1 license is tied to a Katalon account/user.
* 1 account can be activated/used on 1 machine at a time.
* License is transferable (refer to the doc guide how to manage license) 
* License activation and validation require an internet connection

Without the Internet, any license of a KSE subscription can be converted to a node-locked offline license.  A computer ID is required to convert an annual license into an offline license. Once converted, the license is deducted from the KSE subscription and cannot be transferred to another machine or account until it is expired.

#### For Runtime Engine

Runtime Engine license is a node-locked license. When running from the command line, a working session accounted for one license is equal to a process conducted.

* A license is tied to a registered machine.
* A machine can run multiple licenses at the same time if needed.
* The license is transferable.

### Online License vs. Offline License

The **online** license of both KSE and RE is transferable among the organization's registered users as long as the active licenses do not exceed the license and machine quotas.

The **offline** license is for using KSE and RE without the Internet. Once generated, the offline license is irrevocable and cannot be terminated. Also, the expiration date of an offline license cannot be adjusted.

### Free License

The free license granted for each Katalon account only includes the standard Katalon Studio with fundamental features. Currently, the free license for RE is not available. If you wish to execute Katalon Studio in console mode, you need to subscribe to a RE license.

At any time, you can upgrade the free KS to KSE with a paid license without the need to re-download.

## Subscribe to KSE/RE Licenses

You can purchase a Katalon license via Katalon TestOps. Log in to your [Katalon TestOps](https://analytics.katalon.com/home), go to **Organization > Subscriptions >** choose desired products and subscription models, and make payment.

## Manage KSE/RE Licenses

You can access [Katalon TestOps](https://analytics.katalon.com/) to subscribe, create, and distribute licenses. Only an organizational Owner or Admin can access the License tab of the organization. For more details about roles and default permissions, please view [this document](https://docs.katalon.com/katalon-analytics/docs/user-management.html).

### Create an online KSE/RE license

#### KSE

1. On [Katalon TestOps](https://analytics.katalon.com/home), go to **Organization > License**.
2. Register the on-demand users by adding them to the **Registered Users** list. The number of registered users cannot exceed the license quota.

When the registered users activate KSE, their machine IDs are added to the **Online Licenses** on Katalon TestOps.

#### RE

Any members of an organization can use the RE online licenses that the organization has purchased. Users need to add API Keys to the command to run KS/KSE from the CLI.

### Create an offline RE/KSE license

Offline licenses, once generated, cannot be revoked or terminated. Currently, the expiration period for each offline license lasts 60 days. The available licenses for online usage are equal to the license quota subtracting the number of offline licenses created.

You need a machine ID to generate an offline license for both KSE and RE. To view a machine ID, open Katalon Studio, in the **Katalon Studio Activation** window, click **Offline Activation** to view and copy the machine ID.

1. On [Katalon TestOps](https://analytics.katalon.com/home), go to **Organization > License**.
2. Click **Create Offline License** in the KSE or RE view, enter a machine ID, and click **Create**. The newly created offline license is added to the **Offline Licenses** list.

### Assign

Before assigning a license, the organization owner/admin must add the team member(s) to the organization in the Katalon TestOps. Once added, the administrator can assign a Katalon license to any team member, or withdraw a license if no longer needed.

An organizational owner or admin must add the team member to the organization before assigning a license on the Katalon TestOps account. Once added, you can grant the Katalon license to any team members or withdraw a license if no longer needed.

The available licenses are the remaining licenses after the license quota subtracts the total number of offline licenses created and currently active online licenses.

### View License Details

To view details about the Katalon Studio license you are using, from the main menu of Katalon Studio

* Mac Users: **Katalon Studio > About Katalon Studio**

* Windows/Linux Users: **Help > About**

## How to use Katalon Studio licenses

* [Activate Katalon Studio](/katalon-studio/docs/katalon-studio-activation-since-70.html)
* [Activate Katalon Studio Enterprise](/katalon-studio/docs/activate-KSE.html)
* [Activate Katalon Studio or Katalon Studio with Runtime Engine](/katalon-studio/docs/activate-RE.html)


