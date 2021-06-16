---
title: "Troubleshoot Activation Problems"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/troubleshoot-activation-problems.html
---

## Configure Time Zone

When installing Katalon Studio on your machine, make sure you have configured the date and time of the machine based on the local time zone.

Time differences might affect the validation of licenses on the Katalon Server.

## Troubleshoot Common Issues

> **Tips**
>
>* Use **Ctrl+F** to find the exceptions and errors you encountered.
>* Leave a comment below if you cannot find the exceptions and errors you have had.

Here is the list of common issues when activating Katalon Studio and instructions to solve them:

**<details><summary>Cannot connect to Katalon TestOps server. Please check your Internet connection and try again (1).</summary>**

Double-check your Internet connection first.

If you still encounter this error after double-checking, replace the auto-filled Server URL with [https://testops.katalon.io](https://testops.katalon.io).

</details>

**<details><summary>Cannot connect to Katalon TestOps server. Please check your Internet connection and try again (2).</summary>**

This error message means that the application has failed to communicate with Katalon Server for activation.

Check your Internet connection and try again.

If you are behind a **Proxy Server**, configure Authentication Proxy first and then activate Katalon Studio again.

</details>

**<details><summary>CAPTCHA required</summary>**

CAPTCHA is required when you enter incorrect passwords multiple times.

Log into [Katalon TestOps](https://analytics.katalon.com/) using that account and enter the captcha.

You can now activate Katalon Studio.

</details>

**<details><summary>License Quota exceeded</summary>**

This exception means that the number of licenses in use (both online and offline) exceeds the total number of licenses available to your Organization.

This may cause [session termination](https://docs.katalon.com/katalon-studio/docs/session-termination.html).

To ensure business continuity, we recommend you subscribe to more licenses.

</details>

**<details><summary>Machine Quota exceeded</summary>**

> Notes
>
>* One Node-locked license can be assigned to one physical machine ID only.
>* One Floating license can be assigned to up to three dynamic machine IDs but cannot be used on all machines simultaneously.

If the number of machines on which you're using Katalon Studio exceeds the number of licenses that you purchased, you have two options:

* Subscribe to more licenses to cover more machines.
* Remove the machines.

   Follow these steps to remove a registered machine ID.

   1. Log into [Katalon TestOps](https://analytics.katalon.com/).
   2. Select the Organization which permits you to use the license.
   3. Go to the **License Management** panel. Select Katalon Studio Enterprise or Katalon Runtime Engine, depending on which one you are using.
   4. Go to **Licenses** screen view. Scroll down to the **Registered Machines** area. Remove at least one machine ID.
   5. Reactivate the license for the change to take effect.

> More information on this exception can be found [here](https://support.katalon.com/hc/en-us/articles/900004333706-Why-Machine-Quota-Exceeded-message-and-How-to-resolve-it-)

</details>

**<details><summary>Network Security errors</summary>**

For an enterprise user with a private network, you might encounter this problem when executing test scripts or integrating Katalon Studio.

Contact your IT team to whitelist the following domains:

* store.katalon.com
* update.katalon.com
* analytics.katalon.com
* testops.katalon.io
* admin.katalon.com
* katalon-test.s3-accelerate.amazonaws.com (used for uploading reports to [Katalon TestOps](https://analytics.katalon.com))

</details>

**<details><summary>This account has been blocked.</summary>**

This error message indicates that your Katalon account has been registered but not yet verified.

Follow these steps to unblock your Katalon account:

1. Sign in [Katalon website](https://www.katalon.com/).
2. Go to [My Account](https://www.katalon.com/account/).

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/troubleshoot-activation-problems/my-account.png" width=1204>
   
3. Click **Verify Now** and follow the instructions.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/troubleshoot-activation-problems/guide.png" width=602>

After verifying your account, open Katalon Studio and reactivate it.

> If activation still fails, wait for another 5 minutes and try again.

</details>

**<details><summary>Trial license is only available for Katalon accounts registered with a business email.</summary>**

You encounter this exception if you have registered Katalon accounts using your personal email (e.g., an email with a public domain such as `@gmail.com`).

You must register your business email to use the Katalon Studio Enterprise and Katalon Runtime Engine trial license.

</details>

**<details><summary>Your trial has expired. Please subscribe to continue using Katalon Runtime Engine.</summary>**

A valid business email is eligible for a 30-day trial of Katalon Studio Enterprise and Katalon Runtime Engine. The trial license is a floating license.

When your trial period expires, you must subscribe to each product to continue using it.

Currently, the free license for Katalon Runtime Engine is not available.

If you have subscribed but cannot use a Katalon license, check if you have permission to use it. See more instructions [here](https://docs.katalon.com/katalon-studio/docs/use-online-license.html).

</details>

See also:

* [Session Termination Causes](https://docs.katalon.com/katalon-studio/docs/session-termination.html)
