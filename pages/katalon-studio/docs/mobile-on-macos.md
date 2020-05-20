---
title: "Mobile on macOS" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-on-macos.html 
redirect_from:
    - "/display/KD/Mobile+on+macOS/"
    - "/display/KD/Mobile%20on%20macOS/"
    - "/x/9AXR/"
    - "/katalon-studio/docs/mobile-on-macos/"
    - "/katalon-studio/tutorials/set_up_mobile_automation_project_macos.html"
description: 
---

## Supported Environments on macOS

* Appium: 1.12.1 onwards
* Android: 6.x onwards
* iOS: 9.x onwards

> **Note**:
>
> Some emulators have already supported Appium through their installations. Thus, if you want to run an application on an emulator, check your emulators' settings before proceeding with the Appium installation.

## Android

### Required components

If you want to test an Android application on your local device, you need to install [Appium](http://appium.io). The basic steps are:

* Install NodeJS

* `npm install -g appium`

### Setting up the devices

*   Turn on the phone's developer mode (go to **Settings** > **Developer options**).
*   Connect your Android Phone to your computer via a USB cable. Just confirm if prompted to accept/trust the device.
*   Install Android SDK: Katalon Studio will detect and ask you to install Android SDK automatically if your current machine doesn't have it. Please allow Katalon Studio to install it in this case.

### Verify

After completing setting your environment, open a Mobile Testing Sample Project (which is packaged in your Katalon Studio installation) and execute a test suite using an Android device: 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2017-6-29-143A483A34.png)  

Select your device from the **Android Devices** list. Click **OK**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2018-1-26-183A393A1.png)

If your test suite runs successfully, you will see the results in the test reports as follow:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2018-6-15-173A473A28.png)

For more information on how to run a test suite, check out the documentation [here](/pages/viewpage.action?pageId=786668).

## iOS

### Required components

* Appium v1.12.1 or newer
* Xcode 10.2 or newer
* Command-line tool for Xcode
* Carthage 0.33 or newer
* ios-deploy 1.9.4 or newer
* ios-webkit-debug-proxy 1.8.4 or newer
* libimobiledevice 1.2.0 or newer
* usbmuxd 1.0.10 or newer
* WebDriverAgent

### Reference installation guide

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

Additionally, if you want to test iOS applications, you will need to download the packages below (which have been linked to their corresponding setting up instructions):

### Setting up the devices

Connect your iOS Devices to your computer via a USB cable. Just confirm if prompted to accept/trust the phone.

If you want to execute your tests using Safari on iOS (mobile browser), make sure Web Inspector is turned on for Safari (Settings → Safari → Advanced → Web Inspector)

Enable the service UI automation on the device.

Connect the iOS device to Xcode.

**Settings** on the iOS device > **Developer** > turn ON **UIAutomation**

### Verify the mobile app file

Before testing an iOS native application file (**.ipa** file), follow these steps to check if the application file is already built and signed correctly.

Open **Xcode** and navigate to **Window/Devices**

Choose your device from the Devices list.

Press the "+" button and choose your application file.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A5.png)

If installed successfully, the application will appear in the Installed Apps section, as shown below.  

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A14.png)

## Finishing Steps

Once setting up successfully, follow the following guides to perform mobile testing in Katalon Studio:

*   [Record Mobile Utility](/display/KD/Record+Mobile+Utility)
*   [Spy Mobile Utility](/display/KD/Spy+Mobile+Utility)
*   [Execute a Test Case or a Test Suite](/display/KD/Execute+a+Test+Case+or+a+Test+Suite)

## Troubleshooting Common Issues

Please refer to [this](/display/KD/Troubleshooting+automated+mobile+testing) troubleshooting article.
