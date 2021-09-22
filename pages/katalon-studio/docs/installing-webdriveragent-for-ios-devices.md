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

The WebDriverAgent is a WebDriver server used to control iOS devices remotely. It is automatically downloaded with Appium as `appium-webdriveragent`. To learn more about the adoption of WebDriverAgent in Appium, you can refer to the Quamotion document here: [WebDriverAgent vs Appium](https://www.quamotion.mobi/docs/xcuitrunner/webdriver-vs-appium/).

> Requirements:
>
> * Download and install Xcode. You can download it from the Apple developer website here: [Xcode 13](https://developer.apple.com/xcode/).
> 
> * Download and install Appium. To learn more about installing Appium, you can follow the steps in the Appium document here: [Getting started](http://appium.io/docs/en/about-appium/getting-started/#installing-appium).


In this article, we demonstrate how to configure the WebDriverAgent in Xcode to automate iOS devices. Follow these steps:

### Setting up the iOS device

1. Any device that is to be enabled for development use with Xcode must be listed in your online Apple developer portal. To learn more about how to register your device in Apple Developer Portal, you can refer to wikiHow document here: [How to Add a New Device to Your Apple Developer Portal](https://www.wikihow.com/Add-a-New-Device-to-Your-Apple-Developer-Portal).
2. Connect an iOS device to your computer via USB.
3. On your iOS device, confirm that you trust this Mac on the **Trust This Computer** pop up.
4. To enable **UI Automation** on the Device, navigate to **Settings > Developer**. In the **UI Automation** section, turn on the setting for **Enable UI Automation**.

### Configure the WebDriverAgent

1. Open **Xcode**. Go to **Preferences > Accounts**. Click *Add* (+) to add your developer's Apple ID.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/add-apple-id.png" width=85%>

2. To navigate to the location of WebDriverAgent, open **Terminal**, copy and paste the command line arguement below:

   ```groovy
   cd /usr/local/lib/node_modules/appium/node_modules/appium-webdriveragent
   ```

   For Appium version 1.14.2 or older versions, copy the following command: 

   ```groovy
    cd /usr/local/lib/node_modules/appium/node_modules/appium-xcuitest-driver/webdriveragent
   ```

3. After going to the WebDriverAgent location, run the following command to initialize the **WebDriverAgent** project:

   ```groovy
    mkdir -p Resources/WebDriverAgent.bundle
   ```
   
   > **Note**
   >
   > For Appium version below 1.20.0, you also need to run the next script on the same terminal:
   >
   > ```groovy
   > sh ./Scripts/bootstrap.sh -d
   > ```

   > **Common issues**
   >
   > * Error code 13: re-run command with sudo: `sudo ./Scripts/bootstrap.sh -d`
   >
   > * Error _Error StackTrace: Cannot find module 'eslint-config-appium': _missing paramter `-d` when running `/Scripts/bootstrap.sh`


4. Open **Finder** and type **appium-webdriveragent** to quickly search for the folder. In the opened folder, double-click to open the **WebDriverAgent.xcodeproj** file in **Xcode**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/xcodeproj.png" width=85%>

5. After opening **WebDriverAgent.xcodeproj** file in **Xcode**, you need to build **WebDriverAgentLib** and **WebDriverAgentRunner**:

   - Select **WebDriverAgentLib**. In the **Signing & Capabilities** section, check the **Automatically manage signing** box, then choose a team added in Step 1.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/lib.png" width=85%>

      On the menu bar, select **Product > Build**.
         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/build-lib.png" width=85%>

   - Select **WebDriverAgentRunner**. In the **Signing & Capabilities** section, check the **Automatically manage signing** box, then choose a team added in Step 1. 
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/runner.png" width=85%>

      On the menu bar, select **Product > Build**.  
         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/build-runner.png" width=85%>

### See also

- [[Mobile]iOS Setup](https://docs.katalon.com/katalon-studio/tutorials/mobile-ios-setup.html#verify-the-ios-application-file)