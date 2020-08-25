---

title: "[WebUI] Take Area Screenshot"

sidebar: katalon_studio_docs_sidebar

permalink: katalon-studio/docs/webui-take-area-screeenshot.html

---

> From version **7.7.0**, this keyword is available.

  

## takeAreaScreenshot

  

*  **Description**: Take screenshot of a specific area in the viewport. The captured image will be saved in '.png' format.

*  **Keyword name**: takeAreaScreenshotAs

*  **Keyword syntax**: WebUI.takeAreaScreenshot(fileName, rect, flowControl)

*  **Parameters**:
   * Name: fileName 

     * Description: A String that represents the path to the saved image. The path can be absolute path or relative path.

     * Parameter Type: String

     * Mandatory: Optinal
     
    * Name: rect
	    * Description: An Rectangle which defines location and size of the area you want to take screenshot. The area must be within the viewport.

       * Parameter Type: Rectangle

       * Mandatory: Required

   * Name: flowControl

     * Description: Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop.

     * Parameter Type: FailureHandling

     * Mandatory: Optional

* **Examples**:

1. You want to take screenshot of an area at x: 50, y: 25, width: 100, height: 150 and save to file 'advertisements.png' in report folder of current project:
``` groovy
import org.openqa.selenium.Rectangle as Rectangle
import com.kms.katalon.core.configuration.RunConfiguration as RunConfiguration

WebUI.takeAreaScreenshot(RunConfiguration.getReportFolder() + '/advertisements.png', new Rectangle(50, 25, 100, 150))
```
2. You want to take screenshot of an area at x: 50, y: 25, width: 100, height: 150 and use default filename:
``` groovy
import org.openqa.selenium.Rectangle as Rectangle

WebUI.takeAreaScreenshot(new Rectangle(50, 25, 100, 150))
```

2. You want to take screenshot of an area at x: 50, y: 25, width: 100, height: 150 and save to somewhere else:
``` groovy
import org.openqa.selenium.Rectangle as Rectangle

WebUI.takeAreaScreenshot('E:\\area.png', new Rectangle(50, 25, 100, 150))
```