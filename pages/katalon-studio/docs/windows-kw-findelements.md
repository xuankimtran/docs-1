---
title: "[Windows] Find Elements"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-findelements.html
---
> Starting from **version 7.0.0**, Windows desktop application testing is available on Katalon Studio.

## findElements

* **Description**: Find elements by using locator value of the given Windows object.
* **Keyword name**: findElements
* **Keyword syntax**: Windows.findElements(windowsObject)
* **Parameter**: windowsObject
  * Description: An object describing the locator and locator strategy to find a Windows element.
  * Parameter Type: WindowsTestObject
  * Mandatory: Required
* **Returns**: The found elements.
* **Example**:

``` groovy
List<WebElement> foundElements = Windows.findElements(findWindowsObject('Object Repository/Notepad/Edit'))
println "Found " + foundElements.size() + " element(s)"
println "The First found element said: " + foundElements.get(0).getText()
```
