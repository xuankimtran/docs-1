---
title: "[Windows] Switch to Window"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-kw-switch-window.html
---
> Starting from **version 7.2**, this keyword is available for Windows desktop application testing on Katalon Studio.

## switchToWindow

* **Description**: Find and attach the opening application window that describes by the given windows object to the working WindowsDriver session on the current desktop.

    This keyword should be used when:

    * The main application window has been closed and replaced by another window.
    * The application has multiple working windows. We can switch among these windows.
    * We already have an opened application and need to switch to without reopening requires

* **Keyword name**: switchToWindow
* **Keyword syntax**: Windows.switchToWindow(windowsObject, flowControl)
* **Parameters**:
  * Name: windowsObject
    * Description: An object that describes locator and locator strategy to find the opening application.
    * Parameter Type: WindowsTestObject.
    * Mandatory: Required.
  * Name: flowControl
    * Description: Used to control the step if the step failed.\
        STOP_ON_FAILURE: throws a StepFailedException if the step failed (default).\
        CONTINUE_ON_FAILURE: continue the test if the test failed but the test result is still failed.\
        OPTIONAL: continue the test and ignore the test result.
    * Parameter Type: FailureHandling
    * Mandatory: optional
* **Returns**: The WindowsDriver after Katalon Studio switches successfully.
* **Throw**: **StepFailedException** if Katalon Studio could not find any window that matches with the given windows object.
* **Example**:

    ``` groovy
    Windows.switchToWindow(findWindowsObject('Object Repository/Window'))
    ```
