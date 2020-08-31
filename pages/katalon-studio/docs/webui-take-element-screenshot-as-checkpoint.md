---

title: "[WebUI] Take Element Screenshot As Checkpoint"

sidebar: katalon_studio_docs_sidebar

permalink: katalon-studio/docs/webui-take-element-screenshot-as-checkpoint.html

---

> From version **7.7.0**, this keyword is available.

  

## takeElementScreenshotAsCheckpoint

  

*  **Description**: Take screenshot of a specific web element to send to TestOps Vision. The captured image will be saved in '.png' format and stored in 'keyes' folder in report folder.

*  **Keyword name**: takeElementScreenshotAsCheckpoint

*  **Keyword syntax**: WebUI.takeElementScreenshotAsCheckpoint(checkpointName, to, flowControl)

*  **Parameters**:
   * Name: checkpointName 

     * Description: A String that represents the name of the image on TestOps Vision. On local machine this name will be appended with TestOps Vision prefix('keyes-').

     * Parameter Type: String

     * Mandatory: Required
     
    * Name: to
	    * Description: TestObject which represents the element you want to take screenshot.

       * Parameter Type: TestObject

       * Mandatory: Required

   * Name: flowControl

     * Description: Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop.

     * Parameter Type: FailureHandling

     * Mandatory: Optional

* **Examples**:

1. You want to take TestOps Vision screenshot of an element that you captured using WebSpy and stored in Test Object > UI > logo. Checkpoint name is 'logo'. Default [failure handling](/x/qAAM) is used:
``` groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

WebUI.takeElementScreenshotAsCheckpoint('logo', findTestObject('UI/logo'))
```
2. You want to take TestOps Vision screenshot of an TestObject stored in a variable named 'header'. Set the checkpointName to 'header':
``` groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

// where ignoredElements is a user-defined List-typed variable.
WebUI.takeElementScreenshotAsCheckpoint('header', header)
```