---
title: "[Mobile] Verify Image Present" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-verify-image-present.html 
---

## verifyImagePresent

* **Description**: Verify the given image that presents on the device screen or not.
* **Keyword syntax**: `verifyImagePresent(imageFilePath)`
* **Parameter**: imageFilePath
  * Description: Absolute path of the image
  * Parameter Type: String
  * Mandatory: Required
* **Return**: true if the image presents. Otherwise, false.
* **Example**:

    ```java
    boolean isPresent = Mobile.verifyImagePresent("/Users/myaccount/Desktop/image.png")
    assert isPresent
    ```
