---
title: "Fixing broken Web Test Objects with Time Capsule" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/time-capsule.html 
---
Previously, to fix a broken test object, you have to manually reproduce the state of the application under test (AUT) on failure. This approach is time-consuming. With automated tests using a Data-driven testing framework, it is even more tedious, complicating, and exhausting to reproduce the exact state of AUT manually when there is a large amount of test data.

To tackle this issue, Katalon Studio **7.8** supports restoring the AUT to the state when the test fails due to locators not finding Web UI objects. This powerful capability allows you to open a "Time Capsule" for fixing broken objects, reducing reproduction effort, and cutting off time spent on troubleshooting and maintaining your test scripts.

Notably, two enhancements assist you in optimizing the workflow of fixing your tests:

1. The test engine captures the snapshot (in HTML) of your AUT upon failures automatically. The snapshot stored in the **Report** folder of a project allows you to time-travel to AUT's state when it failed.
2. For a specific exception of `com.kms.katalon.core.webui.exception.WebElementNotFoundException: Web element with id ... not found`, you can trigger the 'Time Capsule' in either the **Log Viewer** of a Test Case or a Test Suite Report. 

> Only applicable to Web UI testing on **Chrome** browser.

This document shows you how to turn on/ off the Time Capsule and how to trigger the "Time Capsule" when a test case or a test suite fails in the following usage examples.

### Turn on/ off Time Capsule

  This extension works similar to [**Default Smart Wait**](https://docs.katalon.com/katalon-studio/docs/webui-smartwait.html#temporarily-turn-off-smart-wait). When disabled, the Time Capsule extension will not be installed, and the Time Capsule will not be generated.

   **Prior to 7.8.2**

   Time Capsule is enabled by default.

   **From 7.8.2 onwards**
   
   To turn on/ off the Time Capsule, please do as follows: 

   1. Go to **Project > Settings > Execution > WebUI**

   2. In drop-down list of **Default Time Capsule**, choose **Enable/ Disable > OK**

      <img alt="Enable Time Capsule" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/time-capsule/TS-enable.png" width=95%>

### Failed Test Case Execution scenario

Once a test case execution fails due to `com.kms.katalon.core.webui.exception.WebElementNotFoundException: Web element with id ... not found.` In **Log Viewer** of that test case, you can click on “**Click here to fix broken Test Object**” to open the captured state of the AUT with the Spy Tool automatically.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/time-capsule/test-case-fail.gif">

### Failed Test Suite execution scenario

Similarly, when a Test Suite contains at least one failed Test Case due to broken locators, in Test Suite's Result/Report, you can click on the link “**Click here to fix broken Test Object**” to open the captured state of the AUT with the Spy Tool automatically.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/time-capsule/test-suite-fail.gif">
