---
title: "Introduction to Windows Record Utility" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/intro-record-windows.html 
---

Katalon Studio provides the Windows record utility that allows you to record and playback actions performed in a Windows desktop application. With this utility, you can quickly create a test case, and later manually enhance the test.

This article introduces you to the Windows record utility in Katalon Studio.

> **Requirements**:
>
> * Katalon Studio version 7.0 onwards.
> * WinAppDriver is running on the test machine. To learn how to set up and run WinAppDriver, see: [Set up WinAppDriver](https://docs.katalon.com/katalon-studio/docs/setup-winappdriver.html).

> **Notes**:
> 
> From version 7.7.5, you can record and locate a Windows element by its relative coordinates. 
## The Windows record utility

To open the utility, from the main toolbar, click on **Record Windows Action**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Windows_Record_Action.png" width=70% alt="Windows Record Action icon">

The **Windows Action Recorder** dialog box is displayed as below:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/windows-recorder.png" width=100% alt="Windows Action Recorder dialog">

### Configurations

In the **CONFIGURATIONS** section, you can specify:

* **Configuration**: the WinAppDriver URL and desired capabilities.

* **Application File**: the absolute path to the Windows executable file (*.exe) of the testing machine. For Windows users, click on the **Browse...** button to locate the application file.

### Recorded actions

After you interact with the application under test (AUT) using the built-in actions, the recorded actions are displayed in the **Recorded Actions** tab.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/recorded-action.png" width=70% alt="Recorded Actions tab">

### Captured objects

During a recording session, the captured Windows objects are displayed in the **Captured Objects** tab. You can view and edit the object name, locator and properties.

<img src="https://github.com/katalon-studio/docs-images/raw/e9378ee5895411e9fbdb2d78335d333368698f30/katalon-studio/docs/record-windows-actions/record-captured-object.png" width=70% alt="Captured Objects tab">

You can modify the locator of an object in **Object Properties** and click **Highlight** to verify if the new locator correctly identifies the associated object.

In the **Recorded Actions** tab, you can also view the captured objects in the **Object** column.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/record-object-recorded-action.png" width=70% alt="Recorded Actions tab">

### Screen View

The **Screen View** shows the application screenshots taken when you press either the **Start** button to record or the **Refresh Screen** button to recapture the application images. The size of a captured screenshot is the same as the displayed application window on the testing machine.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/record-screen-view.png" width=70% alt="Screen view">

### Screen Objects

The **Screen Objects** section shows a tree of all Windows objects you can interact with. To update this tree view, you can press the **Refresh Screen** button.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/record-screen-object.png" width=70% alt="Screen objects">

The selected object is highlighted with a green border on the **Screen View**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/screenview.png" width=70% alt="Object highlighted in the Screen View">

### Possible Actions

The **Possible Actions** provides the built-in Windows actions that you can use to interact with the AUT.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/record-possible%20actions.png" width=70% alt="Possible actions">

There are two types of Windows actions:

* Object action: an action that you can perform on a specific Windows object. This type of action requires you to first select the target object on the **Screen Objects**, e.g., performing the *Click* action on a menu item.

* Application action: an action for interacting with the application, e.g., the *Close Application* action.

## Export Option

When you finish the recording session, there are three options to export the recorded actions to a test case:

* Export to new test case (selected by default).
* Append to test case.
* Overwrite test case.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/Record-export-to-new-tc.png" width=70% alt="Export actions dialog">
