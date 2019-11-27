---
title: "[Windows] Start Application with Title"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-start-app-title.html
---
> Starting from **version 7.1**, this keyword is available for Windows desktop application testing on Katalon Studio.

## startApplicationWithTitle

* **Description**: Start Windows driver and starts the Windows application at the given absolute path.
After the application starts, if WinAppDriver cannot detect the main application window correctly, Katalon Studio will use the given window title parameter to find the opened application to continue working.
* **Keyword name**: startApplicationWithTitle
* **Keyword syntax**: Windows.startApplicationWithTitle(appFile, windowTitle, flowControl)
* **Parameters**:
  * Name: appFile
    * Description: Absolute path to the Windows application.
    * Parameter Type: String
    * Mandatory: Required
  * Name: windowTitle
    * Description: Title of the opening application windows. Full text or partial text is acceptable.
    * Parameter Type: String
    * Mandatory: Required
  * Name: flowControl
    * Description: Used to control the step if the step failed.\
        STOP_ON_FAILURE: throws a StepFailedException if the step failed (default).\
        CONTINUE_ON_FAILURE: continue the test if the test failed but the test result is still failed.\
        OPTIONAL: continue the test and ignore the test result.
    * Parameter Type: FailureHandling
    * Mandatory: optional
* **Returns**: void.
* **Throw**: **StepFailedException** if Katalon Studio could not start Windows Driver, could not start the application, the application file doesn't exist or there is no application matches.object.
* **Example**:

``` groovy
Windows.startApplicationWithTitle('C:\\Program Files\\Microsoft Office\\root\\Office16\\EXCEL.exe', 'Excel')
```
