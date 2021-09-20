---
title: "Activate Katalon License"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/activate-license.html
redirect_from:
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html#activating-katalon-studio-enterprise"
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html#other-options"
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html#activating-katalon-studio-enterprise-trial-license"
    - "katalon-studio/docs/activate-KSE.html"
description:
---

In this tutorial, we will guide you through the activation of your 30 days trial and your purchased Katalon licenses, including Katalon Studio Enterprise (KSE) and Katalon Runtime Engine (KRE). You can activate your license with or without Internet access. You can also learn how to configure a proxy if you are behind a proxy server.

To learn more about Katalon licenses, see [Types of License](https://docs.katalon.com/katalon-studio/docs/license.html)

## Activate Licenses

To start your activation, download and open Katalon Studio. The **Katalon Studio Activation** automatically pops up.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/activation.png" alt="activation" width=70%>

### Configure proxy

If you are behind a proxy server, before activating Katalon licenses, you need to configure the Authentication proxy settings. Otherwise, you can skip this step.

Click **Configure Authentication Proxy** at the bottom of the Activation dialog box.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/proxy-preferences/config-proxy-activation.png" width="">

In the Proxy Settings dialog box, you can select one of the three options below.

* **Use system proxy configuration**: Katalon Studio automatically syncs with the proxy server behind your system.
* **No proxy**: There's no proxy.
* **Manual proxy configuration**: You can manually set up your proxy.

> Notes:
>
> If you are using a private network, you might encounter a situation where you fail to execute test scripts or integrate Katalon Studio due to the network security error. To fix this problem, whitelist the following domains:
>
> * store.katalon.com
> * update.katalon.com
> * analytics.katalon.com
> * testops.katalon.io
> * admin.katalon.com
> * katalon-test.s3-accelerate.amazonaws.com (used for uploading reports to [Katalon TestOps](https://analytics.katalon.com))

### Activate Trial License

From Katalon Studio version 7.0.0 onwards, when you first log in to your Katalon account, the trial license associated with your account is automatically activated. Each trial KSE or KRE license is tied to one Katalon account.

To activate the trial license, in the **Katalon Studio Activation** dialog, enter the email and password registered for your Katalon account, then click **Activate**.

You can start using KSE and KRE for 30 days.

### Activate Purchased Licenses with the Internet

When the Owner or Admin of your Organization already granted you a license by adding you to the **Register Users** list, you can activate your KSE and KRE in Katalon Studio.

To activate your license with the Internet, in the **Katalon Studio Activation** dialog, enter the email and password registered for your Katalon account, then click **Activate**.

### Activate Purchased License without the Internet

> Requirement:
>
> * A machine ID. To view your machine ID, see [Machine ID](https://docs.katalon.com/katalon-studio/docs/machine-id.html).
> * A `KSE_<machine_ID>.lic` or `KRE_<machine_ID>.lic` file. To get this license file, provide your machine ID to your Organization Owner or Admin and ask them to grant you an offline license. See [Grant Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html)

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
