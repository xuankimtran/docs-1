---
title: "[Mobile] Take Element Screenshot"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-take-element-screenshot.html
---

> From version **7.8**, this keyword is available.

## takeElementScreenshot 

*  **Description**: Take a screenshot of a specific mobile element. The captured image will be saved in '.png' format.
*  **Keyword name**: takeElementScreenshot
*  **Keyword syntax**: `Mobile.takeElementScreenshot(String fileName, TestObject to, List<TestObject> ignoredElements, Color hidingColor, FailureHandling flowControl)`
*  **Parameters**:

   * Name: fileName 
     * Description: A String that represents a path to the saved image. The path can be absolute path or relative path.
     * Parameter Type: String
     * Mandatory: Optional
     
   * Name: to
     * Description: A Test Object which represents the element you want to take screenshot of.
     * Parameter Type: TestObject
     * Mandatory: Optional

   * Name: flowControl
     * Description: Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop.
     * Parameter Type: FailureHandling
     * Mandatory: Optional

* **Examples**:

1. You want to take a screenshot of an element that you have captured by using Katalon Spy Utility and stored in Test Object > UI > logo. The file name is 'logo.png' and stored in the report folder. Default [failure handling](/x/qAAM) is used:

``` groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.configuration.RunConfiguration as RunConfiguration

Mobile.takeElementScreenshot(RunConfiguration.getReportFolder() + '/logo.png', findTestObject('UI/logo'))
```

2. You want to take a screenshot of a Test Object stored in a variable named 'header' for TestOps Vision. Use the default fileName:

``` groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

// where ignoredElements is a user-defined List-typed variable.
Mobile.takeElementScreenshot(header)
```
