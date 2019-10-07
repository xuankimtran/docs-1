---
title: "[Windows] Get Text"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-get-text.html
---
> Starting from **Katalon Studio version 7.0.0**, Katalon Studio Enterprise users can run a test on a Windows desktop application.

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
