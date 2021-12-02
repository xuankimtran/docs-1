---
title: "Set up Desired Capabilities in Mobile Testing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/desired-capabilities-settings-mobile.html 
redirect_from:
description:
---

Desired capabilities can be useful when a user, for example, wants to run mobile tests with a preferred platform, browser, orientation of the app. 
Katalon Studio uses desired capabilities to communicate with Appium server by sending a POST request.  If users configure the desired capabilities in project settings, Appium server will start a session with predefined capabilities.

Desired capabilities is a JSON object (having keys and values pair). We need to set the capability **Name** as `key` and the capability **Value** as `value`. The capabilities keys are case-sensitive.

This article shows you how to configure some common capabilities in Mobile testing and the location of desired capabilities files.
## Set desired capabilities for Mobile testing in Katalon Studio 

To set desired capabilities for mobile testing, do as follows:

1. Go to **Project > Settings > Desired Capabilities > Mobile > Android/iOS**. You can add, delete or clear (delete all) capabilities.

2. After clicking on **Android/iOS**, choose the device to apply desired capabilities settings from the **Device Name** dropdown list. 

    > When clicking on **Android**, Katalon Studio will detect and ask you to install **Android SDK** automatically if your current machine does not have it.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/image2016-11-1-133A593A38.png" width="100%" alt="Choose device name">


3. Click **Add** on the command toolbar. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-3.png" width="100%" alt="Add Desired Capabilities for Mobile">

    A new row is added to the list.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-4.png" width="100%" alt="Add Desired Capabilities for Mobile">

4. Provide the name of the property, type and value that you'd like to configure, do the same for **Type** and **Value**.

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

You can find the settings files for each environment in the `<your test project location>\settings\internal` folder. The files for each driver are named as follows:

| Driver | Settings' file |
| --- | --- |
| Android | com.kms.katalon.core.mobile.android.properties |
| iOS | com.kms.katalon.core.mobile.ios.properties |