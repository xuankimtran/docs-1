---
title: "[Mobile] Find Image Element" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-find-image-element.html 
---

> This keyword, available in version 7.2+, is for Katalon Studio Enterprise users only.

## findImageElement

* **Description**: Find the mobile element that is recognized by the given image.
* **Keyword syntax**: `findImageElement(imageFilePath,flowControl)`
* **Parameters**:
  * Name: imageFilePath
    * Description: Absolute path of the image
    * Parameter Type: String
    * Mandatory: Required

  * Name: flowControl
    * Description: Control the execution flow if the step fails
    * Parameter Type: FailureHandling
    * Mandatory: Optional

* **Return**: The first found WebElement that is recognized by the given image.

* **Example**:

    ```java
    WebElement element = Mobile.findImageElement("/Users/myaccount/Desktop/image.png")
    println "Element found at: (" + element.getPosition().x + ", " + element.getPosition().y + ")"
    ```
