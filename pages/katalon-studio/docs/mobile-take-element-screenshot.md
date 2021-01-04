---
title: "[Mobile] Take Element Screenshot"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-take-element-screenshot.html
---

> From version **7.9**, this keyword is available.

## takeElementScreenshot 

*  **Description**: Take a screenshot of a UI element to send to TestOps Vision. The test engine will scroll to this element first then taking a screenshot.
*  **Keyword name**: takeElementScreenshot
*  **Keyword syntax**: `Mobile.takeElementScreenshot(String fileName, TestObject to, List<TestObject> ignoredElements, Color hidingColor, FailureHandling flowControl)`
*  **Parameters**:

   * Name: fileName 
     * Description: Absolute path to the stored image file. fileName should contain '.png' as images are stored to the '.png' format. If the file name is not defined, Katalon Studio will generate a random file name.
     * Parameter Type: String
     * Mandatory: Optional
     
   * Name: to
     * Description: UI element to be taken screenshot of.
     * Parameter Type: TestObject
     * Mandatory: Optional

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
* **Throw**: StepFailedException if the UI element cannot be found or Katalon Studio cannot store the image in the disk.

* **Example**:

``` groovy
// add import libs first
import com.kms.katalon.core.configuration.RunConfiguration as RunConfiguration
// take element screenshot and store to report folder
Mobile.takeElementScreenshot(RunConfiguration.getReportFolder() + '/element_screenshot.png', findTestObject('App/screenshot_element'), [findTestObject('hide_element_1'), findTestObject('hide_element_2')], Color.GREEN)
```
