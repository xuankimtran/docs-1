---
title: "Version 7.2 (Beta)" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-72.html
redirect_from:
    - "/katalon-studio/new/version-72/"
    - "/katalon-studio/new/"
    - "/display/KD/Release+Notes/"
    - "/display/KD/Release%20Notes/"
    - "/katalon-studio/new/all-versions.html"
description: Release note 7.2 (Beta)
---

### New Features

* Windows keywords: [`getElementPosition`](https://docs.katalon.com/katalon-studio/docs/windows-kw-get-element-position.html), [`getElementRect`](https://docs.katalon.com/katalon-studio/docs/windows-kw-get-element-rect.html), [`startApplicationWithTitle`](https://docs.katalon.com/katalon-studio/docs/windows-kw-start-app-title.html), [`switchToWindow`](https://docs.katalon.com/katalon-studio/docs/windows-kw-switch-window.html), and [`switchToWindowTitle`](https://docs.katalon.com/katalon-studio/docs/windows-kw-switch-window-title.html).
* Mobile keywords: [`executeMobileCommand`](https://docs.katalon.com/katalon-studio/docs/mobile-execute-command.html), [`doubleTap`](https://docs.katalon.com/katalon-studio/docs/mobile-double-tap.html), [`longPress`](https://docs.katalon.com/katalon-studio/docs/mobile-long-press.html), and [`setEncryptedText`](https://docs.katalon.com/katalon-studio/docs/mobile-set-encrypted-text.html).
* Mobile actions: Get Text, Swipe, Scroll To Text,
* Support adding [Proxy Exceptions](https://docs.katalon.com/katalon-studio/docs/proxy-preferences.html).

### Changes and Improvements

* Add **Profiles** to Test Suite Collection Report.
* [Mobile- iOS] Support **Install Dependencies** and **Install WebDriverAgent** tools on the main menu. [Learn more]().
* [Command Syntax] Support both `-serverUrl` and `-serverURL` arguments.
* Enhance Mobile Recorder Utility.
* Make the `DriverFactory.changeWebDriver()` method a public method.
* [Test Explorer] Support **Open containing folder**: Right-click on a test artifact in Test Explorer > **Open containing folder**.

### Fixes

* Bug: [Windows] An issue related to creating a project.
* Bug: An issue related to saving Web Service Message.
* Bug: Missing paren in method call after editting test steps in Test Scripts.
* Bug: Empty result tab after a Test Suite execution.
* Bug: Test Script lost parens in method call after editing some steps
* Bug: [KRE] an issue related to `retry` option
* Bug: [Web] Cannot set timeout in **Wait for options**
* Bug: [Web Service Request] an issue related to saving HTTP Header.
