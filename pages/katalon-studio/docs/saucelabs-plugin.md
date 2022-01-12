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

Click **Generate Sauce Labs Custom Profile** to finalize your profile. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/saucelabs-plugin/KS-SAUCELABS-Enable-saucelabs-integration.png" width="70%" alt="Enable Sauce Labs integration">

> Notes: 
> * The default custom profile is named `saucelabs_default`. 
> * To be recognized as a Sauce Labs profile, all custom profiles must have the following syntax: `saucelabs_<your-custom-profile-name>`.

You can also view and edit your profile in **Projects > Settings > Desired Capabilities > Custom**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/saucelabs-plugin/KS-SAUCELABS-View-custom-saucelabs-profiles.png" width="70%" alt="View Sauce Labs custom profile">

You can now use the newly created profile to execute tests.
### Execute a test case with Sauce Labs profiles

To execute a test case with Sauce Labs profiles, do as follows:

1. Open a test case.

2. Click the dropdown list next to **Run**.

3. Select **Custom capabilities**.

4. Select your Sauce Labs profile.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/saucelabs-plugin/KS-SAUCELABS-Execute-test-case-saucelabs-profile.png" width="100%" alt="Execute Sauce Labs custom profile in a test case">

### Execute a test suite with Sauce Labs profiles

To execute a test suite with Sauce Labs profiles, do as follows:

1. Open a test suite.

2. Add the test cases you want to execute into the test suite.

3. Click the dropdown list next to **Run**.

4. Select **Custom capabilities**.

5. Select your Sauce Labs profile.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/saucelabs-plugin/KS-SAUCELABS-Execute-test-suite-saucelabs-profile.png" width="100%" alt="Execute Sauce Labs custom profile in a test suite">

### Execute a test suite collection with Sauce Labs profiles

To execute a test suite collection with Sauce Labs profiles, do as follows:

1. Open a test suite collection.

2. Add the test suites you want to execute into the test suite collection. 

3. Double-click on the cell under the **Run with** column. A **Select an environment** dialog opens.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/saucelabs-plugin/KS-SAUCELABS-Select-environment-test-suite-collection.png" width="60%" alt="Choose Sauce Labs custom profile in a test suite collection">

4. Select your Sauce Labs profile.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/saucelabs-plugin/KS-SAUCELABS-Select-environment-TSC.gif" width="100%" alt="Choose Sauce Labs custom profile in a test suite collection">

5. Click **OK**. Then click **Execute**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/saucelabs-plugin/KS-SAUCELABS-Execute-test-suite-collection-saucelabs-profile.png" width="100%" alt="Execute Sauce Labs custom profile in a test suite collection">

### View test execution results on Sauce Labs

To view Katalon test execution results on Sauce Labs, on the Sauce Labs Dashboard, switch to the Automated Tests tab. 

You can see the test results are displayed as follows: 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/saucelabs-plugin/7-result.png" width="100%" alt="View test execution results in Sauce Labs">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/saucelabs-plugin/6-result.png" width="100%" alt="View test execution results in Sauce Labs">

## Sauce Labs for Mobile testing and Hybrid application testing

The plug-in provides you with an intuitive user interface to create Sauce Labs custom profiles for Web Testing. However you can still manually add properties that will make it possible for mobile and hybrid application testing. 

To set up custom profiles for mobile and hybrid app testing, go to **Projects > Settings > Desired Capabilities > Custom**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/saucelabs-plugin/KS-SAUCELABS-Add-saucelabs-profile-mobile-testing.png" width="70%" alt="Add custom profile for mobile testing">

Then add capabilities to enable mobile and hybrid app testing in Sauce Labs. You can follow the Sauce Labs official document here: [Appium Testing with Real Devices](https://docs.saucelabs.com/mobile-apps/automated-testing/appium/real-devices/).
