---
title: "[Mobile] Execute mobile testing with Android Studio (Emulator)"
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-studio/docs/execute-mobile-testing-with-android-studio.html
redirect_from:
description:
---

<INTRODUCTION>

The Android Emulator simulates Android devices on your computer so that you can test your application on a variety of devices and Android API levels without needing to have each physical device. To learn more about the emulator capabilities, you can refer to this Android developer document here: [Run apps on the Android Emulator](https://developer.android.com/studio/run/emulator).

In this article, we guide you step by step how to execute mobile testing in Katalon Studio with Android Studio (Emulator).

> Requirements:
> * Appium installed. To learn more about installing Appium, you can refer to the Appium document here: [Getting started](https://appium.io/docs/en/about-appium/getting-started/?lang=en).

Follow these steps:

## Configure Android Studio
### Installation

Download and install Android Studio. You can download Android Studio from the Android developer website here: [Android Studio](https://developer.android.com/studio). During the installation, Android Studio will guide you through each steps and automatically download necessary components to create emulators.
### Create an Android project

1. After successfully installed, in the **Welcome Page** window, click **Create new project**. Android Studio provides a variety of sample project for you to choose. In this case, we choose **Empty Activity** as an example, then click **Next**.

    <img src="url" width="70%" alt="Choose project template">

2. In the next interface, you can configure the following prospect of your project to build an Android app:

    - Name: The name of your project. 
    - Package Name: By default, this is generated as: `com.example.<projectname>`.
    - Save location: The location to save your project. In case you want to change the default location, click *Browse*.
    - Language: To choose the language to build your Anroid app. You can select either **Java** or **Kotlin** from the drop-down menu.
    - Minimum SDK: To select the lowest version of Android you want your app to support 
    - Use legacy android.support libraries: If your app requires legacy library support, check this box.

    <img src="url" width="70%" alt="Choose project template">

3. Click **Finish**. A new project window opens containing sample files to build an Android app. If you want to learn more about building an Android app, you can refer to this document in the Android developer document here: [Build a simple user interface](https://developer.android.com/training/basics/firstapp/building-ui).
### Create an emulator

1. To create an emulator. In the main toolbar of the new project window, select **AVD manager**. An **Android Virtual Device Manager** opens.
   
   <img src="url" width="70%" alt="Choose project template">

2. Click **Create Virtual Device**. A **Virtual Device Configuration** opens that allows you to choose the size, resolution and density of your emulator. After selecting the hardware, click **Next**.

    <img src="url" width="70%" alt="Choose project template">   

3. The next interface asks you to select the system image for a particular API level or an Android version. To learn more about Android versions and the corresponding API levels, you can refer to the Android developer document here: [Understanding Android API levels](https://docs.microsoft.com/en-us/xamarin/android/app-fundamentals/android-api-levels?tabs=macos).

    Select the system image you want test. If you see **Download** next to the system image you select, you need to click it to download its neccessary components.

    For example: We choose the **Pie** Android version with system image x86. **Pie** is the code name for Android 9.0 and API level 28. This version is tagged with **Google APIs**, meaning that it includes the access to Google Play services. After clicking **Download**, you need to accept Android Software Development Kit License Agreement, then click **Next** to start downloading.

    <img src="url" width="70%" alt="Choose project template"> 

    > Notice:
    >
    > Katalon Studio can only intergrate with Android version 6.x or above. To learn more about supported environment in Katalon Studio, you can refer to this document here: [Supported environment](https://docs.katalon.com/katalon-studio/docs/supported-environments.html#mobile).


4. After choosing the system image, click **Next**. The **Verify Configuration** page appears. 
5. Change the default name of your emulator if neccessary, then click **Finish**. A new emulator appears in the **AVD Manager**.
### Launch an emulator

To launch the emulator, open the **ADV Manager**, select the emulator you want to launch, then click **Run** <img src="url" width="3%" alt="Run button">.

<img src="url" width="70%" alt="Choose project template">

If you want to run the emulator via command line option, you can refer to the Android developer document here: [Start the emulator from the command line](https://developer.android.com/studio/run/emulator-commandline).

## Execute mobile testing with Android Studio in Katalon

After launching the emulator, Katalon automatically recognizes the emulator as an Android device. You can now execute mobile testing with the emulator. 

<img src="url" width="70%" alt="Choose project template">

To learn more about creating and executing mobile testing in Katalon, you can refer to below documents:

- [Mobile Record Tutorials](https://docs.katalon.com/katalon-studio/docs/mobile-recorder-tutorials.html#record).
- [Tutorials for Mobile Object Spy](https://docs.katalon.com/katalon-studio/docs/spy-mobile-utility.html).

> Notice:
> * You must manually launch the emulator with Android Studio or via command line option first for Katalon to regconize the device.  