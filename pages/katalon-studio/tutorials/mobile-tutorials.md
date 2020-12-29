---
title: "Mobile Tutorials"
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
Getting Started
---------------------------------------
This Getting Started Guide gives you a quick introduction from downloading and activating to running your first automated test with **Katalon Studio**.

>You will learn:
>- How to set up your user account and application under test (AUT)
>- How to create and run your first test case using Record and Playback
>- How to view and analyze your test results
To start, select the type of the application you want to test:
   - [Web UI](link)

   - [Mobile](link)

   - [Web Service](link)

   - [Desktop](link)

### **Create first test case using Record and Playback**

To create your first test case, please do as follows.

#### **Create New Project**

1. Click on the blue *New Project* button on the side bar.
2. Name your project and choose the project type.
3. - Select a sample project in the *Project* drop-down list if you want to try it out; the corresponding *Repository URL* will be filled automatically. ([Experience here](link))
   -   Or else, select *Blank* and choose a location to store the project data on your machine.
4. Input in *Description* to describe your project.
5. Choose *Generate gitignore file* and *Generate build.gradle file* if needed > *OK*. A new project will be generated at specified location.

#### **Create First Test Case**

1. Click <img alt="Native Windows Recorder without coordinates" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-09.41.37.png" width=5%> icon to open Katalon Web Utility. The *Web recorder* dialog will be displayed.
2. Enter a URL of your web application (e.g., https://amazon.com/) and select a browser to start recording. The browser instance will be launched automatically.
3. Once the web page is loaded, interact with its elements. Your interaction will be generated automatically in Recorded Actions.
4. To stop recording, click *Stop* or go straight to *Save Script*. The browser will be closed automatically.
5. Choose where to store your script in the *Add element to Object Repository* dialog and click *OK*.
6. Input Name, Descripton and Tag (if any) in the *Test Case* dialog and click *OK*. Your test case is successfully created.

### **Execute the test case**

1. Open the test case.
2. Select one of the supported browsers: *Chrome/ Firefox/ IE/ Safari/ Edge Chromium* in the drop-down list next to the *Run* button in the main toolbar to run the script. 

> If you click *Run* without chosing browser, Chrome is set as defaut to execute the test case.
3. Wait for your excution result shown in the *Job Progress* tab. At this stage, the system will execute all your interaction with the web page's elements of the chosen test case.

### **Investigate excution results**

> Katalon Studio provides a *Job Progress* tab to show the status of your execution as well as the *Log Viewer* to let you identify potential problems that may have occurred.
#### **View Execution Log**

Once your excecution is finished, you can review the results on the *Log Viewer* views as below:

<img alt="Native Windows Recorder without coordinates" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-09.41.37.png" width=100%> 

#### **Analyze Test Results**

- If your test has **passed**, congratulation.
- If your test has **failed**, have a look at *Log Viewer* and *Console* tabs to know what happened during runtime. You should see the root cause on top of the execution log.

<img alt="Native Windows Recorder without coordinates" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-09.41.37.png" width=100%> 

Might you want to filter failed steps only, click <img alt="Native Windows Recorder without coordinates" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-09.41.37.png" width=5%> icon, the *Log Viewer* will show as follows:

<img alt="Native Windows Recorder without coordinates" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-09.41.37.png" width=100%> 

That's it! You’ve just completed your first Web UI automated test using Katalon Studio.

If you’re feeling like more testing action, go ahead and try the short tutorial on causing a test failure below.

Or, simply go to the bottom of the page for a recommendation on how to spend your next hour with Katalon Studio.