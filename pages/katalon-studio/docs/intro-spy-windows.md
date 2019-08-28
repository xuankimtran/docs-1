---
title: "Introduction to Windows Spy Utility" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/intro-spy-windows.html 
---

> Starting with **Katalon Studio version 7.0**, you can spy objects on a Windows desktop application.

## Spying Windows objects

To start spying a Windows object, click **Spy Windows Object** icon on the main toolbar of Katalon Studio.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Spy_Windows_Object.png" width="549" height="61.5">

The `Spy Windows Objects` dialog box is basically similar to the one for [`Mobile Object Spy`](https://docs.katalon.com/katalon-studio/docs/spy-mobile-utility.html#capture-objects-using-spy-mobile-utility).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/Spy-windows-object-dialogue.png" width="532" height="358">

### CONFIGURATIONS

In the **CONFIGURATIONS** section:

* **Configuration**: where you can view and edit the `WinAppDriver URL` and `Desired Capabilities`.

* **Application File**: the absolute path to the `Windows Executable File (*.exe)` of the testing machine. For Windows users, click **Browse...** button to locate the application file.

* The **Start** button is to be enabled after the Application File text box is filled.

When the application starts, Katalon Studio starts capturing all available Windows objects on the current screen of the testing machine and shows them at the **ALL OBJECTS** section.

### SCREEN OBJECTS

The **SCREEN OBJECTS** section shows a tree of all captured Windows elements. Each item represents a Windows element. Its label is a combination of the Windows Element (blue text) and its tag name (black text). When an item is selected, its position is highlighted on the nearby Device View. This helps you easily identify the right object.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/Windows-Objects-Spy-1.png" width="399" height="445">

To add a Windows element to the Object Repository, first you need to check the checkbox on the left of the desired Windows element, then it is added to the **CAPTURED OBJECT** section.

### CAPTURED OBJECT

The **CAPTURED OBJECT** section shows all of the captured Windows elements that you want to add  to the Object Repository. When an item is selected, its information is displayed in the **OBJECT PROPERTIES** section. You can view and edit the object's name, locator and properties before adding it to the Object Repository.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/Windows-Spy-Object-2.png" width="362" height="595">

### OBJECT PROPERTIES

* **Object Name**: the edited Windows object's name.
* **Locator Strategy** and **Locator**: the locator to identify the Windows element.
* **Properties table**: all attributes of the captured elements.

After the desired Windows objects are added, they will be shown under the Object Repository folder of the Tests Explorer.

### WINDOWS OBJECT PART

The Windows Object part is where to display the Locator and properties of a Window Object.

* **Locator**: all locators supported by WinAppDriver will also be supported by Katalon Studio . Please read [this document](https://github.com/microsoft/WinAppDriver#supported-locators-to-find-ui-elements) for more details.
* **Object Properties**: the properties of the Windows Object captured in the Spy or Record sessions. You can also modify these properties.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/spy-windows-object/Windows-Spy-Object-3.png" width="749" height="450">