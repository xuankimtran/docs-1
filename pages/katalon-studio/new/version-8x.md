---
title: "Version History - 8.x" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-8x.html
redirect_from:
    - "/katalon-studio/new/all-versions.html"
description: Release notes 8.x
---

## Official Release - Version 8.0.5

> Download [here](https://www.katalon.com/download/).

### Improvements

* Introduced an option to Record Web with a packed extension, now available on the Chrome Web Store. See [Record Web Utility using Chrome with Profile](https://docs.katalon.com/katalon-studio/docs/record-web-utility-using-chrome-with-profile.html).
* Enhanced Time Capsule by leveraging a built-in ChromeDevTools function to create a MHTML snapshot. Credited to Kazurayam for suggesting [Saving Web Page as MHTML in Katalon Studio](https://forum.katalon.com/t/saving-web-page-as-mhtml-in-katalon-studio/49368).
* [Web UI] Introduced new parameters for `WebUI.takeScreenshot` keyword to print text on captured screenshots. See [Take screenshots with WebUI keywords](https://docs.katalon.com/katalon-studio/docs/webui-take-screenshot.html).

### Fixes

* Fixed issues with Custom Keywords where:
    * Back and Forth navigation in the Editor was not working.
    * Hyperlink was not working.
    * Javadoc was not working.
    * The Declaration of the keyword could not be opened.
    * [Cucumber] Custom Keywords in Step definitions were not working.
* Bug: Resolved activation issue of Enterprise-exclusive plugins.
* Bug: Test Suite stopped executing after some test cases.
* Fixed reports parsing issues:
    * [Katalon Runtime Engine] Could not generate and submit JUnit report to TestOps.
    * Could not generate reports due to `Null` character in log files.
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
