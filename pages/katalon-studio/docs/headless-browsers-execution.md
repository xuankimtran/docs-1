---
title: "Headless Browsers Execution"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/headless-browsers-execution.html
redirect_from:
    - "/display/KD/Headless+Browsers+Execution/"
    - "/display/KD/Headless%20Browsers%20Execution/"
    - "/x/CQ-R/"
    - "/katalon-studio/docs/headless-browsers-execution/"
    - "/katalon-studio/tutorials/headless_browsers_execution.html"
description:
---
In essence, headless browser testing is testing a Web page’s functionality, without the presence of a GUI. One of the major advantages of using a headless browser and performing headless testing is that you can run tests more quickly in a real browser environment. Headless browsers can save project teams a tremendous amount of time and smoothly integrate into the CI/CD process.

Katalon Studio supports headless browsers execution for both Chrome and Firefox. This tutorial will you how to execute tests using headless browsers and additional configurations (if needed) to tweak your browsers.

Configuring headless browsers
-----------------------------

By default, when executing automation tests using one of these headless browsers: [Firefox](https://developer.mozilla.org/en-US/Firefox/Headless_mode) or [Chrome](https://developers.google.com/web/updates/2017/04/headless-chrome), you don’t need to add any additional configurations.

In case you need to add more desired capabilities to those headless browsers:

* Go to **Project > Settings > Desired Capabilities > WebUI >Chrome (Headless)/Firefox (Headless)**.
* Add your desired capabilities. For example, to make your Chrome (headless) start with a smaller Window size:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/headless-browsers-execution/KS-HEADLESS-Set-DC.png" width="100%" alt="Set up desired capbilities for Chrome/Firefox (headless)">

You can learn more about desired capabilities in this document: [Desired capabilities](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html).

Executing automation tests
--------------------------

### Execute test case/test suite

*   Open a test case or test suite you want to execute.

*   Select either Chrome (headless) or Firefox (headless) from the execution items list.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/headless-browsers-execution/KS-HEADLESS-Execute-with-headless.png" width="70%" alt="Execute a test case with a headless browser">

*   Then, your current test case/test suite will be executed using the selected headless browser.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/headless-browsers-execution/KS-HEADLESS-Test%20cases-passed-with-headless-browser.png" width="70%" alt="Execute a test case with a headless browser">

### Execute test suite collection

*   Open a test suite collection that you want to execute.

*   Add a test suite into this test suite collection.

*   Select the **Run with** field.

*   Select either **Chrome (headless)** or **Firefox (headless)**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/headless-browsers-execution/KS-HEADLESS-Choose-headless-env-for-TSC.png" width="100%" alt="Execute a test suite collection with headless browsers">

*   Save changes to your current test suite collection.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/headless-browsers-execution/KS-HEADLESS-Save-headless-env-for-TSC.png" width="100%" alt="Execute a test suite collection with headless browsers">

*   Execute this test suite collection and Katalon Studio will use the selected environment to run.

### Execute using console mode execution

We recommend using the headless browser in console mode execution for faster and more continuous releases. 

*   To start, generate your console mode commands by selecting either Chrome (headless) or Firefox (headless).
*   Click the **Build CMD** button on the main toolbar.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/headless-browsers-execution/KS-HEADLESS-Command-line-for-TSC.png" width="70%" alt="Execute a test suite collection with headless browsers in console mode">

To learn more about console mode execution in Katalon, you can refer to this document: [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#use-plugins-in-console-mode).

*   Execute your tests in console mode using the *generated command script* from Katalon Studio.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/headless-browsers-execution/Execute-using-console-mode-execution-2.png" width="100%" alt="Execute a test suite collection with headless browsers in console mode">

> Notes: 
> * The headless browsers will NOT be displayed during this execution step.

