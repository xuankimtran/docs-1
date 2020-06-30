---
title: "Tutorials for Spy Mobile Utility"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/spy-mobile-utility.html
redirect_from:
    - "/display/KD/Spy+Mobile+Utility/"
    - "/display/KD/Spy%20Mobile%20Utility/"
    - "/x/3QBO/"
    - "/katalon-studio/docs/spy-mobile-utility/"
    - "/display/KD/Spy+Object/"
    - "/display/KD/Spy%20Object/"
description: 
---
From version 7.6 onwards, Katalon Studio fully supports selector strategies supported by Appium except for Android Data Matcher. [Learn more](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html). This tutorial helps you get familiar with capturing Mobile objects on an application by using  **Spy Moble Utility**.

Before capturing Mobile objects on an application, make sure that you have [configured the environment for mobile testing](https://docs.katalon.com/katalon-studio/docs/mobile-on-windows.html) successfully.

1. From the main Toolbar, click on the **Spy Mobile** icon and select your device type, for instance, **Android Devices**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-mobile-utility/spy-icon.png" width=175>

2. In the displayed **Mobile Object Spy** dialog, specify the information at the **Configurations** section:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-mobile-utility/configurations.png" width=365>

   Where:

   * **Device Name**: A mobile device where Katalon launches the application (All of your connected devices should be displayed in this list.)
   * **Start with**: In the drop-down list, you can select either Application File or Application ID
      * **Application File**: Browse your tested application (`.apk` file for Android; `.ipa` file for iOS)
      * **Application ID**: Specify the application ID of your tested application

4. Click **Start** to begin spying the application unter test (AUT). Wait until the AUT is launched, and the **Device View** and **All Objects** are ready for you to capture objects of the AUT.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-mobile-utility/windows.png" width=1101>

5. You can click on any object either in the tree of **All Objects** or in **Device View**; Katalon highlights their counterpart accordingly for verification.

* **Device View** is a simulator of the device's screen.
* **All Objects** captures and organizes all the displayed mobile objects of **Device View** in a tree.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-mobile-utility/highlight.png" width=731>

   To make sure the **Device View** displays the current screen of the AUT on the device, you can click on the **Capture Object** button to reload **Device View** and refresh **All Objects**.

6. Check any objects in **All Objects**. Katalon Studio captures the selected objects and displays objects' properties in the **Object Properties** table.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-mobile-utility/add-object.png" width=1100>

    The most important property of an object is its locator strategy and value. The default locator is a unique value in detecting that object. Katalon Studio 7.6+ fully supports selector strategies supported by Appium except for Android Data Matcher ([Learn more](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html)). If you prefer another locator strategy among the provided option, you can choose it and generate a new locator. Then click **Highlight** to see if your newly updated locator can detect the target object on its screen correctly.

7. Click **Add to Object Repository** to save them to Katalon Studio.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-mobile-utility/image2017-1-23-173A173A48.png)

8. In the displayed **Folder Browser** dialog, you can decide where to save the captured objects. Select your preferred location then click **OK**. The captured objects will be added to **Object Repository** accordingly.
    
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-mobile-utility/save.png" width=310>

You can continue with the current mobile screen or navigate to other interfaces as needed. To reload the **Device View** as well as **All Objects**, click on the **Capture Object** button.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-mobile-utility/image2017-1-23-173A03A31.png)

See also:

* [Locator Strategies for finding Mobile objects](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html)
* [Introduction to Mobile Recorder](https://docs.katalon.com/katalon-studio/docs/katalon_mobile_recorder_introduction.html)
* [Tutorials for recording a Mobile test](https://docs.katalon.com/katalon-studio/docs/mobile-recorder-tutorials.html)
