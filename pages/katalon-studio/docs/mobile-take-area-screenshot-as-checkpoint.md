---
title: "[Mobile] Take Area Screenshot As Checkpoint"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-take-area-screenshot-as-checkpoint.html
---

> From version **7.9**, this keyword is available.

## takeAreaScreenshotAsCheckpoint

*  **Description**: Take a screenshot of a specific area to send to TestOps Vision. The area should be inside the application viewport; otherwise, this keyword will fail.
*  **Keyword name**: takeAreaScreenshotAsCheckpoint
*  **Keyword syntax**: `Mobile.takeAreaScreenshotAsCheckpoint(String checkpointName, Rectangle rect,List<TestObject> ignoredElements, Color hidingColor, FailureHandling flowControl)`
*  **Parameters**:

   * Name: checkpointName 
     * Description: A String representing the name of the image on TestOps Vision. This name will be used to detect which baseline this checkpoint is compared with. This name will be appended with the TestOps Vision prefix ('keyes-') on a local machine.
     * Parameter Type: String
     * Mandatory: Required
     
   * Name: rect
     * Description: A rectangle definding the position and size of the area to be captured.
     * Parameter Type: Rectangle
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
        * STOP_ON_FAILURE: throws a StepFailedException if the step failed (default).
        * CONTINUE_ON_FAILURE: continues the test if the test failed, but the test result is still Failed.
        * OPTIONAL: continues the test and ignores the test result.
     * Parameter Type: FailureHandling
     * Mandatory: Optional

* **Return**: a String representing the path to the captured image.
* **Throw**: StepFailedException if the defined rectangle is outside the application viewport or Katalon Studio can't store the image in the disk.

* **Example**:

``` groovy
// add import libs first
import org.openqa.selenium.Rectangle as Rectangle
// take sreenshot of an area start at (x: 0 , y: 0) with size (height: 1500, width: 1000)
Mobile.takeAreaScreenshotAsCheckpoint('screenshot_area', new Rectangle(0, 0, 1500, 1000), [findTestObject('hide_element_1'), findTestObject('hide_element_2')], Color.BLUE)
```
