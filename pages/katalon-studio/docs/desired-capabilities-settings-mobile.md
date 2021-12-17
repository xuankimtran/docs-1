---
title: "Set up desired capabilities in mobile testing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/desired-capabilities-settings-mobile.html 
redirect_from:
description:
---

Desired capabilities can be useful when a user, for example, wants to run mobile tests with a preferred platform, browser, or app orientation. 
Katalon Studio uses desired capabilities to communicate with Appium server by sending a POST request.  If users configure the desired capabilities in project settings, the Appium server will start a session with predefined capabilities.

This article shows you how to configure some common capabilities in Mobile testing and where they are saved.
## Set desired capabilities for mobile testing in Katalon Studio 

To set desired capabilities for mobile testing, do as follows:

1. Go to **Project > Settings > Desired Capabilities > Mobile > Android/iOS**. You can add, delete or clear (delete all) capabilities.

2. Choose which device will apply the desired capabilities settings. Click **Android/iOS**, then select from the **Device Name** dropdown list. 

    > When clicking on **Android**, Katalon Studio will detect and ask you to install **Android SDK** automatically if your current machine does not have it.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/image2016-11-1-133A593A38.png" width="100%" alt="Choose device name">


3. Click **Add** on the command toolbar. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-3.png" width="100%" alt="Add desired capabilities for mobile">

    A new row is added to the list.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-4.png" width="100%" alt="Add desired capabilities for mobile">

4. Provide the **Name**, **Type** and **Value** of the property that you wish to configure.

      > * Desired capabilities is a JSON object (having keys and values pair). We need to set the capability **Name** as `key` and the capability **Value** as `value`. 
      > * The capabilities keys are case-sensitive.

## Example uses
### Example 1: enable Unicode input

The following example shows the desired capabilities settings for Android to enable Unicode input.
After choosing the device name, click **Add**, then input the following values:

   <table>
   <thead>
   <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Value</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>unicodeKeyboard</td>
      <td>boolean</td>
      <td>true</td>
   </tr>
   </tbody>
   </table>

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-5.png" width="100%" alt="Set Unicodekeyboard for Android">


### Example 2: start the device in a certain orientation

The following example shows the desired capabilities settings for Android to start the device in the portrait orientation.
After choosing the device name, click **Add**, then input the following values:

   <table>
   <thead>
   <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Value</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>orientation</td>
      <td>string</td>
      <td>PORTRAIT</td>
   </tr>
   </tbody>
   </table>

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-6.png" width="100%" alt="Enable device orientation">


### Example 3: set screenshot save directory

The following example shows the desired capabilities settings for Android to set the screenshot save directory.
After choosing the device name, click **Add**, then input the following values:

   <table>
   <thead>
   <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Value</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>androidScreenshotPath</td>
      <td>string</td>
      <td>&lt;screenshot-path&gt; (For example: /sdcard/screenshots/)</td>
   </tr>
   </tbody>
   </table>

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-7.png" width="100%" alt="Enable screenshot path">

## Location of desired capabilities files

You can find the settings files for each environment in the `<your test project location>\settings\internal` folder. The files for each driver are named as follows:

| Driver | Settings' file |
| --- | --- |
| Android | com.kms.katalon.core.mobile.android.properties |
| iOS | com.kms.katalon.core.mobile.ios.properties |