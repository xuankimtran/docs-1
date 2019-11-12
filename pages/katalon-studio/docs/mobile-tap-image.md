---
title: "[Mobile] Tap on Image" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-tap-image.html 
---

> This keyword, available in version 7.2+, is for Katalon Studio Enterprise users only.

## tapOnImage

* **Description**: Find the mobile element that is recognized by the given image and taps on the found element's location.
* **Keyword syntax**: `tapOnImage(imageFilePath,flowControl)`
* **Parameters**:
  * Name: imageFilePath
    * Description: Absolute path of the image
    * Parameter Type: String
    * Mandatory: Required

  * Name: flowControl
    * Description: Control the execution flow if the step fails
    * Parameter Type: FailureHandling
    * Mandatory: Optional

* **Return**: true if the image presents. Otherwise, false.
* **Example**:

    ```java
    Mobile.tapOnImage("/Users/myaccount/Desktop/image.png")
    ```
