---
title: "Troubleshoot Activation Problems"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/troubleshoot-activation-problems.html
---

If you have problems with activation, you can troubleshoot the common issues by following the suggested instructions.

> Tips
>
>* Please use **Ctrl+F** to look for the exceptions and errors you have encountered.
>* If the exception you are looking for is not documented, please leave a comment below.

First, please make sure you have configured the date and time of the machine installing Katalon Studio based on the local time zone. Differences in date and time may affect the license validation of the Katalon Server.

Below are the common issues you may encounter, please troubleshoot correspondingly.

<details><summary>This account has been blocked.</summary>

This error message indicates that your Katalon account has been registered but not verified. To unblock your Katalon account:

1. Sign into [the Katalon website](https://www.katalon.com/). 
2. Go to [My Account](https://www.katalon.com/account/).

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/troubleshoot-activation-problems/my-account.png" width=1204>
   
3. Click **Verify Now** and follow the instructions.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/troubleshoot-activation-problems/guide.png" width=602>

After verifying your account, open Katalon Studio and try activating again. If activation failure still occurs, please wait for 5 minutes and try again.

</details>

<details><summary>Cannot connect to Katalon TestOps server. Please check your Internet connection and try again.</summary>

This error message indicates that Katalon Studio's application cannot communicate with the Katalon server to activate it.

Please check your Internet connection and try again. If you are behind a **Proxy Server**, please configure Authentication Proxy first and try to activate Katalon Studio again.

</details>

<details><summary>Network Security errors</summary>

For Enterprise users with a private network, you may encounter a situation where you fail to execute test scripts or integrate Katalon Studio due to the network security error. Please contact your IT team to whitelist the following domains:

* store.katalon.com
* update.katalon.com
* analytics.katalon.com
* testops.katalon.com
* admin.katalon.com
* katalon-test.s3-accelerate.amazonaws.com (used for uploading reports to [Katalon TestOps](https://analytics.katalon.com))

</details>

<details><summary>CAPTCHA required</summary>

CAPTCHA is required when users enter incorrect passwords for multiple consecutive times. At that time, you should log into [Katalon TestOps](https://analytics.katalon.com/) with that account and enter the captcha. After that, you should be able to activate Katalon Studio normally.

</details>

<details><summary>Machine Quota exceeded</summary>

This exception means the number of machines on which you're using Katalon Studio exceeds the number of licenses that you have. The below section will guide you on how to remove a registered machine ID.

1. Log into [Katalon TestOps](https://analytics.katalon.com/) with your Katalon account.
2. Select the Organization that grants you permission to use the license.
3. In the **License Management** panel, depending on which license in use, select Katalon Studio Enterprise or Katalon Runtime Engine.
4. In the **Licenses** screen view, scroll down to the **Registered Machines** area and remove at least one machine ID.

Please try activating again.

</details>

<details><summary>License Quota exceeded</summary>

This exception means the number of licenses in use (both online and offline) exceeds the total number of licenses that your Organization has subscribed to. This may cause the [sessions terminated](https://docs.katalon.com/katalon-studio/docs/session-termination.html). To ensure the business continuity, we recommend you to subscribe more licenses.

</details>

<details><summary>Your trial has expired. Please subscribe to continue using Katalon Runtime Engine.</summary>

Valid business email registration is eligible for a 30-day trial of both Katalon Studio Enterprise and Katalon Runtime Engine floating licenses. When your trial period expires, you need to subscribe to the paid license of each product to continue using it. Currently, the free license for Katalon Runtime Engine is not available.

If you have subscribed to a Katalon license but cannot use it, please check if you are granted the permission to use. Please see the instruction [here](https://docs.katalon.com/katalon-studio/docs/use-online-license.html).

</details>

<details><summary>Trial license is only available for Katalon accounts registered with a business email.</summary>

If you encounter this exception, properly you have registered a Katalon account with a personal email (e.g. with public domain like `@gmail.com`). Katalon Studio Enterprise and Katalon Runtime Engine trial licenses can only be registered with **business** emails.

</details>

See also:

* [Session Termination Causes](https://docs.katalon.com/katalon-studio/docs/session-termination.html)
