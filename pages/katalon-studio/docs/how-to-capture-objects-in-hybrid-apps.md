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



3. Start Appium ChromeDriver in Terminal (for macOS)/Command Prompt (for Windows):

```groovy

appium --chromedriver-executable "path_to_my_chromedriver"```

Example:

```groovy

appium --chromedriver-executable "/Users/demokatalon/Downloads/Mobile\ testing/chromedriver"

```

4. Start Katalon Studio Mobile [Spy](https://docs.katalon.com/katalon-studio/docs/spy-mobile-utility.html) or [Record](https://docs.katalon.com/katalon-studio/docs/record-mobile-utility.html), and wait for the AUT to start.

5. Open Chrome and navigate to this URL: [chrome://inspect/#devices](chrome://inspect/#devices). The devices will be listed here, click on the [inspect link](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/?utm_source=dcc&utm_medium=redirect&utm_campaign=2016q3) to start Chrome inspecting mode.

6. By default, Katalon Studio starts in the [NATIVE_APP](http://appium.io/docs/en/writing-running-appium/web/hybrid/) mode. To find the objects under *WEBVIEW*, you need switch to WebView by using [switchToWebView](https://api-docs.katalon.com/com/kms/katalon/core/mobile/keyword/MobileBuiltInKeywords.html#switchToWebView()).

Example:

```groovyMobile.switchToWebView()

DriverFactory.changeWebDriver(MobileDriverFactory.getDriver())

TestObject cdmDetails = new TestObject()cdmDetails.addProperty("id", ConditionType.EQUALS, "119")WebUI.setText(cdmDetails, "123")

Mobile.switchToNative()```

To use mobile keyword again, use `Mobile.switchToNative()` to switch back to the native mode.