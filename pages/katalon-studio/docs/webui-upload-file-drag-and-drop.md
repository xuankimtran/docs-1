---
title: "[WebUI] Upload File by Drag-and-Drop"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-upload-file-drag-and-drop.html
---

> Your Katalon Studio version must be **7.5.0+**.

**Precondition**: For the keyword to work, the drop zone must be visible before it is used.

## uploadFileWithDragAndDrop

* **Description**: Upload files to a website by drag-and-drop
* **Keyword name**: uploadFileWithDragAndDrop
* **Keyword syntax**: `uploadFileWithDragAndDrop(TestObject to, String filePath, FailureHandling flowControl)`
* **Parameters**:
  * Name: to
    * Description: An object representing the drop zone. If unspecified, the drop zone is the website’s body element by default.
    * Parameter Type: TestObject
    * Mandatory: Optional
  * Name: filePath
    * Description: The absolute path to the file to be uploaded
    * Parameter Type: String
    * Mandatory: Required
  * Name: flowControl
    * Description: Specify failure handling schema to determine whether the execution should be allowed to continue or stop.
    * Parameter Type: FailureHandling
    * Mandatory: Optional
* **Example**: Given there is a file named `yourImage.jpg` in our project folder that needs uploading on `https://imgur.com/upload?beta`, the snippet below uses `WebUI.uploadFileWithDragAndDrop` to perform the operation. Since the website supports drag and drop on the entire webpage, we don’t have to specify a drop zone.

```groovy
import com.kms.katalon.core.configuration.RunConfiguration as RunConfiguration
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

WebUI.openBrowser('')
WebUI.navigateToUrl('https://imgur.com/upload?beta')
def filePath = RunConfiguration.getProjectDir() + '/yourImage.jpg'
WebUI.uploadFileWithDragAndDrop(filePath)
WebUI.delay(5)
WebUI.closeBrowser()
```

## Variations of the keyword usage

Some websites support uploading a file by drag-and-drop it anywhere on the page, while others only support that in a limited area. Hence, you can omit or keep the `TestObject to` parameter in corresponding use cases.

## Known Limitation

Some website (e.g., https://www.imageupload.net/?lang=en) only shows the drop zone when users drag and drop a file, which means the drop zone is not visible before this keyword is used. In this case, the keyword will not work.
