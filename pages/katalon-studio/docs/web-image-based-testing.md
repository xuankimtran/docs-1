---
title: "Web Image-based Testing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/web-image-based-testing.html 
redirect_from: 
    - "/katalon-studio/docs/web-image-based-object-recognition.html"
---

> Requirements:
>
>* Katalon Studio version 7.2.2 onwards.
>* An active Katalon Studio Enterprise license.

Katalon Studio provides an image locator method to associate Test Objects with images. With this method, you can perform image-based testing when elements of the web application under tests (AUT) retain their appearance even though the underlying structures have changed.

This guide shows you how to configure image-based object recognition, capture screenshots, and reduce the chance of failures in image-based testing.

## Enable Image-based object recognition

**From 7.6 onwards**

Image-based object recognition is enabled by default for web test execution in **Project > Settings > Self-Healing > Web UI > Test Execution** ([See Self-healing Tests](https://docs.katalon.com/katalon-studio/docs/self-healing.html)).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/image-enabled.png" width=70%>

<details>
<summary><strong>Before 7.6</strong></summary>

By default, image-based object recognition is disabled in Project Settings. Please go to <strong>Project > Settings > Execution</strong> and check <strong>Enable Image Recognition</strong> to turn on this fallback strategy.
<br>
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/enable.png" width=70%>
</details>

## Capture screenshots for object recognition

### Using built-in tools 

To produce images associated with captured Test objects, Katalon Studio includes the **Add Screenshot** button in both Web Recorder and Spy utility.

Here we use the **Spy Web Utility** to capture screenshots. Follow these steps:

1. To open the Spy Web Utility, from the main toolbar, select **Spy Web**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/KS-Spy-Web-Utility.png" alt="Toolbar" width=70%>

2. In the displayed **Object Spy** dialog, specify the URL of your AUT and the web browser. Click on the **Start** button to start capturing.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/KS-Object-Spy-dialog.png" alt="Object Spy dialog" width=70%>

3. To capture an object, hover your mouse cursor over the web element and press the combination of **\<Alt + \`\>** keys.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/KS-Object-Spy-capture-object.png" alt="Capture object" width=70%>

4. In the **Captured Objects** view, select the captured object and click the **Add Screenshot** button on the bottom right corner.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/KS-Object-Spy-add-screenshot.png" alt="Add screenshot" width=70%>

5. After the Spy utility verifies the image with the message **"Screenshot taken!"**, click on the **Save** button to save the captured object and its screenshot.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/KS-Object-Spy-screenshot-taken.png" alt="Screenshot taken message" width=70%>

> **Notes**
>
> * The image comparison algorithm in Katalon Studio compares a screenshot of an object with the displayed image of the corresponding web element on the active browser, pixel by pixel. Therefore, if you capture object images using other tools, you have to resize the images to the displayed sizes of the web elements on the active browser.

## Add image locator to objects

**From 7.6 onwards**

After you capture a screenshot using the Web Recorder/Spy utility, Katalon Studio automatically adds an image locator to the associated object.

To use the image locator of an object:

1. Select the object in the **Object Repository**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/KS-Object-repository-select-object.png" alt="Select the object" width=70%>

2. In the **Object** view, navigate to **Selection Method** and select the **Image** option.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/KS-Object-view-select-image.png" alt="Select the image locator" width=70%>

<details>
<summary><strong>Before 7.6</strong></summary>

After you capture a screenshot using Web Recorder/Spy utility, Katalon Studio adds a property called <strong>screenshot</strong> to the associated Test object. This property contains the absolute path to the captured screenshot.
<br>
To enable the image locator of an object:

1. Select the object in the **Object Repository**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/KS-Object-view-image-path.png" alt="Object view">

2. Select <strong>Attributes</strong> as the <strong>Selection Method</strong>.
3. In the <strong>Object's Properties</strong> table, tick the <strong>screenshot</strong> property. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/property.png" width=70% alt="Object's Properties table">
</details>

> **Notes**
>
> To add screenshots captured using other tools, provide the absolute path to the screenshot in the **Path** property when enabling the image locator.
>
> <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/KS-Object-screenshot-path.png" width=70% alt="object screenshot absolute path">

## Reduce image-based testing failures

Since reliable image-based testing depends on image comparison, you can reduce the chance of failures in two ways:

* **Screen Resolution**: The screen resolutions of screenshot capturing devices and test executing devices can affect the accuracy of image comparison. We recommend capturing screenshots and executing tests on the same device for the best results.

* **Capture tool**: We recommend using built-in capture tools in Web Recorder and Spy utility since they automatically resize the captured images.

**See also**: 

* [Sample Project](https://github.com/katalon-studio-samples/image-recognition-web)
* [Self-Healing Tests](https://docs.katalon.com/katalon-studio/docs/self-healing.html)
