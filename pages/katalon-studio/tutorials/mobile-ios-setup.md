---
title: "[Mobile] iOS Setup"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/mobile-ios-setup.html
description:
---

The iOS-mobile-tests perform UI functional automation test on an iOS application using Katalon Studio.
   
This topic describes the preliminary actions you need to perform to prepare the environment for testing iOS applications with Katalon Studio.

To start testing iOS device, you need to equip yourself with a **MacOS**. You can not execute iOS mobile testing in a **Window**.
## Step 1: Set parameter

1. Install Xcode version 10.2 or newer. You can download Xcode from the App Store or the Apple Developer website: [Xcode 13](https://developer.apple.com/xcode/).

   > Notes:
   >
   > * Xcode must support the current version of your iOS device.
   > * Katalon Studio can only support iOS version 9.0 or above. To learn more about the supported environment in Katalon Studio, you can refer to this document: [Supported environment](https://docs.katalon.com/katalon-studio/docs/supported-environments.html#mobile).

2. Install Command-line tool for Xcode. You can download the compatible command-line tool for Xcode version from the Apple Developer website here: [Downloads](https://developer.apple.com/download/all/).

   Alternatively, you can copy and patse respectively the below command line argument to install Command-line tool for Xcode in the **Terminal**:

      `xcode-select --install`

      `sudo xcode-select -s /Applications/Xcode.app/Contents/Developer`

3. Install Appium version 1.12.1 or newer. You can install Appium via NPM or by downloading Appium Desktop. Follow the instructions in the Appium document here: [Getting started](http://appium.io/docs/en/about-appium/getting-started/#installing-appium).

   > Notes:
   > * We recommend installing Appium latest version.
   > * In case you are installing Applium via NPM. Make sure you install Node.js into a location where you have full permission to **Read** and **Write**.
   > * Some emulators/simulators have already supported Appium through their installations. Thus, if you want to run an application on an emulator, check your emulators' settings before proceeding with the Appium installation.
## Step 2: Install extra dependencies to test real iOS device

> If you execute mobile testing on simulators only, skip this step.

1. Install Homebrew. Homebrew is a package manager that makes it easy to install other extra dependencies. To install Homebrew, follow the instructions in the Homebrew website: [Homebrew](https://brew.sh/).

2. After installing Homebrew, you can now use it to install below dependencies in the **Terminal**:

   - ios-deploy version 1.9.4 or newer. The ios-deploy tools allow you to launch iOS apps on an iOS Device from the command line. To install ios-deploy, copy and paste the command line arguement as below:

         `brew install ios-deploy`

   - usbmuxd version 1.0.10 or newer. usbmuxd stands for "USB multiplexing daemon". This daemon is in charge of multiplexing connections over USB to an iPhone or iPod touch. To install usbmuxd, copy and paste the following command line arguements respectively:

         `brew install --HEAD usbmuxd`
         `brew unlink usbmuxd`
         `brew link usbmuxd`

   - libimobiledevice version 1.2.0 or newer. libimobiledevice is a library to communicate with iOS devices natively. To install libimobiledevice, copy and paste the following command line arguement respectively:
         
         `brew install --HEAD libimobiledevice`
         `brew unlink libimobiledevice`
         `brew link libimobiledevice`

   - For Appium version older than 1.20.0, you need to install Carthage. Carthage is a dependency manager for iOS development. To install carthage, copy and paste the command line arguement below:

         `brew install carthage`

   - For Appium version older than 1.15.0, you also need to install ios-webkit-debug-proxy. The ios_webkit_debug_proxy proxies requests from usbmuxd daemon over a websocket connection, allowing developers to send commands to MobileSafari and UIWebViews on real and simulated iOS devices. To install ios-webkit-debug-proxy, copy and paste the command-line as below:

         `brew install ios-webkit-debug-proxy`
## Step 3: Set up the iOS devices/simulators for mobile testing in Katalon Studio
### For iOS simulators

After installing Xcode, Katalon automatically recognizes the simulators as an iOS device. You can now move on to Step 4.
### For real iOS devices

1. Any device for development with Xcode must be listed in the Apple developer portal. To learn more about registering your device in Apple Developer Portal, you can refer to the wikiHow document here: [How to Add a New Device to Your Apple Developer Portal](https://www.wikihow.com/Add-a-New-Device-to-Your-Apple-Developer-Portal).
2. In **Xcode > Preferences > Account**, click *Add* (+) to enter your Mobile Developer Apple ID and password.
3. Connect your iOS devices to your computer via a USB cable. Confirm to accept or trust the phone.
4. To enable **UI Automation** on the device, navigate to **Settings > Developer**. In the **UI Automation** section, turn on the setting for **Enable UI Automation**.
5. If you want to execute your tests using Safari on iOS (mobile browser), you will need to enable the following settings in **Settings > Safari > Advanced > Web Inspector**:

    - JavaScript
    - Web Inspector
    - Remote Automation

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/KS-IOS-Safari-Web-Inspector.png" width="70%" alt="Turn on Safari Web Inspector on iOS mobile">

## Step 4: Build WebDriverAgent

The WebDriverAgent is a WebDriver server used to control iOS devices remotely. To install WebDriverAgent, you can refer to this document: [Install WebDriverAgent for iOS devices](https://docs.katalon.com/katalon-studio/docs/installing-webdriveragent-for-ios-devices.html#setting-up-the-ios-device).
## Step 5: Prepare the iOS application file

### For iOS simulators:

To execute mobile testing with iOS simulators, you need to prepare an `.app` file.
To get the `.app` file from the Xcode project, go to `~/Library/Developer/Xcode/DerivedData/{app name}/Build/Products/{scheme}-iphonesimulator/{app name}.app`.
### For Real iOS devices:

To execute mobile testing with real iOS devices, you need to:
- Prepare an iOS native application file `.ipa` file. If you already have the `.ipa` file built and signed, skip this Step.
- Verify the `.ipa` file. 

1. Prepare the `.ipa` file, do as follows:

   - Open the project file with **Xcode** tool. For example, to open **Coffe Time.xcodeproj**:

      From where you store the project > **App** > **Your-First-iOS-App** > **Coffee Timer** > **Coffee Timer.xodeproj**.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/open-xcode-file.png" width=50%>

   - In Xcode:
      - Select a device to launch the apps.

         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/select-device.png" width=35%>

     - Set deployment iOS version and select device type in **General**/**Deployment Info**.

         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/deployment.png" width=45%>

     - Build the apps by clicking **Product -> Build**. Wait until the build progress is finished.

         > Make sure to select your **Team** in **Signing & Capabilities**.
         >
         ><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/team.png" width=45%> 

     - Export the apps by clicking **Product -> Archive** then follow the instruction to get "**Coffee Time.ipa**" file.

         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/export.gif" width=70%>

2. Verify the `.ipa` file, follow these steps:

   - Open **Xcode** and navigate to **Window/Devices**.
   - Choose your device from the **Devices** list.
   - Click *Add* (+) to choose your application file.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A5.png" width=60%>
      
   - Once installed successfully, the application appears in the **Installed Apps** section, as shown below.  

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A14.png" width=60%>

## Execute mobile testing in iOS device/simulators

After the above steps, you can now execute mobile testing with the emulator. To learn more about creating and executing mobile testing in Katalon, you can refer to this document: [Create your first iOS test case](https://docs.katalon.com/katalon-studio/tutorials/mobile-create-ios-test-case.html).
## See also:
   * [Set up Android-mobile-tests](https://docs.katalon.com/katalon-studio/tutorials/mobile-android-setup.html)
   * [Troubleshoot automated mobile testing](https://docs.katalon.com/katalon-studio/docs/troubleshooting-automated-mobile-testing.html)
