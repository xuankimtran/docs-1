---
title: "[Mobile] iOS Setup"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/mobile-ios-setup.html
description:
---

The iOS-mobile-tests perform UI functional automation test on an iOS application using Katalon Studio.
   
This topic describes the preliminary actions you need to perform to prepare the environment for testing iOS applications with Katalon Studio.

## Set up iOS tests on Windows and macOS
   
### On Windows machine

   You can only test an **iOS** application using **macOS**.

### On macOS machine
   
   1. Supported environments

   * Appium: 1.12.1 onwards
   * iOS: 9.x onwards
   
     > **Note**
     >
     > Some emulators have already supported Appium through their installations. Thus, if you want to run an application on an emulator, check your emulators' settings before proceeding with the Appium installation.
   
   2. Install the following required components

   * Appium v1.12.1 or newer. 
   * Xcode 10.2 or newer.
   * Command-line tool for Xcode.
   * Carthage 0.33 or newer.
   * ios-deploy 1.9.4 or newer.
   * ios-webkit-debug-proxy 1.8.4 or newer.
   * libimobiledevice 1.2.0 or newer.
   * usbmuxd 1.0.10 or newer.
   * WebDriverAgent.

      **<details><summary>Reference installation guide</summary>**
   
      We recommend you to refer to the official documentation of each component for the detailed instructions.

      1. **Install Xcode**
   
         Xcode can be installed via the App Store.

      2. **Install Xcode command-line tool**
   
         `xcode-select --install`\
         `sudo xcode-select -s /Applications/Xcode.app/   Contents/Developer`

      3. **Install homebrew** 
      
         Follow this [link](https://brew.sh/).

      4. **Install [Appium](http://appium.io/docs/en/about-appium/getting-started/#installing-appium)**
   
         `brew install node`\
         `npm install -g appium`
      
         > **Note**
         >
         > Make sure you install Node.js into a location where you have full **Read** and **Write** permissions.

      5. **Install carthage**
   
         `brew install carthage`

      6. **Install ios-deploy**
   
         `brew install ios-deploy`

      7. **Install usbmuxd**
   
         `brew install --HEAD usbmuxd`\
         `brew unlink usbmuxd`\
         `brew link usbmuxd`

      8. **Install libimobiledevice**
   
         `brew install --HEAD libimobiledevice`\
         `brew unlink libimobiledevice`\
         `brew link libimobiledevice`

      9. **Install ios-webkit-debug-proxy**
   
         `brew install ios-webkit-debug-proxy`

      10. **Install WebDriverAgent**

          Follow these links:

          * [Installing WebDriverAgent for iOS devices](/display/KD/Installing+WebDriverAgent+for+iOS+devices).
          * [WebDriverAgent project page](https://github.com/facebook/WebDriverAgent).

      </details>

   3. Set up the devices

   * Connect your iOS devices to your computer via a USB cable. Confirm to accept or trust the phone.
   * If you want to execute your tests using Safari on iOS (mobile browser), make sure **Web Inspector** is turned on for **Safari** (**Settings > Safari > Advanced > Web Inspector**).
   * Enable the service **UI automation** on the devices.
   * Connect the iOS devices to **Xcode**.
   * Go to **Settings** on the iOS devices > **Developer** > turn on **UIAutomation**.

## Verify the iOS application file

   Before testing an iOS native application file (**.ipa** file), follow these steps to check if the application file is already built and signed correctly.

   1. Open **Xcode** and navigate to **Window/Devices**.
   2. Choose your device from the **Devices** list.
   3. Click the "**+**" button and choose your application file.

      ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A5.png)

   If installed successfully, the application will appear in the **Installed Apps** section, as shown below.  

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A14.png)

   Next: [Create your first iOS test case](https://docs.katalon.com/katalon-studio/docs/mobile-recorder-tutorials.html#record)

   See also: 
   * [Set up Android-mobile-tests](https://docs.katalon.com/katalon-studio/tutorials/mobile-android-setup.html)
   * [Troubleshoot automated mobile testing](https://docs.katalon.com/katalon-studio/docs/troubleshooting-automated-mobile-testing.html)
