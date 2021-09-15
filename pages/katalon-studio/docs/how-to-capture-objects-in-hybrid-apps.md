---
title: "Capture elements in hybrid Android apps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/capture-elements-in-hybrid-android-apps.html
redirect_from:
description:
---

You can use mobile keywords to automate your app, but our Mobile Spy/Recorder utility does not detect hybrid mobile elements. This tutorial provides a solution to capture hybrid mobile elements with Appium and Chrome Devtools under the control of Android WebView. You can learn more about Android WebView functionalities from the Android developer documentation here: [WebView](https://developer.android.com/reference/android/webkit/WebView).

Do as follows:

1. Enable WebView debugging in your Android app. To enable this, set the `setWebContentsDebuggingEnabled` property on the `android.webkit.WebView` element to `true`. See also [Automating hybrid Android apps](https://developer.chrome.com/docs/devtools/remote-debugging/webviews/).
   
2. [Download and install](http://appium.io/docs/en/writing-running-appium/web/chromedriver/#chromedriverchrome-compatibility) Chromedriver for Appium. Make sure to download the compatible version with Chrome on your testing devices.

3. Specify the Chromedriver version in the session. Go to **Project > Settings > Desired Capabilities > Mobile > Android** and add this property:

**chromedriverExecutable**: Support specifying Chromedriver version in session capabilities.

**path_to_my_chromedriver**: full path to the downloaded Chromedriver version from Step 1.

Example:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/set-up-android-in-Dc.png" width="70%" alt="Set up Android in Desired Capabilities">


4. Create a New Test Case. Go to **File > New > Test Case**.
5. From the main toolbar in the blank Test Case page, click **Record Mobile** and select **Android Devices**. 
To learn more about Katalon Mobile Record, see also [Tutorials for Mobile Record](https://docs.katalon.com/katalon-studio/docs/record-mobile-utility.html).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/Open-mobile-record.png" width="30%" alt="Open Mobile Record">

6. In the pop-up **Mobile Recorder** dialog, specify the information in the **Configuration** section, then click **Start** to begin recording the application under test (AUT).
   
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/Start-mobile-record.png" width="50%" alt="Start Mobile Record">

>
> **Note**
>
> If your application begins in a WebView, and you don't want to open the AUT in the `NATIVE_APP` context, go to **Project > Settings > Desired Capabilities > Mobile > Android** to set `autoWebview` to `true` in **Desired capabilities**.
>
> With this setting, the AUT automatically enters the `WEBVIEW` context on session start. Skip **Step 6,7,8** and move to **Step 9** to continue to automate your hybrid app.
>
>

7. By default, Katalon Studio Record starts the AUT in the `NATIVE_APP` context. Set to the `WEBVIEW` context by using the [switchToWebView](https://docs.katalon.com/katalon-studio/docs/mobile-switch-to-web-view.html#example) mobile keyword.

In the main toolbar, click **Add > Mobile keyword** > a new command line appears > manually add `switchToWebview` mobile keyword.

```groovy
//to set context to WebView
Mobile.switchToWebView()
```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/add-webview-mobile-keyword.001.jpeg" width="70%" alt="Add switch to Webview">

8. Click **Save Script**. An open dialog asks you to save captured objects into the Object Repository of Katalon Studio. Click **OK** to save recorded actions and objects. 

9. In the new test case saved from step 7, do as follows:
- Switch to the Script tab.
- Remove command line **Close Application**. 
- Run the test script.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/results-after-recording-mobile-test.png" width="70%" alt="Results after recording mobile test">

10. Next, open Chrome Browser and navigate to **chrome://inspect/#devices**.
The **chrome://inspect** page displays:
- The name of your Android testing device.
- The version of Chrome that's running on the device, with the version number in parentheses.
- A list of debug-enabled WebViews on your device. After step 8, you should see the URL of the testing Android application here.
- Click **Inspect** to open a **Chrome Devtools** instance. Use **Chrome Devtools** to inspect WebView elements.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/chrome-inspect-displays-hybrid-app.png" width="50%" alt="Chrome Inspect displays">


To learn more about **Chrome Devtools** and its available function, see also [Chrome Devtools](https://developer.chrome.com/docs/devtools/).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/capture-objects-in-hybrid-apps/Chrome-Devtools.png" width="70%" alt="Debug-enabled Webviews in Devtools">


11. Return to Katalon Studio. Create and automate objects in your test with inspected elements from Step 10. To learn more about creating test objects in Webview, see also [Web Test Object](https://docs.katalon.com/katalon-studio/docs/manage-web-test-object.html#in-manual-view).
In case you are defining test objects programmatically, you can use the following sample code in the script tab of your test:
  
```groovy
// this is unnecessary if your AUT automatically enters the WEBVIEW context on session start.
Mobile.switchToWebView()
// To implement Mobile Driver Factory
DriverFactory.changeWebDriver(MobileDriverFactory.getDriver())

// to create a new test object named cdmDetails
TestObject cdmDetails = new TestObject()
// to add the object's property inspected from step 10
cdmDetails.addProperty("id", ConditionType.EQUALS, "119")
WebUI.setText(cdmDetails, "123")

```

If you wish to stop automating in the `WEBVIEW` context and go back to automate the native portion of the app, use the [switchToNative](https://docs.katalon.com/katalon-studio/docs/mobile-switch-to-native.html) mobile keyword.

```groovy

// to switch back to the native mode.
Mobile.switchToNative()

```
