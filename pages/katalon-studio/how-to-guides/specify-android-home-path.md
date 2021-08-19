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

You can use a custom Android SDK location instead of the Katalon Studio default location. This enhancement resolves the problem when Katalon Runtime Engine cannot find the attached device. See also: [[Mobile] Android Setup](https://docs.katalon.com/katalon-studio/tutorials/mobile-android-setup.html#set-up-android-tests-on-windows-and-macos).
## Using Environment Variable to specify a path to Android SDK root folder

From version 8.1.0 onwards, Katalon Studio supports the **ANDROID_HOME** environment variable to specify the path to the Android SDK root. By default, the Android SDK root folder is located at **~/.katalon/tools/android-sdk**. You can rename or move your Android SDK root folder to another location and point the **ANDROID_HOME** environment variable to that new location.

>To learn more about environment variables, see [Command arguments](https://docs.katalon.com/katalon-studio/docs/common-configuration.html#command-arguments).

### Command-line Option

Use the **ANDROID_HOME** environment variable to point the path to the Android SDK installation directory with this command-line option:

- For Linux and macOS:

```groovy
$export ANDROID_HOME=[Your Android SDK location]
./katalon
```

- For Windows: ``%<export ANDROID_HOME=[Your Android SDK location]>%``

>**Notes**:
>
> For Appium to locate the tools, keep these files as their original name:
>
> - ADB file
> - Build-tools
> - Platform-tools
> - Tools folders

## Use Case

- You have an Android device connect with Katalon Studio. By default, the Android SDK root folder is located at **~/.katalon/tools/android-sdk**.

- You move the Android SDK root folder to the new location: <NEW LOCATION>

- In Katalon Runtime Engine, use this command-line option:

```groovy
$export ANDROID_HOME=[Your new Android SDK location]
./katalon
```

- Restart Katalon Studio and configure your mobile tests. Katalon Runtime Engine finds the new Android SDK root and run the test as usual.