---
title: "Introduction to Windows Spy Utility" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/intro-spy-windows.html 
---

The Windows spy utility offers flexible object capturing capability for testing Windows applications.

This article introduces you to the Windows spy utility in Katalon Studio.

> **Requirements**:
>
> * Katalon Studio version 7.0 onwards.
> * WinAppDriver is running on the test machine. To learn how to set up and run WinAppDriver, see: [Set up WinAppDriver](https://docs.katalon.com/katalon-studio/docs/setup-winappdriver.html).

## Capture objects with the Windows spy utility

To start capturing a Windows object, first you need to open the **Spy Windows Objects** dialog. From the main toolbar, click on the **Spy Windows Object** button.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Spy_Windows_Object.png" width="549" height="61.5">

The **Spy Windows Objects** dialog is displayed as below:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/Spy-windows-object-dialogue.png" width="532" height="358">

### Configure the spy utility

In the **CONFIGURATIONS** section, you can specify:

* **Configuration**: the WinAppDriver URL and desired capabilities.

* **Application File**: the absolute path to the Windows executable file (*.exe) of the testing machine. For Windows users, click on the **Browse...** button to locate the application file.

* **Application Title**: the title of the application under test.

When the application under test (AUT) is started, Katalon Studio captures all available Windows objects on the current window of the AUT and displays them in the **ALL OBJECTS** section.

### Add the captured objects

The **ALL OBJECTS** section shows a tree of all the objects of the AUT, including the associated Windows element names (highlighted in blue) and tag names.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/Windows-Objects-Spy-1.png" width=70% alt="All objects section">

When an object is selected, the position of the associated element is highlighted in the **SCREEN VIEW**. This helps identify the right element displayed on the AUT.

[image-for-screen-view]

To add a Windows object, you need to check the checkbox on the left of the desired Windows object. The added object is then displayed in the **CAPTURED OBJECTS** section.

### View captured objects

The **CAPTURED OBJECTs** section shows all of the captured Windows elements you want to add to the **Object Repository**.

To view details about a captured object, click on it. The detailed information is displayed in the **OBJECT PROPERTIES** section.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/highlight.png" width=70% alt="Captured objects section">

You can view and edit the object name, locator and properties before adding it to the **Object Repository**.

### Configure an object properties

The **OBJECT PROPERTIES** section allows you to configure the following information:

* **Object Name**: the Windows object name.
* **Locator Strategy**: the type of object locator to identify the Windows element. To generate the object locator of the desired locator type, click on the **Generate** button.
* **Locator**: the generated object locator that can be customized.
* **Properties** table: all properties of the captured objects.

To add the captured objects to the **Object Repository**, click **OK** and select the target folder where you want to save the objects.

[image-for-selecting-object-repository-folder]

### View and edit the captured objects

You can view and edit the locator and properties of a captured object in the **Object** view.

From the **Tests Explorer**, expand the **Object Repository** section, and select the desired object.

[image]

Details about the captured object are displayed in the **Object** view as follows:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/Windows-Spy-Object-3.png" width=70% alt="Object view">

In the **Object** view, you view and edit:

* **Locator**: the locator type and locator of the object.
* **Object Properties**: the properties of the object.