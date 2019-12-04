---
title: "[Mobile] Find Image Elements" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-find-image-elements.html 
---

> This keyword, available in version 7.2+, is for Katalon Studio Enterprise users only.

## findImageElements

* **Description**: Find  all mobile elements that are recognized by the given image.
* **Keyword syntax**: `findImageElements(imageFilePath,flowControl)`
* **Parameters**:
  * Name: imageFilePath
    * Description: Absolute path of the image
    * Parameter Type: String
    * Mandatory: Required

  * Name: flowControl
    * Description: Control the execution flow if the step fails
    * Parameter Type: FailureHandling
    * Mandatory: Optional

* **Return**: A list of WebElements that are recognized by the given image.

* **Example**:

    ```java
    List<WebElement> elements = Mobile.findImageElements("/Users/myaccount/Desktop/image.png")
    println "Number of elements found: " + elements.size()
    ```
