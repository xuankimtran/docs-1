---
title: "Manage Mobile Test Object" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/manage-mobile-test-object.html 
---

In version 7.6, Katalon Studio fully support [selector strategies supported by Appium except Android Data Matcher](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html).

## Create a Test Object

**From 7.6 onwards**

Right-click on **Object Repository** and select **New > Mobile Object**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-selector-strategies/create-new-mobile-object.png">

**Before 7.6**

1. Select **File > New > Test Object** from the main menu. The **New Test Object** dialog will be displayed.  

2. Provide the name for the new test object, then click **OK** button. A new test object is created under the **Object Repository** of Katalon Studio.  

## Add an object property

> There cannot be two properties with the same name in the same test object.

1. In the **Object's Properties** panel, click **Add**.  
2. The **Add property** dialog will be displayed.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-mobile-test-object./object-properties.png" width="757" height="275">

   where:

* **Name**: The name of the object property. The drop-down list provides some common options for your selection (XPath, CSS, class, id, title) or you can enter manually.
* **Match condition**: The condition is used for searching for the "_actual_" object in the AUT when executing automation tests.
* **Value**: The value that completes a match condition.

3. The new property is added to the properties list as specified. You can also edit the properties' values here.

## Properties used for detecting an object

Katalon Studio selects **Attributes** by default to locate mobile test objects. A test object is typically built up by a number of properties. During test execution, Katalon Studio bases on such information to detect an object. Using **Detect object by** field, you can determine the properties to be utilized for recognizing objects.  

In the following example, Katalon Studio tries to find any object on AUT with **text** tp satisfy the defined criteria during execution.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-mobile-test-object./detect.png">

## Validate Test Object on AUT

You can add test objects to **Mobile Object Spy** dialog to verify detection in the application under test. Refer to [Spy Mobile Utility](https://docs.katalon.com/katalon-studio/docs/spy-mobile-utility.html) for details regarding how to validate captured objects against the application under test.

To add an object to **Mobile Object Spy**, simply right-click on the item to open its context menu and select the option.  

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-mobile-test-object./add-mobile.png" width="350" height="614">

## Test Objects in Scripting View

The test case **Script View** allows you to programmatically define and handle **Test Objects** as needed. The following is a simple sample demonstrating how to do that:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-mobile-test-object./script-ex.png" width="827" height="258">

1. Refer to existing objects using the _findTestObject()_ method:

```groovy
// Find an object which was defined already in Object Repository
myPredefinedObject = findTestObject('android.widget.TextView - App')
```

2. Create a new object programmatically using _TestObject_ class:

```groovy
// Create a new object programmatically
myNewObject = new TestObject("TestObjectID")
```

3. Add the property to an object using _addProperty()_ method:

```groovy
// Add property to Test Object, a property is defined by:
// property name,
// condition type,
// property value,
// a boolean value to indicate if the property will be used to identify the object during execution
myNewObject.addProperty("class", ConditionType.EQUALS, "android.widget.TextView", true)
```
