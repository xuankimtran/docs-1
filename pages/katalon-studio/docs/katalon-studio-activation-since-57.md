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

## Activating Katalon Studio Enterprise

You need a license to activate Katalon Studio Enterprise that can work without an Internet connection. A machine ID is required for generating a license. In Katalon Studio Activation pop-up window, click **Activate Katalon Studio Enterprise**:

1. Generate a license: To generate a license in Katalon TestOps, access your organization, navigate to the **License** tab, insert a **Machine ID**, then click **Create**.

2. Locate the generated license: To use a license, click the **Download** button, the license will be downloaded as a `license.lic` file. Then click **Choose file** in **Product Offline Activation** to locate the downloaded license file.

3. Click **Activate**.

### Other options

After activating Katalon Studio Enterprise, there will be a pop-up window requiring you to log in to your Katalon account for connecting to [Katalon TestOps](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html) and [Store](https://docs.katalon.com/katalon-store/docs/overview.html).

Currently, the Katalon Studio Enterprise users can use [private plugins](https://docs.katalon.com/katalon-studio/docs/private-plugins.html) as an alternative option of using plugins from Katalon Store.

Regarding TestOps, there is no on-premises version; hence, the automatically generated [JUnit reports](https://docs.katalon.com/katalon-studio/docs/export-test-results-in-junit-format.html), and the [basic report plugin](https://docs.katalon.com/katalon-studio/docs/basic-report.html) can be a substitute for TestOps.

## Activating Katalon Studio Enterprise trial license

You need to generate a trial license for Katalon Studio Enterprise before activating it. Each trial license of Katalon Studio Enterprise  is bound to each machine.

1. Navigate to your organization's profile. On [Katalon TestOps](https://analytics.katalon.com) homepage, click on your profile's icon on the bottom left corner.

> Notes: Only the organizational owner can access the organizational profile.

2. Select the **License** tab, enter a machine ID to create a trial license for it. Download the newly created license.

> Notes: **Machine ID** is granted for each computer installing Katalon Studio. In Katalon Studio Activation pop-up window, click **Activate Katalon Studio Enterprise**, you can view and copy your machine ID.

3. In **Activate Katalon Studio Enterprise** pop-up dialog,  locate the license file you have just downloaded in step 2. Click **Activate**.

## Activating in Console mode

You need a license key that grants you permission to run Katalon Studio from the command line. Before executing Katalon Studio, call the license key by the command-line argument as follows: `licenseFile= [the path to the license key file]`.

For example:
`licenseFile=C:\Users\demokatalon\licensefile\license-window.lic`.
