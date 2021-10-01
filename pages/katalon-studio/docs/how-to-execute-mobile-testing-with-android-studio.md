---
title: "[Mobile] Execute mobile testing with Android Studio (Emulator)"
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-studio/docs/execute-mobile-testing-with-android-studio.html
redirect_from:
description:
---

<INTRODUCTION>

In this article, we guide you step by step how to execute mobile testing in Katalon Studio with Android Studio (Emulator).

Follow these steps:

## Configure Android Studio
### Installation
1. Download and install Android Studio. You can download Android Studio from the Android developer website here: [Android Studio](https://developer.android.com/studio). During the installation, Android Studio will guide you through each steps and automatically download necessary components to create emulators.

### Create an Android project

2. After successfully installed, in the **Welcome Page** window, click **Create new project**. Android Studio provides a variety of sample project for you to choose. In this case, we choose **Empty Activity** as an example, then click **Next**.

    <img src="url" width="70%" alt="Choose project template">

3. In the next interface, you can configure the following prospect of your project:
    - Name: The name of your project
    - Package Name: This is automatically generated based on your project name.
    - Save location: The save location of your project. In case you want to change the default location, click *Browse*.
    - Language: To select either **Java** or **Kotlin** from the drop-down menu.
    - Minimum SDK: To select the lowest version of Android you want your app to support 
    - Use legacy android.support libraries: If your app requires legacy library support, check this box.

4. Click **Finish** to create an Android project.

### Launch an emulator

1. 

> Notice:
>
> Katalon Studio can only intergrate with Android version 6.x or above. To learn more about supported environment in Katalon Studio, you can refer to this document here: [Supported environment](https://docs.katalon.com/katalon-studio/docs/supported-environments.html#mobile).

## Execute mobile testing with Android Studio in Katalon