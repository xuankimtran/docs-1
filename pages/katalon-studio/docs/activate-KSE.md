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
    - "/katalon-studio/docs/active-KRE.html"
description:
---

This guide shows you how to activate Katalon Studio Enterprise (KSE) and Katalon Runtime Engine (KRE) licenses in different scenarios, including:

* Trial license activation.
* Online license activation.
* Offline license activation.

> **Notes**:
>
> * To learn more about Katalon licenses, see: [Types of Licenses](https://docs.katalon.com/katalon-studio/docs/license.html).
> * If you are behind a proxy server, before activating Katalon licenses, you need to configure the Authentication proxy settings. To learn how to configure a proxy, see: [Configure Proxy for Authentication](https://docs.katalon.com/katalon-studio/docs/configure-proxy.html).

## Activate a Trial License

> **Notes**:
>
> From Katalon Studio version 7.0.0 onwards, when you first log in to the Katalon Studio application, the Trial License associated with your account is automatically activated and valid for 30 days. Each trial KSE or KRE license is tied to one Katalon account.

Follow these steps:

1. Open Katalon Studio. 

    The **Katalon Studio Activation** dialog appears.

2. Enter the email and password of your registered Katalon account, then click on the **Activate** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/activation.png" alt="activation" width=70%>

Once you have logged in to Katalon Studio as a user with a Trial license, you can generate an API key to use KRE. For detailed instructions, refer to this guide: [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).

## Activate an Online License

> **Requirements**:
>
> The Owner or Admin of your Organization has added you to the **Licensed Users** list. See: [Grant Katalon Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html).

### Activate an online KSE license

Follow these steps:

1. Open Katalon Studio. The following actions can be different depending on your login status.

    If you open Katalon Studio for the first time, the **Katalon Studio Activation** dialog appears.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/KS-Activation-dialog.png" alt="Katalon Studio Activation dialog" width=70%>

    If you have already logged in to a Katalon account in Katalon Studio, click on the **Profile** button and select **Deactivate**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/KS-Deactivate.png" alt="Katalon Studio Activation dialog" width=70%>

    You have now logged out, and the **Katalon Studio Activation** dialog appears.

2. Enter the email and password registered with the Licensed User account, then click on the **Activate** button.

### Activate an online KRE license

After the Owner or Admin of your Organization has granted you an online KRE license, the license is activated automatically. To generate an API key to use KRE, refer to this guide: [API Keys](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html#generate-a-katalon-api-key).

> **Notes**:
>
> To view details about your current license, see: [View License Details](https://docs.katalon.com/katalon-studio/docs/view-license-details.html).

## Activate Offline Licenses

> **Requirements**:
>
> * A machine ID. To view your machine ID, see [Machine ID](https://docs.katalon.com/katalon-studio/docs/machine-id.html).
> * A `KSE_<machine_ID>.lic` or `KRE_<machine_ID>.lic` license file. To get this license file, provide your machine ID to your Organization Owner or Admin and ask them to grant you an offline license. See [Grant Offline Licenses](https://docs.katalon.com/katalon-studio/docs/use-online-license.html#create-an-offline-license).

### Prepare license files

Put your `.lic` file in the `.katalon/license` folder.

The `.katalon/license` is a hidden folder. To locate the folder in your computer, search for:

* Windows: `C:\Users\<user_name>\.katalon\license`

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-RE/license.png" width="" height="">

* Linux: `/home/<user_name>/.katalon/license`
* macOS: `/Users/<user_name>/.katalon/license`

### Activate an offline KSE license

Follow these steps:

1. To activate your KSE license, in the **Katalon Studio Activation** dialog, select **Offline Activation**. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/KS-Activation-dialog-offline-activation.png" alt="Click on offline activation" width=70%>

    The **Katalon Studio Enterprise Activation** dialog appears.

2. In the **License file** section, enter the path to your `KSE_<machine_ID>.lic` file, or click **Browse** to navigate to your **.lic** file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/offline-license-activation.png" alt="offline activation" width=70%>

3. Click on the **Activate** button.

### Activate an offline KRE license

To activate your offline KRE license, put your `KRE_<machine_ID>.lic` file in the `.katalon/license` folder.

>  To execute multiple KRE sessions in parallel, put multiple license files in the `.katalon/license` folder.

Every time you start running a test with KRE, KRE automatically verifies that your license file is available and valid.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/activate-KSE/KRE-license.png" alt="verify KRE license" width=70%>

> **Notes**:
>
> * To extend Katalon Studio's capabilities and integrate the software with your favorite tools, refer to this document: [Using Plugins with Katalon Studio Enterprise License](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html).
> * If you have any license activation problems, refer to this troubleshooting document: [Troubleshoot Activation Problems](https://docs.katalon.com/katalon-studio/docs/troubleshoot-activation-problems.html).
> * For detailed instructions on working with KRE, refer to this guide: [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#katalon-studio-plugins-in-console-mode).
