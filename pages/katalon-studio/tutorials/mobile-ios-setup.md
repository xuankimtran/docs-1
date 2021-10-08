---
title: "[Mobile] iOS Setup"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/mobile-ios-setup.html
description:
---
   
In this article, we show you how set up Xcode simulators and real iOS devices to test iOS applications with Katalon Studio.

To begin with, you need to equip yourself with a **MacOS**. You can not execute iOS mobile testing in a **Window**.
## Step 1: Setting up the environment for iOS testing

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
## Step 2: Install extra dependencies to test real iOS device

> If you execute mobile testing on Xcode simulators only, skip this step.

1. Install Homebrew. Homebrew is a package manager that makes it easy to install other extra dependencies. To install Homebrew, follow the instructions in the Homebrew website: [Homebrew](https://brew.sh/).

2. After installing Homebrew, you can now use it to install below dependencies in the **Terminal**:

   - ios-deploy version 1.9.4 or newer. You can learn more about ios-deploy in this Github project: [ios-deply](https://github.com/ios-control/ios-deploy). To install ios-deploy via Homebrew, copy and paste the command line arguement as below:

      `brew install ios-deploy`

   - usbmuxd version 1.0.10 or newer. You can learn more about usbmuxd in this Github project: [usbmuxd](https://github.com/libimobiledevice/usbmuxd). To install usbmuxd via Homebrew, copy and paste the following command line arguements respectively:

      `brew install --HEAD usbmuxd`

      `brew unlink usbmuxd`

      `brew link usbmuxd`

   - libimobiledevice version 1.2.0 or newer. You can learn more about libimobiledevice in the libimobiledevice website: [libimobiledevice](https://libimobiledevice.org/). To install libimobiledevice via Homwbrew, copy and paste the following command line arguement respectively:
         
      `brew install --HEAD libimobiledevice`

      `brew unlink libimobiledevice`

      `brew link libimobiledevice`

   - For Appium version older than 1.20.0, you need to install Carthage. You can learn more about Carthage in this Github project: [carthage](https://github.com/Carthage/Carthage). To install Carthage via Homebrew, copy and paste the command line arguement below:

      `brew install carthage`

   - For Appium version older than 1.15.0, you also need to install ios-webkit-debug-proxy. You can learn more about ios-webkit-debug-proxy in this Github project: [ios-webkit-debug-proxy](https://github.com/google/ios-webkit-debug-proxy). To install ios-webkit-debug-proxy via Homwbrew, copy and paste the command-line as below:

      `brew install ios-webkit-debug-proxy`
## Step 3: Set up the iOS devices/ Xocde simulators for mobile testing in Katalon Studio
### For Xcode simulators

   After installing Xcode, Katalon automatically recognizes Xcode simulators as an iOS device. You can now move on to Step 4.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/KS-iOS-Katalon-regconizes-simulators.png" width="40%" alt="Katalon recognizes Xcode simulators">

### For real iOS devices

1. Any device for development with Xcode must be listed in the Apple developer portal. To learn more about registering your device in Apple Developer Portal, you can refer to the wikiHow document here: [How to Add a New Device to Your Apple Developer Portal](https://www.wikihow.com/Add-a-New-Device-to-Your-Apple-Developer-Portal).
2. In **Xcode > Preferences > Account**, click *Add* (+) to enter your Mobile Developer Apple ID and password.
3. Connect your iOS devices to your computer via a USB cable. Confirm to accept or trust the phone.
4. To enable **UI Automation** on the device, navigate to **Settings > Developer**. In the **UI Automation** section, turn on the setting for **Enable UI Automation**.
5. If you want to execute your tests using Safari on iOS (mobile browser), you will need to enable the following settings in **Settings > Safari > Advanced > Web Inspector**:

    - JavaScript
    - Web Inspector
    - Remote Automation

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/KS-IOS-Safari-Web-Inspector.png" width="40%" alt="Turn on Safari Web Inspector on iOS mobile">

## Step 4: Build WebDriverAgent

The WebDriverAgent is a WebDriver server used to control iOS devices remotely. To install WebDriverAgent, you can refer to this document: [Install WebDriverAgent for iOS devices](https://docs.katalon.com/katalon-studio/docs/installing-webdriveragent-for-ios-devices.html#setting-up-the-ios-device).
## Step 5: Prepare the iOS application file
### For Xcode simulators:

To execute mobile testing with Xcode simulators, you need to prepare an `.app` file.
To get the `.app` file from the Xcode project, go to `~/Library/Developer/Xcode/DerivedData/{app name}/Build/Products/{scheme}-iphonesimulator/{app name}.app`. 

> Notes:
> 
> To quickly search for the `DerivedData` folder, copy and patse the following path `~/Library/Developer/Xcode/DerivedData` into the **Spotlight**. 

For example: To find the `app` file from the **Coffee Timer** project, go to: `~/Library/Developer/Xcode/DerivedData/Coffee Timer/Build/Products/Debug-iphonesimulator/Coffee Timer.app`.
### For Real iOS devices:

To execute mobile testing with real iOS devices, you need to:

1. Prepare the `.ipa` file. Follow these steps:
   
   > If you already have the `.ipa` file built and signed, skip this Step.

   - Open the project file with Xcode. For example, to open `Coffee Timer.xcodeproj`:

      From where you store the project > **App** > **Your-First-iOS-App** > **Coffee Timer**. Double-click the `Coffee Timer.xodeproj` file.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/open-xcode-file.png" width=50%>

   - After opening the project in Xcode, select a iOS device to launch the apps.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/select-device.png" width=35%>

   - In the **General** tab, set deployment iOS version and select device type in the **Deployment Info** section.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/deployment.png" width=45%>

   - Switch to the **Signing & Capabilities** tab, check the **Automatically manage signing** box, then choose a team added in Step 3.

   - To build the `.ipa` file, click **Product > Build**. 

   - To export the `.ipa` file, click **Product > Archive** then follow the instruction to get `**Coffee Timer.ipa` file.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/export.gif" width=70%>

2. Verify the `.ipa` file, follow these steps:

   - Navigate to **Window > Devices** in Xcode.
   - Choose your device from the **Devices** list.
   - Click *Add* (+) to choose the `.ipa` file.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A5.png" width=60%>
      
   - Once installed successfully, the application appears in the **Installed Apps** section.  

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A14.png" width=60%>

## Execute mobile testing in iOS devices/simulators

After the above steps, you can now execute mobile testing with the Xcode simulators/real iOS devices. To learn more about creating and executing iOS mobile testing in Katalon, you can refer to this document: [Create your first iOS test case](https://docs.katalon.com/katalon-studio/tutorials/mobile-create-ios-test-case.html).
## See also:
   * [Set up Android-mobile-tests](https://docs.katalon.com/katalon-studio/tutorials/mobile-android-setup.html)
   * [Troubleshoot automated mobile testing](https://docs.katalon.com/katalon-studio/docs/troubleshooting-automated-mobile-testing.html)
