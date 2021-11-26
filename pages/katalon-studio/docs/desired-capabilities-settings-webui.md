---
title: "Introduction to Desired Capabilities" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/desired-capabilities-settings-webui.html 
redirect_from:
description:
---





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