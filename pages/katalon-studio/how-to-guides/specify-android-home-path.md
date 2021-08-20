---
title: "How to specify a path to Android SDk root folder?"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/how-to-guides/how-to-specify-android-home-path.html
redirect_from:
description:
---
<INTRODUCTION>

>**Requirements**
>
> - Katalon Studio version 8.1.0 onwards
> - Katalon Runtime Engine version 8.1.0 onwards

You can use a custom Android SDK location instead of the Katalon Studio default location. From version 8.1.0 onwards, Katalon Runtime Engine supports the **ANDROID_HOME** environment variable to specify the path to the Android SDK root. To learn more about environment variables, see [Command arguments](https://docs.katalon.com/katalon-studio/docs/common-configuration.html#command-arguments).

## Using ANDROID_HOME Environment Variable

By default, the Android SDK root folder locates at **~/.katalon/tools/android_sdk**. You can rename or move your Android SDK root folder to another location and use the **ANDROID_HOME** environment variable to point the path to that new location. See also: [[Mobile] Android Setup](https://docs.katalon.com/katalon-studio/tutorials/mobile-android-setup.html#set-up-android-tests-on-windows-and-macos).

### Command-line Option

Start Katalon Studio with this command-line option instead of double-clicking on the **Katalon** app:

- For Linux and macOS:

    `$export ANDROID_HOME=<Your Android SDK location>`

    For example:

    ```groovy
    $export ANDROID_HOME=/opt/dev/android-sdk-linux
    ./katalon
    ```

- For Windows:
    
    1\. Go to **Edit the system environment variables > Environment Variables > System variables**.
    
    2\. Create a new environment variable with the **Variable** names **ANDROID HOME** and the **Value** is the path to the Android SDK root folder.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/android-home-path/window-android-home-path.png" alt="Window Environment Variable" width="100%">

>**Notes**:
>
> For Appium to locate the tools, keep these folders as their original name:
>
> - ADB file
> - build-tools
> - platform-tools
> - tools folders