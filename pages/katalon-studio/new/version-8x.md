---
title: "Version History - 8.x" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-8x.html
redirect_from:
    - "/katalon-studio/new/all-versions.html"
description: Release notes 8.x
---
## Official Release - Version 8.1.0

> Download [here](https://www.katalon.com/download/).

### New features

* Introduced the Condition to stop test execution.
    * Handle Command Builder.
    * Condition to stop Test Suite Collection executing in Parallel Mode.
    * CLI option used in Test Suite Collection executing in Sequential Mode.
    * CLI option used in Test Suite and Handle Validation Rules.
* [Mobile] [Keyword] Introduced `waitForElementNotPresent`. See [doc's name](url).

### Enhancements

* Supported built-in Excel keywords. See [doc's name](url)
* [Mobile] Improved Setup for Mobile testing on macOS. - Selected for development
* [Katalon Studio Enterprise] Enhanced Retry Immediately Strategy. See [doc's name](url)
    * Changed the condition to stop execution, number of retry times, and Consolidated Execution.Log.
    * Introduced Consolidated Report.
        * Report View of a Test Suite.
        * Supported formats: JUnit, HTML, PDF, and CSV.
        * Updating final status to TestRail.
        * Sending final results to JIRA.
        * Sending final results to Azure DevOps Test Plans.
        * Sending final results to qTest.
* [Azure DevOps Integration] Submitted Release details and Test Run properties to Azure DevOps. See [doc's name](url)
* [Kobiton Integration] Supported customizing remote server protocol.
* [Kobiton Integration] Supported customizing device name.
* Introduced options to include or exclude timestamps in .properties files in the Project Settings folder. See [doc's name](url)
* [Katalon Studio Enterprise] [Katalon Runtime Engine] Supported auto-retry up to three times after failed activation.

### Bug Fixes

STUDIO-890 Bug fixes for UI issues on macOS Big Sur

UI/UX Fixes:

STUDIO-1064 [Regression][Existing Bug][Mac Big Sur] Test Steps are NOT visible in the test cases after recording

STUDIO-1035 [Keyword] verifyElementPropertyValue throws an error message

STUDIO-1013 [Regression][Existing Bug][Big Sur][Desired Capabilities] Items are NOT displayed in the table/tree after importing

STUDIO-1008 [Slack Integration] Failed to connect to Slack

STUDIO-971 [ADO] UI broken when expanding "Submission Options"

STUDIO-957 [Regression][Existing Bug] Some test cases are NOT executed if using "Retry Failed Execution Immediately"

STUDIO-897 Log Viewer does not update when change execution item on Job Progress

STUDIO-892 When users switch the selected Object, Katalon does not switch Object Properties View accordingly.

STUDIO-891 [Big Sur] Text of selecting item on table/tree are hidden

STUDIO-885 [@qbe.com] Executed steps are not displayed in Console log for Katalon-Cucumber

STUDIO-859 [8.0.0] No error message displayed/warning when make a configuration for My SQL after removing its driver

STUDIO-822 Fixing typo in Mobile Object Spy

STUDIO-787 [Regression][Existing Bug] Cancel Export Report via Context Menu return error message

STUDIO-756 [Regression][Existing Bug] Broken GUI when working with TestOps creating new File

STUDIO-746 It takes 2 - 3 paused seconds to create a new sample project

STUDIO-666 [Regression] Problems with Project Settings when having TestRail plugin already installed

STUDIO-628 [Regression 7.8.1] Cannot link an existing Window Object to Window Built In Keyword

STUDIO-613 [Regression] Users cannot configure Report in Project Setting if NOT having internet

STUDIO-611 [Regression] Katalon displayed device's Id instead of device's name in the progress bar

STUDIO-576 [Regression 7.8] Script is automatically delete when using customized keywords with incorrect argument values

STUDIO-537 [Regression 7.8] Activate button is NOT enable if email contains space

STUDIO-534 KRE: Cannot find the attached device in AWS Device Farm

STUDIO-515 [Regression] Event Log shows duplicated information

STUDIO-506 [Regression] Incorrect Object UI when opening it from the script

STUDIO-396 [Regression] Updating Query parameters in WS object does NOT mark the object 'changed'

STUDIO-332 [Regression][UI/UX] Incorrect linked URL

STUDIO-1067 Technical Debt: Handle Command Builder reflecting the scope of Retry Options only at Test Suite level

STUDIO-941 iOS dependencies not found due to default path changes when installing with Homebrew

STUDIO-826 [@caci.nl][@culturatech.com] Code Refactor to resolve issue: Cannot select Run/Debug from here

STUDIO-823 Update message "Object <ObjectId> has been broken. Please fix it before proceeding further."

STUDIO-818 Correct Labels in Project Settings/Library Management and add help link

## Version 8.0.5

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
* Bug: Resolved Test Suite stopped executing after some test cases.
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
