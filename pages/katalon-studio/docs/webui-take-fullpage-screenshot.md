---

title: "[WebUI] Take Full Page Screenshot"

sidebar: katalon_studio_docs_sidebar

permalink: katalon-studio/docs/webui-take-fullpage-screenshot.html

---

> From version **7.7.0**, this keyword is available.

> **Warning**: If this method is used with ignored elements, JavaScript is required to be enabled on test browser. The method used to take screenshot is simulating scroll action to take screenshot to the end the page. If the web page uses infinity-scrolling then it's not recommended to use this keyword.

  

## takeFullPageScreenshot

  

*  **Description**: Take entire-page screenshot, overflow parts included. The captured image will be saved in '.png' format. This method simulates scroll action to take numbers of shot and merges them to make a full-page screenshot.

*  **Keyword name**: takeFullPageScreenshot

*  **Keyword syntax**: WebUI.takeFullPageScreenshot(fileName, ignoredElements, flowControl)

*  **Parameters**:
   * Name: fileName 

     * Description: A String that represents the path to the saved image. The path can be absolute path or relative path.

     * Parameter Type: String

     * Mandatory: Optional
     
    * Name: ignoredElements
	    * Description: List of TestObject you want to hide when taking screenshot.

       * Parameter Type: List<TestObject\>

       * Mandatory: Optional

   * Name: flowControl

     * Description: Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop.

     * Parameter Type: FailureHandling

     * Mandatory: Optional

* **Examples**:

1. You want to take full-page screenshot with default name and use default [failure handling](/x/qAAM). No elements is going to be hidden:
``` groovy
WebUI.takeFullPageScreenshot()
```
2. You want to take full-page screenshot saved to file named 'full_view_no_logo.png' in report folder and hide some web elements:
``` groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.configuration.RunConfiguration as RunConfiguration

WebUI.takeFullPageScreenshot(RunConfiguration.getReportFolder() + '/full_view_no_elements.png', [findTestObject('UI/logo')])
```
3. You want to take full-page screenshot saved to file 'E:\\full_view_no_elements.png' and hide some web elements that defined in variable named 'ignoredElements':
``` groovy
// where ignoredElements is a user-defined List-typed variable.
WebUI.takeFullPageScreenshot('E:\\full_view_no_elements.png', ignoredElements)
```