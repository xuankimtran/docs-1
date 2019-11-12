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

[WebDriverAgent](https://github.com/facebook/WebDriverAgent) is a [WebDriver server](https://w3c.github.io/webdriver/webdriver-spec.html) implementation for iOS that can be used to remote control iOS devices. You need to install and setup WebDriverAgent to allow Katalon Studio to automate iOS devices.

* Open **Xcode > Preferences > Accounts** and add developer's Apple ID.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/image2016-12-21-153A513A4.png)

* Open **Terminal** and enter following command to initialize **WebDriverAgent** project:

  - Appium 1.15.0+
    ```groovy
    brew install carthage
    cd /usr/local/lib/node_modules/appium/node_modules/appium-webdriveragent
    carthage bootstrap
    ```

  - Appium 1.14.2 or older versions
    ```groovy
    cd /usr/local/lib/node_modules/appium/node_modules/appium-xcuitest-driver/WebDriverAgent
    mkdir -p Resources/WebDriverAgent.bundle
    sh ./Scripts/bootstrap.sh -d
    ```

> **Common issues**
>
> * Error code 13: re-run command with sudo: **sudo ./Scripts/bootstrap.sh -d**
>
> * Error _Error StackTrace: Cannot find module 'eslint-config-appium': _missing paramter -d when running **./Scripts/bootstrap.sh**

* Login to Apple developer account and [register device](https://www.wikihow.com/Add-a-New-Device-to-Your-Apple-Developer-Portal) to developer account.

* Open project **WebDriverAgent.xcodeproj** within folder **WebDriverAgent** in Xcode.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/image2016-12-21-153A513A29.png)

* Select target **WebDriverAgentLib**, in the Signing section, check **Automatically manage signing** and select the team.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/image2016-12-21-153A513A56.png)

* Then on the menu bar, select **Product > Build**
    **![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/image2016-12-21-153A523A23.png)**

* Repeat the last two steps for **WebDriverAgentRunner**

* Xcode may fail to create a provisioning profile for the `WebDriverAgentRunner` target:

    [![Xcode provisioning fail](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/xcode-facebook-fail.png)](https://github.com/appium/appium/blob/master/docs/en/drivers/ios-xcuitest-img/xcode-facebook-fail.png)

* This necessitates manually changing the bundle id for the target by going to the **Build Settings** tab, and changing the **Product Bundle Identifier** from `com.facebook.WebDriverAgentRunner` to something that Xcode accepts, for example, "io.appium.WebDriverAgentRunner".

    [![Xcode bundle id](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/xcode-bundle-id.png)](https://github.com/appium/appium/blob/master/docs/en/drivers/ios-xcuitest-img/xcode-bundle-id.png)
