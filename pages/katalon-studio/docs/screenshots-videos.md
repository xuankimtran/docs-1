---
title: "Screenshots and Videos"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/screenshots-videos.html
---

https://docs.cypress.io/guides/guides/screenshots-and-videos.html#Screenshots

Together with execution logs and screenshots, videos are of great assistance for deciding what went wrong during the runtime of automated tests. 

In version **7.7.5**, the Studio team ships video recording **at the browser level** for both full Browsers and Headless Browsers testings.

This document gives you more information on the new-gen video recording and shows you how to configure in project settings and view videos.

## Old-gen video recording vs. new-gen video recording

Katalon Studio has already equipped you with capturing and recording what happened on a screen during runtime for non-headless Browsers testing only. However, since it is screen-based, the video may not capture what you expect in some cases. For instance, you switch to another window while the test runs. Instead of recording the browser instance running test, it records your switching and interacting with another window.

Also, automated test with headless browsers is rising in demand. Without video recorded for headless browser testing, it isn't easy to troubleshoot a failed test.

To address the issues mentioned above, in version 7.7.5, the Studio team ships video recording **at the browser level** for both full Browsers and Headless Browsers testings, which is believed to be incredibly helpful for debugging test scripts when you know what happened during runtime.

With this new-gen of video recording, you can:

* Record browser window only (The old video recorder records the screen instead)
* Record browser window behind another window
* Record headless browser
* Record multiple browsers at the same time (e.g., when running a test suite collection having multiple test suites in parallel)

### Browser-based Video Recording for Headless Browser

### Preconditions

* An active Katalon Studio Enterprise license
* Katalon Studio version 7.7.5

> Limitation: Only available for Chrome, Microsoft Edge (Chromium-based), and [Headless Chrome](https://developers.google.com/web/updates/2017/04/headless-chrome). 

### What is Headless Browser?

Headless Browser is a way to run browsers in a headless environment, which is popularly used for test automation and browser testing in CI/CD pipeline when you don't need a visible GUI.

You can learn more about Headless Browser Execution in this [manual](https://docs.katalon.com/katalon-studio/docs/headless-browsers-execution.html).

## Configurations

To use this feature, you need to enable it in Project Settings of Katalon Studio and install a third-party library used for encoding videos.

### In Katalon Studio

1. Open your project and go to **Project/Settings/Report**
2. Enable Video Recording at the browser level

### Install FFmpeg library:

To install the FFmpeg library, do as follows:

1. Go to the [FFmpeg download web page](https://ffmpeg.org/download.html).
2. Download the package which is appropriate for your operating system.
3. Add the path to the FFmpeg executable file to your PATH environment variable.

## View recorded videos

After configuration, run your web test and see the videos in the Report folder.




