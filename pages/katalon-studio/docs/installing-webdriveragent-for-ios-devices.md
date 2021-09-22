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
> * Download and install Xcode. You can download from the Apple developer website here: [Xcode 13](https://developer.apple.com/xcode/)
> 
> * Download and install Appium. To learn more about installing Appium, you can follow the steps in the Appium document here: [Getting started](http://appium.io/docs/en/about-appium/getting-started/#installing-appium).


In this article, we demonstrate how to configure the WebDriverAgent in Xcode to automate iOS devices. Follow these steps:

### Connect the iOS device to Xcode

1. Add your device to your Apple Developer Portal. To learn more about how to register your device in Apple Developer Portal, you can refer to wikiHow document here: [How to Add a New Device to Your Apple Developer Portal](https://www.wikihow.com/Add-a-New-Device-to-Your-Apple-Developer-Portal)

2. Open **Xcode**. Go to **Preferences > Accounts**. Click *Add* (+) to add your developer's Apple ID.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/add-apple-id.png" width=85%>

### Configure the WebDriverAgent

1. To navigate to the location of WebDriverAgent, open **Terminal**, copy and paste the command line arguement below:

   ```groovy
   cd /usr/local/lib/node_modules/appium/node_modules/appium-webdriveragent
   ```

   For Appium version 1.14.2 or older versions, copy the following command: 

   ```groovy
    cd /usr/local/lib/node_modules/appium/node_modules/appium-xcuitest-driver/webdriveragent
   ```

2. After go to the WebDriverAgent location, run the following command to initialize the **WebDriverAgent** project:

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


3. Return to Xcode to open **WebDriverAgent.xcodeproj** file:
   - Navigate to **File > Open** to browse **appium-webdriveragent** folder. 
   - In the opened folder, select **WebDriverAgent.xcodeproj** file. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/xcodeproj.png" width=85%>

4. After opening **WebDriverAgent.xcodeproj** file in Xcode, you need to build **WebDriverAgentLib** and **WebDriverAgentRunner**:

   - Select **WebDriverAgentLib**. In the **Signing & Capabilities** section, check the **Automatically manage signing** box, then choose a team.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/lib.png" width=85%>

      On the menu bar, select **Product > Build**.
         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/build-lib.png" width=85%>

   - Select **WebDriverAgentRunner**. In the **Signing & Capabilities** section, check **Automatically manage signing**, then choose a team. 
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/runner.png" width=85%>

      On the menu bar, select **Product > Build**.  
         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/installing-webdriveragent-for-ios-devices/build-runner.png" width=85%>
