---
title: "Version 7.1" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-71.html
redirect_from:
    - "/katalon-studio/new/version-71/"
description: Release note 7.1
---

## Version 7.1.0-7.1.1

### New Features

* Release [Katalon TestOps OnPremise](https://docs.katalon.com/katalon-analytics/docs/ktop-overview.html).
* Support [creating testing licenses](https://docs.katalon.com/katalon-studio/docs/license-management.html#create-and-assign-an-offline-rekse-license) to verify machine ID when creating offline licenses on Katalon TestOps.
* [Katalon TestOps] Support Billing Manager role for being in charge of subscription. [Learn more](https://docs.katalon.com/katalon-analytics/docs/kt-user-role-permission.html).
* Support naming test artifacts, including Test Case, Test Object, Test Data File, Test Suite, Test Suite Collection, and Checkpoint with UTF-8 characters.
* Automatically update keywords' references in other custom keyword classes when renaming or drag-and-dropping a custom keyword.

### Changes and Improvements

* [Web Service] Support all file types of the form-data option in HTTP Body when creating a POST request.
* [Web Service] Support API responses in other languages.
* Auto-healing Smart Xpath becomes a built-in feature of Katalon Studio Enterprise. For standard Katalon Studio users who have already subscribed to this plugin, please contact Katalon team via business@katalon.com.
* Display a progress dialog when adding a bulk number of Test Cases to a Test Suite.
* Handle SVG elements and add a context menu during Spying to capture objects.
* [KRE] Improve running multiple projects with multiple sessions concurrently.
* Support turning off Smart Wait with both global and local settings. [Learn more](https://docs.katalon.com/katalon-studio/docs/webui-smartwait.html).
* [Web Service] Support redirection in POST request and 308 status code.
* Tips: You're recommended to open large HAR files with other tools than Katalon Studio or keep those files not too large for Katalon Studio to read it.

### Fixes

* Bug: Test Suite result is incorrect if a called test case gets failed when *log test steps* is disabled.
* Bug: Web Recorder does not generate XPath locators for SVG elements.
* Bug: [Mobile] Cannot run a browser test on Android device using Appium 1.15.0+.
* Bug: Cannot create a new project when failing to read Sample Projects.
* Bug: Cannot execute test scripts having import paths containing wildcard character (`*`).
* Bug: Cannot start a browser when running with an iOS simulator.
* Bug: NullPointerException when using Katalon Studio for the first time.
* Bug: Cannot read variables in a custom profile if executing a test suite collection remotely.
* Bug: Cannot execute test scripts that have Global Variables' names containing the `$` symbol.
* Bug: An issue related to saving changes in Test Case Variable View.
* Bug: Katalon Studio does not read proxy configuration during Recording.
* Bug: Web Recorder simultaneously generates `NavigateToUrl` keyword and action of an element.
