---
title: "Web Test Object" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/manage-web-test-object.html 
redirect_from:
    - "/katalon-studio/docs/manage-test-object.html"
    - "/display/KD/Manage+Test+Object/"
    - "/display/KD/Manage%20Test%20Object/"
    - "/x/HoUw/"
    - "/katalon-studio/docs/manage-test-object/"
    - "/katalon-studio/docs/manage+test+object/"
    - "/katalon-studio/docs/manage%20test%20object/"
    - "/x/ZxlO/"
    - "/katalon-studio/docs/working-with-objects-selection-method-for-spyrecord-web/"
    - "/katalon-studio/docs/working-with-objects-selection-method-for-spyrecord-web.html"
    - "/display/KD/Working+with+Shadow+DOM+Objects/"
    - "/display/KD/Working%20with%20Shadow%20DOM%20Objects/"
    - "/x/SBNO/"
    - "/katalon-studio/docs/working-with-shadow-dom-objects/"
    - "/katalon-studio/docs/working-with-shadow-dom-objects.html"
    - "/display/KD/Change+CSS+selector+of+an+object+at+runtime/"
    - "/display/KD/Change%20CSS%20selector%20of%20an%20object%20at%20runtime/"
    - "/x/dQXR/"
    - "/katalon-studio/docs/change-css-selector-of-an-object-at-runtime/"
    - "/katalon-studio/docs/change-css-selector-of-an-object-at-runtime.html"
    - "/display/KD/Clicking+multiple+objects+without+starting+over/"
    - "/display/KD/Clicking%20multiple%20objects%20without%20starting%20over/"
    - "/x/ZwXR/"
    - "/katalon-studio/docs/clicking-multiple-objects-without-starting-over/"
    - "/katalon-studio/docs/clicking-multiple-objects-without-starting-over.html"
    - "/display/KD/Creation+of+Test+Object+in+Object+Repository+in+Runtime/"
    - "/display/KD/Creation%20of%20Test%20Object%20in%20Object%20Repository%20in%20Runtime/"
    - "/x/SAXR/"
    - "/katalon-studio/docs/creation-of-test-object-in-object-repository-in-runtime/"
    - "/katalon-studio/docs/creation-of-test-object-in-object-repository-in-runtime.html"
description: 
---

## In Manual View

### Create a test object

You can create a test object in two ways:

* From the main menu, select **File > New > Test Object**; Or
* Right-click on **Object Repository** > select **New > Test Object**

In the displayed **New Test Object** dialog, provide a name for the new test object, then click **OK** button. The new test object is created under the **Object Repository** of Katalon Studio.

