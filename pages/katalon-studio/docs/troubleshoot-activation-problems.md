---
title: "Troubleshoot Activation Problems"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/troubleshoot-activation-problems.html
---

If you have problems with activation, you can troubleshoot the common issues yourself.

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

<details><summary>Machine quota exceeded</summary>

</details>

<details><summary>License quota exceeded</summary>

</details>

<details><summary>License quota exceeded</summary>

</details>