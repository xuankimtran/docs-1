---
title: "Capture elements in Android Hybrid apps?"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/capture-elements-in-hybrid-apps.html
redirect_from:
description:
---
<INTRODUCTION>

Katalon Studio partially supports Hybrid Mobile App. You can use Mobile keywords to automate your app but Katalon’s Mobile Spy/Recorder doesn’t support to detect elements at this moment. Hence, this turtorial shows you how to use Appium with built-in hybrid support via Chromedriver, that allows the automation of any Chrome-backed [Android web views](https://developer.android.com/reference/android/webkit/WebView).

> **Requirements**
>
> - Make sure to enable WebView debugging in your native Android app set the [setWebContentsDebuggingEnabled](https://developer.android.com/reference/android/webkit/WebView#setWebContentsDebuggingEnabled(boolean)) property on the android.webkit.WebView element to `true`. See also [Automating hybrid Android apps](https://developer.chrome.com/docs/devtools/remote-debugging/webviews/)
> 

1. [Download](http://appium.io/docs/en/writing-running-appium/web/chromedriver/#chromedriverchrome-compatibility) ChromeDriver for Appium. It is advisible to download the compatible version with Chrome on your testing devices.

2. After starting Chromedriver for Appium at server level, you need to specify Chromeversion in session capabilities by using [Mobile Testing function in Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html#mobile-testing). Go to **Project > Settings > Desired Capabilities > Mobile > Android** and add this property:

**chromedriverExecutable** : Support specifying Chromedriver version in session capabilities.

**path_to_my_chromedriver**: full path to the downloaded Chromversion from Step 1.

Example:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/path-to-chrome-driver-executable.png" width="70%" alt="Set up Android in Desired Capabilities">


3. Start Katalon Studio Mobile [Spy](https://docs.katalon.com/katalon-studio/docs/spy-mobile-utility.html) or [Record](https://docs.katalon.com/katalon-studio/docs/record-mobile-utility.html), and wait for the AUT to start. By default, Katalon Studio starts in the [NATIVE_APP](http://appium.io/docs/en/writing-running-appium/web/hybrid/) mode. Navigate to a portion of your app where a web view is active.
   
4. Next, open Chrome and navigate to this URL: [chrome://inspect/#devices](chrome://inspect/#devices).
The **chrome://inspect** page displays the name of your connecting device and a list of debug-enabled WebViews on your device. After Step 3, you should see your Android app url appears in this page.
Click **Inspect** to open a **Devtools** instance. Use **Devtools** to inspect web view elements.

<img src="url" width="70%" alt="Debug-enabled Webviews in Devtools">


5. Switch bach to Katalon Studio Mobile Spy/Record, click **Save Script**, Katalon automatically generates a new Test case saved to your project.

6. To automate under the `Webview` context, do as follow:

In the mobile test you saved at Step 5

-  Switch to the Script tab.
-  Set to the `WebView` context by using [switchToWebView](https://docs.katalon.com/katalon-studio/docs/mobile-switch-to-web-view.html#example) mobile keywords.
-  Continue writing your script to run in `Webview` context.
  
```groovy
//to set context to WebView
Mobile.switchToWebView()

DriverFactory.changeWebDriver(MobileDriverFactory.getDriver())

TestObject cdmDetails = new TestObject()
cdmDetails.addProperty("id", ConditionType.EQUALS, "119")
WebUI.setText(cdmDetails, "123")

```

7. To stop automating in the web view context and go back to automating the native portion of the app by using [switchToNative](https://docs.katalon.com/katalon-studio/docs/mobile-switch-to-native.html)

```groovy

//to switch back to the native mode.
Mobile.switchToNative()

```

