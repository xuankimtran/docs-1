---
title: "Windows Built-in Keywords"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-keywords.html
---
> Starting with **Katalon Studio version 7.0**, you can run a test on a Windows desktop application.

## startApplication

* **Description**: Start the Windows driver and the Windows application with the given absolute path.
* **Keyword name**: startApplication
* **Keyword syntax**: Windows.startApplication(appFile)
* **Parameter**: appFile
  * Description: The absolute path to the Windows Executable File (*.exe) of the test machine.
  * Parameter Type: String
  * Mandatory: Required
* **Example**:

``` groovy
"Start the note pad application"
Windows.startApplication('C:\\Windows\\System32\\notepad.exe')
```

## closeApplication

* **Description**: Trigger a closing event of the running application on the Windows System. This action is similar to pressing ALT + F4 and does not force the application to close. If there is a pop-up confirmation, you need to take some extra steps to actually close it.
* **Keyword name**: closeApplication
* **Keyword syntax**: Windows.closeApplication()
* **Example**:

``` groovy
"Start the note pad application"
Windows.startApplication('C:\\Windows\\System32\\notepad.exe')

"Close note pad application"
Windows.closeApplication()
```

## switchToDesktop

* **Description**: Switch from the current running driver to a desktop session of the Windows Driver. This keyword initializes another Windows Driver with the `app: Root` (the whole desktop) desired capability and the same WinAppDriver URL and Proxy settings of the application driver. All of Windows built-in keywords now are manipulated by the desktop Windows Driver.
* **Keyword name**: switchToDesktop
* **Keyword syntax**: Windows.switchToDesktop()
* **Example**:

``` groovy
"Start the note pad application"
Windows.startApplication('C:\\Windows\\System32\\notepad.exe')

"Switch to control the Desktop"
Windows.switchToDesktop()
```

## switchToApplication

* **Description**: Switch from the current running driver to the application Windows Driver.
* **Keyword name**: switchToApplication
* **Keyword syntax**: Windows.switchToApplication()
* **Example**:

``` groovy
"Start the note pad application"
Windows.startApplication('C:\\Windows\\System32\\notepad.exe')

"Switch to control the desktop"
Windows.switchToDesktop()

// Do some stuffs with the desktop

"Switch back to control the note pad application"
Windows.switchToApplication()
```

## click

* **Description**: Perform a left-clicking action on the  Web element found by using the locator value of the given Windows object.
* **Keyword name**: click
* **Keyword syntax**: Windows.click(windowsObject)
* **Parameter**: windowsObject
  * Description: An object describing the locator and locator strategy to find a Windows element.
  * Parameter Type: WindowsTestObject
  * Mandatory: Required
* **Example**:

``` groovy
 "Click on the Close button"
 Windows.click(findWindowsObject("Object Repository/CloseButton"))
```

## doubleClick

* **Description**: Perform a double-clicking action on the Web element found by using the locator value of the given Windows object.
* **Keyword name**: doubleClick
* **Keyword syntax**: Windows.doubleClick(windowsObject)
* **Parameter:** windowsObject
  * Description: An object describing the locator and locator strategy to find a Windows element.
  * Parameter Type: WindowsTestObject
  * Mandatory: Required
* **Example**:

``` groovy
"Double-click on the item element to open the editor"
Windows.doubleClick(findWindowsObject("Object Repository/item"))
```

## rightClick

* **Description**: Perform a right-clicking action on the Web element found by using the locator value of the given Windows object.
* **Keyword name**: rightClick
* **Keyword syntax**: Windows.rightClick(windowsObject)
* **Parameter**: windowsObject
  * Description: An object describing the locator and locator strategy to find a Windows element.
  * Parameter Type: WindowsTestObject
  * Mandatory: Required
* **Example**:

``` groovy
"Right-click on the item element to view the context menu"
Windows.rightClick(findWindowsObject("Object Repository/item"))
```

## setText

* **Description**: Perform a text setting action on the Web element found by using the locator value of the given Windows object.
* **Keyword name**: setText
* **Keyword syntax**: Windows.setText(windowsObject,text)
* **Parameters**:
  * Name: windowsObject.
    * Description: An object describing the locator and locator strategy to find a Windows element.
    * Parameter Type: WindowsTestObject.
    * Mandatory: Required.
  * Name: text
    * Description: The text content to set on the element
    * Parameter Type: String
    * Mandatory: Required
* **Example**:

``` groovy
"Set 'Welcome to Katalon Studio' on the edit panel"
Windows.setText(findWindowsObject("Object Repository/Edit"), 'Welcome to Katalon Studio')
```

## getText

* **Description**: Get the text content of the Web element found by using the locator value of the given Windows object. This action appends the given text on the element without clearing its current text.
* **Keyword name**: getText
* **Keyword syntax**: Windows.getText(windowsObject)
* **Parameter**: windowsObject
  * Description: An object describing the locator and locator strategy to find a Windows element.
  * Parameter Type: WindowsTestObject
  * Mandatory: Required
* **Return value**:
  * Description: The text content of the found Windows element
  * Type: String
* **Example**:

``` groovy
"Set 'Welcome to Katalon Studio' on the edit panel"
Windows.setText(findWindowsObject("Object Repository/Edit"), 'Welcome to Katalon Studio')

"Get text of the edit panel and verify"
def text = Windows.getText(findWindowsObject("Object Repository/Edit"))

assert text == 'Welcome to Katalon Studio'
```

## clearText

* **Description**: Clear the text content of the Web element found by using locator value of the given windows object.
* **Keyword name**: getText
* **Keyword syntax**: Windows.clearText(windowsObject)
* **Parameter**: windowsObject
  * Description: An object describing the locator and locator strategy to find a Windows element.
  * Parameter Type: WindowsTestObject
  * Mandatory: Required
* **Example**:

``` groovy
"Set 'Welcome to Katalon Studio' on the edit panel"
Windows.setText(findWindowsObject("Object Repository/Edit"), 'Welcome to Katalon Studio')

"Get text of the edit panel and verify"
def text = Windows.getText(findWindowsObject("Object Repository/Edit"))

assert text == 'Welcome to Katalon Studio'

"Clear text of the edit panel"
Windows.clearText(findWindowsObject("Object Repository/Edit"))

"Get text of the edit panel and verify the text is clear"
text = Windows.getText(findWindowsObject("Object Repository/Edit"))

assert text == 'Welcome to Katalon Studio'
```

## getDriver

* **Description**: Get the current Windows Driver.
* **Keyword name**: getDriver
* **Keyword syntax**: Windows.getDriver()
* **Return Value**
  * Description: The current Windows Driver
  * Parameter Type: WindowsDriver
* **Example**:

``` groovy
"Start the note pad application"
Windows.startApplication('C:\\Windows\\System32\\notepad.exe')

"Get the application title"
Windows.getDriver().getTitle()
```
