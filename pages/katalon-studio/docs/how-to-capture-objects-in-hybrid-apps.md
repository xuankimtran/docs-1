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

1. [Download and install](http://appium.io/docs/en/writing-running-appium/web/chromedriver/#chromedriverchrome-compatibility) ChromeDriver for Appium. It is advisible to download the compatible version with Chrome on your testing devices.

2. Specify Chromedriver version in session capabilities by using **Mobile Testing** function in **Desired Capabilities**. Go to **Project > Settings > Desired Capabilities > Mobile > Android** and add this property:

**chromedriverExecutable** : Support specifying Chromedriver version in session capabilities.

**path_to_my_chromedriver**: full path to the downloaded Chromedriver version from Step 1.

Example:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/set-up-android-in-Dc.png" width="70%" alt="Set up Android in Desired Capabilities">


3. Create a New Test Case. Go to **File > New > Test Case**.
4. In the blank Test Case page, from the main toolbar, click on the **Mobile Record**, and select **Android Devices**. 
To learn more about Katalon Mobile Record, see also [Tutorials for Mobile Record](https://docs.katalon.com/katalon-studio/docs/record-mobile-utility.html).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/Open-mobile-record.png" width="30%" alt="Open Mobile Record">

5. In the pop-up **Mobile Recorder** dialog, specify the information at **Configuration** section, then click **Start** to begin recording the application under test (AUT).
   
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/Start-mobile-record.png" width="50%" alt="Start Mobile Record">

6. By default, Katalon Studio Record starts the AUT in the `NATIVE_APP` context. Set to the `WEBVIEW` context by using [switchToWebView](https://docs.katalon.com/katalon-studio/docs/mobile-switch-to-web-view.html#example) mobile keywords.

In the main toolbar, click **Add > Mobile keyword** > a new command line appears > manually add `switchToWebview` mobile keyword.

```groovy
//to set context to WebView
Mobile.switchToWebView()
```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/switchToWebView-mobile-keyword.png" width="70%" alt="Add switch to Webview">

7. Click **Save Script**. An open dialog asks you to save captured objects into Object Repository of Katalon Studio. Click **OK** to save recorded actions and objects. 

8. In the new test case saved from Step 7, do as follows:
- Switch to the Script tab
- Remove command line **Close Application**. 
- Run the test script.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/results-after-recording-mobile-test.png" width="70%" alt="Results after recording mobile test">

9. Next, open Chrome Browser and navigate to [chrome://inspect/#devices](chrome://inspect/#devices).
The **chrome://inspect** page displays:
- The name of your Android testing device.
- The version of Chrome that's running on the device, with the version number in parentheses.
- A list of debug-enabled WebViews on your device. After Step 8, you should see the URL of the testing Android application here.
- Click **Inspect** to open a **Chrome Devtools** instance. Use **Chrome Devtools** to inspect WebView elements. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/chrome-inspect-displays.png" width="50%" alt="Chrome Inspect displays">


To learn more about **Chrome Devtools** and its available function. See also [Chrome Devtools](https://developer.chrome.com/docs/devtools/)

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/Debugged-enabled-webview-in-chrome-devtools.png" width="70%" alt="Debug-enabled Webviews in Devtools">


10. Switch back to Katalon Studio framework, continue writing your test script with sample code as below:
  
```groovy
//to set context to WebView
Mobile.switchToWebView()

DriverFactory.changeWebDriver(MobileDriverFactory.getDriver())

TestObject cdmDetails = new TestObject()
cdmDetails.addProperty("id", ConditionType.EQUALS, "119")
WebUI.setText(cdmDetails, "123")

```

If you wish to stop automating in the `WEBVIEW` context and go back to automate the native portion of the app, use [switchToNative](https://docs.katalon.com/katalon-studio/docs/mobile-switch-to-native.html) mobile keyword.

```groovy

//to switch back to the native mode.
Mobile.switchToNative()

```

