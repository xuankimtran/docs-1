---
title: "[WebUI] Take Area Screenshot"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-take-area-screenshot.html
---

> From version **7.7.0**, this keyword is available.
  
## takeAreaScreenshot  

*  **Description**: Take screenshot of a specific area in the viewport. The captured image will be saved in '.png' format.
*  **Keyword name**: takeAreaScreenshot
*  **Keyword syntax**: `WebUI.takeAreaScreenshot(fileName, rect, flowControl)`
*  **Parameters**:

   * Name: fileName 
     * Description: A String that represents the path to the saved image. The path can be absolute path or relative path.
     * Parameter Type: String
     * Mandatory: Optional
     
   * Name: rect
     * Description: A Rectangle which defines location and size of the area you want to take screenshot. The area must be within the viewport.
     * Parameter Type: Rectangle
     * Mandatory: Required

   * Name: flowControl
     * Description: Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop.
     * Parameter Type: FailureHandling
     * Mandatory: Optional

* **Examples**:

1. You want to take a screenshot of an area at x: 50, y: 25, width: 100, height: 150 and save the 'advertisements.png' file in the current project's report folder:

``` groovy
import org.openqa.selenium.Rectangle as Rectangle
import com.kms.katalon.core.configuration.RunConfiguration as RunConfiguration

WebUI.takeAreaScreenshot(RunConfiguration.getReportFolder() + '/advertisements.png', new Rectangle(50, 25, 100, 150))
```

2. You want to take a screenshot of an area at x: 50, y: 25, width: 100, height: 150 and use the default file name:

``` groovy
import org.openqa.selenium.Rectangle as Rectangle

WebUI.takeAreaScreenshot(new Rectangle(50, 25, 150, 100))
```

2. You want to take a screenshot of an area at x: 50, y: 25, width: 100, height: 150 and save it somewhere else:

``` groovy
import org.openqa.selenium.Rectangle as Rectangle

WebUI.takeAreaScreenshot('E:\\area.png', new Rectangle(50, 25, 150, 100))
```
