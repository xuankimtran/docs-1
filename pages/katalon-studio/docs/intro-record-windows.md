---
title: "Introduction to Windows Record Utility" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/intro-record-windows.html 
---
From **version 7.0**, you can record a test on a Windows desktop application.

From **version 7.7.5**, you can record and locate a Windows element by its relative coordinates. The `clickElementOffset` and `rightClickElementOffset` keywords are available and their buttons are supported in **Possible Actions**.
* [[Windows] Click Element Offset](https://docs.katalon.com/katalon-studio/docs/windows-kw-click-element-offset.html)
* [[Windows] Right-click Element Offset](https://docs.katalon.com/katalon-studio/docs/windows-kw-rightclick-element-offset.html)

## Windows Action Recorder

To start recording a Windows action, click **Record Windows Action** icon on the main toolbar of Katalon Studio.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Windows_Record_Action.png" width="600.5" height="65">

The `Windows Action Recorder` dialog box is basically similar to the one for [`Mobile Recorder`](https://docs.katalon.com/katalon-studio/docs/record-mobile-utility.html) and has the following components:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/windows-recorder.png" width="1171" height="746">

### Action Bar

The Action Bar located on the top left corner contains the **Refresh screen**, **Start** and **Stop** buttons.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/action%20toolbar.png" width="384" height="52">

### Configurations

**Configuration**: where you can view and edit the `WinAppDriver URL` and `Desired Capabilities`.

**Application File**: the absolute path to the `Windows Executable File (*.exe)` of the testing machine. For Windows users, click **Browse...** button to locate the application file.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/record-config.png" width="386" height="84">

The **Start** button is enabled after the Application File text box is filled.

### Recorded Actions

The **Recorded Actions** part shows all of the recorded built-in actions for interacting with the application.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/recorded-action.png" width="390" height="192">

### Catured Objects

The **Captured Objects** part stores all objects captured during the recording session. You can view and edit the object's name, locator and properties.

<img src="https://github.com/katalon-studio/docs-images/raw/e9378ee5895411e9fbdb2d78335d333368698f30/katalon-studio/docs/record-windows-actions/record-captured-object.png" width="392" height="574">

To customize the locator of a captured object, you can modify its locator in **Object Properties** and click **Highlight** to verify if the new locator correctly identifies the intended object.

In the Recorded Actions, you can also view the captured objects in the Object column.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/record-object-recorded-action.png" width="389" height="154">

> When you press the **OK** button at the bottom of the dialog box to finish the recording session, you will be asked to store all captured objects in the Object Repository.

### Screen View

The **Screen View** is a panel showing the application screenshots that are taken when you press either the **Start** button to record or the **Refresh Screen** button to recapture the application images. Those screenshots and the application on a real machine are of the same size.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/record-screen-view.png" width="477" height="165">

### Screen Objects

The **Screen Objects** section shows a tree of all objects that you can interact with. This tree will be automatically refreshed after you press the **Refresh Screen** button.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/record-screen-object.png" width="322" height="325">

The selected object is highlighted on the Screen View with a green rectangle surrounding it.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/screenview.png" width="633" height="223">

### Possible Actions

The **Possible Actions** section shows a list of action buttons. Each button represents a Windows action.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/record-possible%20actions.png" width="314" height="160">

There are two types of Windows actions, including object action and application action.

* Object action: an action requiring you to select an object on the **Screen Objects** to perform the action.

* Application action: an action for interacting with the application.

## Export Option

When you finish the recording session, there are 3 options to export the recorded actions to a test case:

* Export to new test case (chosen by default).
* Append to test case
* Overwrite test case

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/Record-export-to-new-tc.png" width="492" height="192">
