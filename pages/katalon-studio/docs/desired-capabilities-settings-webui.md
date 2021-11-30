---
title: "Set up Desired Capabilities in WebUI Testing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/desired-capabilities-settings-webui.html 
redirect_from:
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

description:
---

Katalon Studio allows you to define desired capabilities for local execution with Chrome, Firefox, Internet Explorer (IE), Safari, Edge or Edge (Chromium) in **Project > Settings > Desired Capabilities > WebUI > Chrome/Firefox/IE/Safari/Edge/Edge(Chromium)**.

This article shows you how to configure some common capabilities in WebUI testing and the location of desired capabilities files.

> You can find code samples in our Github project: [https://github.com/katalon-studio-samples/tips-and-tricks](https://github.com/katalon-studio-samples/tips-and-tricks).
## Chrome/Chrome (headless)

### Set Chrome/Chrome (headless) desired capabilities in Katalon Studio 

To set Chrome/Chrome (headless) desired capabilities, go to **Project > Settings > Desired Capabilities > WebUI > Chrome/Chrome (headless)**. You can add, delete or clear (delete all) capabilities for Chrome/Chrome (headless) browser.

To see all ChromeDriver supported capabilities, you can refer to the ChromeDriver document here: [Capabilities & ChromeOptions](https://chromedriver.chromium.org/capabilities#h.p_ID_102). 

### Common use cases

Belows are some common use cases of the desired capabilities for Chrome in Katalon Studio:

1. To start Chrome maximized by default. Click **Add** on the command toolbar, then type in the following value:

      <table>
   <thead>
   <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Value</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>args</td>
      <td>List</td>
      <td>--start-maximized</td>
   </tr>
   </tbody>
   </table>

   ```groovy
   {"CHROME_DRIVER":{"args":["--start-maximized"]}}

   ```
   <img src="url" width="70%" alt="Maximize in Chrome">


2. To start Chrome in incognito (private) mode. Click **Add** on the command toolbar, then type in the following value:

      <table>
   <thead>
   <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Value</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>args</td>
      <td>List</td>
      <td>--incognito</td>
   </tr>
   </tbody>
   </table>

   ```groovy
   {"CHROME_DRIVER":{"args":["--incognito"]}}

   ```
   <img src="url" width="70%" alt="Open incognito in Chrome">

3. You can also combine many desired capabilites for starting a browser as follows:

   <table>
   <thead>
   <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Value</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>args</td>
      <td>List</td>
      <td>--start-maximized,--incognito</td>
   </tr>
   </tbody>
   </table>

   ```groovy
   {"CHROME_DRIVER":{"args":["--start-maximized","--incognito"]}}

   ```
   <img src="url" width="70%" alt="Open incognito in Chrome">

> To find other Chrome arguments, you can refer to Peter Beverloo personal weblog here: [List of Chromium Command Line Switches](https://peter.sh/experiments/chromium-command-line-switches/).

## Firefox/Firefox (headless)

To get access to some useful capabilities for Firefox, follow these steps:

1. Open Firefox browser
2. On the address bar type in 'about:config'
3. Search for 'browser' key

   <img src="url" width="70%" alt="FireFox capabilities">
### Set Firefox/Firefox (headless) desired capabilities in Katalon Studio 

To define Firefox desired capabilities in Katalon Studio, follow these steps:

1. Go to **Project > Settings > Desired Capabilities > WebUI > Firefox/Firefox (headless)**. 
2. Click **Add** to create a key called `moz:firefoxOptions`. 
3. Have your capabilities added inside the `moz:firefoxOptions` key.

   <img src="url" width="70%" alt="Create DC for FireFox">

   To learn more about the use of `moz:firefoxOptions` key, you can refer to the Mozilla developer document here: [firefoxOptions](https://developer.mozilla.org/en-US/docs/Web/WebDriver/Capabilities/firefoxOptions).

### Common use cases

Belows are some common use cases of the desired capabilities for Firefox in Katalon Studio:

1. Start Firefox with devtools in the private mode. To do so, click **Add** on the command toolbar, then input the following values:

   <table>
   <thead>
   <tr>
      <th colspan="3">Table 1</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Name</td>
      <td>Type</td>
      <td>Value</td>
   </tr>
   <tr>
      <td>moz:firefoxOptions</td>
      <td>Dictionary</td>
      <td>Click More (...). In the pop-up Dictionary Property Builder dialog, click Add, then input values from the Table 2.</td>
   </tr>
   </tbody>
   </table>

   <table>
   <thead>
   <tr>
      <th colspan="3">Table 2</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Name</td>
      <td>Type</td>
      <td>Value</td>
   </tr>
   <tr>
      <td>args</td>
      <td>List</td>
      <td>--devtools,--private</td>
   </tr>
   </tbody>
   </table>

   ```groovy
   {"FIREFOX_DRIVER":{"moz:firefoxOptions":{"args":["--private","--devtools"]}}}
   ```

   <img src="url" width="70%" alt="Open Firefox with devtools in the private mode">


2. Start Firefox at a default page. To do so, click **Add** on the command toolbar, then input the following values:

   <table>
   <thead>
   <tr>
      <th colspan="3">Table 1</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Name</td>
      <td>Type</td>
      <td>Value</td>
   </tr>
   <tr>
      <td>moz:firefoxOptions</td>
      <td>Dictionary</td>
      <td>Click More (...). In the pop-up Dictionary Property Builder dialog, click Add, then input values from the Table 2.</td>
   </tr>
   </tbody>
   </table>

   <table>
   <thead>
   <tr>
      <th colspan="3">Table 2</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Name</td>
      <td>Type</td>
      <td>Value</td>
   </tr>
   <tr>
      <td>prefs</td>
      <td>Dictionary</td>
      <td>Click More (...). In the pop-up Dictionary Property Builder dialog, click Add, then input values from the Table 3.</td>
   </tr>
   </tbody>
   </table>

   <table>
   <thead>
   <tr>
      <th colspan="3">Table 3</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Name</td>
      <td>Type</td>
      <td>Value</td>
   </tr>
   <tr>
      <td>browser.startup.homepage</td>
      <td>String</td>
      <td>www.google.com</td>
   </tr>
   </tbody>
   </table>

    ```groovy
    {"FIREFOX_DRIVER":{"moz:firefoxOptions":{"prefs":{"browser.startup.homepage":"https://www.google.com/"}}}}
    ```

   <img src="url" width="70%" alt="Create DC for FireFox">

3. You can also combine many preferences for the test execution. For example, we want to ownload .html files automatically to specified folders. Click **Add** in the command toolbar, input the following values:

   <table>
   <thead>
   <tr>
      <th colspan="3">Table 1</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Name</td>
      <td>Type</td>
      <td>Value</td>
   </tr>
   <tr>
      <td>moz:firefoxOptions</td>
      <td>Dictionary</td>
      <td>Click More (...). In the pop-up Dictionary Property Builder dialog, click Add, then input values from the Table 2.</td>
   </tr>
   </tbody>
   </table>

   <table>
   <thead>
   <tr>
      <th colspan="3">Table 2</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Name</td>
      <td>Type</td>
      <td>Value</td>
   </tr>
   <tr>
      <td>prefs</td>
      <td>Dictionary</td>
      <td>Click More (...). In the pop-up Dictionary Property Builder dialog, click Add, then input values from the Table 3.</td>
   </tr>
   </tbody>
   </table>

   <table>
   <thead>
   <tr>
      <th colspan="3">Table 3</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Name</td>
      <td>Type</td>
      <td>Value</td>
   </tr>
   <tr>
      <td>browser.download.folderList</td>
      <td>Number</td>
      <td>2.0</td>
   </tr>
   <tr>
      <td>browser.helperApps.alwaysAsk.force</td>
      <td>Boolean</td>
      <td>False</td>
   </tr>
   <tr>
      <td>browser.download.manager.showWhenStarting</td>
      <td>Boolean</td>
      <td>False</td>
   </tr>
   <tr>
      <td>browser.download.dir</td>
      <td>String</td>
      <td>C:\\Downloads</td>
   </tr>
   <tr>
      <td>browser.download.dir</td>
      <td>String</td>
      <td>C:\\Downloads</td>
   </tr>
   <tr>
      <td>browser.download.defaultFolder</td>
      <td>String</td>
      <td>C:\\Downloads</td>
   </tr>
   <tr>
      <td>browser.helperApps.neverAsk.saveToDisk</td>
      <td>String</td>
      <td>text/html(*)</td>       
   </tr>
   </tbody>
   </table>

<em>(*)Browsers use the MIME type, not the file extension, to determine how to process a URL. You can find the list of common MIME types in the Mozilla developer document here: [Common MIME types](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types/Complete_list_of_MIME_types).</em>

   ```groovy
   {"FIREFOX_DRIVER":{"moz:firefoxOptions":{"prefs":{"browser.download.folderList":2.0,"browser.helperApps.alwaysAsk.force":false,"browser.download.manager.showWhenStarting":false,"browser.download.dir":"C:\\Downloads","browser.download.downloadDir":"C:\\Downloads","browser.download.defaultFolder":"C:\\Downloads","browser.helperApps.neverAsk.saveToDisk":"text/html"}}}}
   ```

   <img src="url" width="70%" alt="Download HTML file automatically to a folder">


### Internet Explorer

Internet Explorer driver supports some important capabilities which can be used to smooth execution of test on Internet Explorer. Some of these capabilities help us to disable JavaScripts, ignore the security domain setting for IE, persistent hovering, require window focus etc. These capabilities ease the way the for automation testing using Selenium Web Driver on Internet Explorer. More details on the Internet Explorer can be found [here](https://code.google.com/p/selenium/wiki/DesiredCapabilities#IE_specific).

The most common use of Internet Explorer desired capabilities is to configure Internet Explorer without having to complete the instructions from this [page](/display/KD/Internet+Explorer+Configurations). You can pass some desired capabilities to Internet Explorer so you don't need to configure your IE anymore.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-internet-explorer/IE.png)

* **ignoreProtectedModeSettings** determines whether to  skip the protected mode check. If set, tests may become flaky or unresponsive, and browsers may hang. If not set, and protected mode settings are not the same for all zones, an exception will be thrown on driver construction. Only "best effort" support is provided when using this capability.
* **ignoreZoomSetting** indicates whether to skip checking that the browser's zoom level is set to 100%. Value is set to false by default.
* **enablePersistentHover** determines whether persistent hovering is enabled (true by default). Persistent hovering is achieved by continuously firing mouse over events at the last location the mouse cursor has been moved to.
* **requireWindowFocus** determines whether to require the IE window to focus before performing any user interaction operations (mouse or keyboard events). This capability is false by default but delivers much more accurate native events interactions.

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
