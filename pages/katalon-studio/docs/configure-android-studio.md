---
title: "[Mobile] Configure Android Studio (Emulator)"
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-studio/docs/configure-android-studio.html
redirect_from:
description:
---

The Android Emulator simulates Android devices on your computer so that you can test your application on a variety of devices and Android API levels without needing to have each physical device. To learn more about the Android emulator capabilities and system requirements, you can refer to this Android developer document: [Run apps on the Android Emulator](https://developer.android.com/studio/run/emulator).

In this article, we guide you step by step on how to configure Android Studio (Emulator) for mobile testing in Katalon.

> Requirements:
> * Appium installed. To learn more about installing Appium, you can refer to the Appium document here: [Getting started](https://appium.io/docs/en/about-appium/getting-started/?lang=en).

## Configure Android Studio
### Installation

Download and install Android Studio. You can download Android Studio from the Android developer website here: [Android Studio](https://developer.android.com/studio). Android Studio will guide you through each step during the installation and automatically download the necessary components to create emulators.
### Create an Android project

1. After installing successfully, in the **Welcome Page** window, click **Create new project**. Android Studio provides a variety of sample projects for you to choose from. Here, we choose **Empty Activity** as an example, then click **Next**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-mobile-testing-with-emulator/KS-EMULATOR-Choose-project-template.png" width="60%" alt="Choose project template">

2. In the next interface, you can configure your project as follows:

    <table width="926">
    <tbody>
    <tr>
    <td>
    <div>
    <div><strong>Name</strong></div>
    </div>
    </td>
    <td>The name of your project.</td>
    </tr>
    <tr>
    <td>
    <div>
    <div><strong>Package Name</strong></div>
    </div>
    </td>
    <td>By default, this is generated as <code>com.example.&lt;projectname&gt;</code>.</td>
    </tr>
    <tr>
    <td>
    <div>
    <div><strong>Save location</strong></div>
    </div>
    </td>
    <td>The save location of your project. In case you want to change the default location, click <em>Browse </em>(folder icon).</td>
    </tr>
    <tr>
    <td>
    <div>
    <div><strong>Language</strong></div>
    </div>
    </td>
    <td>The language to build your Android app. You can select either <strong>Java</strong> or <strong>Kotlin</strong> from the dropdown menu.</td>
    </tr>
    <tr>
    <td>
    <div>
    <div><strong>Minimum SDK</strong></div>
    </div>
    </td>
    <td>&nbsp;The lowest version of Android supported by your app</td>
    </tr>
    <tr>
    <td>
    <div>
    <div><strong>Use legacy android.support libraries.</strong></div>
    </div>
    </td>
    <td>&nbsp;If your app requires legacy library support, check this box. To learn more about Android  support libraries, you can refer to the Android developer document here: <p><a href="https://developer.android.com/topic/libraries/support-library">Support libraries</a></p></td>
    </tr>
    </tbody>
    </table>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-mobile-testing-with-emulator/KS-EMULATOR-Configure-project-settings.png" width="60%" alt="Configure your project">

3. Click **Finish**. A new project window opens containing sample files to build an Android app. If you want to learn more about building an Android app, you can refer to this Android developer document: [Build a simple user interface](https://developer.android.com/training/basics/firstapp/building-ui).
### Create an emulator

1. To create an emulator. In the main toolbar of the new project window, select **AVD manager**. An **Android Virtual Device Manager** opens.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-mobile-testing-with-emulator/KS-EMULATOR-Choose-AVD-Manager.png" width="70%" alt="Choose AVD Manager">

2. Click **Create Virtual Device**. The **Select Hardware** page opens, allowing you to choose your emulator's screen size, resolution, and pixel density. To get an overview about screen variations, you can refer to this Android developer document: [Screen compatibility overview](https://developer.android.com/guide/practices/screens_support). After selecting the hardware, click **Next**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-mobile-testing-with-emulator/KS-EMULATOR-Select-hardware.png" width="60%" alt="Select the hardware">   

3. The **Select system image** page opens, asking you to select the system image for a particular API level or an Android version. To learn more about Android versions and the corresponding API levels, you can refer to the Android developer document here: [Understanding Android API levels](https://docs.microsoft.com/en-us/xamarin/android/app-fundamentals/android-api-levels?tabs=macos).

    Select the system image you want to test. If you see **Download** next to the system image you select, you need to click it to download its necessary components.

    For example: We choose the **Pie** Android version with an x86 system image. **Pie** is the code name for Android version 9.0 and API level 28. After clicking **Download**, you need to accept Android Software Development Kit License Agreement, then click **Next** to start downloading.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-mobile-testing-with-emulator/KS-EMULATOR-Select-system-image.png" width="60%" alt="Select system image"> 

    > Notice:
    >
    > Katalon Studio can only support Android version 6.0 or above. To learn more about the supported environment in Katalon Studio, you can refer to this document: [Supported environment](https://docs.katalon.com/katalon-studio/docs/supported-environments.html#mobile).


4. After choosing the system image, click **Next**. The **Verify Configuration** page appears. 
5. Change the default name of your emulator if necessary, then click **Finish**. A new emulator appears in the **AVD Manager**.

    <img src="https://github.com/katalon-studio/docs-images/raw/65a953207f0945eac8a4367e7e8a0a64f292a671/katalon-studio/docs/execute-mobile-testing-with-emulator/KS-EMULATOR-An-emulator-is-created-2.png" width="60%" alt="Launch the emulator">
### Launch an emulator

To launch an emulator, open the **ADV Manager**, select the emulator you want to launch, then click **Run**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-mobile-testing-with-emulator/KS-EMULATOR-Launch-the-emulator.png" width="60%" alt="Launch the emulator">


If you want to run the emulator via the command-line option, you can refer to the Android developer document here: [Start the emulator from the command line](https://developer.android.com/studio/run/emulator-commandline).

## Execute mobile testing with Android Studio in Katalon

After launching the emulator, Katalon automatically recognizes the emulator as an Android device. 
To check whether Katalon successfully recognizes your Android emulator, on the main toolbar, select the **Android** device in the dropdown list next to **Run**. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-mobile-testing-with-emulator/KS-EMULATOR-Recognize-Android-emulator.png" width="30%" alt="Regconize Android devices">

You should see the name of your emulator appear as an Android device.

> Notes:
> * You must first manually launch the emulator with Android Studio or via the command-line option for Katalon to recognize the device.  

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-mobile-testing-with-emulator/KS-EMULATOR-Choose-emulator-in-Katalon.png" width="50%" alt="Choose emulator in Katalon">

You can now execute mobile testing with the emulator. 

**Next step:**

* [Create your first Android test case](https://docs.katalon.com/katalon-studio/tutorials/mobile-create-android-test-case.html).


