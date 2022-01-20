---
title: "Set up remote server in desired capabilities" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/desired-capabilities-remote-settings.html 
redirect_from:
    - "/katalon-studio/docs/remote-desired-capabilities/"
    - "/katalon-studio/docs/remote-desired-capabilities.html"
    - "/display/KD/Remote+Desired+Capabilities/"
    - "/display/KD/Remote%20Desired%20Capabilities/"
description:
---

Katalon Studio supports defining desired capabilities for execution on remote web server such as Selenium Grid, Katalium Server or cloud services such as Kobiton, SauceLabs or BrowserStacks.

This article shows you how to configure desired capabilities for remote execution and where they are saved.

> You can find some common desired capabilities configurations in our Github sample project: [Tips and tricks](https://github.com/katalon-studio-samples/tips-and-tricks).
## Set desired capabilities for remote execution in Katalon Studio 

> Make sure that you are running Selenium Grid/ Appium Grid while executing the test.

To set desired capabilities for remote execution, do as follows:

1. Go to **Project > Settings > Desired Capabilities > Remote**. 
2. Enter **Remote Server URL**: `http://<localhost>:<port>/wd/hub` - the URL to the remote server.
3. In the **Remote Server Type** box, choose **Selenium/Appium**.
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/project-settings-new-ui/KS-DC-Remote-settings.png" width="100%" alt="Add Desired Capabilities for remote execution">

    From Katalon Studio version 6.3.0 onwards, when choosing **Appium** server, you also need to choose **Android Driver/iOS Driver**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/project-settings-new-ui/KS-DC-Remote-Choose-driver-for-Appium.png" width="100%" alt="Choose Android Driver/iOS Driver">
    
4. Click **Add** on the command toolbar. Provide the **Name**, **Type** and **Value** of the property that you wish to configure.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/project-settings-new-ui/KS-DC-REMOTE-Set-DC-for-Appium-driver.png" width="100%" alt="Add Desired Capabilities for remote execution">

    > * Desired capabilities is a JSON object (having keys and values pair). We need to set the capability **Name** as `key` and the capability **Value** as `value`. 
    > * The capabilities keys are case-sensitive.

    To learn more about configuring desired capabilities in Kobiton, BrowserStacks or Katalium Server, you can refer to the following documents:

    - [Kobiton](https://docs.katalon.com/katalon-studio/docs/integrate_with_kobiton.html#desired-capabilities-for-kobiton-devices)
    - [BrowserStack](https://docs.katalon.com/katalon-studio/docs/browserstack-integration.html)
    - [Katalium Server](https://docs.katalon.com/katalium-server/docs/katalium-server-katalon-studio-remote-machine.html)    
## Location of desired capabilities files

You can find the settings files for each environment in the `<your test project location>\settings\internal` folder. The files for each driver are named as follows:

| Driver | Settings' file |
| --- | --- |
| Remote Web Server| com.kms.katalon.core.webui.remote.properties |

## See also

- [Remote execution for mobile testing](https://docs.katalon.com/katalon-studio/docs/mobile-remote-execution.html#prerequisites)
- [Selenium Grid - Execution on remote machines](https://docs.katalon.com/katalon-studio/docs/selenium-grid-integration.html)
