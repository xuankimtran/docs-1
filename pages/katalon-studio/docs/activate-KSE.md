---
title: "Activate Katalon Studio Enterprise"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/activate-KSE.html
redirect_from:
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html#activating-katalon-studio-enterprise"
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html#other-options"
    - "/katalon-studio/docs/katalon-studio-activation-since-70.html#activating-katalon-studio-enterprise-trial-license"
description:
---
You need a license to activate Katalon Studio Enterprise (KSE) that can work with or without an Internet connection.

> Having problems in activation? [Click here.](https://docs.katalon.com/katalon-studio/docs/troubleshoot-activation-problems.html)

## How to activate KSE online?

You can activate KSE in an online environment with the [Trial KSE license](/katalon-studio/docs/license.html), or any online licenses that grants permission for registered users.

* **Trial License**: The first time you log into Katalon Studio version 7.0.0, the trial license associated with your account will be automatically activated. Please note that each of the trial KSE licenses is bound to only one Katalon account. 

* **Online License**: Only users added to the *Register Users list* can use online licenses.

In the **Katalon Studio Activation** window:

1. Enter your Katalon account then click *Activate*.
2. You will be navigated to your organization, or you can select another one that you belong to in the drop-down list, click *OK*.
3. You are recommended to install the plugins for a better experience with Katalon Studio.
4. Open an existing project or create a new one in Katalon Studio.
5. In Katalon TestOps Integration pop-up window:

   * Select a team in the configured organization that you have permission to access.
   * Select a project you would like to work on or create a new one if permitted.

### How to configure a proxy for online activation?

If you are behind a Proxy Server, you need to configure the Authentication proxy settings before activating KSE. Click *Configure Authentication Proxy* at the bottom of the Activation dialog box.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/proxy-preferences/config-proxy-activation.png" width="">

In the Proxy Settings dialog box, you can select one of three options as follows:

* **Use system proxy configuration**: Katalon Studio will try to guess which proxy server your system is behind then sync it with the settings.
* **No proxy**: there's no proxy.
* **Manual proxy configuration**: you can manually set up your proxy.

## How to activate KSE offline?

A machine ID is required for generating an offline license. In the Katalon Studio Activation window, click **Offline Activation**:

1. **Generate an offline license**: Log into [Katalon Admin](https://admin.katalon.com/) > go to your organization > **License** > **Katalon Studio Enterprise** > **Create Offline License** > insert a **Machine ID** > click **Create**.

    > Notes:
    >* Machine ID is granted for each computer installing Katalon Studio. In the Katalon Studio Activation window, click **Offline Activation**, you can view and copy your machine ID.
    >* Only organizational owners or admins can access **License** in an organization. Learn more about [Roles and Permission](https://docs.katalon.com/katalon-analytics/docs/user-management.html#roles-and-default-permissions).

2. **Locate the generated license**: To use a license, click the **Download** button, the license will be downloaded as a `KSE_<machine_ID>.lic` file. Then click **Browse** in **Katalon Studio Enterprise Activation** to locate the downloaded license file.

3. Click **Activate**.

### Other options

After activating KSE, there will be a window requiring you to log into your Katalon account for connecting to [Katalon TestOps](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html) and [Store](https://docs.katalon.com/katalon-store/docs/overview.html).

KSE users can use plugins both from Store and [offline](https://docs.katalon.com/katalon-studio/docs/offline-plugin.html).
