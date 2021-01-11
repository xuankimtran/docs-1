---
title: "[Mobile] iOS Setup"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/ios-setup.html
redirect_from:
    - "/display/KD/Getting+Started/"
    - "/display/KD/Getting%20Started/"
    - "/display/KD/Installation+and+Setup/"
    - "/x/l4Ei/"
    - "/katalon-studio/docs/getting-started/"
    - "/display/KD/Before+You+Start/"
    - "/display/KD/Before%20You%20Start/"
    - "/x/HwAM/"
    - "/katalon-studio/docs/before-you-start/"
    - "/katalon-studio/docs/before-you-start.html"
    - "/katalon-studio/tutorials/install_setup_katalon_studio.html"
    - "/display/KD/Installation+and+Setup/"
    - "/display/KD/Installation%20and%20Setup/"
description:
---

### Introduction

   The iOS-mobile-tests perform UI functional automation test on an iOS application using Katalon Studio.
   
   This topic describes the preliminary actions you need to perform to prepare the environment for testing iOS applications with Katalon Studio.

### Set up iOS tests on Windows and macOS
   
   #### On Windows machine

   You can only test an **iOS** application using **macOS**. If you wish to set up your macOS environment for Katalon Studio, please refer to [this guide](https://docs.katalon.com/katalon-studio/docs/mobile-on-macos.html#supported-environments-on-macos).


   #### On macOS machine
   
   1. Supported environments

   * Appium: 1.12.1 onwards
   * iOS: 9.x onwards
   
   > **Note**
   >
   > Some emulators have already supported Appium through their installations. Thus, if you want to run an application on an emulator, check your emulators' settings before proceeding with the Appium installation.
   
   2. Install the following required components
   
   * Appium v1.12.1 or newer, follow [these steps](http://appium.io/docs/en/about-appium/getting-started/#installing-appium).

   > **Note**
   >
   > Make sure you install Node.js into a location where you have full **Read** and **Write** permissions.

   * Xcode 10.2 or newer
   * Command-line tool for Xcode
   * Carthage 0.33 or newer
   * ios-deploy 1.9.4 or newer
   * ios-webkit-debug-proxy 1.8.4 or newer
   * libimobiledevice 1.2.0 or newer
   * usbmuxd 1.0.10 or newer
   * WebDriverAgent ([Installation guide](https://docs.katalon.com/katalon-studio/docs/mobile-on-macos.html#reference-installation-guide))
   
   **Reference installation guide**

   We recommend you to refer to the official documentation of each component for the detailed instructions.
   
   **Install Xcode**
   
   Xcode can be installed via Mac App Store.
   
   **Install Xcode command-line tool**
   
   `xcode-select --install`\
   `sudo xcode-select -s /Applications/Xcode.app/Contents/Developer`
   
   **Install homebrew**
   
   Please follow this link: https://brew.sh/.
   
   **Install Appium**
   
   `brew install node`\
   `npm install -g appium`
   
   **Install carthage**
   
   `brew install carthage`
   
   **Install ios-deploy**
   
   `brew install ios-deploy`
   
   **Install usbmuxd**
   
   `brew install --HEAD usbmuxd`\
   `brew unlink usbmuxd`\
   `brew link usbmuxd`
   
   **Install libimobiledevice**
   
   `brew install --HEAD libimobiledevice`\
   `brew unlink libimobiledevice`\
   `brew link libimobiledevice`
   
   **Install ios-webkit-debug-proxy**
   
   `brew install ios-webkit-debug-proxy`
   
   **Install WebDriverAgent**
   
   Please follow these links:
   
   * [Installing WebDriverAgent for iOS devices](/display/KD/Installing+WebDriverAgent+for+iOS+devices)
   
   * [WebDriverAgent project page](https://github.com/facebook/WebDriverAgent)
   
   Additionally, if you want to test iOS applications, you will need to download the packages below (which have been linked to their corresponding setting up instructions).

   3. Set up the devices
   
   * Connect your iOS Devices to your computer via a USB cable. Confirm to accept/trust the phone.
   * If you want to execute your tests using Safari on iOS (mobile browser), make sure Web Inspector is turned on for Safari (Settings > Safari > Advanced > Web Inspector).
   * Enable the service UI automation on the device.
   * Connect the iOS device to Xcode.
   * Go to **Settings** on the iOS device > **Developer** > turn on **UIAutomation**.

### Verify the mobile app file

   Before testing an iOS native application file (**.   ipa** file), follow these steps to check if the    application file is already built and signed correctly.
   
   1. Open **Xcode** and navigate to **Window/Devices**
   
   2. Choose your device from the Devices list.
   
   3. Press the "+" button and choose your application file.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A5.png)

   If installed successfully, the application will appear in the **Installed Apps** section, as shown below.  

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A14.png)

   Next: [Create your first iOS test case](link)

   See also: 
   
   * [Set up Android-mobile-tests](https://docs.katalon.com/katalon-studio/docs/mobile-on-macos.html)
   * [Troubleshoot automated mobile testing](https://docs.katalon.com/katalon-studio/docs/troubleshooting-automated-mobile-testing.html)
   </details>
  