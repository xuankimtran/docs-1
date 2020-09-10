---

title: "[WebUI] Take Screenshot As Checkpoint"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-take-screenshot-as-checkpoint.html

---

> From version 7.7.0, this keyword is available.

## takeScreenshotAsCheckpoint

*  **Description**: Take screenshot of current view-port to send to TestOps Vision. The captured image will be saved in '.png' format and stored in 'keyes' folder in report folder.
*  **Keyword name**: takeScreenshotAsCheckpoint
*  **Keyword syntax**: `WebUI.takeScreenshotAsCheckpoint(checkpointName, flowControl)`
*  **Parameters**:

   * Name: checkpointName 
     * Description: A String that represents the name of the image on TestOps Vision. On local machine this name will be appended with TestOps Vision prefix('keyes-').
     * Parameter Type: String
     * Mandatory: Required

   * Name: flowControl
     * Description: Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop.
     * Parameter Type: FailureHandling
     * Mandatory: Optional

* **Examples**:

1. You want to take screenshot as checkpoint named 'current_viewport' for TestOps Vision and use default [failure handling](/x/qAAM):

``` groovy
WebUI.takeScreenshotAsCheckpoint('current_viewport')
```

2. You want to take screenshot as checkpoint named 'full_view' for TestOps Vision, and need the test to keep running regardless of this step having failed or passed:

``` groovy
import com.kms.katalon.core.model.FailureHandling as FailureHandling

WebUI.takeScreenshotAsCheckpoint('full_view', FailureHandling.CONTINUE_ON_FAILURE)
```
