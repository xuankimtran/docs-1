---
title: "[Windows] Switch to Window Title"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-switch-window-title.html
---
> From **version 7.2**, this keyword is available for Windows desktop application testing on Katalon Studio.

## switchToWindowTitle

* **Description**: Find and attach the opening application window that describes by the given windows object to the working WindowsDriver session on the current desktop by the given title.

    This keyword should be used when:
    * The main application window has been closed and replaced by another window.
    * The application has multiple working windows. We can switch among these windows.
    * We already have an opened application and need to switch to without reopening requires

* **Keyword name**: switchToWindowTitle
* **Keyword syntax**: Windows.switchToWindowTitle(windowTitle, flowControl)
* **Parameters**:
  * Name: windowTitle
    * Description: Title of the opening application windows. Full text or partial text is acceptable.
    * Parameter Type: String
    * Mandatory: Required
  * Name: flowControl
    * Description: Used to control the step if the step failed.\
        STOP_ON_FAILURE: throws a StepFailedException if the step failed (default).\
        CONTINUE_ON_FAILURE: continue the test if the test failed, but the test result is still failed.\
        OPTIONAL: continue the test and ignore the test result.
    * Parameter Type: FailureHandling
    * Mandatory: optional
* **Returns**:  The WindowsDriver after Katalon Studio switches successfully.
* **Throw**: **StepFailedException** if Katalon Studio could not find any window that matches with the given windows object.
* **Example**:

    ``` groovy
    Windows.switchToWindowTitle("Excel")
    ```

## Setting timeout

In the previous Katalon Studio's versions, users may have encountered the timeout exception during recording a Desktop application and executing a Windows test. To address this issue, from version **7.5.5**, Katalon Studio increases the default timeout for finding a Windows title from 60 to 120 seconds when recording and executing tests.

Additionally, users are allowed to change this default timeout value when using the keyword for executing tests via Script (in milliseconds) to make sure the WinAppDriver has enough time to perform the action.

```groovy
import com.kms.katalon.core.windows.keyword.helper.WindowsActionSettings

'Change the default timeout for finding a Windows title to 180000 milliseconds'
WindowsActionSettings.DF_WAIT_ACTION_TIMEOUT_IN_MILLIS = 180000;
```
