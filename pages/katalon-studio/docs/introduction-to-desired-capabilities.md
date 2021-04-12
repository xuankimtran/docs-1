---
title: "Desired Capabilities" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/introduction-to-desired-capabilities.html 
redirect_from:
    - "/display/KD/Introduction+to+Desired+Capabilities/"
    - "/display/KD/Introduction%20to%20Desired%20Capabilities/"
    - "/x/ywbR/"
    - "/katalon-studio/docs/introduction-to-desired-capabilities/"
    - "/display/KD/Remote+Desired+Capabilities/"
    - "/display/KD/Remote%20Desired%20Capabilities/"
    - "/x/KAzR/"
    - "/katalon-studio/docs/remote-desired-capabilities/"
    - "/katalon-studio/docs/remote-desired-capabilities.html"
    - "/katalon-studio/docs/windows-desired-capabilities.html"
    - "/x/SgzR/"
    - "/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/"
    - "/katalon-studio/docs/desired-capabilities-for-chromechrome-headless.html"
    - "/x/TAzR/"
    - "/katalon-studio/docs/desired-capabilities-for-firefoxfirefox-headless/"
    - "/katalon-studio/docs/desired-capabilities-for-firefoxfirefox-headless.html"
    - "/display/KD/Desired+Capabilities+for+Internet+Explorer/"
    - "/display/KD/Desired%20Capabilities%20for%20Internet%20Explorer/"
    - "/x/TgzR/"
    - "/katalon-studio/docs/desired-capabilities-for-internet-explorer/"
    - "/katalon-studio/docs/desired-capabilities-for-internet-explorer.html"
    - "/katalon-studio/tutorials/desired_capabilities_in_katalon.html"
    - "/katalon-studio/docs/desired_capabilities_in_katalon.html"
    - "/display/KD/Override+desired+capabilities+at+runtime/"
    - "/display/KD/Override%20desired%20capabilities%20at%20runtime/"
    - "/x/dwXR/"
    - "/katalon-studio/docs/override-desired-capabilities-at-runtime/"
    - "/katalon-studio/docs/override-desired-capabilities-at-runtime.html"
description:
---

**Desired Capabilities** are key/value pairs that tell the browser properties such as browser name, browser version, and the path of the browser driver in the system to determine the browsers' behaviors at runtime. Desired capabilities which can be used to configure such additional driver instances as FirefoxDriver, ChromeDriver, InternetExplorerDriver, Selenium WebDriver are useful in the following cases:

* Setting the browser and device properties in mobile testing
* Adding extra settings to browsers in web testing

Katalon Studio allows you to define these Desired Capabilities in Project Settings. You need to identify which environment you want to customize its behaviors before defining desired capabilities in a Katalon project. After selecting the environment, you can manage its desired capabilities with:

* **Add**: to add a new row to the **Desired Capabilities** list.
  * Provide the name of the property that you'd like to configure and its type.
  * Define value for the property. Refer to [Value Types](/display/KD/Value+Types) for details regarding how to input value for different types.
* **Delete**: to delete selected records.
* **Clear**: to clear all existing records.

Below is the list of supported environments as well as how to configure them in project settings:

## Web Testing

* Define Desired Capabilities for local execution using Chrome, Firefox, IE, Safari, Edge or Edge (Chromium).
* **Project > Settings > Desired Capabilities > WebUI > Chrome/Firefox/IE/Safari/Edge/Edge(Chromium)**.

### Chrome/Chrome (headless)

The Desired Capabilities available for Chrome is listed [here](http://chromedriver.chromium.org/capabilities). You can locate Chrome settings file at this path: **<Project_folder>\\settings\\internal\\com.kms.katalon.core.webui.chrome.properties.**

Please refer to some common examples below regard to how to manage Desired Capabilities for Chrome in Katalon Studio:

1. To start Chrome maximized by default: [`--start-maximized`](https://peter.sh/experiments/chromium-command-line-switches/#start-maximized)

   ```groovy
   {"CHROME_DRIVER":{"args":["--start-maximized"]}}

   ```

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/Screen-Shot-2018-07-17-at-16.38.57.png)

2. To disable notification bars : [`--disable-infobars`](https://peter.sh/experiments/chromium-command-line-switches/#disable-infobars)

   ```groovy
   {"CHROME_DRIVER":{"args":["--start-maximized","--disable-infobars"]}}
   ```

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/Screen-Shot-2018-07-17-at-17.03.42.png)

3. To start Chrome in incognito (private) mode : [`--incognito`](https://peter.sh/experiments/chromium-command-line-switches/#incognito)

   ```groovy
   {"CHROME_DRIVER":{"args":["--start-maximized","--disable-infobars","--incognito"]}}

   ```

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/Screen-Shot-2018-07-18-at-10.06.27.png)

> Code sample can be found in this project: [https://github.com/katalon-studio-samples/tips-and-tricks](https://github.com/katalon-studio-samples/tips-and-tricks)

### Firefox/Firefox (headless)

You can locate Firefox settings file at this path: **_<Project_folder>\\settings\\internal\\com.kms.katalon.core.webui.firefox.properties._**

You can access the useful Desired Capabilities for Firefox through:

1. Open Firefox browser
2. On the address bar type in 'about:config'
3. Search for 'browser' keys
4. Create a key called 'firefox_profile' in Katalon Studio settings and add your settings there.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-firefoxfirefox-headless/Untitled.png)

Some common Desired Capabilities:

1. Start Firefox at default page: browser.startup.homepage

    ```groovy
    {"FIREFOX_DRIVER":{"firefox_profile":{"browser.startup.homepage":"www.google.com"}}}
    ```

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-firefoxfirefox-headless/Untitled2.png)

