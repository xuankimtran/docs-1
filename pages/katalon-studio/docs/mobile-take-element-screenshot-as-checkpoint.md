---
title: "[Mobile] Take Element Screenshot As Checkpoint"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-take-element-screenshot-as-checkpoint.html
---

> From version **7.8**, this keyword is available.

## takeElementScreenshotAsCheckpoint

*  **Description**: Take a screenshot of a specific web element to send to TestOps Vision. The captured image will be saved in '.png' format and stored in the 'keyes' folder in the report folder.
*  **Keyword name**: takeElementScreenshotAsCheckpoint
*  **Keyword syntax**: `Mobile.takeElementScreenshotAsCheckpoint(String checkpointName, TestObject to, List<TestObject> ignoredElements, Color hidingColor, FailureHandling flowControl)`
*  **Parameters**:

   * Name: checkpointName 
     * Description: A String that represents the name of the image on TestOps Vision. On a local machine, this name will be appended with TestOps Vision prefix('keyes-').
     * Parameter Type: String
     * Mandatory: Required
     
    * Name: to
       * Description: TestObject which represents the element you want to take screenshot.
       * Parameter Type: TestObject
       * Mandatory: Required

   * Name: flowControl
     * Description: Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop.
     * Parameter Type: FailureHandling
     * Mandatory: Optional

* **Examples**:

1. You want to take a screenshot of an element that you have captured by using Katalon Spy Utility and stored in Test Object > UI > logo for TestOps Vision. The checkpoint's name is 'logo'. Default [failure handling](/x/qAAM) is used:

``` groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

Mobile.takeElementScreenshotAsCheckpoint('logo', findTestObject('UI/logo'))
```

2. You want to take a screenshot of a Test Object stored in a variable named 'header' for TestOps Vision. Set the checkpointName to 'header':

``` groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

// where ignoredElements is a user-defined List-typed variable.
Mobile.takeElementScreenshotAsCheckpoint('header', header)
```
