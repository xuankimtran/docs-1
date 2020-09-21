---
title: "[Windows] Right-click Element Offset"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-rightclick-element-offset.html
---

> From version 7.7.5, this keyword is available.

**Prerequisites**: 

* In **Native Windows Recorder**, enable **coordinate-based recording** in the window. `click` and `rightClick` actions are recorded as `clickElementOffset` and `rightClickElementOffset` actions respectively.
* In **Windows Recorder**, `Click Element Offset` and `Right-click Element Offset` buttons are supported in **Possible Actions**. 

## rightClickElementOffset

* **Description**: Performs a right-click action at the provided offset on the WebElement that is found by using locator value of the given windowsObject.
* **Keyword name**: rightClickElementOffset
* **Keyword syntax**: `Windows.rightClickElementOffset(windowsObject, offsetX, offsetY, FailureHandling)`
* **Parameters**:
  * Name: windowsObject
    * Description: An object describing the locator and locator strategy to find a Windows element.
    * Parameter Type: WindowsTestObject
    * Mandatory: Required
  * Name: offsetX
    * Description: The horizontal offset relative to the top-left corner of the element.
    * Parameter Type: Integer
    * Mandatory: Required
  * Name: offsetY
    * Description: The vertical offset relative to the top-left corner of the element.
    * Parameter Type: Integer
    * Mandatory: Required
  * Name: flowControl
    * Description: Used to control the step if the step failed.\
        STOP_ON_FAILURE: throws a StepFailedException if the step failed (default).\
        CONTINUE_ON_FAILURE: continue the test if the test failed but the test result is still failed.\
        OPTIONAL: continue the test and ignore the test result.
    * Parameter Type: FailureHandling
    * Mandatory: optional

* **Throws**: `StepFailedException` if the Windows element doesn't exist, or Katalon Studio could not perform a click action on the element.
* **Example**:

``` groovy
Windows.startApplicationWithTitle('katalon.exe', 
    'Katalon Studio')
'Wait for Katalon help tab to be present'
Windows.waitForElementPresent(findWindowsObject('TabItem'), 10)
'Right click on the tab'
Windows.rightClickElementOffset(findWindowsObject('TabItem'), 107, 13)
'Switch to the context menu'
Windows.switchToApplication();
'Click on the context menu item'
Windows.click(findWindowsObject('ContextMenuItem'))
'Verify clicking on Close in context menu closes the tab'
Windows.verifyElementNotPresent(findWindowsObject('Object Repository/TabItem'), 5)
Windows.closeApplication()
'Click on OK to really close Katalon Studio'
Windows.click(findWindowsObject('Close Katalon Button'))
```
