---
title: "[Windows] Right-click"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-rightclick.html
---
> Starting from **Katalon Studio version 7.0.0**, Katalon Studio Enterprise users can run a test on a Windows desktop application.

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
