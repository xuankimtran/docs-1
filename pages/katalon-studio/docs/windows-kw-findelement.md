---
title: "[Windows] Find Element"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-findelement.html
---
> Starting from **version 7.0.0**, Windows desktop application testing is available on Katalon Studio.

## findElement

* **Description**: Find an element by using locator value of the given Windows object.
* **Keyword name**: findElement
* **Keyword syntax**: Windows.findElement(windowsObject)
* **Parameter**: windowsObject
  * Description: An object describing the locator and locator strategy to find a Windows element.
  * Parameter Type: WindowsTestObject
  * Mandatory: Required
* **Returns**: The found element.
* **Example**:

``` groovy
WebElement foundElement = Windows.findElement(findWindowsObject('Object Repository/Notepad/Edit'));
println "The Found element said: " + foundElement.getText()
```
