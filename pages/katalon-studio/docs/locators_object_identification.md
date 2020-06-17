---
title: "Mobile Object Locators and Identification"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/locators_object_identification.html
redirect_from:
    - "/katalon-studio/tutorials/locators_object_identification.html"
---

## Locator Strategies for detecting a mobile object

From 7.6 backwards, Katalon Studio only supports the Attributes Selection Method that allows selecting an object’s properties to generate its selector. The generated selector can be XPATH selector or in some cases, Android UiSelector.

From 7.6 onwards, Katalon Studio fully support [selector strategies supported by Appium except Android Data Matcher](http://appium.io/docs/en/commands/element/find-elements/index.html#selector-strategies), including:

1. **Accessibility ID**

2. **Class name**

3. **ID**

4. **Name**

5. **XPath** (not recommended due to performance issues)

6. **Image**

7. **Android UiAutomator**

8. **Android View Tag**

9. **iOS Predicate String**: [Learn more](http://appium.io/docs/en/writing-running-appium/ios/ios-predicate/)
10. **iOS Class Chain**: [Learn more](https://github.com/facebookarchive/WebDriverAgent/wiki/Class-Chain-Queries-Construction-Rules)

11. **Custom**: [Learn more](http://appium.io/docs/en/advanced-concepts/element-finding-plugins/)

### In Manual View

### In Script View

## Mobile Test Object's View

In versions before 7.6, a Mobile object's view is the same as a Web object's view, which is not intuitive and misleading for users to design a Mobile test object. From 7.6 onwards, Katalon Studio launches a new UI of Mobile Test Object's view that reflects our latest enhancements for better designing Mobile objects.

## Mobile Object Spy

In previous versions, you can capture and rename captured objects but cannot change a Mobile object’s locator nor verify and highlight them. From version 7.6, you can capture, edit, verify and highlight a captured object to optimize its locator.

The **Object Properties** section now allows:

* Editing locator and locator strategies of an object.
* Verifying and highlighting the object with the newly updated locator.

## Mobile Recorder

In previous versions, in Mobile Recorder you can stimulate Mobile actions but cannot add built-in actions like in Web Recorder. From version 7.6, Katalon Studio supports adding built-in and custom actions when recording. The new UI is similar to the Windows Recorder.

## Known Limitation

Katalon Studio currently doesn’t support [Android Data Matcher](http://appium.io/docs/en/commands/element/find-elements/index.html#selector-strategies) since Appium Java Client 7.1.0 doesn’t support Android Data Matcher.
