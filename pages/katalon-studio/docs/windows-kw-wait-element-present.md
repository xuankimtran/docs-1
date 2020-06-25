---
title: "[Windows] Wait for Element Present"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-wait-element-present.html
---

> From version 7.6.0, this keyword is available.

## waitForElementPresent

* **Description**: Wait for the given element to present (appear) within the given time in the second unit.
* **Keyword name**: waitForElementPresent
* **Keyword syntax**: `Windows.waitForElementPresent(windowsObject, timeout)`
* **Parameters**:

   * Name: windowsObject
      * Description: An object that describes locator and locator strategy of the target element that needs to wait for
      * Parameter Type: WindowsTestObject
      * Mandatory: Required

   * Name: timeout
      * Description: System will wait at most timeout (seconds) to return the result.
         * If timeout = 0, Katalon Studio will use the default page load timeout.
         * If timeout < 0, throws IllegalArgumentException
      * Parameter Type: Integer
      * Mandatory: Required

* **Return value**:
   * Description: true if the element presents; otherwise, false.
   * Type: Boolean

* **Example**:

```java
"Wait to expect the edit panel presents with waitForElementPresent keyword"
assert Windows.waitForElementPresent(findWindowsObject('Object Repository/Edit') 10)
```
