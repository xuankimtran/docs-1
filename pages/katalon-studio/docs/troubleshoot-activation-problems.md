---
title: "Troubleshoot Activation Problems"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/troubleshoot-activation-problems.html
---

If you have problems with activation, you can troubleshoot the common issues yourself.

> Tips
>
>* Please use **Ctrl+F** to look for the exceptions and errors you have encountered.
>* If the exception you are looking for is not documented, please leave a comment below to request a proposed solution from the Katalon team.

First, please make sure you have configured the date and time of the machine installing Katalon Studio based on the local time zone. Differences in date and time may affect the license validation of the Katalon Server.

Below are the common issues you may encounter, please troubleshoot correspondingly.

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

This exception means the number of machines you're using Katalon Studio exceeds the number of licenses that you have. The below section will guide you on how to remove a registered machine ID.

1. Log into [Katalon TestOps](https://analytics.katalon.com/) with your Katalon account.
2. Select your Organization that associates with your Katalon account.
3. In the **License Management** panel, select Katalon Studio Enterprise.
4. In the **Licenses** screen view, scroll down to the **Registered Machines** area and remove at least one machine ID.

</details>

<details><summary>License Quota exceeded</summary>

</details>

<details><summary>Your trial has expired. Please subscribe to continue using Katalon Runtime Engine.</summary>

</details>

<details><summary>Trial license is only available for Katalon accounts registered with a business email.</summary>

</details>

See also:

* [Session Termination Causes](https://docs.katalon.com/katalon-studio/docs/session-termination.html)
