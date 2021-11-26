---
title: "Set up Desired Capabilities in Mobile Testing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/desired-capabilities-settings-mobile.html 
redirect_from:
description:
---





## Mobile Testing

Through using Desired Capabilities, we can communicate with Appium server by sending a POST request. For example, a user would like to run mobile test with a preferred platform, browser, orientation of the app, etc. If the user has already set the desired capability preferences setting, Appium server will start a session with the capabilities that user has set initially.

Desired capabilities is a JSON object (having keys and values pair). Within each desired capability, there are few inbuilt capabilities. We need to set the capability **name** as '**key**' and **capability** value as '**value**'. The capabilities keys are **case-sensitive**.

* **Project > Settings > Desired Capabilities > Mobile > Android/iOS**.

After clicking on Android, it will display a screen with a dropdown with **Device Name** and **Add**, **Delete**, **Clear** buttons. Steps to **add** a property for execution are as following:

You need to select the device when configuring Desired Capabilities.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/image2016-11-1-133A593A38.png)

Where:

* **Device Name**: the device to apply Desired Capabilities settings on.

Click **Add** button of command toolbar above the **Desired Capabilities** list.

![Desired Capabilities for Mobile](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-3.png)

A new row will be added to the list.

![Desired Capabilities for Mobile](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-4.png)

Provide the name of the property that you'd like to configure, do the same for **Type** and **Value**.

### Example 1

The example below shows the desired capabilities settings for Android to enable Unicode input.

![Desired Capabilities for Mobile](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-5.png)

### Example 2

The example below shows the desired capabilities settings for Android to enable device orientation.

![Desired Capabilities for Mobile](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-6.png)

### Example 3

The example below shows the desired capabilities settings for Android to enable screenshot path.

![Design Capabilities for Mobile](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-7.png)

The source code is available [here](https://github.com/katalon-studio/katalon-mobile-automation). For further instructions and help, please refer to [Execution Settings](/display/KD/Execution+Settings) guideline and join us on [Katalon Forum](http://forum.katalon.com/).

## Location of Desired Capabilities files

Defined configuration settings are saved in separated files under the "**<your test project location>\\settings\\internal**" location (or "**<your test project location>\\settings\\external\\execution**" in case of custom execution), as below:

| Driver | Settings' file |
| --- | --- |
| Chrome | com.kms.katalon.core.webui.chrome.properties |
| Firefox | com.kms.katalon.core.webui.firefox.properties |
| Chrome (Headless)| com.kms.katalon.core.webui.chrome (headless).properties |
| Firefox (Headless) | com.kms.katalon.core.webui.firefox (headless).properties |
| IE | com.kms.katalon.core.webui.ie.properties |
| Safari | com.kms.katalon.core.webui.safari.properties |
| Edge | com.kms.katalon.core.webui.edge.properties |
| Edge (Chromium)| com.kms.katalon.core.webui.edge chromium.properties |
| Remote Web | com.kms.katalon.core.webui.remote.properties |
| Android | com.kms.katalon.core.mobile.android.properties |
| iOS | com.kms.katalon.core.mobile.ios.properties |