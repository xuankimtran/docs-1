---
title: "Manage Web Test Object" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/manage-web-test-object.html 
redirect_from:
    - "/display/KD/Manage+Test+Object/"
    - "/display/KD/Manage%20Test%20Object/"
    - "/x/HoUw/"
    - "/katalon-studio/docs/manage-test-object/"
    - "/katalon-studio/docs/manage+test+object/"
    - "/katalon-studio/docs/manage%20test%20object/"
description: 
---
## Create a Test Object

1. Select **File > New > Test Object** from the main menu. The **New Test Object** dialog is displayed.  

2. Provide a name for the new test object, then click **OK** button. The new test object is created under the **Object Repository** of Katalon Studio.  

## Add an object property

> There cannot be two properties with similar names in the same test object.

1. In the **Test Object Editor**, click **Add**.  
2. The **Add property** dialog is displayed.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-web-test-object/add-property.png" width="473" height="162">

where:

* **Name**: The name of the object property. The drop-down list provides some standard options for your selection (XPath, CSS, class, id, title), or you can enter manually.
* **Match condition**: to search for the "_actual_" object in the AUT when executing automation tests.
* **Value**: to complete a match condition.

3. The new property is added to the properties list as specified. You can also edit the properties' values here.

## Manage parent object

Nowadays, there are many web applications rendering elements in an [iframe](https://www.w3schools.com/tags/tag_iframe.asp). Therefore, you have to tell your script how to traverse a website's **iframes** and select the correct **iframe** where the text and its object are present. To do so, you have to use the '[Switch To Frame](/display/KD/%5BWebUI%5D+Switch+To+Frame)' keyword before interacting with the elements.

Katalon Studio supports an ability to define parent iframe object within the test object view, so you only need to select the parent iframe, and the execution automatically switches to that iframe.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-object/image2018-9-6-103A263A6.png)

## Properties used for detecting an object

> * Available since version 5.0+
> * [How to get Web objects XPath or CSS Locator](/x/5BZO#SpyWebUtility(latest)-HowtogetwebobjectsXPathorCSSLocator)
> * [Object Identification Best Practices](/display/KD/Optimizing+Object+Identification+and+Tools)
> * Configure [Web Object Locators Settings](https://docs.katalon.com/katalon-studio/docs/web-locators-settings-since-v571.html)

### Selection Method

> Read more about [Selection Method](/x/ZxlO).

Katalon Studio allows you to choose different ways to locate objects.

#### XPath

* Katalon Studio supports _Relative XPath_ for better object recognition. If an element cannot be consistently located using its direct attributes, Katalon Studio identifies the element by using its more robust neighbors.

#### Attributes

* Katalon Studio _automatically_ generates its **XPath** combined with object **properties** to locate the object. This **XPath** is displayed in **Selector Editor**.
* A test object is typically built up by several properties. During test execution, Katalon Studio uses them to detect an object. Using the **Detect object by** field, you can determine which properties to be utilized for recognizing objects.  
  
  In the following example, Katalon Studio tries to find any object on AUT with both **text** and **XPath** to satisfy the defined criteria during execution.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-object/image2018-9-5-193A133A19.png)

#### CSS

* With CSS, you are allowed to input **CSS** locator for objects in **Selector Editor** manually.

## Validate Test Object on AUT

You can add test objects to the **Web Object Spy** dialog to verify the detection in the application under test. Refer to [Spy Web Utility (version 4.8 and below)](https://docs.katalon.com/katalon-studio/docs/spy-web-utility-version-48-and-below.html) for details regarding how to validate captured objects against the application under test.

To add an object to **Web Object Spy**, right-click on the item to open its context menu and select the option.  
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-object/image2018-9-6-103A303A22.png)

## Test Objects in Scripting View

The test case **Script View** allows you to define **Test Objects** as needed programmatically. The following is a simple sample demonstrating how to define the *Medicare* option with the Attributes, XPath and CSS selection methods.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-web-test-object/medicare.png" width="670" height="567">

Step 1: Create a new object programmatically using _TestObject_ class:

    ```groovy
    // Create a new object programmatically
    TestObject myNewObject = new TestObject('ObjectID')
    ```
    
Step 2:

* With the **Attributes** selection method, add the property to an object using _addProperty()_ method:

    ```groovy
    //Attributes
    //Add property to Test Object, a property is defined by:
    // property name,
    // condition type,
    // property value,
    // a boolean value to indicate if the property will be used to identify the object during execution
    myNewObject.setSelectorMethod(SelectorMethod.BASIC)
    myNewObject.addProperty('xpath', "//*[@id=\"appointment\"]/div/div/form/div[3]/div/label[1]", true) //Medicare
    ```

* With **XPath** and **CSS**: Specify a selection method and set a value to the locator:

    ```groovy
    //XPATH
    myNewObject.setSelectorValue(SelectorMethod.XPATH,"//*[@id=\"appointment\"]/div/div/form/div[3]/div/label[1]") //Medicare
    myNewObject.setSelectorMethod(SelectorMethod.XPATH)
    ```

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/param-web-object/xpath.png" width="379" height="126">

    ```groovy
    //CSS
    myNewObject.setSelectorValue(SelectorMethod.CSS,"#appointment > div > div > form > div:nth-child(3) > div > label:nth-child(1)") //Medicare
    myNewObject.setSelectorMethod(SelectorMethod.CSS)
    ```

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/param-web-object/css-locator.png" width="528" height="124">

The following API docs may prove useful when working with test objects:

| Class | Method | Description |
| --- | --- | --- |
| [Test Object](http://api-docs.katalon.com/studio/v4.6.0.2/api/com/kms/katalon/core/testobject/TestObject.html) | [addProperty(String name, ConditionType condition, String value)](http://api-docs.katalon.com/studio/v4.6.0.2/api/com/kms/katalon/core/testobject/TestObject.html#addProperty(java.lang.String,%20com.kms.katalon.core.testobject.ConditionType,%20java.lang.String)) | Add a new property to the test object. |
| setProperties(List <TestObjectProperty> properties) | Set the properties of the test object. |
| [getObjectId()](http://api-docs.katalon.com/studio/v4.6.0.2/api/com/kms/katalon/core/testobject/TestObject.html#getObjectId()) | Get an object ID. |
| [findPropertyValue(String name, boolean caseSensitive)](http://api-docs.katalon.com/studio/v4.6.0.2/api/com/kms/katalon/core/testobject/TestObject.html#findPropertyValue(java.lang.String,%20boolean)) | Find the value of a property using the property name.|
