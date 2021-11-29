---
title: "Set up Remote Server in Desired Capabilities" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/desired-capabilities-remote-settings.html 
redirect_from:
    - "/katalon-studio/docs/remote-desired-capabilities/"
    - "/katalon-studio/docs/remote-desired-capabilities.html"
    - "/display/KD/Remote+Desired+Capabilities/"
    - "/display/KD/Remote%20Desired%20Capabilities/"
description:
---





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