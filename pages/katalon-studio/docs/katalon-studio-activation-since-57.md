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
After installing Katalon Studio, you will be asked to activate it. There are two ways of activating Katalon Studio: online and offline activations.

## Online activating Katalon Studio

You need to create a Katalon Account and specify your Organization to log in to Katalon Studio.

> Notes: If you don't have an account, click [here](https://www.katalon.com/create-account/) to sign up or you can register for one right inside Katalon Studio by clicking **Register**. Once you have signed up successfully, Katalon Studio will automatically be activated.

Follow these steps to activate Katalon Studio:

1. Enter the email and password registered for your Katalon account then click **Activate**.
2. You are navigated to your own organization or you can select one of the organizations you belong to in the drop-down list, click **OK**.
3. You're recommended to install the plugins for a better experience with Katalon Studio.
4. Open an existing project or create a new one in Katalon Studio.
5. In Katalon Analytics Integration pop-up window:

* Select a team in the configured organization that you have permission to access.
* Select a project under that team you’d like to work on or create your own one if you have permission.

### Configuring Proxy for online activation

If you're behind a Proxy Server, you'll need to configure the proxy settings before activating Katalon Studio. Click **Config Proxy** at the bottom of the Activation dialog box. In the Proxy Settings dialog box, you can select one of three options below.

* **Use system proxy configuration**: Katalon Studio tries to guess which proxy server is your system behind and sync with these settings.
* **No proxy**: there's no proxy.
* **Manual proxy configuration**: you can manually set up your proxy.

### Troubleshooting a common problem when activation

"_Network error! Please try Offline Activation_"- This error message indicates Katalon Studio application cannot communicate with Katalon server to activate it.

Please check your Internet connection and try again. If you are behind a **Proxy Server**, please **Config Proxy** first and try to activate Katalon Studio again.

## Offline activating Katalon Studio

You need a license key to offline activate Katalon Studio when there's no Internet. A Katalon account is required for generating a license key. In Katalon Studio Activation pop-up window, click **Offline Activation**:

1. Generate a license key: To generate a license key in Katalon Analytics, access your organization, navigate to the **License Keys** tab, insert a **Machine ID**, then click **Create**.

> Notes: **Machine ID** is granted for each computer installing Katalon Studio. In Katalon Studio Activation pop-up window, click **Offline Activation**, you can view and copy your machine ID.

2. Locate the generated license key: To use a license key, click the **Download** button, the license key will be downloaded as a `license.lic` file. Then click **Choose file** in **Product Offline Activation** to locate the downloaded license key file.

3. Click **Activate**.
