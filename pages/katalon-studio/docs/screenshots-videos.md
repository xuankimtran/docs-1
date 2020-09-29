---
title: "Screenshots and Videos"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/screenshots-videos.html
---

Test scripts debugging can be time-consuming and challenging for many automation testers. Katalon Studio solves this problem by equipping you with the capabilities to capture screenshots and record videos of test execution. In this manual, you can learn how Katalon Studio takes screenshots and records videos of test runs; where those artifacts are stored and options of using them to debug.

## Screenshots

By default, you have the test engine capture screenshots automatically upon test failures. This feature is currently applicable to Web UI and Mobile testings. To turn off this function, do as follows:

* In version **7.7.5 onwards**: Go to **Project/Settings/Execution**. In the displayed **Execution** view, uncheck **Take Screenshot when execution failed** in the **During Execution Options** panel and click **OK**.
* In versions **before 7.7.5**: Go to **Project/Settings/Report**. In the displayed **Report** view, uncheck **Take Screenshot when execution failed** and click **OK**.

If you wish to take screenshots of the application under test during runtime manually, you can use the following built-in keywords for Web UI and Mobile respectively:

* [[WebUI] Take Screenshot](https://docs.katalon.com/katalon-studio/docs/webui-take-screenshot.html)
* [[WebUI] Take Screenshot As Checkpoint](https://docs.katalon.com/katalon-studio/docs/webui-take-screenshot-as-checkpoint.html) (Available in 7.7)
* [[WebUI] Take Area Screenshot As Checkpoint](https://docs.katalon.com/katalon-studio/docs/webui-take-area-screenshot-as-checkpoint.html) (Available in 7.7)
* [[WebUI] Take Area Screenshot](https://docs.katalon.com/katalon-studio/docs/webui-take-area-screenshot.html) (Available in 7.7)
* [[WebUI] Take Element Screenshot As Checkpoint](https://docs.katalon.com/katalon-studio/docs/webui-take-element-screenshot-as-checkpoint.html) (Available in 7.7)
* [[WebUI] Take Element Screenshot](https://docs.katalon.com/katalon-studio/docs/webui-take-element-screenshot.html) (Available in 7.7)
* [[WebUI] Take Full Page Screenshot As Checkpoint](https://docs.katalon.com/katalon-studio/docs/webui-take-fullpage-screenshot-as-checkpoint.html) (Available in 7.7)
* [[WebUI] Take Full Page Screenshot](https://docs.katalon.com/katalon-studio/docs/webui-take-fullpage-screenshot.html) (Available in 7.7)

* [[Mobile] Take Screenshot](https://docs.katalon.com/katalon-studio/docs/mobile-take-screenshot.html)

Screenshots are stored in

You can view it **Log Image**.

You can use the taken screenshots for visual testing with TestOps Vision. [Learn more](https://forum.katalon.com/t/update-with-katalon-studio-7-7-early-release-of-katalon-testops-visual-testing-image-comparison/45557)

## Videos

Together with execution logs and screenshots, videos are of great assistance for deciding what went wrong during the runtime of automated tests. By watching how the automated test was executed, the testing team can identify exactly where the test failed. Thus, time and resources are managed more efficiently and effectively.

> Notes
> * Video recorder is applicable to Web UI testing only.
> * For remote browsers, you're recommended to use [Katalium Server](https://docs.katalon.com/katalium-server/docs/katalium-server-katalon-studio-remote-machine.html) to view captured sessions.

## Screen Video Recorder

Screen Video Recorder captures and records what happens on a screen during runtime for non-headless Browsers testing.

Screen Video Recorder is currently available for:

* Test Suite execution. For recording **parallel execution**, please see [Browser-based Video Recorder]()
* Chrome, Firefox, Safari, Microsoft Edge, and IE

> [K-Lite Codec](https://www.codecguide.com/download_kl.htm) is recommended to play the recorded screen-based video.

Follow the steps below to see how to record screen:

### In version 7.7.5 onwards

### In versions before 7.7.5

1. After creating a test suite in Katalon Studio, go to **Project/ Settings/Report** to open the **Report** view.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/video-capturing/image2017-8-25-143A243A12.png)  

2. Check the "**Enable Video Recorder during execution**" option. By default, Katalon Studio only captures **Failed** test cases. However, you can decide to capture only the **Passed** or **Failed** test cases or both.  

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/video-capturing/image2017-8-25-153A43A45.png)  

3. Specify Video settings based on your preferences. Katalon Studio recommends AVI (`.avi`) format and low quality to save disk space. The higher the video quality is, the bigger the file size is.

* **Video format**: AVI (`.avi`) or MOV (`.mov`)
* **Video quality**: Low; Medium or High

4. After running the test suite, navigate to the **Result** tab, you can view the list of test cases in the test cases table with its video attached accordingly. Click on the play icon in the 'Video' column to play the video. Test steps descriptions are embedded as subtitles. For example, please take a look at below screenshot:  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/video-capturing/image2017-8-25-153A353A13.png)

## Browser-based Video Recorder

In version **7.7.5**, the Studio team ships browser-based video recording for both full Browsers and Headless Browsers, which is believed to be incredibly helpful for troubleshooting a failed test. With Screen Recorder, you can capture what's visible on the screen while with the Browser-based Video Recorder, you can:

* **Record video of browser window only** (Even it's hidden behind another window): Browser-based video recorder is preferred in case you are running tests when a window pops up, or the testing browser instance is hidden behind another window. 
* **Record video of Headless browser**: Headless Browser is a way to run browsers in a headless environment, which is popularly used for test automation and browser testing in CI/CD pipeline when you don't need a visible GUI. You can learn more about Headless Browser Execution in this [manual](https://docs.katalon.com/katalon-studio/docs/headless-browsers-execution.html).
* **Record videos of multiple browsers simultaneously** e.g., parallel execution of Test Suite Collection

**Preconditions**

* An active Katalon Studio Enterprise license
* Katalon Studio version 7.7.5

> Note
> * Available for Chrome, Microsoft Edge (Chromium-based), and [Headless Chrome](https://developers.google.com/web/updates/2017/04/headless-chrome). 
> * Support Test Suite and Test Suite Collection execution

The below section guides you on how to configure Browser-based video recorder in project settings and view videos.

## Configurations for Browser-based Video Recorder

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




