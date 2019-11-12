---
title: "[Mobile] Image-based Testing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-image-based-testing.html 
---

Starting from **version 7.2**, image-based testing is available for Katalon Studio Enterprise users.

This feature allows you to locate and interact with Mobile objects by their images. It is particularly helpful in the following use cases:

* Dynamic test objects without unique selectors (their values are passed through the parameters during execution) or visual objects that are traditionally identified by their orders in a list.

* Objects in a canvas of 2D or 3D game (you can conventionally identify the canvas elements, not what's inside).

Built upon Appium, image-based testing for Mobile in Katalon Studio relies on Appium's finding image objects. Read more about it [here](http://appium.io/docs/en/advanced-concepts/image-elements/). Katalon Studio automatically encodes images to Base64 for reference during test execution. The reference images will be used for finding the most matching area of the screen, which means the key to successfully finding visual elements is capturing reference images. This section will guide you through how to set up visual element testing, best practice for capturing images, and custom acceptance threshold.

## Set-up

You need the native OpenCV library in nodejs. Install [opencv4nodejs](https://www.npmjs.com/package/opencv4nodejs), which supports OpenCV 3 and OpenCV 4.

### Windows

1. Download and install [CMake](https://cmake.org/download/).
2. Add CMake binary folder to PATH in Environment Variables
3. Run the following commands

```bash
    npm install -g appium
    npm install -g windows-build-tools
    npm install -g opencv4nodejs
```

### macOS

Run the following commands

```bash
    brew update
    brew install cmake
    npm install -g appium
    npm install -g opencv4nodejs
```

**Troubleshoot**:

You may encounter this error:

```groovy
make: *** [all] Error 2
ERR! child process exited with code 2 (for more info, set '--loglevel silly') 
npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! opencv-build@0.1.9 install: `node ./install.js`
npm ERR! Exit status 1
```

That means the auto-build may fail to install opencv4nodejs, please try out with the following commands:

```bash
    brew unlink tesseract
    npm install -g opencv4nodejs
    brew link tesseract
```

### Linux

1. Download and install [CMake](https://cmake.org/download/)
2. Export CMake binary folder to PATH of Environment Variables
3. Run the following commands

```bash
    npm install -g appium
    npm install -g opencv4nodejs
```

> Note: It takes 30-40 minutes to complete the installation.

## Keywords

1. [Verify Image Present](https://docs.katalon.com/katalon-studio/docs/mobile-verify-image-present.html)
2. [Tap On Image](https://docs.katalon.com/katalon-studio/docs/mobile-tap-image.html)
3. [Find Image Element](https://docs.katalon.com/katalon-studio/docs/mobile-find-image-element.html)
4. [Find Image Elements](https://docs.katalon.com/katalon-studio/docs/mobile-find-image-elements.html)

## Capture Images

### Tutorial

Below is how to capture an image of the desired Mobile elements for interaction during test executions:

1. Start your AUT with Mobile Spy/Recorder. Remember to have your mobile device connected to Katalon Studio.

2. Click **Capture Object** to capture an image of the screen.

3. Open a screenshot in the **screenshot** folder and crop the recognition area that Katalon Studio will use for searching matching elements during test execution (reference image).

### Capture Tool and Storage

You're recommended to take a screenshot by Appium Driver in Mobile Spy/Recorder since those screenshots are automatically resized. Image size and resolution significantly affect the visual element comparison.

To find and view screenshots of the captured objects:

* macOS: **/Applications/Katalon Studio.app/Contents/MacOS/screenshot/**
* Windows: **Katalon Studio\config\screenshot**.

It is recommended to save the image representing a Mobile element in its project folder for managing objects easier.

## Acceptance Threshold

There is an acceptance threshold to define the possible outcome of image comparison. Acceptance threshold in Katalon Studio is set 0.4 by default, which means any found image with the similarity measure less than 0.4 will be rejected. This threshold is based on the default match threshold in Appium.

On the scale from 0 to 1, you can customize the acceptance threshold, which defines the degrees of match by using the `IMAGE_MATCH_THRESHOLD` option. It's recommended to use the default threshold **0.4** to find your match. If you're not finding matching objects, you can try a lower acceptance level; if the returned objects are wrongly matched, raise the threshold value. For example, to set 0.6 as the match threshold:

```groovy
Mobile.startExistingApplication('com.google.android.youtube')

MobileDriverFactory.getDriver().setSetting(Setting.IMAGE_MATCH_THRESHOLD, 0.6)

Mobile.findImageElements("/Users/demokatalon/Katalon Studio/image based testing/Screenshot/hat.png")
```
