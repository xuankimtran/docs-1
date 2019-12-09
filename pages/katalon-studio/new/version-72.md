---
title: "Version 7.2 (Beta)" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-72.html
description: Release note 7.2 (Beta)
---

## Version 7.2 (Beta)

A beta version of Katalon Studio 7.2 can be downloaded [here](https://github.com/katalon-studio/katalon-studio/releases).

> Note: This version is not available on the [Katalon downloading web page](https://www.katalon.com/download/).

### New Features

* Windows keywords: [`getElementPosition`](https://docs.katalon.com/katalon-studio/docs/windows-kw-get-element-position.html), [`getElementRect`](https://docs.katalon.com/katalon-studio/docs/windows-kw-get-element-rect.html), [`startApplicationWithTitle`](https://docs.katalon.com/katalon-studio/docs/windows-kw-start-app-title.html), [`switchToWindow`](https://docs.katalon.com/katalon-studio/docs/windows-kw-switch-window.html), and [`switchToWindowTitle`](https://docs.katalon.com/katalon-studio/docs/windows-kw-switch-window-title.html).
* Mobile keywords: [`executeMobileCommand`](https://docs.katalon.com/katalon-studio/docs/mobile-execute-command.html), [`doubleTap`](https://docs.katalon.com/katalon-studio/docs/mobile-double-tap.html), [`longPress`](https://docs.katalon.com/katalon-studio/docs/mobile-long-press.html), and [`setEncryptedText`](https://docs.katalon.com/katalon-studio/docs/mobile-set-encrypted-text.html).
* Support adding [Proxy Exceptions](https://docs.katalon.com/katalon-studio/docs/proxy-preferences.html) in Proxy Preferences and `-proxy.excludes` option in console mode.
* [Mobile Recorder] Implement the following actions: Get Text, Swipe, and Scroll To Text.

### Changes and Improvements

* Add **Profiles** to Test Suite Collection Report.
* [Mobile- iOS] Support **Install Dependencies** and **Install WebDriverAgent** tools on the main menu. Please be noted that you have to install [homebrew](https://brew.sh/) manually.
* [Command Syntax] Support both `-serverUrl` and `-serverURL` arguments.
* Make the `DriverFactory.changeWebDriver()` method a public method.
* Support **Open containing folder** for Folders in Test Explorer.

### Fixes

* Bug: [Windows] An issue related to creating a project.
* Bug: An issue related to saving Web Service Message.
* Bug: Empty result tab after a Test Suite execution.
* Bug: Test Script lost parens in method call after editing some steps.
* Bug: [KRE] an issue related to the `retry` option.
* Bug: [Web] Cannot set a timeout in **Wait for options**.
* Bug: [Web Service Request] an issue related to saving HTTP Header.
