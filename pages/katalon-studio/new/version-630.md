---
title: "Version 6.3.0" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-630.html
redirect_from:
    - "/katalon-studio/new/version-630/"
description: Release note 6.3.0
---

## Version 6.3.0

## New Features

* Support Dark theme in addition to the default Light theme. See [Using Katalon Studio in Dark theme](https://docs.katalon.com/katalon-studio/docs/dark-theme.html).
* Support spying, recording and executing the Mobile script on custom cloud-based testing tools; and an option to choose between AndroidDriver or iOSDriver when Appium is set as `Remote server type`. See [Testing Mobile Apps Using Custom Cloud Devices](/katalon-studio/docs/mobile-testing-apps-cloud-devices.html) and [Remote Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/remote-desired-capabilities.html).
* Support testing existing applications on Android and iOS devices. See [[Mobile] Start Existing Application](/katalon-studio/docs/mobile-keyword-start-existing-apps.html) and [Spy and Record Utilities for testing an existing application](/katalon-studio/docs/mobile-spy-record-existing-apps.html).

### Improvements

* Allow Test Reports to be viewed directly in Test Suite and Test Suite Collection Views in Result Tab. See [Test Suite Report](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html) or [Test Suite Collection Report](https://docs.katalon.com/katalon-studio/docs/test-suite-collection-report.html).
* Support sending custom headers in SOAP requests.
* Directly parameterize Global variables in Test Objects. See [Global Variables](https://docs.katalon.com/katalon-studio/docs/global-variables.html).
* Allow implementing variable binding without converting test data to strings. See [Enhanced Variable Binding](https://docs.katalon.com/katalon-studio/docs/bind-as-string.html#variable-binding-for-test-data-with-option-embind-into-test-case-as-stringem-enabled).
* Support implementing an annotation called BeforeTestDataBindToTestCase in test listener. See [[Quick tip] Enhanced Variable Binding](https://docs.katalon.com/katalon-studio/docs/bind-as-string.html).
* Support Move up and Move down items in the default profile. See [Global Variables](https://docs.katalon.com/katalon-studio/docs/global-variables.html).
* Support quickly setting up your devices by displaying sub-menus of Android, iOS and Kobiton devices in Mobile Spy and Recorder tool items.
* Enhancement: Remove the **-- disable-extensions** argument from Chrome Desired Capabilities.
* Support Chrome version 76.

### Fixes

* Bug: Test object references are displayed incorrectly when new test objects are created from the existing ones.
* Bug: The scroll bar disappears in the Variables section.
* Bug: Incorrectly detect and highlight Mobile Test Objects when using Mobile Recorder or Mobile Object Spy.
* Bug: Incorrectly detect Test Objects’ locations when using Mobile Recorder or Mobile Object Spy.
* Bug: Cannot record additional items when using Web Recorder on existing test cases.
* Bug: Cannot activate Katalon Studio after resetting the password.
* Bug: Cannot load test steps in Manual View of a test case when *Initially open Test Case in Script view* is set by default.
* Bug: Cannot run test cases with Microsoft Edge 18.0 on BrowserStack.
* Bug: Katalon Studio always uses Xpath as a default element locator instead of Web Locators defined by users.
* Bug: *Continue Recording* silently deletes WebService parameters.
* Bug: The new checkpoint dialog box is not resizable and does not display all UI elements on Windows 10.
* Bug: The Sender field is empty when users send an email.
* Bug: An issue related to running a test suite with too large test data.
* Bug: NullPointerException occurs when using Web Recorder on an empty test case.
* Bug: Global Variables initialization fails when an existing WebDrivers’ instance is used in a custom profile.
* Bug: "Bind to test case as string" checkbox in Test Data is always checked while a test suite is executed.
* Bug: Slow performance of adding Variables to test cases.
* Bug: HAR files fail to be logged when the **SendRequestAndVerify** keyword is used.
* Bug: The **TapAtPosition** keyword fails to run.
