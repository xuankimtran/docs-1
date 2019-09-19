---
title: "[Windows] Set Text"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-set-text.html
---
> Starting from **Katalon Studio version 7.0.0**, Katalon Studio Enterprise users can run a test on a Windows desktop application.

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
