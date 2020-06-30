---
title: "Introduction to Mobile Recorder"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/katalon_mobile_recorder_introduction.html
description: "Katalon Studio Record Mobile feature allows users to record and run the same tests on multiple devices. This is an introduction to Katalon Mobile Recorder."
redirect_from:
    - "/katalon-studio/tutorials/katalon_mobile_recorder_introduction.html"
    - "/katalon-studio/tutorials/mobile-testing/index.html"
---

## Mobile Recorder

To start recording a Mobile test, click on the **Mobile Recorder** icon on the main toolbar, and select your device type. Katalon Studio supports local Android or iOS/Remote/Kobiton mobile devices. The Mobile Recorder dialog with multiple components is displayed for your recording sessions.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/recorder-icon.png" width=174>

## Action Bar

**Action Bar** located on the top left corner contains the **Capture Object**, **Start**, and **Stop** buttons.

* **Capture Object**: When you click this button, Katalon Studio captures all mobile elements displayed on the current screen of the device.
* **Start**: Click on this button to start recording; Katalon will deploy and open the application on the configured device. This button is enabled after you specify the AUT.
* **Stop**: Click on this button to pause recording.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/action-bar.png" width=260>

## Configurations

The **Configurations** area is where you choose a mobile device and application under test (AUT) for the recording session.

* **Device Name**: A mobile device where Katalon launches the application (All of your connected devices should be displayed in this list.)
* **Start with**: In the drop-down list, you can select either Application File or Application ID
   * **Application File**: Browse your tested application (`.apk` file for Android; `.ipa` file for iOS)
   * **Application ID**: Specify the application ID of your tested application

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/configurations.png" width=369>

## Device View and All Objects

To select an object, you can click on any object either in the tree of **All Objects** or in **Device View**; Katalon highlights their counterpart accordingly for verification.

* **Device View** is a simulator of the device's screen. You can interact with the AUT in this view.
* **All Objects** captures and organizes all the displayed mobile objects of **Device View** in a tree.

To make sure the **Device View** displays the current screen of the AUT on the device, you can click on the **Capture Object** button to reload **Device View** and refresh **All Objects**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/highlight.png">

## Available Actions

**Available Actions** contains multiple buttons representing Mobile actions that can be performed on the AUT. There are two types of Mobile actions, including object action and application action.

* Object action: Object actions require you to select an object on **Device View** or **All Objects** to perform the action. Select an object, and you can see which actions are enabled for that object.
* Application action: application actions do not require a selected object to perform.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/possible-actions.png" width=367>

## Recorded Actions

The Recorded Actions table shows all of the recorded actions and related input/output that you have performed on the AUT. These items later become test steps of your test case.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/recorded-actions.png" width=361>

## Captured Objects

**Captured Objects** display all objects that you have interacted during the recording session. For each object captured by Katalon, you can find its detailed properties shown in the **Object Properties** table by double-clicking on it.

The most important property of an object is its locator strategy and value. The default locator is a unique value in detecting that object. Katalon Studio 7.6+ fully supports selector strategies supported by Appium except for Android Data Matcher. [Learn more](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html). If you prefer another locator strategy among the provided option, you can choose it and generate a new locator. Then click **Highlight** to see if your newly updated locator can detect the target object correctly.

* Default locator is unique in detecting that object:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/default-unique-locator.png" width=355>

* You can always choose your preferred locator strategy among the provided options:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/select-selection-method.png" width=361>
   
* Remember to verify if your newly created locator can identify the target object:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/selector-highlight.png">

See also:

* [Selector Strategies for finding Mobile Objects](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html)
* [Tutorials of Mobile recording utility](https://docs.katalon.com/katalon-studio/docs/mobile-recorder-tutorials.html)
* [Image-based testing for Mobile](https://docs.katalon.com/katalon-studio/docs/mobile-image-based-testing.html)
