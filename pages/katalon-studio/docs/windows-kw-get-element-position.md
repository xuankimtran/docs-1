---
title: "[Windows] Get Element Position"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-get-element-position.html
---
> Starting from **version 7.2**, this keyword is available for Desktop testing on Katalon Studio.

## getElementPosition

* **Description**: Get the bounding rectangle of the WebElement that is found by using locator value of the given windowsObject.
* **Keyword name**: getElementPosition
* **Keyword syntax**: Windows.getElementPosition(windowsObject)
* **Parameter**: windowsObject
  * Description: An object that describes locator and locator strategy to find Windows Element.
  * Parameter Type: WindowsTestObject
  * Mandatory: Required
* **Return**: Point indicating the element's position.
* **Throw**: **StepFailedException** if Katalon Studio cannot find the specified element.
* **Example**:

``` groovy
import org.openqa.selenium.Point as Point
Point position = Windows.getElementPosition(findWindowsObject('Object Repository/Notepad/Edit'))
println String.format("{ x: %d, y: %d }", position.getX(), position.getY())
```
