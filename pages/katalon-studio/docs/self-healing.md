---
title: "Self-healing Tests"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/self-healing.html
---

Commonly, object locators are easily broken or unable to identify the target element when the application under test (AUT) changes. Hence creating and using correct and resilient locators are crucial to the success of Web UI test automation.

Before introducing the self-healing execution mode in version 7.6, Katalon Studio supported Auto-healing Smart XPath. This plugin recovers the broken default locator by trying other available XPath alternatives. Inheriting the idea of Auto-healing smart XPath, Katalon Studio launches a Self-healing mechanism that is more advanced and comprehensive to tackle the issue of broken locator during execution. We hope this powerful utility to reduce your test maintenance effort substantially, exceptionally when the test cases run in batch overnight.

## Self-healing mechanism

When the self-healing mode is activated (by default), and Katalon Studio fails to find an object with its default locator, Katalon tries other pre-configured locators associated with that object. If Katalon Studio finds an object by any of the alternative selectors, the test continues running using that object. When the test execution is over, Katalon Studio will propose replacing the broken locator with the locator having found the object.

Unless Katalon Studio can find the target object, depending on the [failure handling option](https://docs.katalon.com/katalon-studio/docs/failure-handling.html) that you have designed, the test execution may stop or keep going.

**Requirements**

* Katalon Studio version 7.6 onwards
* An active Katalon Studio Enterprise license

In a Katalon Studio project, you can find a screen in project settings dedicated to Self-healing. You can change the default settings to make the utility better suit your need.

* Go to **Project/Settings/Self-Healing/Web UI** or
* From the toolbar of Katalon Studio, click on the **Self-Healing** icon and select **Open Self-Healing Settings**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/selfhealing-icon.png" width=251>

## Configure Test Design

Go to **Project/Settings/Self-healing/Web UI/Test Design**, select one of the provided options to decide the default selection method used during spying and recording. Katalon Studio supports:

* [XPath](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#xpath): Once a test object is captured by using Spy/Recorder, a set of XPath locators are generated. The first value is the object's default XPath locator.
* [Attributes](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#attributes)
* [CSS](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#css)
* [Image](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#image)

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/test-design.png">

If you choose XPath or Attributes, you need to configure some additional settings:

* **XPath**: set the priority of XPath locators. Click **Reset Default** to return to the default order.
* **Attributes**: select the attributes used for detecting an object. Click **Reset Default** to return to the default setting.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/test-design-attributes.png">

## Configure Self-healing Execution

As aforementioned, Katalon Studio enables the Self-healing mode for your project by default.

You can decide which alternative locators to be used in terms of selection methods and their priorities in **Project/Settings/Self-Healing/Web UI/ Test Execution**. During execution, when Katalon fails to find an object, the selected selection methods in this global setting are used in the predefined order.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/selfhealing-execution.png">

In the **Test Execution** view:

1. Select one or multiple selection methods used for self-healing tests:

* **XPath**: If Katalon fails to detect an object with its default XPath value, other XPath options are applied automatically.
* **Attributes**
* **CSS**
* **Image**: Image-based object recognition allows using an image representing an object to find that object.

2. Prioritize the selected ones by moving them up and down.

### Exclude objects used with keywords

In some scenarios, you don't need the test engine to try out different locators to find a non-existing object. Hence, you can turn off the Self-healing mode when detecting objects used with specific keywords.

To decide which keyword to exclude from the Self-healing mode, in **Project/Settings/Self-Healing/Web UI/Test Execution**, add keywords to the exception list. When an object is used with the specified keywords in this field, Katalon Studio does not try locating that object with self-healing mode.

For example:

**Given** the `verifyElementPresent` keyword is added to the exception list, and the **input_Username_username** object's default locator is broken.

**When** we run the following block of codes:

```java
WebUI.openBrowser('https://katalon-demo-cura.herokuapp.com/')
WebUI.click(findTestObject('null'))
def username = findTestObject('Object Repository/Page_CURA Healthcare Service/input_Username_username')
WebUI.setText(username, 'John Doe')
WebUI.verifyElementPresent(username, 5)
```

**Then** the **input_Username_username** object cannot be self-healed, and the test fails as expected.

### Override in Object's view

In an Object's view, you can decide the default Selection Method for detecting that object during execution. This configuration overrides the global setting of *Self-Healing/Web UI/Test Execution* in that project.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/override.png">

## Enable and disable Self-healing mode

Self-healing mode is turned on by default in a project. If you wish to disable this mode in the project, please go to **Project/Settings/Self-Healing/Web UI/Test Execution** and uncheck **Enable self-healing execution**.

From the toolbar of Katalon Studio, click on the **Self-Healing** icon, toggle between **Enable** and **Disable Self-Healing**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/selfhealing-icon.png" width=251>

## Understand Self-healing Insights

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/self-healing-report.png">

When Katalon Studio finds an object thanks to the Self-healing mechanism, all the replacements are recorded in **Self-Healing Insights** when the test run is over. The locator replacement is **temporary** during the test run. To make the change permanent, you need to approve the change.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/Self-healing-insights.png">

Right next to the Log Viewer tab, there is a new tab called **Self-Healing Insights** which displays the following information:

* **Test Object ID**: The ID of broken test objects.
* **Broken Locator**:  The default locator that couldn't detect the object during execution.
* **Proposed Locator**: The alternative locator that located the object during execution. The proposed locator is the newly generated smart XPath of that element if the object is found by using its screenshot.
* **Recovered By**: The Selection Method that Katalon Studio used for detecting the object.
* **Screenshot**: When finding an object with its alternative locator, Katalon would capture a screenshot of the test object for you to verify whether the found object is the wanted one. Click **Preview** to check the healed object.
* **Select**: Decide which locator for you to take action.

After selecting one or multiple proposed locators, you can **discard** or **approve** the permanent replacements.

## Tutorial and Usage Example

> A sample project is available [here](https://github.com/katalon-studio/self-healing-demo#self-healing-sample-project).

### Capture objects with Recording/Spying

1. Since Self-healing is active by default, go to **Project/Settings/Self-Healing/Web UI/Test Design** to choose the default selection method during spying/recording.
2. Capture objects and change the locators as your wish

### Execute the test case

1. Go to **Project/Settings/Self-Healing/Web UI/Test Execution** to choose selection methods for self-healing execution and their order.
2. Run your test case

### Approve the replacement

1. Have a look at **Self-Healing Insights** and discover if there is any broken locator that has been recovered by Self-healing at runtime.
2. Verify if the found object is the one you expect
3. Approve the replacement to make it permanent

## Known limitations

* Only available for Web UI testing
* Image-based testing: During recording and spying, you have to decide which elements whose pictures are taken for creating an image property. It's sometimes hard to know which elements can be broken during execution. Thus, you have to take screenshots of them all manually; or predict certain elements should be backed up with an image.
