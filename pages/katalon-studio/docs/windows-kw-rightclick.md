---
title: "[Windows] Right-click"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-rightclick.html
---
> Starting from **version 7.0.0**, Windows desktop application testing is available on Katalon Studio.

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
