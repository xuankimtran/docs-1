---
title: "[Mobile] Double Tap"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-double-tap.html
---
> Starting from **version 7.2**, this keyword is available for Mobile testing on Katalon Studio.

## doubleTap

* **Description**: Perform a double-tap action on a mobile element.
* **Keyword syntax**: Mobile.doubleTap(testObject, timeout, flowControl)
* **Parameters**:
  * Name: testObject
    * Description: Represent a mobile element.
    * Parameter Type: TestObject
    * Mandatory: Requiredz
  * Name: timeout
    * Description: System will wait at most _timeout_ (seconds) to return a result.
    * Parameter Type: int
    * Mandatory: Required
  * Name: flowControl
    * Description: Used to control the step if the step failed.
    * Parameter Type: FailureHandling
    * Mandatory: optional
* **Returns**: void.
* **Throw**: **StepFailedException** if Katalon Studio could not find the specified element.
* **Example**:

  ``` groovy
  Mobile.doubleTap(findTestObject('android.widget.Button0 - NEXT'), 0)
  ```
