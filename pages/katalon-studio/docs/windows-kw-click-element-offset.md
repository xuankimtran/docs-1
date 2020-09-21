---
title: "[Windows] Click Element Offset"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-click-element-offset.html
---

> From version 7.7.5, this keyword is available.

**Prerequisites**: 

* In **Native Windows Recorder**, enable **coordinate-based recording** in the window. `click` and `rightClick` actions are recorded as `clickElementOffset` and `rightClickElementOffset` actions respectively.
* In **Windows Recorder**, `Click Element Offset` and `Right-click Element Offset` buttons are supported in **Possible Actions**. 

## clickElementOffset

* **Description**: Performs a click action at the given offset of the Windows Element (relative to its top-left corner) that is found by using locator value of the given windowsObject.
* **Keyword name**: clickElementOffset
* **Keyword syntax**: `Windows.clickElementOffset(windowsObject, offsetX, offsetY, FailureHandling)`
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

* **Example**:

``` groovy
Windows.startApplicationWithTitle('katalon.exe', 'Katalon Studio')
'Wait for Katalon help tab to be present'
Windows.waitForElementPresent(findWindowsObject('TabItem'), 10)
'Click on X button using Click Element Offset, the coordinate is retrieved by cropping the tab and use https://www.mobilefish.com/services/record_mouse_coordinates/record_mouse_coordinates.php to extract the coordinates.'
Windows.clickElementOffset(findWindowsObject('TabItem'), 107, 13)
'Katalon Help tab is closed successfully as a result of clicking on X button'
Windows.verifyElementNotPresent(findWindowsObject('Object Repository/TabItem'), 5)
Windows.closeApplication()
'Click on OK to really close Katalon Studio'
Windows.click(findWindowsObject('Close Katalon Button'))
```
