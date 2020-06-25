---
title: "[Windows] Wait for Element Attribute Value"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-wait-element-attribute-value.html
---

> From version 7.6.0, this keyword is available.

## waitForElementAttributeValue

* **Description**: Wait until the given element has an attribute with the specified name and value within the given time in the second unit.
* **Keyword name**: waitForElementAttributeValue
* **Keyword syntax**: `Windows.waitForElementAttributeValue(windowsObject, attributeName, attributeValue, timeout)`
* **Parameters**:

   * Name: windowsObject
      * Description: An object that describes locator and locator strategy of the target element that needs to wait for
      * Parameter Type: WindowsTestObject
      * Mandatory: Required

   * Name: attributeName
       * Description: The name of the attribute name to verify
       * Parameter Type: String
       * Mandatory: Required

   * Name: attributeValue
       * Description: The value of the expected attribute value to verify
       * Parameter Type: String
       * Mandatory: Required

   * Name: timeout
       * Description: System will wait at most timeout (seconds) to return the result
          * If timeout = 0, Katalon Studio will use the default page load timeout
          * If timeout < 0, throws IllegalArgumentException
       * Parameter Type: Integer
       * Mandatory: Required

* **Return value**:
   * Description: true if the element has the attribute with the specified name and value; Otherwise, false
   * Type: Boolean

* **Example**:

```java
"Wait to expect 'Text Editor' is the value of attribute 'Name' of the edit panel"
assert Windows.waitForElementAttributeValue(findWindowsObject('Object Repository/Edit'), 'Name', 'Text Editor', 10)
```
