---
title: "Installation Overview"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/getting-started.html
redirect_from:
    - "/display/KD/Getting+Started/"
    - "/display/KD/Getting%20Started/"
    - "/display/KD/Installation+and+Setup/"
    - "/x/l4Ei/"
    - "/katalon-studio/docs/getting-started/"
    - "/display/KD/Before+You+Start/"
    - "/display/KD/Before%20You%20Start/"
    - "/x/HwAM/"
    - "/katalon-studio/docs/before-you-start/"
    - "/katalon-studio/docs/before-you-start.html"
    - "/katalon-studio/tutorials/install_setup_katalon_studio.html"
    - "/display/KD/Installation+and+Setup/"
    - "/display/KD/Installation%20and%20Setup/"
description:
---

## Environment Requirements

Verify whether your device meets the [System Requirements](http://docs.katalon.com/display/KD/System+Requirements) to run Katalon Studio.

## Download Katalon Studio

* [Download](https://www.katalon.com/download/) the latest Katalon Studio version. Our system will automatically detect a suitable version for your device, but you can also select a preferred one. 
* Do a quick check on [System Requirements](/display/KD/System+Requirements) before using Katalon Studio.

> [Download](https://github.com/katalon-studio/katalon-studio/releases) **older versions** of Katalon Studio.

## Start Katalon Studio

### For Windows

To open **Katalon Studio**, double-click on the *katalon.exe*.

![Download and Start Katalon Studio](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/install_setup_katalon_studio/Starting-Katalon-Studio.png)

Ensure you are using Katalon Studio with the default font size set to 100% in both Katalon Studio and your current OS to avoid the name field not being displayed on some > *pop-up windows*:
* Windows: [https://www.pcworld.com/article/242942/how\_to\_change\_font\_size.html](https://www.pcworld.com/article/242942/how_to_change_font_size.html)
* Katalon Studio: *Window* → *Preferences* → *General* → *Appearance* → *Colors and Fonts*. Select **Dialog Font** and edit the font size.

### For macOS

**Katalon Studio** (macOS) file is stored where you unpack it.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/install_setup_katalon_studio/Katalon-MacOS.png "init-size")

> **For macOS Catalina users:**
> 
> If you currently use macOS Catalina, you have to enable Katalon Studio and Katalon Studio Engine applications in  *System Preferences/ Security & Privacy/ General*.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/getting-started/KS-Catalina.png" width="662" height="569"> 

Once started, the application should display the splash screen similar to the following screenshot:

![Katalon Studio Loading](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/install_setup_katalon_studio/image2016-10-20-143A113A21.png)

## Activate Katalon Studio

If you do not have a Katalon Studio account, sign up after the app is launched. If you already have one, please read more about [Katalon Studio Licensing](https://docs.katalon.com/katalon-studio/docs/license.html) and how to activate each license. 

## Configure Katalon Studio

### Configurations for Web UI Testing

* If you want to conduct a **Web Testing**, make sure to install your preferred web browser. For more details, please refer to the [supported browsers list](/display/KD/Supported+Environments).

* **Katalon Automation Recorder** extension is required to capture objects in **Active Browser** referring to [Spy Web Utility](/x/5BZO#SpyWebUtility(sinceversion5.0.0)-CaptureobjectsusingWebObjectSpy) and [Record & Playback](/display/KD/Record+Web+Utility). Please follow this [guide](/x/JYgw) for more information.

* **Internet Explorer** must be configured to run automation tests on IE. Kindly check on the [IE configurations guide](/x/iwEo) for your reference.

### Configurations for Mobile UI Testing

* [Mobile on Windows](/display/KD/Mobile+on+Windows)

* [Mobile on macOS](/display/KD/Mobile+on+macOS)

Get a Sample Project Up and Running
---------------------------------------

When you use Katalon Studio for the first time, you will have an option to create New Project or Sample Projects to get familiar with the tool.

- Create a new sample project in *File → New Sample Project* and select your preferred one. Name and choose where to store the project data on your device.

- When the sample project is loaded, you can view a test case or a test suite by selecting in the *Tests Explorer* on the left of the UI.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/getting-started/Screen-Shot-2018-09-06-at-2.32.06-PM.png)

- To execute the script, go to the *Run* command on the Main toolbar. You can specify the target browser to be launched by selecting from the _Run_ drop-down list.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/getting-started/Screen-Shot-2018-09-06-at-2.33.04-PM.png)

**Katalon Studio** provides a **Job Progress** tab to show the status of your execution as well as the **Log Viewer** to let you identify any potential problems that may occur.

That's it! Open a project and execute a test using Katalon Studio now. Try to modify parts of those provided sample projects to get familiar with the tool.

## Where to Go Next?

### Katalon TestOps

[Katalon TestOps](https://analytics.katalon.com) is a set of cloud-based services to help you streamline software quality by continuous test executions and intelligent analytics. As this moment, Katalon TestOps consists of the following services:

* **Katalon TestOps Center**: the test hub to gather and connect quality data from multiple sources, including Katalon Studio, JUnit, TestNG, and Jira.
* **Katalon TestOps CI**: the CI for managing test environments and scheduling remote executions on local machines, Kubernetes, and CircleCI. It is designed and built with ease of deployment and configuration in mind to let QAs focus on testing activities.
* **Katalon TestOps Reports**: provide dynamic perspectives and an insightful look at your automated testing activities.
* **Katalon TestOps Vision**: the visual-based testing service which is powered by AI to identify new defects on application GUIs quickly.
