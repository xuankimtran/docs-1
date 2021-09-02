---
title: "Capture elements in hybrid Android apps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/capture-elements-in-hybrid-android-apps.html
redirect_from:
description:
---
<INTRODUCTION>

Katalon Studio partially supports Hybrid Mobile App. You can use Mobile keywords to automate your app but Katalon’s Mobile Spy/Recorder doesn’t support to detect elements at this moment. Hence, this turtorial shows you how to capture elements in hybrid Android apps with Appium and Chrome Devtools under the control of [Android WebView](https://developer.android.com/reference/android/webkit/WebView).

> Requirements
>
> - Make sure to enable WebView debugging in your native Android app by setting the `setWebContentsDebuggingEnabled` property on the `android.webkit.WebView` element to `true`. See also [Automating hybrid Android apps](https://developer.chrome.com/docs/devtools/remote-debugging/webviews/)
> 

Do as follows:

1. [Download](http://appium.io/docs/en/writing-running-appium/web/chromedriver/#chromedriverchrome-compatibility) ChromeDriver for Appium. It is advisible to download the compatible version with Chrome on your testing devices.

2. Specify Chromedriver version in session capabilities by using **Mobile Testing** function in **Desired Capabilities**. Go to **Project > Settings > Desired Capabilities > Mobile > Android** and add this property:

**chromedriverExecutable** : Support specifying Chromedriver version in session capabilities.

**path_to_my_chromedriver**: full path to the downloaded Chromedriver version from Step 1.

Example:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/path-to-chrome-driver-executable.png" width="70%" alt="Set up Android in Desired Capabilities">


3. From the main toolbar, click on the **Mobile Spy** or **Mobile Record**, and select **Android Devices**. 

If you wish to learn more about Katalon Mobile Spy or Katalon Mobile Record, see also examples at:
- [Tutorials for Mobile Spy](https://docs.katalon.com/katalon-studio/docs/spy-mobile-utility.html) 
- [Tutorials for Mobile Record](https://docs.katalon.com/katalon-studio/docs/record-mobile-utility.html)

<img src="url" width="70%" alt="Open Mobile Spy/Record">

1. In the pop-up **Mobile Spy/ Mobile Recorder** dialog, specify the information at **Configuration** section, then click **Start**.
   
<img src="url" width="70%" alt="Start Mobile Spy/Record">

5. By default, Katalon Studio Spy/Rrecord starts the application under test (AUT) in the `NATIVE_APP` mode. Navigate to a portion of your app where a `WEBVIEW` is active.


6. Next, open Chrome Broswers and navigate to [chrome://inspect/#devices](chrome://inspect/#devices).
The **chrome://inspect** page displays the name of your testing device and a list of debug-enabled WebViews on your device. After Step 5, you should see the URL of AUT under the name of your testing device.

<img src="url" width="70%" alt="Chrome Inspect displays">


Click **Inspect** to open a **Devtools** instance. Use **Devtools** to inspect WebView elements.

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

