---
title: "[Mobile] iOS Setup"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/mobile-ios-setup.html
description:
---

The iOS-mobile-tests perform UI functional automation test on an iOS application using Katalon Studio.
   
This topic describes the preliminary actions you need to perform to prepare the environment for testing iOS applications with Katalon Studio.
   
## On Windows machine

   You can only test an **iOS** application using **macOS**.

## On macOS machine
   
### Supported environments

   * Appium: 1.12.1 onwards
   * iOS: 9.x onwards
   
     > **Note**
     >
     > Some emulators have already supported Appium through their installations. Thus, if you want to run an application on an emulator, check your emulators' settings before proceeding with the Appium installation.
   
### Installation

1. Install Xcode version 10.2 or newer. You can download Xcode from the App Store or the Apple Developer website [here](https://developer.apple.com/xcode/).
2. Install Command-line tool for Xcode. You can download the compatible command-line tool for Xcode version from the Apple Developer website here: [Downloads](https://developer.apple.com/download/all/).

3. Install Appium version 1.12.1 or newer. You can install Appium via NPM or by downloading Appium Desktop. Follow the instruction in the Appium document here: [Getting started](http://appium.io/docs/en/about-appium/getting-started/#installing-appium).

      > **Note**
      >
      > In case you are installing Applium via NPM. Make sure you install Node.js into a location where you have full permission to **Read** and **Write** 

4. Install Homebrew. To install Homebrew, follow the instruction in the Homebrew website: [Homebrew](https://brew.sh/).

5. After installing Homebrew, open the **Terminal** to install:

   - Carthage version 0.33 or newer. Carthage is a dependency manager for iOS development. To install carthage, copy and paste the command line arguement below:

      `brew install carthage`
   
   - ios-deploy version 1.9.4 or newer. The ios-deploy tools allow you to launch iOS apps on an iOS Device from the command-line. To install ios-deploy, copy and paste the command-line below:

      `brew install ios-deploy`

   - usbmuxd version 1.0.10 or newer: usbmuxd stands for "USB multiplexing daemon". This daemon is in charge of multiplexing connections over USB to an iPhone or iPod touch. 

         `brew install --HEAD usbmuxd`
         `brew unlink usbmuxd`
         `brew link usbmuxd`

   - libimobiledevice version 1.2.0 or newer. libimobiledevice is a cross-platform software library that talks the protocols to support iPhone, iPod Touch, iPad® and Apple TV devices.
         
         `brew install --HEAD libimobiledevice`
         `brew unlink libimobiledevice`
         `brew link libimobiledevice`

   - ios-webkit-debug-proxy version 1.8.4 or newer. The ios_webkit_debug_proxy (aka iwdp) proxies requests from usbmuxd daemon over a websocket connection, allowing developers to send commands to MobileSafari and UIWebViews on real and simulated iOS devices.

         `brew install ios-webkit-debug-proxy`

         > Note:
         >
         > For Appium 1.15 or above, you do not need to install ios_webkit_debug_proxy.

6. Install WebDriverAgent 

The WebDriverAgent is a WebDriver server used to control iOS devices remotely. To install WebDriverAgent, you can refer to this document: [Install WebDriverAgent for iOS devices](https://docs.katalon.com/katalon-studio/docs/installing-webdriveragent-for-ios-devices.html#setting-up-the-ios-device).
### Set up the iOS devices for mobile testing in Katalon Studio

1. iOS emulators:



2. Real iOS devices:

   * Connect your iOS devices to your computer via a USB cable. Confirm to accept or trust the phone.
   * If you want to execute your tests using Safari on iOS (mobile browser), make sure **Web Inspector** is turned on for **Safari** (**Settings > Safari > Advanced > Web Inspector**).
   * Enable the service **UI automation** on the devices.
   * Connect the iOS devices to **Xcode**.
   * Go to **Settings** on the iOS devices > **Developer** > turn on **UIAutomation**.

## Prepare the iOS application file

1. With iOS emulators:


2. With Real iOS devices:

Before diving further into testing, make sure the iOS native application file (**.ipa** file) is verified.

   - If the application file is already built and signed correctly, follow these steps:

      - Open **Xcode** and navigate to **Window/Devices**.
      - Choose your device from the **Devices** list.
      - Click the "**+**" button and choose your application file.

         <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A5.png" width=60%>
      
   - If the application is not built, do as follows:

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
         - Store **Coffee Time.ipa** file into **App** folder. Katalon Studio will use the exported file to start Coffee Timer application.

            <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/export.gif" width=70%>
            
   Once installed successfully, the application appears in the **Installed Apps** section, as shown below.  

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A14.png" width=60%>

   Next: [Create your first iOS test case](https://docs.katalon.com/katalon-studio/tutorials/mobile-create-ios-test-case.html)

   See also:
   * [Set up Android-mobile-tests](https://docs.katalon.com/katalon-studio/tutorials/mobile-android-setup.html)
   * [Troubleshoot automated mobile testing](https://docs.katalon.com/katalon-studio/docs/troubleshooting-automated-mobile-testing.html)
