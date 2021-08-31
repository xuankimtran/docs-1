---
title: "Capture elements in Android Hybrid apps?"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/capture-elements-in-hybrid-apps.html
redirect_from:
description:
---
<INTRODUCTION>

Katalon Studio partially supports Hybrid Mobile App. You can use Mobile keywords to automate your app but Katalon’s Mobile Spy/Recorder doesn’t support to detect elements at this moment. Hence, this turtorial shows you how to use Appium with built-in hybrid support via Chromedriver, that allows the automation of any Chrome-backed [Android web views](https://developer.android.com/reference/android/webkit/WebView).

1. [Download](http://appium.io/docs/en/writing-running-appium/web/chromedriver/#chromedriverchrome-compatibility) ChromeDriver for Appium. It is advisible to download the compatible version with Chrome on your testing devices.

2. To specify Chromedriver version at runtime, open Appium ChromeDriver in **Command Prompt** (for Windows)/ **Terminal** (for macOS), along with the full path to the downloaded Chromedriver from Step 1:

```groovy

appium --chromedriver-executable "path_to_my_chromedriver"

```

Example:

```groovy

appium --chromedriver-executable "/Users/yen.nguyen/Downloads/node_modules/appium/node_modules/appium-chromedriver"

```

3. After starting Chromedriver for Appium at server level, you need to specify Chromeversion in session capabilities by using [Mobile Testing function in Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html#mobile-testing). Go to **Project > Settings > Desired Capabilities > Mobile > Android** and add this property:
**chromedriverExecutable** : Support specifying Chromedriver version in session capabilities.
**path_to_my_chromedriver**: full path to the downloaded Chromversion from Step 1.

Example:

   <img src="url" width="70%" alt="Set up Android in Desired Capabilities">


4. Start Katalon Studio Mobile [Spy](https://docs.katalon.com/katalon-studio/docs/spy-mobile-utility.html) or [Record](https://docs.katalon.com/katalon-studio/docs/record-mobile-utility.html), and wait for the AUT to start.

5. By default, Katalon Studio starts in the [NATIVE_APP](http://appium.io/docs/en/writing-running-appium/web/hybrid/) mode. Navigate to a portion of your app where a web view is active. Click **Save Script**

6. To automate under the `Webview` context, do as follow:
In the mobile test you have just saved at Step 5

-  Switch to the Script tab.
-  Set the WebView context by using [switchToWebView](https://docs.katalon.com/katalon-studio/docs/mobile-switch-to-web-view.html#example).
-  Continue writing your script to run in Webview context.
  
```groovy
//to set context to WebView
Mobile.switchToWebView()

DriverFactory.changeWebDriver(MobileDriverFactory.getDriver())

TestObject cdmDetails = new TestObject()
cdmDetails.addProperty("id", ConditionType.EQUALS, "119")
WebUI.setText(cdmDetails, "123")

```
<img src="url" width="70%" alt="Chrome inspecting mode after switching webview">

7. To stop automating in the web view context and go back to automating the native portion of the app by using [switchToNative](https://docs.katalon.com/katalon-studio/docs/mobile-switch-to-native.html)

```groovy

//to switch back to the native mode.
Mobile.switchToNative()

```
>
> **Detect Webview Elements**
>
> Android testers can use **Devtools** at [chrome://inspect/#devices](chrome://inspect/#devices) to detach the web elements from the applications. 
> For **Devtool** to discover testing Android device, set up your Android device for remote debugging. [See also](https://developer.chrome.com/docs/devtools/remote-debugging/)
> On your development machine, open Chrome browser and navigate to [chrome://inspect/#devices](chrome://inspect/#devices), this page displays the name of your connecting device and a list of debug-enabled WebViews on your device.
> Click **Inspect** to open a **Devtools** instance.
>


