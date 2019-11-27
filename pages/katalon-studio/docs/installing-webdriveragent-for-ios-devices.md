---
title: "Installing WebDriverAgent for iOS devices"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/installing-webdriveragent-for-ios-devices.html
redirect_from:
    - "/display/KD/Installing+WebDriverAgent+for+iOS+devices/"
    - "/display/KD/Installing%20WebDriverAgent%20for%20iOS%20devices/"
    - "/x/TwbR/"
    - "/katalon-studio/docs/installing-webdriveragent-for-ios-devices/"
description:
---

> This setup process is **NOT** required if you use **Android** devices. Please go straight to this [step](/pages/viewpage.action?pageId=13698548#MobileonmacOS(new)-Android) instead.

[WebDriverAgent](https://github.com/facebook/WebDriverAgent), a [WebDriver server](https://w3c.github.io/webdriver/webdriver-spec.html) implementation for iOS, is used for controlling iOS devices remotely. You need to install and set up WebDriverAgent for Katalon Studio to automate iOS devices.

1\. Open **Xcode > Preferences > Accounts**, and add your developer's Apple ID.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/image2016-12-21-153A513A4.png)

2\. Open **Terminal**, and enter the following commands to initialize the **WebDriverAgent** project:

  - Appium 1.15.0+
    ```groovy
    cd /usr/local/lib/node_modules/appium/node_modules/appium-webdriveragent
    mkdir -p Resources/WebDriverAgent.bundle
    sh ./Scripts/bootstrap.sh -d
    ```

  - Appium 1.14.2 or older versions
    ```groovy
    cd /usr/local/lib/node_modules/appium/node_modules/appium-xcuitest-driver/webdriveragent
    mkdir -p Resources/WebDriverAgent.bundle
    sh ./Scripts/bootstrap.sh -d
    ```

    > **Common issues**
    >
    > * Error code 13: re-run command with sudo: **sudo ./Scripts/bootstrap.sh -d**
    >
    > * Error _Error StackTrace: Cannot find module 'eslint-config-appium': _missing paramter -d when running **./Scripts/bootstrap.sh**

3\. Log in to you Apple developer account and [register your device](https://www.wikihow.com/Add-a-New-Device-to-Your-Apple-Developer-Portal).

4\. Open the **WebDriverAgent.xcodeproj** project in the **appium-webdriveragent** folder with Xcode.

![project](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/project.png)

5\. Select **WebDriverAgentLib** > in the Signing section, check **Automatically manage signing** > select a team.

![lib](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/lib.png)

Then on the menu bar, select **Product > Build**.

![build](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/build.png)

6\. Select **WebDriverAgentRunner** > check **Automatically manage signing** > select a team. On the menu bar, select **Product > Build**.
