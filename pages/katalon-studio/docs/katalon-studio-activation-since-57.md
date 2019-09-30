---
title: "Activate Katalon Studio"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon-studio-activation-since-70.html
redirect_from:
    - "/x/ERLR/"
    - "/katalon-studio/docs/katalon-studio-activation-since-70/"
    - "/display/KD/Installation+and+Setup/"

description:
---
After installing Katalon Studio, you will be asked to activate it. If you currenly use a Katalon Studio Enterprise license, refer to [Activate Katalon Studio Enterprise](https://docs.katalon.com/katalon-studio/docs/activate-KSE.html).

## Activating Katalon Studio

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

If you're behind a Proxy Server, you'll need to configure the proxy settings before activating Katalon Studio. Click **Config Proxy** at the bottom of the Activation dialog box. In the Proxy Settings dialog box, you can select one of three options below.

* **Use system proxy configuration**: Katalon Studio tries to guess which proxy server your system is behind and sync with these settings.
* **No proxy**: there's no proxy.
* **Manual proxy configuration**: you can manually set up your proxy.

### Troubleshooting a common problem when activation

"_Network error! Please try Offline Activation_"- This error message indicates Katalon Studio's application cannot communicate with Katalon server to activate it.

Please check your Internet connection and try again. If you are behind a **Proxy Server**, please **Config Proxy** first and try to activate Katalon Studio again.

## Activating in Console mode

You need a license key that grants you permission to run Katalon Studio from the command line. Before executing Katalon Studio, call the license key by the command-line argument as follows: `licenseFile= [the path to the license key file]`.

For example:
`licenseFile=C:\Users\demokatalon\licensefile\license-window.lic`.
