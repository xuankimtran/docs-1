---
title: "Self-healing Tests"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/self-healing.html
---

Is is common that object locators are easily broken or unable to identify the target element when the application under test (AUT) changes. Hence creating and using correct and resilient locators are crucial to the success of Web UI test automation. Before the self-healing execution mode is introduced in version 7.6, Katalon Studio supports Auto-healing Smart XPath, which is a plugin that recovers the broken default locator by trying other available XPath alternatives.

Inheriting the idea of auto-healing smart XPath, Katalon Studio launches Self-healing mechanism which is more advanced and comprehensive to tackle the broken locator issue during execution. We hope this powerful utility to reduce your test maintenance effort substantially.

## Self-healing mechanism

When the self-healing mode is activated (by default) and Katalon Studio fails to find an object with the default locator, Katalon tries other pre-configured locators that are associated with that object. You can decide what alternative locators are and their priorities.

If Katalon Studio finds an object by any of the alternative selectors, the test continues running using that object. When the test execution is over, Katalon Studio will propose replacing the broken locator with the locator that actually detects the found object. If still Katalon Studio cannot find the target object, it depends on the [failure handling option](https://docs.katalon.com/katalon-studio/docs/failure-handling.html) that you have designed, the test execution may stop or keep going.

**Requirements**

* Katalon Studio version 7.6 onwards
* An active Katalon Studio Enterprise license
* Only available for WebUI testing

In a Katalon Studio project, you can find a screen in project setting that is dedicated to Self-healing. You can change the default settings to make the utility better suit your need.

**Project/Settings/Self-healing**

<img src="">

### Configure Test Design

Go to **Project/Settings/Self-healing/Test Design**, select one of the provided options to decide the default selection method used during spying and recording an AUT to capture an object's locator. Katalon Studio supports:

* [Xpath](): Once test objects in test cases are created by Recording or Spying feature in Katalon Studio, a set of XPath values will be generated respectively to the XPath generator provider list. The first values in the lists are the default XPath values of the test objects. During execution, if a test object is failed to detect by its default XPath value, the other XPath options in the list will be automatically applied; and the first successful value will be used. The execution will continue as if no failed detection has happened. This will help significantly save time updating test cases, especially when the test cases are executed in batch overnight.
* [Attributes]()
* [CSS]()
* [Image]()

If you choose XPath or Attributes, you need to configure some additional settings:

* **XPath**: configure the priority of XPath locators. Click **Reset Default** to return to the default order
* **Attributes**: select the attributes used for detecting an object.

### Configure Self-healing Execution

As aforementioned, Katalon Studio enables Self-healing mode for your project by default in **Project/Settings/Self-Healing/Execution**. During execution, the selected selection methods in this global setting are used for self-healing in the predefined order.

In the **Self-healing Execution Settings** view:

1. Select the selection methods used for self-healing tests:

* [Xpath](): During execution, if a test object is failed to detect by its default XPath value, the other XPath options in the list will be automatically applied; and the first successful value will be used. The execution will continue as if no failed detection has happened. This will help significantly save time updating test cases, especially when the test cases are executed in batch overnight.
* [Attributes]()
* [CSS]()
* [Image]()

2. Move the selected selection methods in your prefered order.

To override

In an Object’s detailed view, decide the default selection method to be used during test execution, this config overrides the config in Project/Settings/Self-Healing/ Execution

Exclude objects used with keywords: List out specific keywords that would not apply Self-Healing when it is enabled.
Ex: As the settings above, we have the following script:
We need to heal the input_Username_username object. But when we run to the 5th line, it would fail because self-healing would not apply to verifyElementPresent.

```java
WebUI.openBrowser('https://katalon-demo-cura.herokuapp.com/')
WebUI.click(findTestObject('null'))
def username = findTestObject('Object Repository/Page_CURA Healthcare Service/input_Username_username')
WebUI.setText(username, 'John Doe')
WebUI.verifyElementPresent(username, 5)
```

## Execution with Self-healing mode

, when Katalon fails to find an object, different strategies to locate the target object in the predefined order.



It is active by default for a project

Decide which locators are used and their priority

Decide which keyword to exclude from the Self-healing mode

When an object is used with the specified keywords in this field, Katalon Studio does not try locating that object with self-healing mode.

### Enable and disable Self-healing mode

Enable self-healing execution: Tick the radio button for enabling self-healing execution. Or we can click the Self-Healing icon on the main screen, choose Enable Self-Healing.

Prioritize selection methods for self-healing execution: Change the order of Selection Methods by dragging/dropping or using buttons and choose which Selection Methods to be used. So, when applying Self-Healing mode, Katalon Studio will auto Self-Healing with chosen and ordered Selection Methods.


Turn off the Self-healing mode

 Go to Project/Settings/Self-Healing/Execution

Uncheck the option Enable Self-Healing execution

### Understand Self-healing Insights

The replacement is temporary during the test run. After the test run is over, to make the change permanent, users should approve the change.
For elements found by their screenshots, Katalon Studio generates smart locators for that element and suggests the replacement of the default XPath with the newly generated XPath.

* Test Object ID: The ID of broken test objects.
* Broken Locator:  The current locator of the test object that caused broken.
* Proposed Locator:  The suggestion of another locator that helps find the test object.
* Recovered By: The Selection Method that Self Healing used to recover the test object.
* Screenshot: After healing, Katalon would capture that test object, so that the user can verify it.
* Approve: Users can choose which test object(s) can be healed.

Click Preview in the Screenshot column to verify the healed object.

Discard All: Click Discard All if you don’t want to update the broken test object as proposed.

Approve: Tick the radio button in the Approve column to choose which one to be approved. Click Approve. So that chosen objects will be updated as suggested.

### Sample Usage

## Known limitations
