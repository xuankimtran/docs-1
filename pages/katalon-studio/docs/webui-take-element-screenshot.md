---

title: "[WebUI] Take Element Screenshot"

sidebar: katalon_studio_docs_sidebar

permalink: katalon-studio/docs/webui-take-element-screeenshot.html

---

> From version **7.7.0**, this keyword is available.

  

## takeElementScreenshot

  

*  **Description**: Take screenshot of a specific web element. The captured image will be saved in '.png' format.

*  **Keyword name**: takeElementScreenshot

*  **Keyword syntax**: WebUI.takeElementScreenshot(fileName, to, flowControl)

*  **Parameters**:
   * Name: fileName 

     * Description: A String that represents the path to the saved image. The path can be absolute path or relative path.

     * Parameter Type: String

     * Mandatory: Optional
     
    * Name: to
	    * Description: TestObject which represents the element you want to take screenshot.

       * Parameter Type: TestObject

       * Mandatory: Optional

   * Name: flowControl

     * Description: Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop.

     * Parameter Type: FailureHandling

     * Mandatory: Optional

* **Examples**:

1. You want to take screenshot of an element that you captured using WebSpy and stored in Test Object > UI > logo. Filename is 'logo.png' and stored in report folder. Default [failure handling](/x/qAAM) is used:
``` groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.configuration.RunConfiguration as RunConfiguration

WebUI.takeElementScreenshot(RunConfiguration.getReportFolder() + '/logo.png', findTestObject('UI/logo'))
```
2. You want to take TestOps Vision screenshot of an TestObject stored in a variable named 'header'. Use default fileName:
``` groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

// where ignoredElements is a user-defined List-typed variable.
WebUI.takeElementScreenshot(header)
```