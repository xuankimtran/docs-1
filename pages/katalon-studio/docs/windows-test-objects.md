---
title: "Windows Test Objects"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-test-objects.html
---

## Manage Windows Test Objects

### Create a test object

1. Select **File > New > Windows Object** from the main menu. The **New Windows Object** dialog is displayed.
2. Provide a name for the new test object, then click **OK** button to create a new object under the **Object Repository** of Katalon Studio.

### Locator strategy for detecting an object

Built upon Windows Application Driver, Katalon Studio supports 6 locator strategies to identify UI elements of a Desktop application. You can choose different ways to locate a Windows test object.

* **Accessibility ID**: The AutomationId of an object

  * E.x.: `AppNameTitle`
  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/windows-test-objects/accessibility-id.png" width="" height="">

* **Class Name**: The ClassName property of an object

  * E.x.: TextBlock
  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/windows-test-objects/class-name.png" width="" height="">

* **ID**: The unique runtime ID of an object

  * E.x.: 42.333896.3.1
  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/windows-test-objects/runtime-id.png" width="" height="">

* **Name**: The name of an object

  * E.x.: Calculator
  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/windows-test-objects/name.png" width="" height="">

* **Tag Name**: The tag name (aka the element type) of an object

  * E.x.: `Text`
  <img src="" width="" height="">

* **XPath**

  * E.x.: `//Button[0]`
  <img src="" width="" height="">

### Test Objects in Script View

The Script View of a test script allows you to define Windows objects programmatically. Below are the code snippets of an object with different locator strategies.

**ACCESSIBILITY_ID**

```java
WindowsTestObject wo = new WindowsTestObject('')
wo.setLocatorStrategy(LocatorStrategy.ACCESSIBILITY_ID)
wo.setLocator("accessibility id value here")
```

**CLASS_NAME**

```java
WindowsTestObject wo = new WindowsTestObject('')
wo.setLocatorStrategy(LocatorStrategy.CLASS_NAME)
wo.setLocator("classname value here")
```

**ID**

```java
WindowsTestObject wo = new WindowsTestObject('')
wo.setLocatorStrategy(LocatorStrategy.ID)
wo.setLocator("id here")
```

**NAME** 

```java
WindowsTestObject wo = new WindowsTestObject('')
wo.setLocatorStrategy(LocatorStrategy.NAME)
wo.setLocator("name here")
```

**TAG_NAME** 

```java
WindowsTestObject wo = new WindowsTestObject('')
wo.setLocatorStrategy(LocatorStrategy.TAG_NAME)
wo.setLocator("tag name here")
```

**XPATH**

```java
WindowsTestObject wo = new WindowsTestObject('')
wo.setLocatorStrategy(LocatorStrategy.XPATH)
wo.setLocator("XPATH here")
```

### Verify and Highlight

Katalon Studio Windows Object Spy and Recorder have a built-in **Highlight** feature that allows double-checking if the Windows objects are able to be located.

Katalon Studio displays a message on how many elements are found or NOT found with the selected locator strategy and locator. If the object is found, it will be highlighted with the **green** border.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/windows-test-objects/name-highlight.png" width="" height="">

## Parameterize Windows Test Objects

> Parameterizing Windows test objects is available in version 7.3.0+.

The benefit of parameterizing test objects in general is to handle object with dynamic properties ([Read more](https://docs.katalon.com/katalon-studio/docs/manage-web-test-object.html#parameterize-web-test-objects)). With this feature, you can update test objects' locators dynamically by using either local or global variables.

Here are the steps demonstrating how to use this feature:

1. Select a Windows object you want to parameterize
2. Capture its locator with Katalon Studio Windows Object Spy or Recorder and create a variable with this syntax `${variable_name}` as a place holder for its dynamic locator. For example, we create the `${xpath}` variable for the XPATH locator strategy. You can parameterize test objects with other locator strategies as well.
3. Use the parameterized test object.

### In Manual View

Open your Test Case in the **Manual** View and double-click on the object that you want to parameterize its locator.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/windows-test-objects/img_manual.png" width="" height="">

In the displayed **Test Object Input** dialog, declare the expected dynamic locator as a variable in the **Variables** panel.

* **Param Type**: the variable type (The default type is String).
* **Param**: the variable name.
* **Value Type**: the type of the variable's value.
* **Value**: a specific value of that variable.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/windows-test-objects/img_test_object_input.png" width="" height="">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/windows-test-objects/img_variables.png" width="" height="">

For instance, Katalon Studio uses the `xpath` variable created in step 2, with its specific value as `//Button[0]` to find the `txt_UserName` object.

### In Script View

Once the locator is declared, you can switch to the **Script** View and modify the perceived value of the locator. Typically, users want to pass the locator value as a variable or refer to data files.

The general syntax to find a Windows test object using a dynamic locator is as follows:

```java
findWindowsTestObject('{your test object}', [('{variable}') : '{value of variable}'])
```

For example:

```java
findWindowsObject('New Windows Object', [('xpath') : '//Button[0]'])
```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/windows-test-objects/img_script_view.png" width="" height="">