---
title: "[WebUI] Enhanced Click" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-enhanced-click.html
---

> Your Katalon Studio version must be **7.2.5+**.

> Warning: This keyword uses Javascript click as the last fallback which may not have the same effect as an actual click on an element.

## enhancedClick

* **Description**: Click on the given element using various trial-and-error methods
* **Keyword name**: Enhanced Click
* **Keyword syntax**: `enhancedClick(TestObject to, FailureHandling flowControl)`
* **Parameters**:
  * Name: to
    * Description: An object representing a web element
    * Parameter Type: TestObject
    * Mandatory: Required
  * Name: flowControl
    * Description: Specify failure handling schema to determine whether the execution should be allowed to continue or stop.
    * Parameter Type: FailureHandling
    * Mandatory: Optional
* **Throw**: StepFailedException
* **Example**:

```groovy
'Open browser and navigate to demo AUT site.'
WebUI.openBrowser(GlobalVariable.G_SiteURL)

'Click on \'Book Appointment\' button'
WebUI.enhancedClick(findTestObject('Page_CuraHomepage/btn_MakeAppointment'))

'Close browser'
WebUI.closeBrowser()
```
