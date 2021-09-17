---
title: "Release Notes - 8.x" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-8x.html
redirect_from:
    - "/katalon-studio/new/all-versions.html"
description: Release notes 8.x
---

> Download [here](https://www.katalon.com/download/).

## Official Release - Version 8.1.0

### New features

* [Katalon Runtime Engine] Introduced an ability to terminate execution based on the maximum number of test failures allowed. See [Terminate Execution Conditionally](https://docs.katalon.com/katalon-studio/docs/terminate-execution-conditionally.html)
* [Mobile testing] Introduced `waitForElementNotPresent`. See [[Mobile] Wait For Element Not Present](https://docs.katalon.com/katalon-studio/docs/mobile-wait-for-element-not-present.html)

### Enhancements

* [Katalon Studio Enterprise] Improved the Retry Failed Executions Immediately feature and Introduced the consolidated execution reports to address test flakiness. See [Retry Failed Execution Immediately](https://docs.katalon.com/katalon-studio/docs/create-test-suite.html#retry-failed-execution-immediately).
* [Azure DevOps Integration] Introduced an option to submit Release Information together with Test Run to Azure DevOps. See [Integration with Azure DevOps Test Plans](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html#configure-the-integration)
* [Kobiton Integration] Introduced custom remote server and device name functionality. See [Mobile Testing with Kobiton Devices](https://docs.katalon.com/katalon-studio/docs/integrate_with_kobiton.html)
* Added Chrome 92 compatibility.
* Added Microsoft Edge (Chromium) 92 compatibility.
* [Plugin] Introduced new APIs for the Plugin platform. See [new APIs list](https://github.com/katalon-studio/katalon-studio-platform/blob/master/docs/turorials/apilist.md)
* Performance: Reduced time to open a Test Case with many variables.
* [Katalon Runtime Engine] Passed a path to the Android SDK root folder by using ANDROID_HOME environment variable. See [Specify a path to Android SDK root folder](https://docs.katalon.com/katalon-studio/how-to-guides/how-to-specify-android-home-path.html)

### Fixes

* Fixed UI issues:
    * [Azure DevOps] Expanding Submission Options broke the UI.
    * [TestOps] Creating new files with TestOps broke the UI.
    * Expanding Execution Information broke the UI.
    * [macOS Big Sur] Could not switch to Object Properties View.
    * [macOS Big Sur] Text of selected items on table and tree were hidden.
    * [macOS Big Sur] Could not update Log Viewer when the execution items were changed on the Job Progress.
    * [Mobile Object Spy] Fixed typo error "Application ID".
    * [Mobile] An issue of displaying device ID instead of device name in the Progress bar.
    * [Mobile] An incorrect UI thrown when opening Object from the script.
    * [API Testing] An issue of displaying incorrect redirect link to "Customize API method".
    * Could not display test steps after recording.
    * Clarified warning message for when broken Test Object could not be moved.
    * Options in "Retry after executing all" were disabled when generating command.
    * Fixed labels and added referral link in the Library Management.
* Fixed Report issues:
    * An incorrect test status thrown when finish executing in the BDD Report.
    * An issue of displaying incorrect in-line color and icon for failed test steps in the Report and Report Viewer when using assertion.
    * Skipped Test Cases were marked as Passed in HTML report.
    * [Cucumber] Executed steps were not displaying correctly in the Console log. 
    * Duplicated information in the Event log.
    * An incorrect response thrown when users cancel the Export Report.
    * Could not configure Report in Project Setting without internet connection.
* Bug: [Slack Integration] Failed to connect to Slack.
* Bug: [TestRail Integration] Solved issues with Project Settings.
* Bug: [Katalon Studio Enterprise] Could not select Run and Debug from here in specific cases.
* Bug: [Katalon Runtime Engine] Failed to replace excluded built-in libraries with external libraries.
* Bug: [API Testing] An incorrect response thrown when leaving the parameter blank in the request URL path.
* Bug: [API Testing] Could not change object status after updating query parameters in Web Service object.
* Bug: `waitForImagePresent` returned False despite the image appearing correctly.
* Bug: `verifyElementPropertyValue` returned an incorrect error message.
* Bug: An error message thrown when continuing to record scripts with an existing test case returned error messages incorrectly.
* Bug: An issue of deleting script when using customized keywords with incorrect values.
* Bug: Could not link an existing Window Object to Window built-in keyword.
* Bug: Could not activate Katalon Studio by providing email with extra spacing.
* Bug: Browser-based recorder could not record videos for the second test case if reusing an open browser.
* Bug: Explorer Configuration in Project Settings was not working as intended.

### Known issues

* Bug: [Windows OS] Import error of some javax classes: "Groovy:unable to resolve class javax.*". Address [here](https://forum.katalon.com/t/katalon-8-customkeywords-groovy-import-error/58225).

## Version 8.0.5

### Improvements

* Introduced an option to Record Web with a packed extension, now available on the Chrome Web Store. See [Record Web Utility using Chrome with Profile](https://docs.katalon.com/katalon-studio/docs/record-web-utility-using-chrome-with-profile.html).
* Enhanced [Time Capsule](https://docs.katalon.com/katalon-studio/docs/time-capsule.html) by leveraging a built-in ChromeDevTools function to create a MHTML snapshot. Credited to Kazurayam for suggesting [Saving Web Page as MHTML in Katalon Studio](https://forum.katalon.com/t/saving-web-page-as-mhtml-in-katalon-studio/49368).
* [Web UI] Introduced new parameters for `WebUI.takeScreenshot` keyword to print text on captured screenshots. See [Take screenshots with WebUI keywords](https://docs.katalon.com/katalon-studio/docs/webui-take-screenshot.html).

### Fixes

* Fixed Katalon Docker Image not sending reports to Katalon TestOps.
* Fixed issues with Custom Keywords where:
    * Back and Forth navigation in the Editor was not working.
    * Hyperlink was not working.
    * Javadoc was not working.
    * The Declaration of the keyword could not be opened.
    * [Cucumber] Custom Keywords in Step definitions were not working.
* Bug: Resolved activation issue of Enterprise-exclusive plugins.
* Bug: Resolved Test Suite stopped executing after some test cases.
* Fixed reports parsing issues:
    * [Katalon Runtime Engine] Could not generate and submit JUnit report to Katalon TestOps.
    * Could not generate reports due to `Null` character in log files.
    * [Katalon Runtime Engine] Katalon Studio Image could not send report to Katalon TestOps.
* Fixed Katalon Runtime Engine hanging issues when:
    * Running tests with Selenium Grid.
    * [Test Suite Collection] The number of Java threads kept increasing during execution.

## Version 8.0.0 - 8.0.1

### New Features

* [Katalon Studio Enterprise] Supported native integration with Azure DevOps Test Plans. [Learn more](/katalon-studio/docs/azure-devops-test-plans.html)
* [Katalon Studio Enterprise] Imported/Exported desired capabilities. [Learn more](/katalon-studio/docs/import-export-desired-capabilities.html)
* [Katalon Runtime Engine License] Added a parameter to release the previous execution session before checking the license. [Learn more](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options)
* Provided Product Tours for new Web UI and Web Service users.

### Improvements

* Supported Chrome 90.
* Supported Microsoft Edge (Chromium) 90.
* Updated the embedded GeckoDriver to 0.29 (Firefox 88).
* Improved Performance: Load large projects faster and consume less memory during execution.
* Edge Chromium was now the default **embedded browser** (used to be Internet Explorer).
* [Windows OS] Replaced embedded Oracle JRE 8 with Azul Zulu OpenJDK 8.
* Enhanced Katalon TestOps Integration:
    * [Katalon Runtime Engine] Supported query for Test Suite Collection. [Learn more](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options)
    * [Katalon Runtime Engine] Supported new parameters for the new Build concept. [Learn more](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options)
* [Katalon Runtime Engine] Passed HashMap for Global Variables from CLI.
* [Katalon Runtime Engine] Added an option to Command Builder for updating WebDriver automatically.
* [Enhanced Report] Added profile details to the email reports.

### Changes

* Katalon accounts registered with personal email are eligible for Katalon Studio Enterprise and Katalon Runtime Engine trial licenses for 30 days.
* MySQL became an external library. To keep it in use, follow [this guide](/katalon-studio/how-to-guides/how-to-implement-ddt-mysql.html) to configure MySQL database connection.

### Fixes

* Bug: Fixed all blocker & critical security vulnerabilities reported by SonarQube in static code analysis and 3rd-party libraries scanning tools. 
* Bug: [Katalon Runtime Engine] Lacking of tracking event for activation.
* Bug: [Windows] Missing Network connection Preference.
* Bug: [Chrome 86] Recorder utility was not working.
* Bug: Could not import Swagger JSON files.
* Bug: The Bypass Certificate validation option was not working.
* Bug: [Katalon Runtime Engine] An issue of not sending emails via command syntax `sendMail`.
* Bug: An issue of deleting scripts when renaming the folder name.
* Bug: Could not drag and drop a custom keyword from Keyword Browser.
* Bug: Could not update References of Called Test Cases when the test cases are moved by drag and drop or cut and paste.
* Bug: [Mobile testing] Could not capture object(s) while testing.
