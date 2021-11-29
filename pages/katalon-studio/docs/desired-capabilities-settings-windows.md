---
title: "Set up Desired Capabilities in Windows Desktop App Testing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/desired-capabilities-settings-windows.html 
redirect_from:
    - "/katalon-studio/docs/windows-desired-capabilities.html"
description:
---




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
   * **appArguments**: Support passing arguments to the Application Under Test. You can also use this desired capabilities to record action without opening a Windows.
   * **appWorkingDir**: Support overriding the Application Under Test's working directory.

The example below shows you:

* The desired capabilities set for a Windows Application Under Test;

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/desired-capabilities.png">

* How to use them in the Native Windows Recorder.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/use-windows-capabilities.png">

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