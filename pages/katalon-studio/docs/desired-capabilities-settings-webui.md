---
title: "Set up Desired Capabilities for WebUI Testing" 
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

> You can find some common desired capabilities configurations in our Github sample project: [Tips and tricks](https://github.com/katalon-studio-samples/tips-and-tricks).
## Chrome/Chrome (headless)

### Set Chrome/Chrome (headless) desired capabilities in Katalon Studio 

To set Chrome/Chrome (headless) desired capabilities, go to **Project > Settings > Desired Capabilities > WebUI > Chrome/Chrome (headless)**. You can add, delete or clear (delete all) capabilities for Chrome/Chrome (headless) browser.

After clicking **Add**, provide **Name**, **Type** and **Value** of the property that you wish to configure.

> Desired capabilities is a JSON object (having keys and values pair). We need to set the capability **Name** as `key` and the capability **Value** as `value`. The capabilities `keys` are case-sensitive.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/KS-DC-Chrome-settings.png" width="70%" alt="Set DC in Chrome">

Alternatively, you can also go to `<your test project location>\settings\internal`, open the settings files for Chrome/Chrome (headless), and edit the capabilities in the Groovy script.

   <table>
   <thead>
   <tr>
      <th>Driver</th>
      <th>Settings file</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Chrome</td>
      <td>com.kms.katalon.core.webui.chrome.properties</td>
   </tr>
   <tr>
   <td>Chrome (Headless)</td>
   <td>com.kms.katalon.core.webui.chrome (headless).properties</td>
   </tr>
   </tbody>
   </table>

To see all ChromeDriver supported capabilities, you can refer to the ChromeDriver document here: [Capabilities & ChromeOptions](https://chromedriver.chromium.org/capabilities#h.p_ID_102). 

### Common use cases

Below are some common use cases of the desired capabilities for Chrome in Katalon Studio:

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

   Alternatively, you can copy and paste the following script into the settings files.
 
   ```groovy
   {"CHROME_DRIVER":{"args":["--start-maximized"]}}

   ```
   <a class="pop">
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/KS-DC-Start-chrome-maximized.png" width="70%" alt="Maximize in Chrome">
   </a>
   <p style="text-align: center;"><em>Click the image to enlarge it</em></p>


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

   Alternatively, you can copy and paste the following script into the settings files.

   ```groovy
   {"CHROME_DRIVER":{"args":["--incognito"]}}

   ```
   <a class="pop">
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/KS-DC-Start-Chrome-incognito.png" width="70%" alt="Open Chrome in incognito">
   </a>
   <p style="text-align: center;"><em>Click the image to enlarge it</em></p>

3. You can also combine many desired capabilities for starting a browser as follows:

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

   Alternatively, you can copy and paste the following script into the settings files.

   ```groovy
   {"CHROME_DRIVER":{"args":["--start-maximized","--incognito"]}}

   ```
   <a class="pop">
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/KS-DC-start-chrome-incognito-maximized.png" width="70%" alt="Open Chrome maximized in incognito">
   </a>
   <p style="text-align: center;"><em>Click the image to enlarge it</em></p>

> To find other Chrome arguments, you can refer to Peter Beverloo's personal weblog here: [List of Chromium Command Line Switches](https://peter.sh/experiments/chromium-command-line-switches/).

## Firefox/Firefox (headless)

To get access to some useful capabilities for Firefox, follow these steps:

1. Open Firefox browser
2. On the address bar, type `about:config`
3. Search for 'browser' key

   <img src="https://github.com/katalon-studio/docs-images/raw/d027a61c115c7330238389b4f226150aaf477f2e/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/KS-DC-capabilities-in-Firefox.png" width="70%" alt="FireFox capabilities">
### Set Firefox/Firefox (headless) desired capabilities in Katalon Studio 

To define Firefox desired capabilities in Katalon Studio, follow these steps:

1. Go to **Project > Settings > Desired Capabilities > WebUI > Firefox/Firefox (headless)**. 
2. Click **Add** to create a key called `moz:firefoxOptions`. 
3. Have your capabilities added inside the `moz:firefoxOptions` key.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/KS-DC-firefoxOptions-Key.png" width="70%" alt="Create DC for FireFox">

   To learn more about the use of `moz:firefoxOptions` key, you can refer to the Mozilla developer document here: [firefoxOptions](https://developer.mozilla.org/en-US/docs/Web/WebDriver/Capabilities/firefoxOptions).

   Alternatively, you can also go to `<your test project location>\settings\internal`, open the settings files for Firefox/Firefox (headless), and edit the capabilities in the Groovy script.

   <table>
   <thead>
   <tr>
      <th>Driver</th>
      <th>Settings file</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Firefox</td>
      <td>com.kms.katalon.core.webui.firefox.properties</td>
   </tr>
   <tr>
   <td>Firefox (Headless)</td>
   <td>com.kms.katalon.core.webui.firefox (headless).properties</td>
   </tr>
   </tbody>
   </table>
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
      <td>Click More (...). In the pop-up <strong>Dictionary Property Builder</strong> dialog, click <strong>Add</strong>, then input values from the Table 2.</td>
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

   Alternatively, you can copy and paste the following script in the settings files.

   ```groovy
   {"FIREFOX_DRIVER":{"moz:firefoxOptions":{"args":["--private","--devtools"]}}}
   ```
   <a class="pop">
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/KS-DC-OPEN-private-devtools-firefox.png" width="70%" alt="Open Firefox with devtools in the private mode">
   </a>
   <p style="text-align: center;"><em>Click the image to enlarge it</em></p>

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
      <td>Click More (...). In the pop-up <strong>Dictionary Property Builder</strong> dialog, click <strong>Add</strong>, then input values from the Table 2.</td>
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
      <td>Click More (...). In the pop-up <strong>Dictionary Property Builder</strong> dialog, click <strong>Add</strong>, then input values from the Table 3.</td>
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

   Alternatively, you can copy and paste the following script in the settings files.

    ```groovy
    {"FIREFOX_DRIVER":{"moz:firefoxOptions":{"prefs":{"browser.startup.homepage":"https://www.google.com/"}}}}
    ```
   <a class="pop">
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/KS-DC-Open-startup-default-page-firefox.png" width="70%" alt="Start Firefox with default startup page">
   </a>
   <p style="text-align: center;"><em>Click the image to enlarge it</em></p>

3. Download files to specified folders. Here, we want to download .html files to the `C:\Downloads` folder. To do so, click **Add** in the command toolbar, input the following values:

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
      <td>Click More (...). In the pop-up <strong>Dictionary Property Builder</strong> dialog, click <strong>Add</strong>, then input values from the Table 2.</td>
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
      <td>Click More (...). In the pop-up <strong>Dictionary Property Builder</strong> dialog, click <strong>Add</strong>, then input values from the Table 3.</td>
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
      <td>C:\Downloads</td>
   </tr>
   <tr>
      <td>browser.download.dir</td>
      <td>String</td>
      <td>C:\Downloads</td>
   </tr>
   <tr>
      <td>browser.download.defaultFolder</td>
      <td>String</td>
      <td>C:\Downloads</td>
   </tr>
   <tr>
      <td>browser.helperApps.neverAsk.saveToDisk</td>
      <td>String</td>
      <td>text/html</td>
   </tr>
   </tbody>
   </table>

   Explanation of the settings:

   <table>
   <thead>
   <tr>
      <th>Settings</th>
      <th>Description</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>browser.download.folderList</td>
      <td>Setting this preference as <code>2</code> tells Firefox to use the directory specified in <code>browser.download.dir</code> as the download folder instead. <br>You can learn more about this preference in the MozillaZine document here: <a href="http://kb.mozillazine.org/About:config_entries" target="_blank" rel="noopener noreferrer">About:config entries</a>.</td>
   </tr>
   <tr>
      <td>browser.download.manager.showWhenStarting</td>
      <td>Setting this preference as <code>False</code> turns off the showing of download progress.</td>
   </tr>
   <tr>
      <td>browser.download.dir</td>
      <td>This preference is to set path for the downloading folder, for example, <code>C:\Downloads</code>.</td>
   </tr>
   <tr>
      <td>browser.helperApps.neverAsk.saveToDisk</td>
      <td>This preference tells Firefox to automatically download the files of the selected MIME types. The list of MIME types is comma-separated.<br>To find the MIME types of the files you want to download, you can refer to the Mozilla developer document here: <a href="https://developer.mozilla.org/en-US/docs/Learn/Server-side/Configuring_server_MIME_types#how_to_check_the_mime_type_of_received_content" target="_blank" rel="noopener noreferrer">Check MIME types</a>.</td>
   </tr>
   </tbody>
   </table>

   Alternatively, you can copy and paste the following script in the settings files.

   ```groovy
   {"FIREFOX_DRIVER":{"moz:firefoxOptions":{"prefs":{"browser.download.folderList":2.0,"browser.helperApps.alwaysAsk.force":false,"browser.download.manager.showWhenStarting":false,"browser.download.dir":"C:\\Downloads","browser.download.downloadDir":"C:\\Downloads","browser.download.defaultFolder":"C:\\Downloads","browser.helperApps.neverAsk.saveToDisk":"text/html"}}}}
   ```

   <a class="pop">
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-chromechrome-headless/KS-DC-download-files-firefox.png" width="70%" alt="Download HTML file automatically to a folder">
   </a>
   <p style="text-align: center;"><em>Click the image to enlarge it</em></p>

## Internet Explorer

Internet Explorer (IE) driver supports some essential capabilities which can be used for smooth test execution. These capabilities ease the way for automation testing using Selenium WebDriver on Internet Explorer. You can learn more about supported IE capabilities here: [IE specific](https://github.com/SeleniumHQ/selenium/wiki/DesiredCapabilities#ie-specific).  

### Set desired capabilities for IE in Katalon Studio

To set desired capabilities for IE, go to **Project > Settings > Desired Capabilities > WebUI > IE**.

Alternatively, you can also go to `<your test project location>\settings\internal`, open the settings files for Internet Explorer, and edit the capabilities in the Groovy script.

   <table>
   <thead>
   <tr>
      <th>Driver</th>
      <th>Settings file</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>Internet Explorer</td>
      <td>com.kms.katalon.core.webui.ie.properties</td>
   </tr>
   </tbody>
   </table>

### Common use cases

The most common use of Internet Explorer desired capabilities is to configure Internet Explorer for automation testing. To do so, click **Add** on the common toolbar, input the following values:

> If you want to configure Internet Explorer globally, you can refer to this document: [Internet Explorer Configurations](https://docs.katalon.com/katalon-studio/docs/internet-explorer-configurations.html).

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
      <td>ignoreProtectedModeSettings</td>
      <td>Boolean</td>
      <td>True</td>
   </tr>
   <tr>
      <td>ignoreZoomSetting</td>
      <td>Boolean</td>
      <td>True</td>
   </tr>
   <tr>
      <td>enablePersistentHover</td>
      <td>Boolean</td>
      <td>false</td>
   </tr>
      <td>requireWindowFocus</td>
      <td>Boolean</td>
      <td>false</td>
   </tr>
   </tbody>
   </table>

   <a class="pop">
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-for-internet-explorer/IE.png" width="70%" alt="Set DC for IE">
   </a>
   <p style="text-align: center;"><em>Click the image to enlarge it</em></p>

   Explanation of the settings:

   <table>
   <thead>
   <tr>
      <th>Settings</th>
      <th>Description</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>ignoreProtectedModeSettings</td>
      <td>This capability determines whether to skip the protected mode check. Enable this capabilities for smooth test execution with IE.</td>
   </tr>
   <tr>
      <td>ignoreZoomSetting</td>
      <td>This capability indicates whether to skip checking that the browser's zoom level is set to 100%. Value is set to false by default.</td>
   </tr>
   <tr>
      <td>enablePersistentHover</td>
      <td>This capability determines whether persistent hovering is enabled (true by default).<br>Persistent hovering is achieved by continuously firing the mouse over events at the last location where the mouse cursor has been moved to.</td>
   </tr>
   <tr>
      <td>requireWindowFocus</td>
      <td>This capability determines whether to require the IE window to focus before performing any user interaction operations (mouse or keyboard events).<br>This capability is false by default.</td>
   </tr>
   </tbody>
   </table>

## Location of Desired Capabilities files

You can find the settings files for each environment in the `<your test project location>\settings\internal` folder. The files for each driver are named as follows:

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
