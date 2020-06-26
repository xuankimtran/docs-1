---
title: "Remote Execution for Mobile Testing"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-remote-execution.html
---
This tutorial guides you to configure Desired Capabilities for executing mobile tests remotely with local Appium server (Appium Grid).

Currently, Katalon Studio only supports testing an iOS application using macOS. With remote execution, you can use a Windows machine and remote to a macOS for iOS application testing.

## Prerequisites

- [Set up Katalon Studio for mobile testing on Windows](https://docs.katalon.com/katalon-studio/docs/mobile-on-windows.html)
- [Set up Katalon Studio for mobile testing on macOS](https://docs.katalon.com/katalon-studio/docs/mobile-on-macos.html)
- A started Appium server on the remote machine
- Connected Android or iOS devices

## Tutorials

Open your project in Katalon Studio and go to **Project/Settings/Desired Capabilities/Remote**:

1. In **Remote server URL**, enter the Appium server URL and select **Appium** in **Remote server type**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-remote-execution/remote.png">

2. In **Appium driver**, select Android Driver for Android devices; or iOS Driver for iOS devices

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-remote-execution/remote1.png">

3. Add desired capabilities to the table

* For **Android** app: you need to add `platformName`, `platformVersion` and `deviceName` capabilities
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-remote-execution/remote3.png">

   > Tip: In remote machine, type ```adb devices``` in Command Prompt to retrieve `deviceName` (Id of an Android device/simulator)

* For **iOS** app: you need to add `platformName`, `platformVersion`, `deviceName` and `udid` capabilities
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-remote-execution/remote4.png">

   > Tip: In remote machine, type ```idevice_id -l``` in Terminal to retrieve `udid` (id of an iOS device/simulator)

* For **Chrome** browser on **Android** devices: you need to add `platformName`, `platformVersion`, `deviceName` and `browerName` (its value should be **chrome**) capabilities
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-remote-execution/remote5.png">


* For **Safari** browser on **iOS** devices: you need to add `platformName`, `platformVersion`, `deviceName`, `udid` and `browerName` (its value should be **safari**) capabilities
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-remote-execution/remote6.png">

The above examples only show the minimum capabilities to run a Mobile test. Katalon Studio also supports other desired capabilities listed in [Appium document](http://appium.io/docs/en/writing-running-appium/caps/#general-capabilities).
