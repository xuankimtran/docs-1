---
title: "Selection Methods for Web Tests"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/web-selection-methods.html
---

In Web UI automated testing, a primary concern for testers is high maintenance costs of test scripts, which are usually caused by unstable and broken locators. A locator is a mechanism used by Selenium to identify an element during test execution. 



### Selection Method

Katalon Studio allows you to choose different ways to locate objects.

#### XPath

* Katalon Studio supports _Relative XPath_ for better object recognition. If an element cannot be consistently located using its direct attributes, Katalon Studio identifies the element by using its more robust neighbors.

> Learn more about [Smart XPath (_a.k.a._ Relative XPath).](https://www.katalon.com/resources-center/blog/smart-xpath-generator/)

Katalon Studio supports _Relative XPath_ for better object recognition. If an element cannot be consistently located using its direct attributes, Katalon Studio will identify the element by using its more robust neighbors. This method is visually intuitive as it reflects the way users often identify a visible element on the user interface.

If **Xpath** option is selected, Katalon Studio will automatically generate a list of **Relative Xpath** based on your _Web Locators Setting_ to identify the element.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/working-with-objects-selection-method-for-spyrecord-web/image2018-9-5-183A573A11.png)

#### Attributes

* Katalon Studio _automatically_ generates its **XPath** combined with object **properties** to locate the object. This **XPath** is displayed in **Selector Editor**.
* A test object is typically built up by several properties. During test execution, Katalon Studio uses them to detect an object. Using the **Detect object by** field, you can determine which properties to be utilized for recognizing objects.  
  
  In the following example, Katalon Studio tries to find any object on AUT with both **text** and **XPath** to satisfy the defined criteria during execution.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-object/image2018-9-5-193A133A19.png)

If _Attributes_ option is **selected**, Katalon Studio will automatically generate **XPath** locator that **combined** all **selected** object **properties** to locate that object. You can _checked/unchecked_ preferred properties in the object **properties table.**

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/working-with-objects-selection-method-for-spyrecord-web/image2018-9-5-183A293A36.png)

## CSS

* With CSS, you are allowed to input **CSS** locator for objects in **Selector Editor** manually.

Test engineers who wish to manually input their own **CSS** locator for test objects can select CSS option. Once selected, object **properties table** will be **collapsed** and **Selector Editor** field becomes **editable**. Simply provide **CSS** locator in the _Selector Editor_ text box. 

Same as Attributesoption, click on **Verify and Highlight** button to make sure Katalon Studio can locate the web objects. Katalon Studio will display the message on how many elements are **found** or **NOT** **found** with input XPath or CSS locator. If the object is **found**, it will be highlighted with the **red **border. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/working-with-objects-selection-method-for-spyrecord-web/image2018-9-5-183A503A16.png)

Once finished, click **Save** to add objects to **Object Repository** as normal.

### Change CSS selector of an object at runtime

To change a Test Object's CSS value at runtime:

```groovy
import com.kms.katalon.core.testobject.SelectorMethod

TestObject to = findTestObject('your_test_object_id')

//Change value of CSS selector
to.setSelectorValue(SelectorMethod.CSS, 'your_desired_value')

//Change selection method from another selector to CSS selector
to.setSelectorMethod(SelectorMethod.CSS)
```

See also:

* [getSelectorCollection](https://api-docs.katalon.com/com/kms/katalon/core/testobject/SelectorCollector.html#getSelectorCollection())
* [getSelectorMethod](https://api-docs.katalon.com/com/kms/katalon/core/testobject/SelectorCollector.html#getSelectorMethod())
* [setSelectorMethod](https://api-docs.katalon.com/com/kms/katalon/core/testobject/SelectorCollector.html#setSelectorMethod(com.kms.katalon.core.testobject.SelectorMethod))
* [setSelectorValue](https://api-docs.katalon.com/com/kms/katalon/core/testobject/SelectorCollector.html#setSelectorValue(com.kms.katalon.core.testobject.SelectorMethod,%20java.lang.String))

## Image

From 7.2.2 onwards, Katalon supports visual object recognition, so-called image-based testing. 
Please see image-based testing 


> * Katalon Studio **Object Properties** has the capability to **auto-save** the content of **Selector Editor** when switching between modes of **Selection Method**.

Katalon Studio **Object Properties** makes Spying and Recording Web feature easier and more powerful. Enhanced Object Properties allows users:

* Choose objects locating strategies including XPath, Attributes, CSS or Image.
* Check only preferred object's properties on the grid.
* Manually input the desired XPath or CSS locator in Selector Editor.