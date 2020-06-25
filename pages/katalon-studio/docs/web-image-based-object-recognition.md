---
title: "How to Capture Screenshots of Web Elements for Image-based Testing"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/web-image-based-object-recognition.html
---

## Requirements

* Your Katalon Studio version must be 7.2.2 or later.
* You need an active Katalon Studio Enterprise license.

This tutorial shows you how to capture screenshots of web objects and create their corresponding properties used for the [image-based object locator algorithm](https://docs.katalon.com/katalon-studio/docs/manage-web-test-object.html#visual-object-recognition).

**From 7.6 onwards**

Image-based object recognition is enabled by default for web test execution in **Project > Settings > Self-Healing > Web UI > Test Execution** ([See Self-healing Tests](https://docs.katalon.com/katalon-studio/docs/self-healing.html)).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/image-enabled.png" width="" height="">

**Before 7.6**

By default, image-based object recognition is disabled in Project Settings. Please go to **Project > Settings > Execution** and check **Enable Image Recognition** to turn on this fallback strategy.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/enable.png" width="" height="">

## Use built-in tool

### Capture screenshots

In order to produce the screenshots associated with web elements, Katalon Studio adds a button to Web Recorder and Spy Tool to allow users to take screenshots of their desired web elements.

Below is how to capture an image of the desired Web object:

1. Open your AUT with Recorder/Spy tools.
2. In the **Captured Objects** view, select a captured object and click **Add Screenshot** on the bottom right corner.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/recorder.png" width="" height="">

   Katalon Studio takes a screenshot of the selected captured object in the currently displayed screen. The screenshot is added to the **Targets** folder. By default, the **Screenshots/Targets** folder is created in the current project to store the screenshots of the web elements.

## Image locator added automatically

**From 7.6 onwards**

After capturing a screenshot using Spy/Recorder, an image locator is added to that object automatically. In an Object's view, select **Image** as the Selection Method and you can see the created image locator.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/image-locator.png">

**Before 7.6**

After capturing a screenshot using Spy/Recorder, a property called **screenshot** containing the absolute path to the taken screenshot is added to the corresponding Test Object. To view this property, select **Attributes** as the Selection Method. In the **Object's Properties** table, you can see the **screenshot** property.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/property.png" width="" height="">

## Use other tools

We recommend capturing screenshots by Web Recorder/Spy Tool since it takes care of resizing screenshots to the displaying sizes of the web elements. If you capture a screen by other tools, you have to resize the images manually. Image size does affect the image comparison.

### Create an image locator

**From 7.6 onwards**

1. In an Object's view, select **Image** as the Selection Method
2. In **Path**, browse your target image and **Save**

**Before 7.6**

1. In an Object's view, select **Attributes** as the Selection Method
2. In the **Object's Properties** table, add a **screenshot** property that points its image and **Save**

**See also**:

* [Factors affecting image comparison](https://docs.katalon.com/katalon-studio/docs/manage-web-test-object.html#factors-affecting-image-comparison)
* [Sample Project](https://github.com/katalon-studio-samples/image-recognition-web)
* [Self-Healing Tests](https://docs.katalon.com/katalon-studio/docs/self-healing.html)
