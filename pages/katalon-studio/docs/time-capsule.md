---
title: "Fixing broken Web Test Objects with "time capsule"" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/time-capsule.html 
---
Previously, to fix a broken test object, you have to manually reproduce the state of the application under test (AUT) on failure. This approach is time-consuming. With automated tests using Data-driven testing framework, it is even more tedious, complicating and exhausting to reproduce the exact state of AUT manually when there is a large amount of test data.

To tackle this issue, Katalon Studio **7.8** supports restoring the AUT to the state it was when the test failed due to locators not finding objects for Web UI testing. This powerful capability allows you to open a "time capsule" for fixing broken objects, which reduces reproduction effort, and cuts off time spent on troubleshooting and maintaining your test scripts. 

> Only applicable to Web UI testing.

## How to trigger a "time capsule"

Currently, if your Web tests fail due to broken test objects. You can trigger the time capsule in either the **Log Viewer** of a Test Case or a Test Suite **Report**. Specifically, you can see links right next to broken objects. Click on the links to open the captured snapshot (in HTML) of the AUT with the Spy Tool automatically. In the opened web page, you can re-capture the broken object with Spy Tool as usual.

## Usage Examples

### Failed Test Case Execution scenario

**Given** a test case execution fails due to broken locators.
**When** users click on the Test Case row in Log Viewer.
**Then**:

* Users should see a link: “Click here to fix broken Test Object”.
* Clicking on the link opens the Spy Tool at the captured state of the AUT.
* Trigger the Given Prerequisites of Fix broken test objects scenarios

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/time-capsule/test-case-fail.gif">

### Failed Test Suite execution scenario

**Given** a Test Suite execution contains at least one Test Case that fails due to broken locators.
**When** users view the Test Suite report.
**Then**:

* Users should see link “Open in Spy Tool”.
* Clicking on the link opens the Spy Tool at the captured state of the AUT.
* Trigger the Given Prerequisites of Fix broken test objects scenarios

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/time-capsule/test-suite-fail.gif">


