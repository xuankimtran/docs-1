---
title: "How to Capture Screenshots of Web Elements for Image-based Testing"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/web-image-based-object-recognition.html
---
## Requirements

* Your Katalon Studio version must be 7.2.2 or later.
* You need an active Katalon Studio Enterprise license.

The goal of this tutorial is to provide screenshots of web objects and their corresponding properties that the [image-based object locator algorithm](https://docs.katalon.com/katalon-studio/docs/manage-web-test-object.html#visual-object-recognition) uses when Katalon Studio fails to locate objects by other locators.

Go to **Project > Settings > Execution** and check **Enable Image Recognition** to turn on this fallback strategy.

## Use built-in tool

In order to produce the screenshots associated with web elements, Katalon Studio adds a button to Web Recorder and Spy Tool to allow users to take screenshots of their desired web elements.

Below is how to capture an image of the desired Web object for image-based object recognition during test executions.

1. Open your AUT with Recorder/Spy tools.
2. In the **Captured Objects** view, click **Add Screenshot** on the bottom right corner.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/recorder.png" width="" height="">

* Katalon Studio takes a screenshot of the selected captured object in the currently displayed screen.
* The screenshot is added to the **Targets** folder. By default, the **Screenshots/Targets** folder is created in the current project to store the screenshots of the web elements.
* A property called **screenshot** containing the absolute path to the taken screenshot is added to the corresponding Test Object.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/image-based-web-elements-recognition/property.png" width="" height="">

## Use other tools

We recommend capturing screenshots by Web Recorder/Spy Tool since it takes care of resizing screenshots to the displaying sizes of the web elements. If you capture a screen by other tools, you have to resize the images manually. Image size does affect the image comparison.

Remember to add a **screenshot** property of a Test Object manually in its **Object Details** view to point it to its image.

**See also**:

* [Factors affecting image comparison](https://docs.katalon.com/katalon-studio/docs/manage-web-test-object.html#factors-affecting-image-comparison)
* [Sample Project](https://github.com/katalon-studio-samples/image-recognition-web)
