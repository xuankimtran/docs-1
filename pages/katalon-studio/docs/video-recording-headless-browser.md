---
title: "Browser-based Video Recording for Headless Browser"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/video-recording-headless-browser.html
---
Together with execution log and screenshots, videos is of great assistance for you to decide what actually went wrong during runtime. For a particular use case of test having failed due to an uninteractable element, you have more evidence to decide why it was uninteractable. 

Katalon Studio has equipped you with video recording for Web testing on GUI-ed Browsers. In version 7.7.5, the Studio team makes the capability available for Headless Browsers, which is believed to be incredibly helpful for debugging test scripts when running test with Headless Browsers.

This document gives more information about video recording in Katalon Studio and shows you how to configure this feature with a usage example.

**Preconditions**

* An active Katalon Studio Enterprise license
* Katalon Studio version 7.7.5
* Install third-party libraries

> Limitation: Only available for Chrome, Microsoft Edge (Chromium-based), and Headless Chrome. 

## What is Headless Browser?

Headless Browser 

, popularly used in CI/CD pipeline, 

debug test scripts when you know what actually happened during runtime. 

You can learn more about Headless Browser Execution in this [manual](https://docs.katalon.com/katalon-studio/docs/headless-browsers-execution.html).

## Video Recording for Headless Browser


## Video Recording at Browser level 

To distinguish different video recording capabilities, we need to include the context of each. Katalon Studio also supports capturing and recording what happened on a screen. This is prevalent in any test automation tool. However, since it is screen-based, the video may not capture what you expect in some cases, for instance, you switch to another window while the test runs. Instead of recording the browser instance running test, it records your action switching and interacting with another windows. 

To address this issue, a browser-based video recording is introduced in version 7.7.5. 



## Configurations

### In Katalon Studio

You need to enable this feature in Project settings.

1. Open your project and go to **Project/Settings/Report**
2. Enable Video Recording at browser level

### Install FFmpeg library:

The built-in video recording cannot , this alternative solution requires instalation of a third-party libary, FFmpeg

* Go to FFmpeg download page: https://ffmpeg.org/download.html
* Download the package appropriate for your operating system
* Add the path to the FFmpeg executable file to your PATH environment variable.

3. Run your test
4. Open the report folder and see the recorded video.

### Usage Examples

### Summary 

With this enhancement of video recording, you can:

* Record browser window only (The old video recorder will record all your screen instead)
* Record browser window that behind another window
* Record headless browser
* Record multiple browsers at the same time (Like when running multiple test suites in parallel in a test suite collection)



