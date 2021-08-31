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


6. By default, Katalon Studio starts in the [NATIVE_APP](http://appium.io/docs/en/writing-running-appium/web/hybrid/) mode. To find the objects under *WEBVIEW*, you need switch to WebView by using [switchToWebView](https://docs.katalon.com/katalon-studio/docs/mobile-switch-to-web-view.html#example).

```groovy
//to switch to WebView
Mobile.switchToWebView()

```

7. After switching to the Webview, to identify hybrid app elements, navigate to [chrome://inspect/#devices](chrome://inspect/#devices). The **chrome://inspect** page displays a list of debug-enabled WebViews on your device 

>Make you have turned on **USB debugging mode** on your testing Anrdoid devices. Go to **Setting > System > Developer Options > USD debugging > ON**


8. Click **Inspect** below the WebView you want to debug, this opens the Webview in **DevTools**, here you can inspect elements in your testing hybrid app.

<img src="url" width="70%" alt="Chrome inspecting mode after switching webview">


9. After inspecting hybrid app elements by **Devtools**, use below sample code to automate hybrid app’s elements:

```groovy

DriverFactory.changeWebDriver(MobileDriverFactory.getDriver())

TestObject cdmDetails = new TestObject()
cdmDetails.addProperty("id", ConditionType.EQUALS, "119")WebUI.setText(cdmDetails, "123")

```
<img src="url" width="70%" alt="Chrome inspecting mode after switching webview">

You can then change back to mobile keywords by using.

```groovy

//to switch back to the native mode.
Mobile.switchToNative()

```
9.  Results



