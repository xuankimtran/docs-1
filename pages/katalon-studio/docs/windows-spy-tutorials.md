---
title: "Capture Windows Objects using the Windows Spy Utility"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-spy-tutorials.html
---

This guide shows you how to capture Windows objects with the Windows spy utility.

> **Requirements**:
>
> * Katalon Studio version 7.0 onwards.
> * WinAppDriver is running on the test machine. To learn how to set up and run WinAppDriver, see: [Set up WinAppDriver](https://docs.katalon.com/katalon-studio/docs/setup-winappdriver.html).

To use the utility, first you need to open the **Spy Windows Objects** dialog. From the main toolbar, click on the **Spy Windows Objects** icon.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/KS-Windows-Spy-Objects-button.png" width=30% alt="Spy Windows Objects dialog">

The **Spy Windows Objects** dialog is displayed as below:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/KS-Spy-Windows-dialog.png" width=70% alt="Spy Windows Objects dialog">

## Configure the Windows spy utility

To configure the utility, in the **Configurations** section, specify the following fields:

* **Configuration**: the WinAppDriver URL and desired capabilities.

* **Application File**: the absolute path to the Windows executable file (*.exe) of the testing machine. For Windows users, click on the **Browse...** button to locate the application file.

For example, we provide the IP address to the remote Windows machine and the path to Notepad executable as the AUT.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/spy2.png" width=70% alt="CONFIGURATIONS section">

> **Notes**:
>
> For Universal Windows Platform (UWP) applications, the executable file should be:
> * *ApplicationID*, if the application is published on the Microsoft store.
> * *PackageFamilyName!Application ID*, if the application is still in development.

## Capture Windows objects

To capture Windows objects, follow these steps:

1. Start the connection to the WinAppDriver by clicking on the **Start** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/KS-Windows-spy-utility-start-button.png" width=30% alt="Start button">

    You can see the opened window of the executed AUT in the **Screen View** section:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/KS-Windows-spy-utility-executed-AUT.png" width=70% alt="Screen View section">

    All available objects on the window are displayed in the **All Objects** section. You can verify an object by clicking on it; the utility highlights the object with a green border in **Screen View**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/KS-Windows-spy-utility-executed-highlighted-object.png" width=70% alt="Highlighted object in the Screen View">

2. Add the captured objects. Select the objects you want to capture by checking on the checkbox on the left.

    The selected objects are displayed in the **Captured Objects** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/highlight-spy.png" width=70% alt="Added object in the Captured Objects section">

3. To save the captured objects, click on the **Add to Object Repository** button. In the opened dialog, select your desired folder, then click **OK**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/KS-Add-objects-to-Object-Repository.png" width=70% alt="Add to Object Repository">

    The captured objects are added to the selected folder in the **Object Repository**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/saved-objects.png" width=70% alt="Added objects in the Object Repository">

4. To end the capturing session, click on the **OK** button at the bottom of the dialog.

>**Notes**:
>
> While spying, recording, or executing a test on a desktop application:
>   * Do not lock the screen of the testing machine 
>   * Do not to run multiple instances of the AUT simultaneously.