2. Never ask for file download for file MIME type mentioned. The list of MIME type can be found [here](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types/Complete_list_of_MIME_types).

   ```groovy
   {"FIREFOX_DRIVER":{"firefox_profile":{"browser.download.folderList":"2","browser.helperApps.alwaysAsk.force":false,"browser.download.manager.showWhenStarting":false,"browser.download.dir":"C:\\Downloads","browser.download.downloadDir":"C:\\Downloads","browser.download.defaultFolder":"C:\\Downloads","browser.helperApps.neverAsk.saveToDisk":"text/html"}}}
   ```

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-firefoxfirefox-headless/Untitled.png)

> Code sample can be found in this project: [https://github.com/katalon-studio-samples/tips-and-tricks](https://github.com/katalon-studio-samples/tips-and-tricks)

### Internet Explorer

Internet Explorer driver supports some important capabilities which can be used to smooth execution of test on Internet Explorer. Some of these capabilities help us to disable JavaScripts, ignore the security domain setting for IE, persistent hovering, require window focus etc. These capabilities ease the way the for automation testing using Selenium Web Driver on Internet Explorer. More details on the Internet Explorer can be found [here](https://code.google.com/p/selenium/wiki/DesiredCapabilities#IE_specific).

The most common use of Internet Explorer desired capabilities is to configure Internet Explorer without having to complete the instructions from this [page](/display/KD/Internet+Explorer+Configurations). You can pass some desired capabilities to Internet Explorer so you don't need to configure your IE anymore.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-internet-explorer/IE.png)

* **ignoreProtectedModeSettings** determines whether to  skip the protected mode check. If set, tests may become flaky or unresponsive, and browsers may hang. If not set, and protected mode settings are not the same for all zones, an exception will be thrown on driver construction. Only "best effort" support is provided when using this capability.
* **ignoreZoomSetting** indicates whether to skip checking that the browser's zoom level is set to 100%. Value is set to false by default.
* **enablePersistentHover** determines whether persistent hovering is enabled (true by default). Persistent hovering is achieved by continuously firing mouse over events at the last location the mouse cursor has been moved to.
* **requireWindowFocus** determines whether to require the IE window to focus before performing any user interaction operations (mouse or keyboard events). This capability is false by default but delivers much more accurate native events interactions.

> Code sample can be found in this project: [https://github.com/katalon-studio-samples/tips-and-tricks](https://github.com/katalon-studio-samples/tips-and-tricks)

## Mobile Testing

Through using Desired Capabilities, we can communicate with Appium server by sending a POST request. For example, a user would like to run mobile test with a preferred platform, browser, orientation of the app, etc. If the user has already set the desired capability preferences setting, Appium server will start a session with the capabilities that user has set initially.

Desired capabilities is a JSON object (having keys and values pair). Within each desired capability, there are few inbuilt capabilities. We need to set the capability **name** as '**key**' and **capability** value as '**value**'. The capabilities keys are **case-sensitive**.

* **Project > Settings > Desired Capabilities > Mobile > Android/iOS**.

After clicking on Android, it will display a screen with a dropdown with **Device Name** and **Add**, **Delete**, **Clear** buttons. Steps to **add** a property for execution are as following:

You need to select the device when configuring Desired Capabilities.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/image2016-11-1-133A593A38.png)

Where:

* **Device Name**: the device to apply Desired Capabilities settings on.

Click **Add** button of command toolbar above the **Desired Capabilities** list.

![Desired Capabilities for Mobile](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-3.png)

A new row will be added to the list.

![Desired Capabilities for Mobile](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-4.png)

Provide the name of the property that you'd like to configure, do the same for **Type** and **Value**.

### Example 1

The example below shows the desired capabilities settings for Android to enable Unicode input.

![Desired Capabilities for Mobile](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-5.png)

### Example 2

The example below shows the desired capabilities settings for Android to enable device orientation.

![Desired Capabilities for Mobile](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-6.png)

### Example 3

The example below shows the desired capabilities settings for Android to enable screenshot path.

![Design Capabilities for Mobile](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/desired_capabilities_in_katalon/Design-Capabilities-for-Mobile-in-Katalon-Studio-7.png)

The source code is available [here](https://github.com/katalon-studio/katalon-mobile-automation). For further instructions and help, please refer to [Execution Settings](/display/KD/Execution+Settings) guideline and join us on [Katalon Forum](http://forum.katalon.com/).

## Windows Desktop App Testing

* Define Desired Capabilities for execution on WinAppDriver of desktop applications testing.
* **Project > Settings > Desired Capabilities > Windows**.

> Change updates
>
> From **version 7.0 onwards**, Windows desktop application testing is available.
>
> From **version 7.5 onwards**, Native Windows Recorder is available for Katalon Studio Enterprise users.
> 
> From **version 7.7 onwards**, Desired Capabilities for Native Windows Recorder are available.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/windows-desired-capabilities/desired-capa-win.png"  width="796" height="600">

These settings are applied to a test execution on a Windows desktop app. You are allowed to configure the WinAppDriver URL and Desired Capabilities for Windows to start a Windows Application Driver.

* **WinAppDriver URL**: a URL to the WinAppDriver server. By default, Katalon Studio is set to http://127.0.0.1:4723.
* **Desired Capabilities**: Katalon Studio supports the same [capabilities](https://github.com/microsoft/WinAppDriver/blob/master/Docs/AuthoringTestScripts.md#user-content-supported-locators-to-find-ui-elements) as WinAppDriver does. For Native Windows Recorder, only **appArguments** and **appWorkingDir** are supported (available in version 7.7).
   * **appArguments**: Support passing arguments to the Application Under Test
   * **appWorkingDir**: Support overriding the Application Under Test's working directory  

The example below shows you:

* The desired capabilities set for a Windows Application Under Test;

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/desired-capabilities.png">

* How to use them in the Native Windows Recorder.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/use-windows-capabilities.png">

## Remote Server

* Define Desired Capabilities for execution on a remote web server.
* **Project > Settings > Desired Capabilities > Remote**.

There will be cases you need to connect and execute your tests on remote environments such as Selenium Grid and Katalium Server or cloud services such as Kobiton, SauceLabs or BrowserStacks. Katalon Studio does support this remote execution.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/remote-desired-capabilities/Remote-desired-capabilities.png)

Please refer to some documents below as examples how to pass in desired capabilities from these providers:

1. [Kobiton](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-for-kobiton-devices.html)
2. [SauceLabs](/display/KD/SauceLabs+Integration)
3. [BrowserStack](/display/KD/BrowserStack+Integration)
4. [Katalium Server](https://docs.katalon.com/katalium-server/docs/katalium-server-katalon-studio-remote-machine.html)

Note that this Remote option is applied for all executions which support this kind of remote execution, so you can apply them in this option as well.

> Code sample can be found in this project: [https://github.com/katalon-studio-samples/tips-and-tricks](https://github.com/katalon-studio-samples/tips-and-tricks)

Starting with **Katalon Studio version 6.3.0**, when Appium is set as `Remote server type`,  the **Appium Driver** option is available for you to choose between *Android Driver* and *iOS Driver*.
Then this selection is used for launching the correct Appium Driver to connect to Cloud Devices.

## Custom Desired Capabilities

* Define a custom option for execution.
* **Project > Settings > Desired Capabilities > Custom**.

> If you want to make a list of your own custom Desired Capabilities for some environments, then it's suggested to use '**Custom**' settings in this case.

Custom execution is slightly different from other execution settings. Follow these steps to create a custom execution with its desired capabilities:

1. Click **Add** on the command toolbar to add a custom execution to the custom execution list.
2. Change the name if needed, then click on the **More** icon under the **Value** column.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/image2016-11-1-143A263A29.png)
3. In the **Custom Execution Configuration Builder** dialog, specify the **Driver Name** for your custom execution.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/image2016-11-1-143A293A6.png)

    > You can have at most one web driver and one mobile driver here since there may be a potential conflict if you use multiple web or mobile drivers in the same test execution.
4. Click on the **More** icon under the **Preferences** column.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/image2016-11-1-143A303A6.png)
5. The **Driver Builder** dialog is displayed for you to set desired capabilities for the selected Driver. The steps to add new Desired Capabilities here is similar to other settings above. Click **OK** when you finish.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/image2016-11-1-143A353A10.png)

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

## Override desired capabilities at runtime

If you want to override desired capabilities of a browser before it's started, refer to the sample code below.

```groovy
import com.kms.katalon.core.configuration.RunConfiguration
RunConfiguration.setWebDriverPreferencesProperty("key", "value")
```

**See also:**

* [Run Configuration](https://api-docs.katalon.com/com/kms/katalon/core/configuration/RunConfiguration.html)
* [Import/Export Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/import-export-desired-capabilities.html)