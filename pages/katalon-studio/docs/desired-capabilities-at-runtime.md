---
title: "Pass Desired Capabilities at Runtime" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/desired-capabilities-at-runtime.html 
redirect_from:
description:
---





## Passing Desired Capabilities at Runtime

Desired capabilities added to project settings apply at a global level.
Configuring desired capabilities programmatically helps you scope down the application in a specific test case.

Use the sample code below to pass desired capabilities to a specific test script, which also overrides the desired capabilities predefined in project settings.

```groovy
import com.kms.katalon.core.configuration.RunConfiguration
RunConfiguration.setWebDriverPreferencesProperty(“key”, “value”)
```

### Example 1

The example below shows how to pass the desired capability to a test case. The desired capability is window-sized 100x100.

1. Open the test case in Script mode.

2. Use the sample code but change the `key, value` into `window-size=100,100`.

```groovy
import com.kms.katalon.core.configuration.RunConfiguration
RunConfiguration.setWebDriverPreferencesProperty("args", ["window-size=100,100"])
```

3. Continue writing the script, then run the test in browser.

   ![run-chrome](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/pass-dynamically-4.png)

> Make sure the browser is updated by clicking **Tools** > **Update WebDrivers** > Choose browser. 

   ![test-pass](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/pass-dynamically-5.png)

The test passes successfully with window-size 100x100.

### Example 2

Suppose you want to override desired capabilities of a browser before it's started. In that case, you need to define the value in the project settings first, then refer to the sample code to override that value.

The example below shows how to override Chrome window-sized 1200x600 and run the test in Chrome window-sized 100x100 instead.

1. Click **Project** > **Settings** > **Desired Capabilities** > **Web UI** > **Chrome**.

   ![project-settings](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/override-crop0.png)

2. Insert `window-size=1200,600` value > **Apply and Close**.

   ![insert-value](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/override-crop2.png)

3. Open the test case in Script mode, use the sample code above but change the `key, value` into `window-size=100,100`. Run the test in Chrome browser.

   ![override-script](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/override-crop4.png)

   ![override-demo](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/override-crop5-highlighted.png)

The test passes successfully with Chrome window-size 100x100 (overriding Chrome window-size 1200x600).

> If you run the test in a different browser (not Chrome), the test passes without overriding desired capabilities predefined in project settings (see Example 1).

**References:**

* [RunConfiguration](https://docs.katalon.com/javadoc/com/kms/katalon/core/configuration/RunConfiguration.html)

## Location of Desired Capabilities files

Defined configuration settings are saved in separated files under the "**<your test project location>\\settings\\internal**" location (or "**<your test project location>\\settings\\external\\execution**" in case of custom execution), as below:

| Driver | Settings' file |
| --- | --- |
| Chrome | com.kms.katalon.core.webui.chrome.properties |
| Firefox | com.kms.katalon.core.webui.firefox.properties |
| Chrome (Headless)| com.kms.katalon.core.webui.chrome (headless).properties |
| Firefox (Headless) | com.kms.katalon.core.webui.firefox (headless).properties |
| IE | com.kms.katalon.core.webui.ie.properties |
| Safari | com.kms.katalon.core.webui.safari.properties |
| Edge | com.kms.katalon.core.webui.edge.properties |
| Edge (Chromium)| com.kms.katalon.core.webui.edge chromium.properties |
| Remote Web | com.kms.katalon.core.webui.remote.properties |
| Android | com.kms.katalon.core.mobile.android.properties |
| iOS | com.kms.katalon.core.mobile.ios.properties |