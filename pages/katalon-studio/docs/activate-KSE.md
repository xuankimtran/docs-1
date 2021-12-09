---
title: "Activate Katalon License"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/activate-license.html
redirect_from:
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html#activating-katalon-studio-enterprise"
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html#other-options"
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html#activating-katalon-studio-enterprise-trial-license"
    - "/katalon-studio/docs/activate-KSE.html"
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html"
    - "/x/ERLR/"
    - "/katalon-studio/docs/katalon-studio-activation-since-70/"
    - "/katalon-studio/docs/katalon-studio-activation-since-57/"
    - "/katalon-studio/docs/katalon%20studio%20activation%20since%2057/"
    - "/katalon-studio/docs/katalon-studio-activation-since-57.html"
description:
---

In this tutorial, we will guide you through the activation of your Katalon Studio Enterprise (KSE) and Katalon Runtime Engine (KRE) licenses. This guide is for:

* Trial license users.
* Users with internet access.
* Users in offline work environments.

> Notes:
>
> * To learn more about Katalon licenses, see [Types of Licenses](https://docs.katalon.com/katalon-studio/docs/license.html).
> * If you are behind a proxy server, before activating Katalon licenses, you need to configure the Authentication proxy settings. To learn more about how to configure a proxy, see [Configure Proxy for Authentication](https://docs.katalon.com/katalon-studio/docs/configure-proxy.html).

## Activate Trial License

From Katalon Studio version 7.0.0 onwards, when you first log in to the Katalon Studio application, the trial license associated with your account is automatically activated and valid for 30 days. Each trial KSE or KRE license is tied to one Katalon account.

First, download and open Katalon Studio. The **Katalon Studio Activation** automatically pops up. Enter the email and password registered for your Katalon account, then click **Activate**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/activation.png" alt="activation" width=70%>

## Activate a license with Internet access

> Requirements:
>
> Owner or Admin of your Organization has added you to the **Licensed Users** list. See [Grant Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html).

To activate your license with the Internet, do as follow:

1. Open Katalon Studio:

* If you open Katalon Studio for the first time, the **Katalon Studio Activation** dialog automatically pops up.

* If you are already logged in to a Katalon account in Katalon Studio, click on the _Profile_ button and select **Deactivate**. You are now logged out and the **Katalon Studio Activation** dialog appears.

2. Log in with the Licensed User account email and password. Click **Activate**.

You can now use KSE, and can also reserve an available KRE license by using KRE. If you wish to use KRE but no licenses are available, contact your Organization Owner or Admin.

> Notes:
>
> To view your current license, see [View License Details](https://docs.katalon.com/katalon-studio/docs/view-license-details.html).

## Activate a license while offline

> Requirement:
>
> * A machine ID. To view your machine ID, see [Machine ID](https://docs.katalon.com/katalon-studio/docs/machine-id.html).
> * A `KSE_<machine_ID>.lic` or `KRE_<machine_ID>.lic` file. To get this license file, provide your machine ID to your Organization Owner or Admin and ask them to grant you an offline license. See [Grant Offline Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html#create-an-offline-license).

For offline license activation, follow these steps:

Put your **.lic** file in the **license** folder. With KRE, to execute multiple sessions in parallel, put multiple license files in the **license** folder.

**.katalon** is a hidden folder. To find the **license** folder in your computer, search for:

* Windows: **C:\Users\<user_name>\.katalon\license**

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-RE/license.png" width="" height="">

* Linux: **/home/<user_name>/.katalon/license**
* macOS: **/Users/<user_name>/.katalon/license**

**For KRE**:

Put your `KRE_<machine_ID>.lic` file in the **license** folder. Your KRE license is now activated. Every time you start running a test with KRE, KRE automatically verifies that your license file is available and valid.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/KRE-license.png" alt="verify KRE license" width=70%>

**For KSE**

1. To activate your KSE license, in the **Katalon Studio Activation** dialog, click **Offline Activation**. The **Katalon Studio Enterprise Activation** dialog appears.

2. In the **License file** section, enter the path to your `KSE_<machine_ID>.lic` file, or click **Browse** to navigate to your **.lic** file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/offline-license-activation.png" alt="offline activation" width=70%>

3. Click **Activate**.

> Notes:
>
> * For a better experience with Katalon Studio, you can also install our plugins. See [Using Plugins with Katalon Studio Enterprise License](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html).
> * If you have any activation problems, see [Troubleshoot Activation Problems](https://docs.katalon.com/katalon-studio/docs/troubleshoot-activation-problems.html).
> * For further instructions on working with KRE, refer to [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#katalon-studio-plugins-in-console-mode).
