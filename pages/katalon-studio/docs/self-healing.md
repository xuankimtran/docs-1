---
title: "Self-healing Tests"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/self-healing.html
---

Is is common that object locators are easily broken or unable to identify the target element when the application under test (AUT) changes. Hence creating and using correct and resilient locators are crucial to the success of Web UI test automation. Before the self-healing execution mode is introduced in version 7.6, Katalon Studio supports Auto-healing Smart XPath, which is a plugin that recovers the broken default locator by trying other available XPath alternatives. Inheriting the idea of Auto-healing smart XPath, Katalon Studio launches Self-healing mechanism which is more advanced and comprehensive to tackle the broken locator issue during execution. We hope this powerful utility to reduce your test maintenance effort substantially.

## Self-healing mechanism

When the self-healing mode is activated (by default) and Katalon Studio fails to find an object with the default locator, Katalon tries other pre-configured locators that are associated with that object. You can decide what alternative locators are in terms of selection methods and their priorities.

If Katalon Studio finds an object by any of the alternative selectors, the test continues running using that object. When the test execution is over, Katalon Studio will propose replacing the broken locator with the locator that actually detects the found object. If still Katalon Studio cannot find the target object, it depends on the [failure handling option](https://docs.katalon.com/katalon-studio/docs/failure-handling.html) that you have designed, the test execution may stop or keep going.

**Requirements**

* Katalon Studio version 7.6 onwards
* An active Katalon Studio Enterprise license

In a Katalon Studio project, you can find a screen in project settings that is dedicated to Self-healing. You can change the default settings to make the utility better suit your need.

Go to **Project/Settings/Self-healing** or from the tool bar of Katalon Studio, click on the **Self-healing** icon, select **Go to Self-healing Settings**.

<img src="">

## Configure Test Design

Go to **Project/Settings/Self-healing/Test Design**, select one of the provided options to decide the default selection method used during spying and recording an AUT to capture an object's locator. Katalon Studio supports:

* [Xpath](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#xpath): Once test objects in test cases are created by Recording or Spying feature in Katalon Studio, a set of XPath values will be generated respectively to the XPath generator provider list. The first values in the lists are the default XPath values of the test objects.
* [Attributes](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#Attributes)
* [CSS](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#css)
* [Image](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#image)

If you choose XPath or Attributes, you need to configure some additional settings:

* **XPath**: configure the priority of XPath locators. Click **Reset Default** to return to the default order
* **Attributes**: select the attributes used for detecting an object.

## Configure Self-healing Execution

As aforementioned, Katalon Studio enables Self-healing mode for your project by default in **Project/Settings/Self-Healing/Execution**. During execution, when Katalon fails to find an object, the selected selection methods in this global setting are used for self-healing in the predefined order.

In the **Self-healing Execution Settings** view:

1. Select the selection methods used for self-healing tests:

* Xpath: During execution, if a test object is failed to detect by its default XPath value, the other XPath options in the list will be automatically applied; and the first successful value will be used. The execution continues as if no failed detection has happened. This will help significantly save time updating test cases, especially when the test cases are executed in batch overnight.
* Attributes
* CSS
* Image: During execution, image-based object recognition in web testing allows using an image representing an object to find that object.

2. Prioritize selection methods for self-healing execution by moving the selected selection methods in your prefered order.

### Override in Object view

In an Object view, you can decide the default Selection Method to be used for execution, this configuration overrides the above global setting.

### Exclude objects used with keywords

In some scenarios, you don't need the test engine to take time trying out different locators to find a non-existing object; hence, you're allowed to turn off the Self-healing mode when detecting objects used with certain keywords. 

To decide which keyword to exclude from the Self-healing mode, in **Project/Settings/Self-Healing/Execution**, add keywords to the exception list. When an object is used with the specified keywords in this field, Katalon Studio does not try locating that object with self-healing mode.

For example:

**Given** we have added the `verifyElementPresent` keyword to the exception list; and the default locator of the **input_Username_username** object is broken.

**When** we run the following block of codes:

```java
WebUI.openBrowser('https://katalon-demo-cura.herokuapp.com/')
WebUI.click(findTestObject('null'))
def username = findTestObject('Object Repository/Page_CURA Healthcare Service/input_Username_username')
WebUI.setText(username, 'John Doe')
WebUI.verifyElementPresent(username, 5)
```

**Then** the **input_Username_username** object cannot be self-healed, and the test fails as expected.

## Enable and disable Self-healing mode

Self-healing mode is turned on by default in a project. If you wish to disable this mode in the project, please go to **Project/Settings/Self-Healing/Execution** and uncheck **Enable self-healing execution**.

From the tool bar of Katalon Studio, click on the **Self-healing** icon, toggle between Enable and Disable Self-healing.

## Understand Self-healing Insights

When Katalon Studio finds an object thanks to Self-healing mechanism (trying out different predefined locators of an object until it is located), all the replacements are recorded in **Self-healing Insights** when the test run is over. The replacement of locator is **temporary** during the test run. To make the change permanent, you need to approve the change.

Right next to the Log Viewer tab, there is a new tab called **Self-healing Insights** which displays the following information:

* **Test Object ID**: The ID of broken test objects.
* **Broken Locator**:  The default locator that couldn't detect the object during execution.
* **Proposed Locator**: The alternative locator that located the object during execution. If the object is found by using its screenshot, the proposed locator is the newly generated smart XPath of that element image.
* **Recovered By**: The Selection Method that Katalon Studio used for detecting the object.
* **Screenshot**: When finding an object with its alternative locator, Katalon would capture a screenshot of the test object for you to verify whether the found object is the wanted one. Click **Preview** to verify the healed object.
* **Select**: Decide which locator for you to take action.

After selecting one or multiple proposed locators, you can **discard** or **approve** the permanent replacements.

## Tutorial and Usage Example

> A sample project is available [here](https://github.com/katalon-studio/self-healing-demo#self-healing-sample-project)

### Capture objects with Recording/Spying

1. Since Self-healing is active by default, go to **Project/Settings/Self-healing/Test Design** to choose the default selection method to be used during spying/recording
2. Capture objects and change the locators as your wish

### Execute the test case

1. Go to **Project/Settings/Self-healing/Execution** to choose selection methods to be used for self-healing execution and their order.
2. Run your test case

### Approve the replacement

1. Have a look at **Self-healing Insights** and discover if there is any broken locator that has been recovered by Self-healing at runtime.
2. Verify if the found object is really the one you expect
3. Approve the replacement to make it permanent

## Known limitations

* Only available for WebUI testing
* Image-based testing: During recording and spying, you have to decide which elements whose pictures are taken for creating an image property. It's sometimes hard to know which elemnt can be broken during execution, which means you have to taking pictures of them all manually; or predict certain elements should be backed up with an image.
