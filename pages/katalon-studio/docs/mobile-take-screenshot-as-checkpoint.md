---
title: "[Mobile] Take Screenshot As Checkpoint"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-take-screenshot-as-checkpoint.html
---

> From version **7.9**, this keyword is available.

## takeScreenshotAsCheckpoint

*  **Description**: Take a screenshot of the current application to send to TestOps Vision. The captured image will be saved to the **keyes** folder in the report. The screenshot will not include OS's status and navigation bars.
*  **Keyword name**: takeScreenshotAsCheckpoint
*  **Keyword syntax**: `Mobile.takeScreenshotAsCheckpoint(String checkpointName, List<TestObject> ignoredElements, Color hidingColor, FailureHandling flowControl)`
*  **Parameters**:

   * Name: checkpointName 
     * Description: A String representing the name of the image on TestOps Vision. This name will be used to detect which baseline this checkpoint is compared with. This name will be appended with the TestOps Vision prefix ('keyes-') on a local machine.
     * Parameter Type: String
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
* **Throw**: StepFailedException If the test engine can't store the image in the disk.
* **Example**:

``` groovy
Mobile.takeScreenshotAsCheckpoint('screenshot_keyes', [findTestObject('hide_element_1'), findTestObject('hide_element_2')], Color.RED, FailureHandling.STOP_ON_FAILURE)
```
