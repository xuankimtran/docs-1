---
title: "Sauce Labs Integration" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/saucelabs-plugin.html
redirect_from:
    - "/katalon-studio/docs/saucelabs-integration.html"
    - "/display/KD/SauceLabs+Integration/"
    - "/display/KD/SauceLabs%20Integration/"
    - "/x/UBVO/"
    - "/katalon-studio/docs/saucelabs-integration/"
description: Guide to use the plugin to integrate Katalon Studio with Sauce Labs.
---

> Requirements:
> * An active Katalon Studio Enteprise license. To learn more about activating your license, you can refer to this document: [Activate Katalon license](https://docs.katalon.com/katalon-studio/docs/activate-license.html).

## Install the Sauce Labs Integration plugin

Download and install the **Sauce Labs Integration** plugin. You can download the plugin from the Katalon Store here: [Sauce Labs Integration](https://store.katalon.com/product/75/Sauce-Labs-Integration#pricing-content).

To activate the plugin, navigate to Account Settings in Katalon Studio and click **Reload Plugin**.
## Sauce Labs for Web testing
### Create a Sauce Labs custom profile

Go to **Project > Settings > Plugins > Sauce Labs Integration**. Enter your credentials and your desired Sauce Labs operating environments and systems, including: 

* **API Key**: enter an API Key generated from the User Settings in Sauce Labs. For further details about retrieving the API key in Sauce Labs, you can refer to this Sauce Labs document: [User Settings](https://docs.saucelabs.com/basics/acct-team-mgmt/managing-user-info/#user-settings).
* **Username**: enter your username displayed in Sauce Labs.
* **Browser's name**: enter your desired execution browser.
* **Platform**: enter the operating system you want to execute with. By default, Katalon automatically generates your operating system.
* **Version**: enter the version of the operating system you want to execute with. By default, Katalon automatically generates the installed version of your operating system.
* **Job's Name**: The Sauce Labs session you want to execute. By default, this is set to **Default Job**.

Click  **Generate Sauce Labs Custom Profile** to finalize your profile. 

> Notes: 
> * The default custom profile is named `saucelabs_default`. 
> * To be recognized as a Sauce Labs profile, all custom profiles must have the following syntax: `saucelabs_<your-custom-profile-name>`.

<img src="url" width="70%" alt="Enable Sauce Labs integration">

You can also view and edit your profile in **Projects > Settings > Desired Capabilities > Custom**.

<img src="url" width="70%" alt="View Sauce Labs custom profile">

You can now use the newly created profile to execute tests.
### Execute a test case with Sauce Labs profiles

1. Open a test case.

2. Click the dropdown list next to **Run** (Command + Shift + A).

3. Select **Custom capabilities**.

4. Select your Sauce Labs profile.

<img src="url" width="70%" alt="Execute Sauce Labs custom profile in a test case">

### Execute a test suite with Sauce Labs profiles

1. Open a test suite.

2. Add the test cases you want to execute into the test suite.

3. Click the dropdown list next to **Run** (Command + Shift + A).

4. Select **Custom capabilities**.

5. Select your Sauce Labs profile.

<img src="url" width="70%" alt="Execute Sauce Labs custom profile in a test suite">

### Execute a test suite collection with Sauce Labs profiles

1. Open a test suite collection.

2. Add the test suites you want to execute into the test suite collection. 

3. Double-click on the cell under the **Run with** column. A **Select an environment** dialog opens.

4. Select your Sauce Labs profile.

<img src="url" width="70%" alt="Execute Sauce Labs custom profile in a test suite collection">

5. Click **OK**. Then click **Execute**.

<img src="url" width="70%" alt="Execute Sauce Labs custom profile in a test suite collection">

### On Sauce Labs Dashboard, under Automated Tests tab the following result is displayed

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/saucelabs-plugin/7-result.png" width="70%" alt="Execute Sauce Labs custom profile in a test suite collection">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/saucelabs-plugin/6-result.png" width="70%" alt="Execute Sauce Labs custom profile in a test suite collection">

## Sauce Labs for Mobile testing and Hybrid application testing

The plug-in provides you with an intuitive user interface to create Sauce Labs custom profiles for Web Testing. However you can still manually add properties that will make it possible for mobile and hybrid application testing. 

To set up custom profiles for mobile and hybrid app testing, go to **Projects > Settings > Desired Capabilities > Custom**.

<img src="url" width="70%" alt="a">

You can access and add capabilities to your profile. You will need to add specific capabilities that follow [Sauce Labs's official document on mobile/hybrid application testing](https://wiki.saucelabs.com/display/DOCS/Examples+of+Test+Configuration+Options+for+Mobile+Native+Application+Tests).
