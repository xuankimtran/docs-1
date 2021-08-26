---
title: "Specify a path to Android SDK root folder"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/how-to-guides/how-to-specify-android-home-path.html
redirect_from:
description:
---

>**Requirements**
>
> - Katalon Studio version 8.1.0 onwards
> - Katalon Runtime Engine version 8.1.0 onwards

You can use a custom Android SDK location instead of the Katalon Studio default location. From version 8.1.0 onwards, Katalon Runtime Engine supports the **ANDROID_HOME** environment variable to specify a path to Android SDK root folder. To learn more about environment variables, see [Command arguments](https://docs.katalon.com/katalon-studio/docs/common-configuration.html#command-arguments).

## Specify a path to Android SDK root folder

By default, the Android SDK root folder is located at **~/.katalon/tools/android_sdk**. You can rename or move your Android SDK root folder to another location and use the **ANDROID_HOME** environment variable to point the path to that new location. See also: [[Mobile] Android Setup](https://docs.katalon.com/katalon-studio/tutorials/mobile-android-setup.html#set-up-android-tests-on-windows-and-macos).

### Command-line Option

Start Katalon Studio with this command-line option instead of double-clicking on the **Katalon** app:

- For Linux and macOS:

    `$ export ANDROID_HOME=<Your Android SDK location>`

    For example:

    ```groovy
    $ export ANDROID_HOME=/opt/dev/android-sdk-linux
    $ ./katalon <arguments>
    ```

- For Windows:
    
    1\. In your Window, search for **Edit the system environment variables**. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/android-home-path/KS-android-home-edit-environment-variables.png" alt="Edit the system environment variable" width=70%>

    The **System Properties** dialog appears. Click **Environment Variables**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/android-home-path/KS-android-home-environment.png" alt="system properties" width=70%>
    
    2\. In the **System variables**, click **New** to create a new environment variable where:

    * **Variable**: **ANDROID_HOME**
    * **Value**: the path to the Android SDK root folder

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/android-home-path/KS-android-home-new.png" alt="new" width=70%>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/how-to-guides/android-home-path/KS-android-home-value.png" alt="Window Environment Variable" width="70%">

>**Notes**:
>
> For Appium to locate the tools, keep the ADB file and these folders as their original names:
>
> - build-tools
> - platform-tools
> - tools