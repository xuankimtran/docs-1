---

title: "[WebUI] Take Full Page Screenshot As Checkpoint"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-take-fullpage-screenshot-as-checkpoint.html

---

> From version **7.7.0**, this keyword is available.

**Warning**: If this method is used with the ignored elements, JavaScript is required to be enabled on test browser. The method used to take an entire-page screenshot is simulating a scroll action to the end of the page. If the web page uses infinity-scrolling, it's not recommended to use this keyword.

## takeFullPageScreenshotAsCheckpoint

*  **Description**: Take an entire-page screenshot to send to TestOps Vision. The captured image will be saved in '.png' format and stored in the 'keyes' folder in the report folder. This method simulates a scroll action, takes a numbers of shots, then merges them together to make a full-page screenshot.
*  **Keyword name**: takeFullPageScreenshotAsCheckpoint
*  **Keyword syntax**: `WebUI.takeFullPageScreenshotAsCheckpoint(checkpointName, ignoredElements, flowControl)`
*  **Parameters**:

   * Name: checkpointName 
     * Description: A String that represents the name of the image on TestOps Vision. On local machine, this name will be appended with TestOps Vision prefix('keyes-').
     * Parameter Type: String
     * Mandatory: Required
     
   * Name: ignoredElements
     * Description: List of Test Objects you want to hide when taking a screenshot.
     * Parameter Type: List<TestObject\>
     * Mandatory: Optional

   * Name: flowControl
     * Description: Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop.
     * Parameter Type: FailureHandling
     * Mandatory: Optional

* **Examples**:

1. You want to take a full-page screenshot as TestOps Vision checkpoint named 'full-page' and use default [failure handling](/x/qAAM):
``` groovy
WebUI.takeFullPageScreenshotAsCheckpoint('current_viewport')
```
2. You want to take a full-page screenshot as TestOps Vision checkpoint named 'full_view_no_logo' and hide some web elements:

``` groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

WebUI.takeFullPageScreenshotAsCheckpoint('full_view_no_elements', [findTestObject('UI/logo')])
```

3. You want to take a full-page screenshot as TestOps Vision checkpoint named 'full_view_no_elements' and hide some web elements defined in a variable named 'ignoredElements':

``` groovy
// where ignoredElements is a user-defined List-typed variable.
WebUI.takeFullPageScreenshotAsCheckpoint('full_view_no_elements', ignoredElements)
```
