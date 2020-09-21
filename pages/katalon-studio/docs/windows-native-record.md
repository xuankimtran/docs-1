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

**Preconditions**

* [Setting up WinAppDriver](https://docs.katalon.com/katalon-studio/docs/setup-winappdriver.html)
* Installing [Microsoft .NET Framework 4.5.2 or later](https://dotnet.microsoft.com/download/dotnet-framework/net452)

If your machine hasn't installed them yet, you could use Katalon tools.

* **Tools > Windows > Install WinAppDrivers**
* **Tools > Windows > Install .NET Framework 4.5.2**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/kat-tool.png">

## Coordinate-based Recording

> From **version 7.7.5**, you can record and locate a Windows element by its relative coordinates.

In **Native Windows Recorder**, with the enabled **coordinate-based recording**, `click` and `rightClick` actions are recorded as `clickElementOffset` and `rightClickElementOffset` actions respectively. The following keywords are supported: 

* [[Windows] Click Element Offset](https://docs.katalon.com/katalon-studio/docs/windows-kw-click-element-offset.html)
* [[Windows] Right-click Element Offset](https://docs.katalon.com/katalon-studio/docs/windows-kw-rightclick-element-offset.html)

With coordinates-based recording, Katalon Studio records an element's relative coordinates in addition to its selector. For instance, you want to click on the red X part to close a tab in Notepad. Katalon Recorder records the button's offsets (its relative coordinates to its top-left corner) as a set of parameters representing an X and Y offset, and save them in clickElementOffset. It uses them to identify the exact location to perform a click action during runtime.

Without that element's offsets, the test engine can only click on the button's center, resulting in a failed test.
ß
## Recording

1. Right-click on the Windows Recorder icon and select **Native Windows Recorder** to open the Native Windows Recorder windows.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/open.png">

2. The **Native Windows Recorder** dialog box is displayed. Specify the information at the CONFIGURATIONS section.

   **Application File**: the absolute path to the Windows Executable File (*.exe) on the testing machine. Click the **Browse...** button to locate the application file.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/app-file.png">

   To start a UWP application, the application's execute file should be:

   * *ApplicationID* if your app is published on Microsoft store
   * *PackageFamilyName!Application ID* if your app is still in development.

3. Click **Start** deploy and open the specified Windows application.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/action-bar.png">

4. When you hover over an element of the AUT, Katalon Studio highlights the identified object with a red rectangle.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/hover-highlight.png">

5. When you perform an action on the AUT, the action is recorded in the **Recorded Actions** section. The list of available actions is the same as Katalon Studio's built-in keywords. You can add any action, call another test case, and/or use Custom Keywords.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/recorded-actions.png">

6. All of the specified actions above are recorded at the **Recorded Actions** section.

   In **Captured Objects**, you can view all elements captured during the recording session. Here you can customize the locator of a captured object by modifying it in the **Locator** tab of **Object Properties**. The captured objects’ locators are their absolute XPaths.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/captured-objects.png">

7. When you’re done with recording, click **OK** to save the recorded actions in Katalon Studio.
8. You will be prompted to save the captured objects in the Object Repository of Katalon Studio. Choose an existing folder or create a new one, then click **OK** to continue.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/Step9.png" width="267" height="258">

9. When you finish your recording session, export the recorded steps to a new test case.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/Export-new-TC.png" width="494" height="197">

10. Recorded objects and actions are saved in the test case.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/test-case.png" width="609" height="191">

## Executing a test case

Remember to turn on the WinAppDriver before executing a test case.

Select the **Windows** icon in the **Run** button on the main Toolbar to execute the script.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/step13.png" width="228" height="330">

The Windows test is executed with those recorded steps accordingly.
