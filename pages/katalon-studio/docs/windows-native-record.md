---
title: "Native Windows Recorder"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-native-record.html
---
From version 7.0.0, Katalon supports the recording utility for Desktop apps testing. From version **7.5.0**, Native Windows Recorder is available for Windows machines. This new-generation Windows Recorder gives you a seamless recording experience that is similar to Web Recorder.

**Requirements**

* Your Katalon Studio version must be **7.5.0+**
* You need an active **Katalon Studio Enterprise** license
* This feature is supported on **Windows only**

**Precondition**

* [Setting up WinAppDriver](https://docs.katalon.com/katalon-studio/docs/setup-winappdriver.html)
* Installing [Microsoft .NET Framework 4.5.2 or later](https://dotnet.microsoft.com/download/dotnet-framework/net452)

If your machine hasn't installed them yet, you could use Katalon tools to install them.

* **Tools > Windows > Install WinAppDrivers**
* **Tools > Windows > Install .NET Framework 4.5.2**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/kat-tool.png">

## Recording and Playing back

1. Right-click on the Windows Recorder icon and select **Native Windows Recorder** to open the Native Windows Recorder windows.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/open.png">

2. The **Native Windows Recorder** dialog box is displayed. Specify the information at the CONFIGURATIONS section.

   **Application File**: the absolute path to the Windows Executable File (*.exe) on the testing machine. Click the **Browse...** button to locate the application file.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/app-file.png">

   To start an UWP application, the application's execute file should be:

   * *ApplicationID* if your app is published on Microsoft store
   * *PackageFamilyName!Application ID* if your app is still in development.

3. The **Start** button is enabled after the Application File text box is filled. Click **Start** when you're done with the settings.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/action-bar.png">

4. The specified Windows application is deployed and opened.

## Modifying Recorded Actions

The list of available actions is the same as Katalon Studio built-in keywords. You can add any action, call another test case, and/or use Custom Keywords.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/recorded-actions.png">

## Modifying Recorded Objects

In Captured Objects, you can view all elements captured during the recording session. Here you can customize the locator of a captured object by modifying it in the Locator tab of Object Properties and clicking **Highlight** to verify if the new locator correctly identifies the intended object.

After you finish your recording, Native Windows Recorder exports a list of test objects used in the test case.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/captured-objects.png">

Upon satisfactorily creating your test case, click **OK** to add the recorded steps to the test case. Choose the directory you want your test objects to reside to continue. Here, Katalon Studio automatically detects similar existing objects in the Objects Repository and will ask you for further action. This helps users optimize object repositories.

You will be prompted to save the captured objects in the Object Repository of Katalon Studio. Choose an existing folder or create a new one, then click **OK** to continue.

When you finish your recording session, export the recorded steps to a new test case.

## Executing

Recorded objects and actions are saved in the test case.

Select the Windows icon in the Run button on the main Toolbar to execute the script.

The Windows test is executed with those recorded steps accordingly.
