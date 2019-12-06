---
title: "[Mobile] Set Encrypted Text"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-set-encrypted-text.html
---
> Starting from **version 7.2**, this keyword is available for Mobile testing on Katalon Studio.

## setEncryptedText

* **Description**: Enter an encrypted text in an input field and clear the existing value of the input field. To encrypt a raw text, from the main menu, **Help > Encrypt Text**.
* **Keyword syntax**: Mobile.setEncryptedText(testObject, encryptedText, timeout, flowControl)
* **Parameters**:
  * Name: testObject
    * Description: Represent a mobile element.
    * Parameter Type: TestObject
    * Mandatory: Required
  * Name: encryptedText
    * Description: The encrypted text set to the mobile element.
    * Parameter Type: String
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
* **Throw**: **StepFailedException** If there are some errors during execution.
* **Example**:

    ``` groovy
    Mobile.setEncryptedText(findTestObject('New One/android.widget.EditText0 (1)'), 'IEW1vyGbESL6h22Ztkgy5Q==', 0)
    ```
