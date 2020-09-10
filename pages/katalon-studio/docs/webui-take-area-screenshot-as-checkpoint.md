---
title: "[WebUI] Take Area Screenshot As Checkpoint"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-take-area-screenshot-as-checkpoint.html
---

> From version **7.7.0**, this keyword is available.

## takeAreaScreenshotAsCheckpoint

*  **Description**: Take screenshot of a specific area in the viewport to send to TestOps Vision. The captured image will be saved in '.png' format and stored in 'keyes' folder in report folder.
*  **Keyword name**: takeAreaScreenshotAsCheckpoint
*  **Keyword syntax**: `WebUI.takeAreaScreenshotAsCheckpoint(checkpointName, rect, flowControl)`
*  **Parameters**:

   * Name: checkpointName 
     * Description: A String that represents the name of the image on TestOps Vision. On local machine this name will be appended with TestOps Vision prefix('keyes-').
     * Parameter Type: String
     * Mandatory: Required
     
   * Name: rect
     * Description: A Rectangle which defines location and size of the area you want to take screenshot. The area must be within the viewport.
     * Parameter Type: Rectangle
     * Mandatory: Required

   * Name: flowControl
     * Description: Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop.
     * Parameter Type: FailureHandling
     * Mandatory: Optional

* **Examples**:

You want to take TestOps Vision screenshot of an area at x: 50, y: 25, width: 100, height: 150 :

``` groovy
import org.openqa.selenium.Rectangle as Rectangle

WebUI.takeAreaScreenshotAsCheckpoint('advertisements', new Rectangle(50, 25, 150, 100))
```
