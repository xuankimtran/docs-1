---
title: "Mobile Recorder Tutorials"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-recorder-tutorials.html
description: Mobile Recorder Tutorials version 7.6
---

From version 7.6 onwards, Katalon Studio fully supports selector strategies supported by Appium except Android Data Matcher. [Learn more](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html). This tutorials helps you get familiar with the Record and Playback features for Mobile Tests.

## Record

1. From the main toolbar, click on the **Record Mobile** icon and select your device type (Katalon Studio supports local Android or iOS/Remote/Kobiton mobile devices.)
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/recorder-icon.png" width=174>

2. In the displayed **Mobile Recorder** dialog, specify the information at the **Configurations** section:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/configurations.png" width=369>
   
   Where:

   * **Device Name**: A mobile device where Katalon launches the application (All of your connected devices should be displayed in this list.)
   * **Start with**: In the drop-down list, you can select either Application File or Application ID
      * **Application File**: Browse your tested application (`.apk` file for Android; `.ipa` file for iOS)
      * **Application ID**: Specify the application ID of your tested application

3. Click **Start** to start deploying and opening the application on the configured device. Katalon Studio will displays the **Device View** as a screen simulator for you to interact with the application.

   The **All Objects** section captures and organizes all the displayed mobile objects in a tree. You can click on any object either in the tree or in **Device View**, Katalon highlights their counterpart accordingly for verification.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/device-view.png">

4. After selecting an object, you can choose an action to be performed at the **Possible Actions** section

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/possible-actions.png" width=367>

5. The selected object is captured in **Captured Objects** while the performed action is recorded in **Recorded Actions**

   * **Recorded Actions** include recorded steps, related input and output.
   * **Captured Objects**: For each object captured by Katalon, you can find its default selection method and locator value in the **Object Properties** table. The default locator is unique in detecting that object. However, if you prefer another locator strategy, you can choose it and generate a new locator. Then click **Highlight** to see if your newly updated locator can detect the target object correctly.
   
   Default locator is unique in detecting that object:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/default-unique-locator.png" width=355>

   You can always choose your preferred locator strategy among the provided options:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/select-selection-method.png" width=361>
   
   Remember to verify if your locator can detect the target object:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/selector-highlight.png">

6. After finishing recording, click **OK** to save the recorded test steps and captured objects to a test case. They can be added to a new test case or appended to an existing one. Similarly, the captured objects can be saved in a new folder or an existing folder in **Object Repository**.

## Playback

To playback the recorded scenario, 

1. Select the test case where you have saved the recorded actions
2. From the main **Toolbar**, open the drop-down list next to the **Run** button and to select a mobile device type

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/playback.png">

3. In the displayed dialog, select a device and click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/device.png" width=452>

   Katalon Studio executes the mobile test with the recorded steps accordingly.