Moreover, you can capture objects using Web [Spy](https://docs.katalon.com/katalon-studio/docs/spy-web-utility.html) or [Recorder](https://docs.katalon.com/katalon-studio/docs/record-web-utility.html).

### Create an object's locator

You can add multiple locators to an object but you must select one of them as a default locator. The default locator is used for detecting the object during test execution. From 7.6, you can use [Self-healing mechanism](https://docs.katalon.com/katalon-studio/docs/self-healing.html) to utilize multiple locators of an object.

Katalon Studio supports the [following selection methods](https://docs.katalon.com/katalon-studio/docs/web-selection-methods.html): XPath, Attributes, CSS and Image. You can freely switch from one selection method to another. The detailed content of each selection method is saved automatically.

* **XPath/CSS**: Enter a desired XPath locator in **Selected Locator**.
* **Image**: Browse an image to compose an image locator for the object. [Learn more](https://docs.katalon.com/katalon-studio/docs/web-image-based-object-recognition.html)
* **Attributes**: Check on one or multiple **Detect object by** in the **Object's Properties** table to compose a **Selected Locator** of this method for the object.

   You can add multiple object properties to the **Object's Properties** table. Please note that object properties cannot share the same name in an object.

1. In a **Test Object**'s view, select **Attributes** as the default Selection Method.
2. In the **Object's Properties** table, click **Add**.
2. In the displayed **Add property** dialog, specify the required information:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-web-test-object/add-property.png" width="473" height="162">

   where:

* **Name**: The object property's name. You can select one of the provided options (class, css, id, name, title, xpath) or enter a name manually.
* **Match condition**: The condition is used for detecting the target object during execution.
* **Value**: The value to complete a match condition.

   The new property is added to the properties list as configured above. You can also change the properties' values here.

## Manage parent object

Nowadays, there are many web applications rendering elements in an [iframe](https://www.w3schools.com/tags/tag_iframe.asp). Therefore, you have to tell your script how to traverse a website's **iframes** and select the correct **iframe** where the text and its object are present. To do so, you have to use the '[Switch To Frame](/display/KD/%5BWebUI%5D+Switch+To+Frame)' keyword before interacting with the elements.

Katalon Studio supports an ability to define parent iframe object within the test object view, so you only need to select the parent iframe, and the execution automatically switches to that iframe.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-object/image2018-9-6-103A263A6.png)

## In Script view

**Script View** allows defining **Test Objects** programmatically. The following example demonstrates how to define the **Medicare** option with the Attributes, XPath and CSS selection methods.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-web-test-object/medicare.png" width="670" height="567">

1. Create a new object programmatically using the `TestObject` class:

    ```groovy
    // Create a new object programmatically
    TestObject myNewObject = new TestObject('ObjectID')
    ```
2. Add an object locator

* With the **Attributes** selection method, add a property to an object using the `addProperty()` method:

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

* With **XPath** or **CSS** selection method: Specify a selection method and set a value to the locator:

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

The following Java docs may prove useful when working with test objects:

| Class | Method | Description |
| --- | --- | --- |
| [Test Object](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html) | [addProperty(String name, ConditionType condition, String value)](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#addProperty(java.lang.String,%20com.kms.katalon.core.testobject.ConditionType,%20java.lang.String)) | Add a new property to the test object. |
|| [setProperties(List &lt;TestObjectProperty&gt; properties)](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#setProperties(List%3CTestObjectProperty%3E)) | Set the properties of the test object. |
|| [getObjectId()](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#getObjectId()) | Get an object ID. |
||[findPropertyValue(String name, boolean caseSensitive)](https://docs.katalon.com/javadoc/com/kms/katalon/core/testobject/TestObject.html#findPropertyValue(java.lang.String,%20boolean)) | Find the value of a property using the property name.|

## Validate a test object

You can add test objects to the **Web Object Spy** dialog to verify the detection in the application under test. To add an object to **Web Object Spy**, right-click on the item to open its context menu and select the option.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/manage-test-object/image2018-9-6-103A303A22.png)

### Verify and Highlight

Katalon Studio **Object Properties** has a built-in **Verify and Highlight** feature to help users double-check if the web objects can be located. Katalon Studio will display the message on how many elements are **found** or **NOT found** with generated XPath locator. If the object is **found**, it will be highlighted with the **red** border.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/working-with-objects-selection-method-for-spyrecord-web/image2018-9-5-183A303A43.png)

Once finished, click **Save** to add the object to **Object Repository** as normal.

## Visual Object Recognition

**Requirements**

* Your Katalon Studio version must be 7.2.2 or later.
* You need an active Katalon Studio Enterprise license.

Image-based object recognition in web testing allows using an image representing an object to find that object during test execution. This feature proves helpful in case the web elements retain their appearances even though the underlying HTML structures have changed.

**Given** that a web element has the screenshot property.\
**When** Katalon fails to find a web element by its selected locator.\
**Then** Katalon tries using the associated screenshot to find the web element.

Using the image-based locating algorithm, Katalon Studio identifies the recognition area on the current screen based on the **target** screenshot. However, because typically a viewport of a browser is limited, what is present on the screen is also limited. Katalon attempts to scroll the page down and apply the image-based locating algorithm repeatedly. The final web element stored in the **Matched Elements** folder is the one that resembles the screenshot the most.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/fallback-strategy.gif" width="" height="">

### Enable Image-based object recognition

**From 7.6 onwards**

Image-based object recognition is enabled by default for web test execution in **Project > Settings > Self-Healing > Web UI > Test Execution** ([See Self-healing Tests](https://docs.katalon.com/katalon-studio/docs/self-healing.html)).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/image-enabled.png" width="" height="">

**Before 7.6**

By default, image-based object recognition is disabled in Project Settings. Please go to **Project > Settings > Execution** and check **Enable Image Recognition** to turn on this fallback strategy.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/enable.png" width="" height="">

### Capture screenshot and create screenshot property of an object

The ingredients required for the image-based object location to work include:

* Target screenshots of a web element
* The screenshot property of that element

There are two ways to create the required ingredients:

* [Using the built-in feature in Web Recorder and Spy](https://docs.katalon.com/katalon-studio/docs/web-image-based-object-recognition.html#use-built-in-tool)
* [Using a manual way](https://docs.katalon.com/katalon-studio/docs/web-image-based-object-recognition.html#use-other-tools)

In Tests Explorer, under the **Screenshots** folder, you can see the **Matched Elements** and **Targets** folders.

* The **Matched Elements** folder contains objects that are located by Katalon Studio based on the target images.
* The **Targets** folder is for containing the images that Katalon Studio uses for locating objects.
  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/folders.png" width="493" height="">

> For a sample project, please download [here](https://github.com/katalon-studio-samples/image-recognition-web)

### Factors Affecting Image Comparison

**Screen Resolution**: The screen resolutions of tests executing machines and screenshots capturing machines may affect the effectiveness of image comparison. We recommende capture screenshots and execute tests on the same machine for a better result.

**Capture Tool**: To capture screenshots associated with your preferred web elements, we recommend using the built-in screen-capturing feature in Web Recorder and Spy Tools. Particularly, on the expanded view after clicking **Show Captured Objects**, select the **Add Screenshot** button on the bottom right corner.
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/recorder.png" width="" height="">

## Work with Shadow DOM Objects

[Shadow DOM](https://developer.mozilla.org/en-US/docs/Web/Web_Components/Shadow_DOM) provides a powerful and useful solution for Web Developers. However, it becomes a challenge for automation testing because Shadow DOM elements inside a shadow root technically do not exist in the main document. Therefore, test automation frameworks that relying on XPath or querySelector to discover elements will not work with Shadow DOM.

Katalon Studio allows users to work with Shadow DOM elements. First, users need to use Spy Web feature to capture parent objects that contains Shadow DOM elements.

Next step is to identify the properties of Shadow DOM element and create a new object in Katalon Studio with properties defined accordingly.

In the new object setting, select **Shadow Root Parent** option and define with parent object from the firs step. This allows Katalon Studio traverse through parent object via generated CSS selector to detect Shadow DOM object by its properties (Refer to [Object Properties](/display/KD/Manage+Test+Object#ManageTestObject-Propertiesusedfordetectingobject)).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/working-with-shadow-dom-objects/image2017-8-24-153A273A58.png)

For example, the following test execution log shows Katalon Studio tried to find parent object first. Once parent object was found, Katalon Studio will try to find Shadow DOM element by CSS selector:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/working-with-shadow-dom-objects/image2017-8-24-163A43A40.png)

### Limitations

* Only for **[Chrome](http://caniuse.com/#feat=shadowdom)** browser (53 to latest Version). Other browsers will be considered for future releases.
* Only allow 1 level of nested Shadow DOM parent
* Record and Spy feature will not work with Shadow DOM (due to elements do not exist in the DOM).

## Modify object properties at runtime

If you have multiple and similar objects you want to quickly interact with during test execution, and you really don't want to spend time writing duplicate steps to interact with them, the approach below will help you reduce the time and make your code nicer:

Use CSS or XPath to locate your elements, and then you start changing the IDs (let's say). For example:

```groovy
TestObject yourObject = WebUI.modifyObjectProperty(findTestObject('Object Repository/Some object'), 'css', 'equals', '#${i}', true)
```

where 'i' is the loop counter. You can put it all inside of a loop that will read your excel sheet:

```groovy
for (def i=0; i <= fineTestData('Path to your excel').getRowNumbers(); i++) {}

```

```groovy
https://www.katalon.com/resources-center/tutorials/data-driven-testing/ for linking data with test.
```

_Credit to [Mate Mrse](https://forum.katalon.com/discussion/7010/how-to-test-clicking-multiple-objects-without-starting-over#lComment_16209)_

## Creation of Test Object in Memory at Runtime

You can create a new Test Object in Object Repository during runtime using this custom keyword:

```groovy
/**
* Construct a Katalon-compatible TestObject in memory.
* @param css (String) The CSS selector used to find the target element.
* @return (TestObject) The constructed TestObject. 
*/
@Keyword
static TestObject makeTO(String css) {
	TestObject to = new TestObject()
	to.addProperty("css", ConditionType.EQUALS, css)
	return to
}
```

_Credit to [Russ Thomas](https://forum.katalon.com/discussion/6171/creation-of-test-object-in-object-repository-in-runtime#Comment_13991)_