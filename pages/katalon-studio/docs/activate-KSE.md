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

In this tutorial, we will guide you through the activation of your Katalon Studio Enterprise (KSE) and Katalon Runtime Engine (KRE) licenses, including:

* Activate your trial license
* Activate your granted licenses with the Internet
* Activate your granted licenses without the Internet

> Notes:
>
> * To learn more about Katalon licenses, see [Types of Licenses](https://docs.katalon.com/katalon-studio/docs/license.html).
> * If you are behind a proxy server, before activating Katalon licenses, you need to configure the Authentication proxy settings. To learn more about how to configure a proxy, see [Configure Proxy](https://docs.katalon.com/katalon-studio/docs/configure-proxy.html).

## Activate Trial License

From Katalon Studio version 7.0.0 onwards, when you first log in to your Katalon account, the trial license associated with your account is automatically activated. Each trial KSE or KRE license is tied to one Katalon account.

To start your activation, download and open Katalon Studio. The **Katalon Studio Activation** automatically pops up. Enter the email and password registered for your Katalon account, then click **Activate**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/activation.png" alt="activation" width=70%>

## Activate Granted Licenses with the Internet

When the Owner or Admin of your Organization already granted you a license by adding you to the **Register Users** list, you can activate your KSE and KRE in Katalon Studio.

To activate your license with the Internet, in the **Katalon Studio Activation** dialog, log in with the Katalon account that already granted a license, then click **Activate**.

## Activate Granted License without the Internet

> Requirement:
>
> * A machine ID. To view your machine ID, see [Machine ID](https://docs.katalon.com/katalon-studio/docs/machine-id.html).
> * A `KSE_<machine_ID>.lic` or `KRE_<machine_ID>.lic` file. To get this license file, provide your machine ID to your Organization Owner or Admin and ask them to grant you an offline license. See [Grant Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html).

To activate your license without the Internet, follow these steps:

Put your **.lic** file in the **license** folder. With KRE, to execute multiple sessions in parallel, put multiple license files in the **license** folder.

You can find the **license** folder at:

* Windows: **C:\Users\<user_name>\.katalon\license**

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-RE/license.png" width="" height="">

* Linux: **/home/<user_name>/.katalon/license**
* macOS: **/Users/<user_name>/.katalon/license**

> Notes:
>
> **.katalon** is a hidden folder.

**For KRE**:

After you put your `KRE_<machine_ID>.lic` file in the **license** folder, you successfully activate your KRE license. Every time you start running a test with KRE, KRE automatically verifies your valid licenses available in the **license** file.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/verify-offline-kre-license.png" alt="verify KRE license" width=70%>

**For KSE**

1. To activate your KSE license, in the **Katalon Studio Activation** dialog, click **Offline Activation**. The **Katalon Studio Enterprise Activation** dialog appears.

2. In the **License file** section, enter the path to your `KSE_<machine_ID>.lic` file, or click **Browse** to navigate to your **lic.** file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/offline-license-activation.png" alt="offline activation" width=70%>

3. Click **Activate**.

> Notes:
>
> * For a better experience with Katalon Studio, you can also install our plugins. See [Using Plugins with Katalon Studio Enterprise License](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html).
> * If you have any activation problems, see [Troubleshoot Activation Problems](https://docs.katalon.com/katalon-studio/docs/troubleshoot-activation-problems.html).
> * For further instructions on working with KRE, refer to [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#katalon-studio-plugins-in-console-mode).
