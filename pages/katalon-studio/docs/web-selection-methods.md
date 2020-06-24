---
title: "Selection Methods for Web Tests"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/web-selection-methods.html
---

Katalon Studio allows you to choose different strategies to locate WebUI objects.

To set the default selection method used in Spy/Recorder of a project:

* From 7.6 onwards: Go to **Project/Settings/Self-healing/Web UI/Test Design**
* From 7.6 backward: Go to **Project/Settings/Test Design/Web Locators**

Regarding XPath, you can additionally set the priority of XPath locators while with Attributes, you can decide which object properties to be used for recognizing objects.

You're allowed to override the global settings above in a specific object. Open an object's view, configure a selection method used for this object particularly.

## Switch Selection Method in an object's view

In an object's view, you can freely switch from one selection method to another. The detailed content of each selection method is saved automatically.

In an object's view, you can:

* Choose an object locating strategy among XPath, Attributes, CSS or Image
* Check only preferred properties of an object
* Input a desired XPath or CSS locator in the Selector Editor manually

## XPath

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/selection-methods/XPath.png">

Katalon Studio supports Smart XPath (a.k.a Relative XPath) for better object recognition. If an element cannot be consistently located using its direct attributes, Katalon Studio identifies the element by using its more robust neighbors. This method is visually intuitive as it reflects the way users often identify a visible element on the user interface.

> [Learn more about how Katalon generates Smart XPaths](https://www.katalon.com/resources-center/blog/smart-xpath-generator/)

If **XPath** is set as the default selection method when spying and recording, Katalon Studio generates a list of **Smart XPaths** automatically.

> [Learn more about how Katalon detects objects with XPath](https://docs.katalon.com/katalon-studio/tutorials/detect_elements_xpath.html)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/working-with-objects-selection-method-for-spyrecord-web/image2018-9-5-183A573A11.png)

## Attributes

A test object is typically built up by several properties. During test execution, Katalon Studio uses them to detect an object.

If **Attributes** is set as the default selection method during spying and recording, Katalon Studio generates **XPath** locator automatically that combines all the selected object properties to locate that object. Again, you can check/uncheck preferred properties in the **Object's Properties** table.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/selection-methods/Attributes.png">

## CSS

Those who wish to input their **CSS** locator of a test object manually can select the **CSS** option. Open an object's view and enter a **CSS** locator value in **Selector Editor**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/selection-methods/CSS.png">

### Change the CSS selector of an object at runtime

To change a Test Object's CSS value at runtime, you can use the following code snippet:

```java
import com.kms.katalon.core.testobject.SelectorMethod

TestObject to = findTestObject('your_test_object_id')

//Change value of CSS selector
to.setSelectorValue(SelectorMethod.CSS, 'your_desired_value')

//Change selection method from another selector to CSS selector
to.setSelectorMethod(SelectorMethod.CSS)
```

See also:

* [getSelectorCollection](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#getSelectorCollection())
* [getSelectorMethod](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#getSelectorMethod())
* [setSelectorMethod](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#setSelectorMethod(com.kms.katalon.core.testobject.SelectorMethod))
* [setSelectorValue](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#setSelectorValue(com.kms.katalon.core.testobject.SelectorMethod,%20java.lang.String))

## Image

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/selection-methods/image.png">

From 7.2.2 onwards, Katalon supports [visual object recognition](https://docs.katalon.com/katalon-studio/docs/manage-web-test-object.html#visual-object-recognition). You can learn more about [how to create image property for an object](https://docs.katalon.com/katalon-studio/docs/web-image-based-object-recognition.html)

See also

* [Self-healing Tests](https://docs.katalon.com/katalon-studio/docs/self-healing.html)
* [Generate reliable object locators](https://docs.katalon.com/katalon-studio/docs/generate_css_xpath_selector_spy_web_utility.html)
