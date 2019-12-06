---
title: "[Mobile] Long Press"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-long-press.html
---
> Starting from **version 7.2**, this keyword is available for Mobile testing on Katalon Studio.

## longPress

* **Description**: Perform a long press action on a mobile element.
* **Method**: longPress
* **Keyword syntax**: Mobile.longPress(testObject, timeout, flowControl)
* **Parameters**:
  * Name: testObject
    * Description: Represent a mobile element.
    * Parameter Type: TestObject
    * Mandatory: Required
  * Name: timeout
    * Description: System will wait at most _timeout_ (seconds) to return a result.
    * Parameter Type: int
    * Mandatory: Required
  * Name: flowControl
    * Description: Used to control the step if the step failed.
    * Parameter Type: FailureHandling
    * Mandatory: Optional
* **Returns**: void.
* **Throw**: **StepFailedException** if Katalon Studio could not find the specified element.
* **Example**:

    ``` groovy
    Mobile.longPress(findTestObject('android.widget.Button0 - NEXT'), 0)
    ```
