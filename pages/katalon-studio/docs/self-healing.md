---
title: "Self-healing Tests"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/self-healing.html
---

> Requirements
>
> * Katalon Studio version 7.6.0 onwards
> * An active Katalon Studio Enterprise license

When the application under test (AUT) changes, object locators might be broken or unable to identify the target element. Hence, creating and using correct, resilient locators are crucial to the success of Web UI test automation.

From Katalon Studio version 7.6.0, Katalon Studio supports the self-healing mechanism to tackle the issue of broken locators during execution. This feature can reduce your test maintenance effort substantially, exceptionally when the test cases run in batch overnight.

This article will guide you through:

* Understanding the self-healing mechanism
* Configuring and executing a test with the self-healing feature
* Viewing self-healing insights and replacing broken locators

We also prepare a sample project for you to try out. You can clone or download a sample project from our GitHub repository: [Self-healing sample project](https://github.com/katalon-studio/self-healing-demo#self-healing-sample-project).

## Self-healing mechanism

With the self-healing enabled, when Katalon Studio fails to find an object with its default locator, Katalon tries other pre-configured locators associated with that object.

If Katalon Studio finds an object by any of the alternative selectors, the test continues running. Once the broken object is self-healed, the alternative locator finding the object is used for that particular broken test object for the remaining execution. This helps shorten execution time by preventing self-healing from taking place again and again with the same broken object.

When the test execution is over, Katalon Studio proposes replacing the broken locator with the locator having found the object. Unless Katalon Studio can find the target object, depending on the failure handling option that you have designed, the test execution may stop or keep going. To learn more about the failure handling option, see [Failure Handling](https://docs.katalon.com/katalon-studio/docs/failure-handling.html).

## Configure Test Design

To learn how to configure test design, see [Configure Test Design](http://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#configure-test-design).

## Configure Self-healing Execution

### Enable and disable Self-healing mode

In Katalon Studio, the self-healing feature is enabled by default. To disable the self-healing mode, there are two ways:

* Go to **Project > Settings > Self-Healing > WebUI**, then uncheck the box **Enable Self-healing execution**.
* From the toolbar of Katalon Studio, click on the **Self-Healing** icon, then select **Disable Self-healing**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/selfhealing-icon.png" width=30%>

### Locator Method

You can decide which alternative locators to be used in terms of selection methods and their priorities. During execution, when Katalon fails to find an object, the selected selection methods in this global setting are used in the predefined order.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/self-healing-settings.png" alt="self-healing" width="100%">

Under the line **Select and prioritize element locator methods for Self-healing execution**, your can find a the **Element locator method** table.

1. Select one or multiple selection methods used for self-healing tests:

* **XPath**: If Katalon fails to detect an object with its default XPath value, other XPath options are applied automatically.
* **Attributes**
* **CSS**
* **Image**: Image-based object recognition allows using an image representing an object to find that object.

2. Prioritize the selected ones by moving them up and down.

3. If you click on **Configure default locator**, you are redirect to the **Test Design** section.

### Exclude objects used with keywords

In some scenarios, you don't need the test engine to try out different locators to find a non-existing object. Hence, you can turn off the self-healing mode when detecting objects used with specific keywords. For example, the `verifyElementPresent` and `verifyElementNotPresent` are excluded by default.

To decide which keyword to exclude from the Self-healing mode, go to **Project > Settings > Self-Healing > Web UI**, then add keywords to the exception list. When an object is used with the specified keywords in this field, Katalon Studio does not try locating that object with the self-healing mode.

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

Then the **input_Username_username** object cannot be self-healed, and the test fails as expected.

### Override in Object's view

In an Object's view, you can decide the default Selection Method for detecting that object during execution. This configuration overrides the global setting of *Self-Healing/Web UI/Test Execution* in that project.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/Override-object-view.png" alt="override object view" width="70%">

## Self-healing Insights

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/self-healing-report.png">

When Katalon Studio finds an object thanks to the Self-healing mechanism, all the replacements are recorded in **Self-Healing Insights** when the test run is over. The locator replacement is **temporary** during the test run. To make the change permanent, you need to approve the change.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/self-healing/self-healing-insights-766.png">

Right next to the Log Viewer tab, there is a new tab called **Self-Healing Insights** which displays the following information:

* **Test Object ID**: The ID of broken test objects.
* **Broken Locator**:  The default locator that couldn't detect the object during execution.
* **Proposed Locator**: The alternative locator that located the object during execution. The proposed locator is the newly generated smart XPath of that element if the object is found by using its screenshot.
* **Recovered By**: The Selection Method that Katalon Studio used for detecting the object.
* **Screenshot**: When finding an object with its alternative locator, Katalon would capture a screenshot of the test object for you to verify whether the found object is the wanted one. Click **Preview** to check the healed object.
* **Select**: Decide which locator for you to take action.

After selecting one or multiple proposed locators, you can **discard** or **approve** the permanent replacements.

## Tutorial and Usage Example

> You can clone or download a sample project from our GitHub repository: [Self-healing sample project](https://github.com/katalon-studio/self-healing-demo#self-healing-sample-project).

### Capture objects with Recording/Spying

1. Since Self-healing is active by default, go to **Project > Settings > Test Design > Web UI** to choose the default selection method during spying/recording.
2. Capture objects and change the locators as your wish.

### Execute the test case

1. Go to **Project > Settings > Self-Healing > Web UI** to choose selection methods for self-healing execution and their order.
2. Run your test case

### Approve the replacement

1. Have a look at **Self-Healing Insights** and discover if there is any broken locator that has been recovered by Self-healing at runtime.
2. Verify if the found object is the one you expect.
3. Approve the replacement to make it permanent.

> Known limitations
>
> * Only available for Web UI testing.
> * Image-based testing: During recording and spying, you have to decide which elements whose pictures are taken for creating an image property. It's sometimes hard to know which elements can be broken during execution. Thus, you have to take screenshots of them all manually; or predict certain elements should be backed up with an image.
