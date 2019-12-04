---
title: "[Windows] Get Element Position"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-get-element-position.html
---
> Starting from **version 7.2**, this keyword is available for Desktop testing on Katalon Studio.

## getElementPosition

* **Description**: Get the bounding rectangle of the WebElement that is found by using locator value of the given windowsObject.
* **Keyword name**: getElementRect
* **Keyword syntax**: Windows.getElementRect(windowsObject)
* **Parameter**: windowsObject
  * Description: An object that describes locator and locator strategy to find Windows Element.
  * Parameter Type: WindowsTestObject
  * Mandatory: Required
* **Return**: Rectangle indicating the element's bounding rectangle.
* **Throw**: **StepFailedException** if Katalon Studio cannot find the specified element.
* **Example**:

``` groovy
import org.openqa.selenium.Rectangle as Rectangle
Rectangle rect = Windows.getElementRect(findWindowsObject('Object Repository/Notepad/Edit'))
println String.format("{ x: %d, y: %d, width: %d, height: %d }", rect.getX(), rect.getY(), rect.getWidth(), rect.getHeight())
```
