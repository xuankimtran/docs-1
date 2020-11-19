---
title: "[Mobile] Take Element Screenshot As Checkpoint"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-take-element-screenshot-as-checkpoint.html
---

> From version **8.0**, this keyword is available.

## takeElementScreenshotAsCheckpoint

*  **Description**: Take a screenshot of a UI element to send to TestOps Vision. The test engine will scroll to this element first then taking a screenshot. The captured image will be saved to the `keyes` folder in the report.
*  **Keyword name**: takeElementScreenshotAsCheckpoint
*  **Keyword syntax**: `Mobile.takeElementScreenshotAsCheckpoint(String checkpointName, TestObject to, List<TestObject> ignoredElements, Color hidingColor, FailureHandling flowControl)`
*  **Parameters**:

   * Name: checkpointName 
     * Description: A String representing the name of the image on TestOps Vision. This name will be used to detect which baseline this checkpoint is compared with. On a local machine, this name will be appended with the TestOps Vision prefix ('keyes-').
     * Parameter Type: String
     * Mandatory: Required
     
    * Name: to
       * Description: UI element to be taken screenshot of.
       * Parameter Type: TestObject
       * Mandatory: Required

    * Name: ignoredElements 
     * Description: List of the ignored elements. These elements will be hidden by drawing an overlap color layer. If the test engine failed to hide the element by any problems, this keyword would continue without impacting the result.
     * Parameter Type: List<TestObject>
     * Mandatory: Optional
     
   * Name: hidingColor 
     * Description: The color used to draw the overlap layer. If not defined, Color.GRAY is used.
     * Parameter Type: Color
     * Mandatory: Optional

    * Name: flowControl
     * Description: Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop.
        * STOP_ON_FAILURE: throws a StepFailedException if the step fails (default).
        * CONTINUE_ON_FAILURE: continues the test if the test fails, but the test result is still FAILED.
        * OPTIONAL: continues the test and ignores the test result.
     * Parameter Type: FailureHandling
     * Mandatory: Optional

* **Return**: a String representing the path to the captured image.
* **Throw**: StepFailedException if the UI element cannot be found or Katalon Studio cannot store the image in the disk.

* **Example**: 

```java
Mobile.takeElementScreenshotAsCheckpoint('screenshot_element', findTestObject('App/screenshot_element'), [findTestObject('hide_element_1'), findTestObject('hide_element_2')], Color.GREEN)
```