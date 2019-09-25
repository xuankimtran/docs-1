---
title: "Parameterize Mobile Test Object"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/parameterize-mobile-test-object-properties.html
---
> Parameterizing Mobile Test Object Properties is only available with the **Attributes** Selection Method.

The benefits of parameterizing mobile test objects are similar to those of parameterizing web test objects. Refer to [this document](https://docs.katalon.com/katalon-studio/docs/parameterize-web-test-object-properties.html) for further details.

Below is an example of how to parameterize test objects in Mobile testing. Open a sample project of Mobile testing on Android devices by accessing **File> New Sample Project> Sample Android Mobile Tests Project**.

Navigate to **Object Repository/Application/android.widget.TextView - App** in Test Explorer, open the test object view of `android.widget.TextView - App` whose property will be parameterized.

In this example, we want to find a test object that has `//*[(text() = 'demokatalon' or . = 'demokatalon')]` as its selector. Here are the steps to apply this feature:

Step 1: Parameterize the test object's dynamic property

Create a property with its value as a variable having this syntax: `${Variable_name}`. For this example, in the **Object's Properties** panel, add an object's property with:

* Name: `text`
* Value: `${text}`

Its selected locator is generated as `//*[(text() = '${text}' or . = '${text}')]` and identified at runtime with passing data.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/param-mobile-object/selector.png" width="" height="">

Step 2: Use the parameterized test object in a test case

**In Manual View**

In the `Verify Correct Alarm Message` test case, double-click the test object that contains the parameterized property, which is `android.widget.TextView - App`. The **Test Object Input** dialog is displayed.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/param-mobile-object/test-case.png" width="" height="">

In the Variable panel, add a new variable with the following properties:

* Param Type: the variable type (The default type is String).
* Param: the variable name of the property created in step 1.
* Value Type: the type of the variable's value.
* Value: a specific value of that variable.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/param-mobile-object/test-object-input.png" width="" height="">

**In Scripting View**

You can also switch to the **Scripting Mode** of the current Test Case to adjust the property's value at any time. The predefined variable is automatically mapped when you select a mobile object from manual mode, so you don't need to define them again manually. In this example, the `tap` keyword is performed on the object with the text value that we have just specified.

```groovy
Mobile.tap(findTestObject('Application/android.widget.TextView - App', [('text') : 'demokatalon']), 10)
```
