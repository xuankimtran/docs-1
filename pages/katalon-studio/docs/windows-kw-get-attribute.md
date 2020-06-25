---
title: "[Windows] Get Attribute"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-get-attribute.html
---

> From version 7.6.0, this keyword is available.

## getAttribute

* **Description**: Get the attribute value of a Windows element
* **Keyword name**: getAttribute
* **Keyword syntax**: `Windows.getAttribute(windowsObject, attribute)`
* **Parameters**:

   * Name: windowsObject
      * Description: An object describing the locator and locator strategy to find a Windows element
      * Parameter Type**: WindowsTestObject
      * Mandatory: Required

   * Name: attribute
      * Description: Name of the attribute
      * Parameter Type: String
      * Mandatory: Required

* **Return value**:
   * Description: Value of the attribute
   * Type: String

* **Example**:

```java
"Get attribute value of 'Name' of the edit panel"
def attributeValue = Windows.getAttribute(findWindowsObject("Object Repository/Edit"), 'Name')
assert attributeValue == 'Text Editor'
```
