---
title: "[Mobile] Android Setup"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/mobile-android-setup.html
description:
---

The Android-mobile-tests perform UI functional automation test on an Android application using Katalon Studio.

This topic describes the preliminary actions you need to perform to prepare the environment for testing Android applications with Katalon Studio.

## Set up Android tests on Windows and macOS
   
### On Windows machine

   1. Supported environments 
   
   * Appium: 1.12.1 onwards.
   * Android: 6.x onwards (official releases).

   2. Install [Appium](http://appium.io/docs/en/about-appium/getting-started/#installing-appium)
   
      > **Note**
      >
      > Make sure you install Node.js into a location where you have full **Read** and **Write** permissions.

   3. Set up the devices
   
   * Turn on the phone's developer mode. Go to **Settings** > **Developer options**, enable:
   
      - USB debugging – Debug mode when USB is connected.
      - Install via USB – Allow installing apps via USB.
      - USB debugging (Security Setting) – Allow granting permissions and simulating input via USB debugging. 
   
   * Connect your Android phones to your computer via a USB cable.
   * Confirm to accept or trust the device.

   4. Install Android SDK
   
      Katalon Studio will detect and ask you to install **Android SDK** automatically if your current machine does not have it.

### On macOS machine

   1. Supported environments

   * Appium: 1.12.1 onwards.
   * Android: 6.x onwards.
   
     > **Note**
     >
     > Some emulators have already supported Appium through their installations. Thus, if you want to run an application on an emulator, check your emulators' settings before proceeding with the Appium installation.

   2. Install [Appium](http://appium.io/docs/en/about-appium/getting-started/#installing-appium)

      `brew install node`\
      `npm install -g appium`

      > **Note**
      >
      > Make sure you install Node.js into a location where you have full **Read** and **Write** permissions.
   
   3. Set up the devices

   * Turn on the phone's developer mode (go to **Settings** > **Developer options**).
   * Connect your Android Phone to your computer via a USB cable. Just confirm if prompted to accept or trust the device.
   * Install **Android SDK**: Katalon Studio will detect and ask you to install Android SDK automatically if your current machine does not have it.

## Verify the Android application file

   After completing setting your environment, open a    Mobile Testing Sample Project (which is packaged in  your Katalon Studio installation) and execute a test suite using an Android device. 
   
   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2017-6-29-143A483A34.png)  

   Select your device from the **Android Devices** list > click **OK**. 

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2018-1-26-183A393A1.png)

   If your test suite runs successfully, you will see the results in the test reports as follow:

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2018-6-15-173A473A28.png)
   
   Next: [Create your first Android test case](https://docs.katalon.com/katalon-studio/tutorials/mobile-android-setup.html).

   See also:
   * [Set up iOS-mobile-tests](https://docs.katalon.com/katalon-studio/tutorials/mobile-ios-setup.html).
   * [Troubleshoot automated mobile testing](https://docs.katalon.com/katalon-studio/docs/troubleshooting-automated-mobile-testing.html).

