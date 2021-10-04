---
title: "Troubleshoot Activation Problems"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/troubleshoot-activation-problems.html
redirect_from: /katalon-analytics/docs/network-config.html
---

## Configure Time Zone

When installing Katalon Studio on your machine, make sure you have configured the date and time of the machine based on the local time zone.

Time differences might affect the validation of licenses on the Katalon Server.

## Troubleshoot Common Issues

> **Tips**
>
> * To find the exceptions and errors you encountered, use **Ctrl+F**.
> * If you cannot find the exceptions or error message you encountered, you can leave a comment below for further support.

Here is the list of common issues when activating Katalon Studio and/or starting Katalon TestOps, followed by the instructions to solve them:

**<details><summary>Cannot connect to Katalon TestOps server. Please check your Internet connection and try again (1).</summary>**

Double-check your Internet connection first.

If you still encounter this error after double-checking, replace the auto-filled Server URL with [https://testops.katalon.io](https://testops.katalon.io).

</details>

**<details><summary>Cannot connect to Katalon TestOps server. Please check your Internet connection and try again (2).</summary>**

This error message means that the application has failed to communicate with Katalon Server for activation.

Check your Internet connection and try again.

If you are behind a **Proxy Server**, configure proxy authentication first and then activate Katalon Studio again. See: [Configure Proxy for Authentication](https://docs.katalon.com/katalon-studio/docs/configure-proxy.html).

</details>

**<details><summary>CAPTCHA required</summary>**

CAPTCHA is required when you enter incorrect passwords multiple times.

Log into [Katalon TestOps](https://testops.katalon.io) using that account and enter the captcha.

You can now activate Katalon Studio.

</details>

**<details><summary>License Quota exceeded</summary>**

This exception means that the number of licenses in use exceeds the total number of licenses available to your Organization.

This may cause [session termination](https://docs.katalon.com/katalon-studio/docs/session-termination.html).

To ensure business continuity, we recommend you subscribe to more licenses.

</details>

**<details><summary>Machine Quota exceeded</summary>**

If the number of machines on which you're using Katalon Studio exceeds the number of licenses that you purchased, you have two options:

* Subscribe to more licenses to cover more machines and execution sessions. See [Upgrade Subscriptions](https://docs.katalon.com/katalon-studio/docs/upgrade-subs.html).
* Remove the machines. See [Revoke and transfer a license](https://docs.katalon.com/katalon-studio/docs/license-management.html#revoke#a#license).

</details>

**<details><summary>Network Security errors</summary>**

For Enterprise users with a private network, you might encounter a situation where you fail to execute test scripts, integrate Katalon Studio, and/or access Katalon TestOps, due to the network security errors.

Contact your IT team to whitelist the following domains:

* store.katalon.com
* update.katalon.com
* analytics.katalon.com
* testops.katalon.io
* admin.katalon.com
* katalon-test.s3-accelerate.amazonaws.com (used for uploading reports to [Katalon TestOps](https://testops.katalon.io))

</details>

**<details><summary>IP Addresses errors</summary>**

For Katalon TestOps's network configuration, you might encounter a problem if you are integrating with an On-Premises development system such as Jira Server or Azure DevOps Server.

Contact your IT team to whitelist the following IP addresses:

* 52.45.203.41

* 52.203.34.201

* 35.172.81.5

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

**<details><summary>Your trial has expired. Please subscribe to continue using Katalon Runtime Engine.</summary>**

A valid business email or personal email is eligible for a 30-day trial of Katalon Studio Enterprise and Katalon Runtime Engine. The trial license is a floating license.

When your trial period expires, you must subscribe to each product to continue using it.

Currently, the free license for Katalon Runtime Engine is not available.

If your Enterprise has purchased Katalon licenses but you are not able to use them, check if you have permissions to use the licenses. See [Grant Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html).

</details>

See also:

* [Session Termination Causes](https://docs.katalon.com/katalon-studio/docs/session-termination.html)
