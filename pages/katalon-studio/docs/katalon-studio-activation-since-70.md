---
title: "Activate Katalon Studio"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-studio-activation-since-70.html
redirect_from:
    - "/x/ERLR/"
    - "/katalon-studio/docs/katalon-studio-activation-since-70/"
    - "/katalon-studio/docs/katalon-studio-activation-since-57/"
    - "/katalon-studio/docs/katalon%20studio%20activation%20since%2057/"
    - "/katalon-studio/docs/katalon-studio-activation-since-57.html"
description:
---
After installing Katalon Studio, you will be asked to activate it. If you currenly use a Katalon Studio Enterprise license, refer to [Activate Katalon Studio Enterprise](https://docs.katalon.com/katalon-studio/docs/activate-KSE.html).

Every Katalon account is eligible for 30-day [trials](/katalon-studio/docs/license.html) of Katalon Studio Enterprise and Runtime Engine. When your trial period expires, you need to subscribe to the paid license of each product to continue using it, or the Katalon Studio free license is automatically activated. At any time, you can upgrade the free Katalon Studio to Katalon Studio Enterprise with a paid license without the need to re-download.

You need to create a Katalon Account and specify your Organization to log in to Katalon Studio.

> Notes: If you don't have an account, click [here](https://www.katalon.com/create-account/) to sign up, or you can register for one right inside Katalon Studio by clicking **Register**. Once you have signed up successfully, Katalon Studio will automatically be activated.

Follow these steps to activate Katalon Studio:

1. Enter the email and password registered for your Katalon account then click **Activate**.
2. You are navigated to your own organization, or you can select one of the organizations you belong to in the drop-down list, click **OK**.
3. You're recommended to install the plugins for a better experience with Katalon Studio.
4. Open an existing project or create a new one in Katalon Studio.
5. In Katalon TestOps Integration pop-up window:

* Select a team in the configured organization that you have permission to access.
* Select a project under that team you’d like to work on or create your own one if you have permission.

### Configuring proxy for online activation

If you're behind a Proxy Server, you need to configure the Authentication proxy settings before activating Katalon Studio. Click **Configure Authentication Proxy** at the bottom of the Activation dialog box.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/proxy-preferences/config-proxy-activation.png" width="">

In the Proxy Settings dialog box, you can select one of three options below.

* **Use system proxy configuration**: Katalon Studio tries to guess which proxy server your system is behind and sync with these settings.
* **No proxy**: there's no proxy.
* **Manual proxy configuration**: you can manually set up your proxy.

### Troubleshooting common issues with network

"_Cannot connect to Katalon TestOps server. Please check your Internet connection and try again._"- This error message indicates Katalon Studio's application cannot communicate with Katalon server to activate it.

Please check your Internet connection and try again. If you are behind a Proxy Server, please configure Authentication Proxy first and try to activate Katalon Studio again.

For Enterprise users with a private network, you may encounter a situation where you fail to execute test scripts or integrate Katalon Studio due to the network security error. Please contact your IT team to whitelist the following domains:

* store.katalon.com
* update.katalon.com
* analytics.katalon.com
* testops.katalon.com

### CAPTCHA required

CAPTCHA is required when a user enters an incorrect password for 5 consecutive times. At that time, you should log into [Katalon TestOps](https://analytics.katalon.com/) with that account and enter the captcha. After that, you should be able to activate Katalon Studio normally.
