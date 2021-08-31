---
title: "How to capture objects in Hybrid apps?"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/how-to-capture-objects-in-hybrid-apps.html
redirect_from:
description:
---
<INTRODUCTION>

Katalon Studio partially supports Hybrid Mobile App. You can use Mobile keywords to automate your app but Katalon’s Mobile Spy/Recorder doesn’t support to detect elements at this moment. Hence, this turtorial shows you how to use Appium with built-in hybrid support via Chromedriver, that allows the automation of any Chrome-backed [Android web views](https://developer.android.com/reference/android/webkit/WebView).

1. [Download]((http://appium.io/docs/en/writing-running-appium/web/chromedriver/#chromedriverchrome-compatibility)) ChromeDriver for Appium. It is advisible to download the compatible version with Chrome on your testing devices.

2. Go to *Project > Settings > Desired Capabilities > Mobile > Android* and add this property *chromedriverExecutable: "path_to_my_chromedriver"*.

Example:

   <img src="url" width="70%" alt="Set up Android in Desired Capabilities">


3. Start Appium ChromeDriver in Terminal (for macOS)/Command Prompt (for Windows):

```groovy

appium --chromedriver-executable "path_to_my_chromedriver"

```

Example:

```groovy

appium --chromedriver-executable "/Users/yen.nguyen/Downloads/node_modules/appium/node_modules/appium-chromedriver"

```

4. Start Katalon Studio Mobile [Spy](https://docs.katalon.com/katalon-studio/docs/spy-mobile-utility.html) or [Record](https://docs.katalon.com/katalon-studio/docs/record-mobile-utility.html), and wait for the AUT to start.

5. Open Chrome and navigate to this URL: [chrome://inspect/#devices](chrome://inspect/#devices). The devices will be listed here, 

   <img src="url" width="70%" alt="Inspection view">


6. By default, Katalon Studio starts in the [NATIVE_APP](http://appium.io/docs/en/writing-running-appium/web/hybrid/) mode. To find the objects under *WEBVIEW*, you need switch to WebView by using [switchToWebView](https://api-docs.katalon.com/com/kms/katalon/core/mobile/keyword/MobileBuiltInKeywords.html#switchToWebView()).

- Continue writing your script.

Example:

```groovy
//to switch to WebView
Mobile.switchToWebView()

DriverFactory.changeWebDriver(MobileDriverFactory.getDriver())

TestObject cdmDetails = new TestObject()
cdmDetails.addProperty("id", ConditionType.EQUALS, "119")WebUI.setText(cdmDetails, "123")

```
<img src="url" width="70%" alt="Script view after switching webview">

7. After switch to the Webview, sour hybrid app url should show in Chrome url [chrome://inspect/#devices](chrome://inspect/#devices) from Step 5. 

<img src="url" width="70%" alt="Chrome inspecting mode after switching webview">

8. After finishing capturing objects in Webview, you wish to change back to mobile key by using.

```groovy

//to switch back to the native mode.
Mobile.switchToNative()

```

<img src="url" width="70%" alt="Script view after switching to mobile key">

