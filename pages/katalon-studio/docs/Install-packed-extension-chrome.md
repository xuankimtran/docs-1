---
title: "Installing and Using Packed Extensions for Web Recorder Utility" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/record-web-utility-using-chrome-with-profile.html 
redirect_from:

description: 
---
> Requirements: Katalon Studio version 8.0.5 or higher. A Chrome user account.

On some environments, using the Web Recorder utility with Chrome will prompt this error:
> “Loading the unpacked extensions is disabled by the administrators.”

Unpacked extensions are disabled on some environments as a security feature.

It is possible to use the packed extension **Katalon Record Utility** as an alternative. The extension is available on the Google Chrome store.

This article will show you how to install the extension, configure your profile, and use this alternative recording method when using the Record feature in Katalon Studio.

> Notice: Using the Record Web feature in this way uses your currently active Chrome profile. You can only have one active session at any given time.

## Installing Katalon Record Utility

1. Go to the [Chrome Web Store](https://chrome.google.com/webstore/category/extensions). Search for **Katalon Record Utility** or navigate to the extension page: [Katalon Record Utility](https://chrome.google.com/webstore/detail/katalon-record-utility/nhjadcbdhpaglfenolfcepmoeifeaijd)

2. Download and Install **Katalon Record Utility**.

3. Make sure the extension is now active. You can find instructions to manage your chrome extensions in this guide: [Install and Manage Extensions](https://support.google.com/chrome_webstore/answer/2664769).

## Configuring Katalon Studio Recorder to use your Chrome Profile

You will need to find the local path to your current Chrome profile, and apply it in the Katalon Studio preference menu for Recorder.

1. Open Chrome. In the address bar, type `chrome://version` and press Enter.

2. Find the line "Profile Path:" Select and copy the displayed path, for example: `C:\Users\username\AppData\Local\Google\Chrome\User Data\Default`. Close Chrome.

3. Open Katalon Studio. Go to **Window > Katalon Studio Preferences > Katalon > Recorder**

4. Next to **Chrome profile**, click on the text box and paste your Profile Path. Click on **Apply and Close**.

5. Click on **Record Web**. Click on the dropdown menu on the right of the **Record** button. Under the **New Browsers** section, select **Chrome (with Profile)**.

Katalon Studio now launches the Katalon Record Utility with your associated Chrome profile.

You can now record your test script.
