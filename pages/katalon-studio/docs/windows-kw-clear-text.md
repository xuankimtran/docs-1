---
title: "[Windows] Clear Text"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-clear-text.html
---
> Starting from **version 7.0.0**, Windows desktop application testing is available on Katalon Studio.

## clearText

* **Description**: Clear the text content of the Web element found by using locator value of the given windows object.
* **Keyword name**: getText
* **Keyword syntax**: Windows.clearText(windowsObject)
* **Parameter**: windowsObject
  * Description: An object describing the locator and locator strategy to find a Windows element.
  * Parameter Type: WindowsTestObject
  * Mandatory: Required
* **Example**:

``` groovy
"Set 'Welcome to Katalon Studio' on the edit panel"
Windows.setText(findWindowsObject("Object Repository/Edit"), 'Welcome to Katalon Studio')

"Get text of the edit panel and verify"
def text = Windows.getText(findWindowsObject("Object Repository/Edit"))

assert text == 'Welcome to Katalon Studio'

"Clear text of the edit panel"
Windows.clearText(findWindowsObject("Object Repository/Edit"))

"Get text of the edit panel and verify the text is clear"
text = Windows.getText(findWindowsObject("Object Repository/Edit"))

assert text == 'Welcome to Katalon Studio'
```
