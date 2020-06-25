---
title: "[Windows] Set Encrypted Text"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-set-encrypted-text.html
---

> From version 7.6.0, this keyword is available.

## setEncryptedText

* **Description**: Perform a set text action on the Web element that is found by using the locator value of the given Windows object. This action will append the given text on the element and clear the current text of the element if it exists
* **Keyword name**: setEncryptedText
* **Keyword syntax**: `Windows.setEncryptedText(windowsObject, encryptedText)`
* **Parameters**:

   * Name: windowsObject
      * Description: An object describing the locator and locator strategy to find a Windows element
      * Parameter Type: WindowsTestObject
      * Mandatory: Required

   * Name: encryptedText
      * Description: The encrypted text content to set on the element
      * Parameter Type: String
      * Mandatory: Required

* **Example**:

```java
"Set encrypted text with raw text 'Welcome to Katalon Studio' on the edit panel"
Windows.setEncryptedText(findWindowsObject("Object Repository/Edit"), 'e9PbN3GBjir0NOof/VoZqBq1r+JLZAemMs+JZGunvlQ=')
```

> If something goes wrong when decoding encrypted text, please check your encrypted text with **Help > Encrypt Text** on the main Menu.
