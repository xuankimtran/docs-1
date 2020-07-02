---
title: "Manage Mobile Test Object" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/manage-mobile-test-object.html 
---

In version 7.6, Katalon Studio fully support [selector strategies supported by Appium except for Android Data Matcher](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html).

## In Manual View

### Create a Mobile Object

We recommend creating a Mobile object by using [Katalon Mobile Spy](https://docs.katalon.com/katalon-studio/docs/spy-mobile-utility.html) since the object locators are captured automatically for detecting objects during test execution.

You can also create an object in Object Repository by right-click on **Object Repository** and selecting **New > Mobile Object**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/create-new-mobile-object.png">

The most important property of an object is its locator strategy and value. The locator should be unique in detecting that object. Select a locator strategy among the provided option and enter a locator.

Katalon Studio 7.6+ fully supports [selector strategies supported by Appium except for Android Data Matcher](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html).

### Validate Test Object on AUT

You can add test objects to **Mobile Object Spy** to verify if the object can be detected successfully in the application under test. Refer to [Spy Mobile Utility](https://docs.katalon.com/katalon-studio/docs/spy-mobile-utility.html) for more details regarding how to validate captured objects against the application under test.

To add an object to **Mobile Object Spy**, right-click on the item to open its context menu and select the option.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-mobile-test-object./add-mobile.png" width="350" height="614">

### Add an object's property

You can add multiple object properties to the Object's Properties table. Please note that object properties cannot share the same name in an object.

1. In the **Object's Properties** panel, click **Add**.
2. In the displayed **Add property** dialog, specify the required information:

* **Name**: The object property's name. You can select one of the provided options (class, css, id, name, title, xpath) or enter a name manually.
* **Match condition**: The condition is used for detecting the target object during execution.
* **Value**: The value that completes a match condition.

The new property is added to the properties list as configured above. You can also change the properties' values here.

## In Script View

**Script View** allows defining and handling **Test Objects** programmatically. The following is a usage example demonstrating how to do that:

<details><summary>In versions <strong>before 7.6</strong></summary>

## In Manual View

### Create a Mobile Test Object and its locator

To create a new Mobile test object, do as follows:

1. Select **File > New > Test Object** from the main menu.
2. In the displayed **New Test Object** dialog, provide a name for the new test object, then click **OK** button.

A new test object is created under the **Object Repository** of Katalon Studio.

Katalon Studio selects **Attributes** by default to locate mobile test objects. A test object is typically built up by a number of properties. Check on one or multiple **Detect object by** in the **Object's Properties** table to compose a **Selected Locator** for the object. During test execution, Katalon Studio bases on such information to detect an object.

In the following example, Katalon Studio tries to find any object on AUT with **text** to satisfy the defined criteria during execution.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-mobile-test-object./detect.png">

### Add an object's property

You can add multiple object properties to the Object's Properties table. Please note that object properties cannot share the same name in an object.

1. In the **Object's Properties** panel, click **Add**.
2. In the displayed **Add property** dialog, specify the required information:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-mobile-test-object./object-properties.png" width="757" height="275">

   where:

* **Name**: The object property's name. You can select one of the provided options (class, css, id, name, title, xpath) or enter a name manually.
* **Match condition**: The condition is used for detecting the target object during execution.
* **Value**: The value that completes a match condition.

The new property is added to the properties list as configured above. You can also change the properties' values here.

### Validate Test Object on AUT

You can add test objects to **Mobile Object Spy** to verify if the object can be detected successfully in the application under test. Refer to [Spy Mobile Utility](https://docs.katalon.com/katalon-studio/docs/spy-mobile-utility.html) for more details regarding how to validate captured objects against the application under test.

To add an object to **Mobile Object Spy**, right-click on the item to open its context menu and select the option.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-mobile-test-object./add-mobile.png" width="350" height="614">

## In Script View

**Script View** allows defining and handling **Test Objects** programmatically. The following is a usage example demonstrating how to do that:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-mobile-test-object./script-ex.png" width="827" height="258">

1. Refer to existing objects using the `findTestObject()` method:

```groovy
// Find an object which was defined already in Object Repository
myPredefinedObject = findTestObject('android.widget.TextView - App')
```

2. Create a new object programmatically using the `TestObject` class:

```groovy
// Create a new object programmatically
myNewObject = new TestObject("TestObjectID")
```

3. Add a property to an object using the `addProperty()` method:

```groovy
// Add property to Test Object, a property is defined by:
// property name,
// condition type,
// property value,
// a boolean value to indicate if the property will be used to identify the object during execution
myNewObject.addProperty("class", ConditionType.EQUALS, "android.widget.TextView", true)
```
