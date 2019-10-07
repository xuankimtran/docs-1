---
title: "[Windows] Send Keys"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-senkey.html
---
> Starting from **Katalon Studio version 7.0.0**, you can run a test on a Windows desktop application.

## Keyword sendKeys

* **Description**: Simulate keystroke events on the specified element by pressing a key or a combination of keys.
* **Keyword name**: sendKeys
* **Keyword syntax**: sendKeys(windowsObject,strKeys)
* **Parameters**:
  * Name: windowsObject
    * Description: An object that describes the locator and locator strategy to find Windows Element.
    * Parameter Type: WindowsTestObject
    * Mandatory: Required
  * Name: strKeys
    * Description: A combination of keys to press.
    * Parameter Type: String
    * Mandatory: Required

## Method Keys.chord

For pressing a combination of keys, the `Keys.chord` method is used along with the `sendKeys` keyword.

* **Description**:

  > **chord() of org.openqa.selenium.Keys**
  >
  > Simulate pressing many keys at once in a "chord". Takes a sequence of Keys.XXXX or strings; appends each of the values to a string, and adds the chord termination key (`Keys.NULL`) and returns the resultant string. Note: When the low-level webdriver key handlers see `Keys.NULL`, active modifier keys (CTRL/ALT/SHIFT/etc) release via a keyup event.
  
  Please see [this document](https://www.codota.com/code/java/methods/org.openqa.selenium.Keys/chord) for further instructions and examples.
* **Method name**: Keys.chord
* **Method syntax**: Keys.chord(...)

## Example

``` groovy
//Press Ctrl+A on the Edit element
Windows.sendKeys(findWindowsObject('Object Repository/Notepad/Edit'),Keys.chord(Keys.CONTROL,'a'))
```
