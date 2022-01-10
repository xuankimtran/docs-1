---
title: "Windows Spy Utility" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/intro-spy-windows.html 
---

The Windows spy utility helps capture test objects quickly and allows you to specify several properties and object locator strategies.

This article introduces you to the components of the Windows spy utility in Katalon Studio.

> **Requirements**:
>
> * Katalon Studio version 7.0 onwards.
> * WinAppDriver is running on the test machine. To learn how to set up and run WinAppDriver, see: [Set up WinAppDriver](https://docs.katalon.com/katalon-studio/docs/setup-winappdriver.html).

## The Windows spy utility

To open the utility, from the main toolbar, click on the **Spy Windows Object** button.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/KS-Windows-Spy-Objects-button.png" width=30% alt="Spy Windows Objects icon">

The **Spy Windows Objects** dialog is displayed as below:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/Spy-windows-object-dialogue.png" width=70% alt="Spy Windows Objects dialog">

### Configurations

In the **Configurations** section, you can specify:

* **Configuration**: the WinAppDriver URL and desired capabilities.

* **Application File**: the absolute path to the Windows executable file (*.exe) of the testing machine. For Windows users, click on the **Browse...** button to locate the application file.

When the application under test (AUT) is started, the utility captures all available Windows objects on the current window of the AUT and displays them in the **All Objects** section.

### All objects

The **All Objects** section shows a tree of all the objects of the AUT, including the associated Windows element names (highlighted in blue) and tag names.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/Windows-Objects-Spy-1.png" width=70% alt="All objects section">

To add a Windows object, check the checkbox on the left of the desired Windows object. The added object is then displayed in the **Captured Objects** section.

## Screen view

When an object is selected in the **All Objects** section, the position of the associated element is highlighted in the **Screen View**. This helps verify the selected Windows element.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/KS-Windows-Spy-Utility-Screen-View.png" width=70% alt="Captured objects section">

### Captured objects

The **Captured Objects** section shows all the captured Windows elements you want to add to the **Object Repository**.

To view details about a captured object, click on it. The detailed information is displayed in the **Object Properties** section.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/highlight.png" width=70% alt="Captured objects section">

You can view and edit the object name, locator and properties before adding it to the **Object Repository**.

### Object properties

The **Object Properties** section allows you to configure the following information:

* **Object Name**: the Windows object name.
* **Locator Strategy**: the type of object locator to identify the Windows element. To generate the object locator of the desired locator type, click on the **Generate** button.
* **Locator**: the generated object locator that can be customized.
* **Properties** table: all properties of the captured objects.

To add the captured objects to the **Object Repository**, click **OK** and select the target folder where you want to save the objects.

## View and edit the captured objects

You can view and edit the locator and properties of a captured object in the **Object** view.

Go to **Tests Explorer**> **Object Repository**, and select the desired Windows object. Details about a captured object are displayed in the **Object** view as follows:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/Windows-Spy-Object-3.png" width=70% alt="Object view">

In the **Object** view, you can view and edit:

* **Locator**: the locator type and locator of the object.
* **Object Properties**: the properties of the object.