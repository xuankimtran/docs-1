---
title: "Using Packed Extension to Record with Chrome" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/record-web-utility-using-chrome-with-profile.html 
redirect_from:

description: 
---
> Requirements:
>
>* Katalon Studio version 8.0.5 or higher.
>* A Chrome Profile.

On some environments, using the Web Recorder utility with Chrome will prompt this error:
> “Loading the unpacked extensions is disabled by the administrators.”

Unpacked extensions are disabled on some environments as a security feature.

It is possible to use the packed extension **Katalon Record Utility** as an alternative. The extension is available on the Google Chrome store.

This article will show you how to install the extension, configure your profile, and use this alternative recording method when using the Record feature in Katalon Studio.

> Notes: This utility is associated to your Chrome Profile, which means you can only have one active session at any given time.

## Installing Katalon Record Utility

1. Open Chrome. Make sure you are using the Profile you want to Record with.

2. Navigate to the Chrome Web store page for this extension: [Katalon Record Utility](https://chrome.google.com/webstore/detail/katalon-record-utility/nhjadcbdhpaglfenolfcepmoeifeaijd).

3. Download and Install **Katalon Record Utility**.

4. Make sure the extension is now active. You can find instructions to manage your Chrome extensions in this guide: [Install and Manage Extensions](https://support.google.com/chrome_webstore/answer/2664769).

## Configuring and Using the Record Utility with Chrome Profile

The next steps will help you associate this Chrome profile with the Record Chrome (with Profile) function in Katalon Studio.

### Finding your Chrome Profile in the User Data Directory

This section will help you select the path to the correct Chrome Profile in your User Data Directory.

There are multiple Profiles in a given User Data Directory.

1. Open Chrome with the Profile you installed the extension with. In the address bar, type `chrome://version` and press Enter. 

2. Find the line "Profile Path:" Select and copy the displayed path, for example: `C:\Users\username\AppData\Local\Google\Chrome\User Data\Default`. This is the path to your *active* Profile.

3. Close Chrome.

### Configuring and using Katalon Record Utility with Chrome Profile

1. Open Katalon Studio, then:

   * As a Windows user: Click on **Window > Katalon Studio Preferences > Katalon > Recorder**
   * As a macOS user: Click on **Katalon Studio > Preferences > Katalon > Recorder**

2. Next to **Chrome profile**, click on the text box and paste your Profile Path. Click on **Apply and Close**.

>You can also click on **Browse** and navigate to the folder you wish to use. Find out more information about user data directory paths here: [User Data Directory](https://chromium.googlesource.com/chromium/src/+/HEAD/docs/user_data_dir.md#Introduction)

3. Click on **Record Web**. Click on the dropdown menu. Under the **New Browsers** section, select **Chrome (with Profile)**.

Katalon Studio now launches the Katalon Record Utility with your associated Chrome profile.

You can now record your test script.

You can find more information about the record function here: [Creating test cases using Record & Playback](https://docs.katalon.com/katalon-studio/docs/create_test_case_using_record_playback.html).
