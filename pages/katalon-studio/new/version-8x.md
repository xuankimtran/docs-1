---
title: "Release Notes - 8.x" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-8x.html
redirect_from:
    - "/katalon-studio/new/all-versions.html"
description: Release notes 8.x
---
## Version 8.3.0 Beta 

> Download from our GitHub repository: [Katalon Studio version 8.3.0 Beta](https://github.com/katalon-studio/katalon-studio/releases/tag/v8.3.0.beta).

### Enhancements

* [Security Compliance] Upgraded Log4j to version 2.17.1.

### Fixes

* Bug: [BDD] "KeywordUtil.markFailed" logged the error but did not continue execution in the BDD framework.  
* Bug: Obsolete proxy desired capabilities for Firefox caused test failures.
* Bug: [Katalon Runtime Engine] Did not recognize the `-projectPath` and `-apiKey` parameters in the .properties file when executing in Katalon Runtime Engine.
* Bug: [Katalon Runtime Engine] Did not print specific names of empty test suites when executing in Katalon Runtime Engine.
* Bug: [Katalon Runtime Engine] Failed to terminate all chrome.exe and chromedriver.exe files after Katalon Runtime Engine execution.
* Bug: [Mobile] Screenshots unexpectedly taken twice when using the `Mobile.TakeScreenShot()` keyword once.
* Bug: Could not refresh the project root folder when clicking **Project** > **Refresh** or right-clicking in the **Tests Explorer** panel > **Refresh**.
* Bug: Could not update Test Object references after renaming Test Objects.

## Version 8.2.5 - Official Release

> Download from our official website: [Katalon Studio version 8.2.5](https://www.katalon.com/download/).

### New features

* [WebUI] Introduced an option to use the Spy, Record, and Smart Wait function with a packed extension, now available on the Chrome Web Store. This extension is compatible with Katalon Studio version 8.2.5 onwards. See [Katalon Compact Utility](https://docs.katalon.com/katalon-studio/docs/katalon-compact-utility.html).
    * Introduced an option to enable/disable Xpath visibility on the Katalon Compact Utility extension. See [Disable XPath visibility](https://docs.katalon.com/katalon-studio/docs/katalon-compact-utility.html#disable-xpath-visibility).
* Introduced TestCloud integration (Beta). See [Integrate TestCloud with Studio](https://docs.katalon.com/katalon-studio/docs/testcloud-integration.html) and [Run TestCloud with Katalon Runtime Engine](https://docs.katalon.com/katalon-studio/docs/testcloud-integration-kre.html).

### Enhancements

* Added Microsoft Edge (Chromium) 96 compatibility.
* Added Chrome 97 compatibility.
* [Operating System] Windows 11 support: You can use Katalon Studio and Katalon Runtime Engine on computers running under Windows 11.
* [Security Compliance]:
    * Upgraded Netty library to netty-all 4.1.61.Final.
    * Upgraded jsoup library to jsoup 1.14.3.
* Enabled the connection to the SAP HANA database. To set up SAP HANA database for Data-driven testing, download this executable jar file: [SAP HANA JDBC Driver](https://mvnrepository.com/artifact/com.sap.cloud.db.jdbc/ngdbc) and follow this tutorial: [Connect to a database with an external JDBC driver](https://docs.katalon.com/katalon-studio/docs/database-settings.html#connect-to-a-database-with-an-external-jdbc-driver).
* Introduced the `xpath:customAttributes` in the web locator strategies. See [Configure XPath](https://docs.katalon.com/katalon-studio/docs/web-selection-methods.html#configure-xpath).
* Introduced an option in the **Project Setting** to include/exclude timestamps in the .properties files. See [Include/Exclude timestamp in .properties files](https://docs.katalon.com/katalon-studio/docs/execution-settings.html#includeexclude-timestamp-in-proprerties-files).
* [TestOps Integration]:
    * Removed the **Create Script Repository** and **Update Script Repository** options.
    * Turned on Katalon TestOps Integration by default for new Web and API users.
* [License Activation] Changed the Katalon license server to [https://admin.katalon.com/](https://admin.katalon.com/). For authentication, Katalon Studio and Katalon Runtime Engine call this new server URL.
* Improved the visibility of the search function. See [Search Test Cases](https://docs.katalon.com/katalon-studio/docs/search.html).
* Removed unused messages in Test Suite.
* [UI changes]:
    * [Dynamic Test Suite] Updated UI for the retry function in Dynamic Test Suite.
    * Changed the **Communication**, **Feedback**, and **Support Portal** buttons.
    * [TestOps Integration] Changed the UI in the **Katalon TestOps Integration** dialog. See [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).
    * [License Activation] Changed UI text from **Deactivate** to **Log out**.

### Fixes

* Bug: Editing script and executing a test could intermittently cause the error: "java.lang.ClassFormatError: Truncated class file".
* Bug: [qTest] Missing screenshots in the qTest HTML report.
* Bug: [qTest] Could not run test suite right after configuring qTest integration.
* Bug: Failed to update webdriver automatically when using custom desired capabilities.
* Bug: [Katalon Runtime Engine] Not sending all Jira IDs test results in the Jira report when executing with Katalon Runtime Engine.
* Bug: [On-Premises and Cloud Licensing Servers] Not showing the terminate session popup when deleting online licenses.
* Bug: [Web Recorder] Lacked test steps in the Recorder Logs when playing back the test case.
* Bug: Inside the **Log Viewer**, unable to navigate to a specific step by right-clicking on the step and choosing **Go to this step in Script View**.
* Bug: [Docker Image] Unable to send email reports when running test script from Docker Image.

## Version 8.2.0

### New features

* [Web Service] Introduced `setHarFileGeneration(boolean enable)` and `getHarFileGeneration` Web Service Keywords for disabling HAR file generation on demand. See [[WS] Set HAR File Generation](https://docs.katalon.com/katalon-studio/docs/ws-set-har-file-generation.html) and [[WS] Get HAR File Generation](https://docs.katalon.com/katalon-studio/docs/ws-get-har-file-generation.html).

### Enhancements

* Added Chrome 95 compatibility.
* Added Microsoft Edge (Chromium) 95 compatibility.
* [Security] Addressed Security Vulnerabilities of Open-Source Software.
* Added an option in Katalon Studio Preferences to automatically disable connection to external domains.
* [Performance] Improved Katalon Studio IDE and Katalon Runtime Engine performance:
    * Introduced **Delay between instances** option in Katalon Studio and `-delayBetweenInstances` parameter in Katalon Runtime Engine to execute Test Suite Collection in parallel mode. See [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html), quick tip: search for `-delay`.
    * Improved loading time in Katalon Runtime Engine. Results from our benchmarking tests show: 2x faster for big projects, 1.5x faster for small and medium projects.
    * Improved responsiveness and loading time for big projects in Katalon Studio. Results from our benchmarking tests show: renaming/opening test cases 2x faster, moving test cases 1.5x faster.
    * Reduced 12% memory consumption on average of Katalon Studio when opening/executing tests.
    * Reduced 30% memory consumption on average of Katalon Runtime Engine for long execution sessions.
* [Web Testing] Improved Synchronization Handling for Web Testing:
    * [Katalon Studio and Katalon Runtime Engine] Improved the `Click` and `Click Offset` Keywords to automatically delay and click again on an element behind a loading overlay. See [Click](https://docs.katalon.com/katalon-studio/docs/webui-click.html) and [Click Offset](https://docs.katalon.com/katalon-studio/docs/webui-click-offset.html).
    * [Smart Wait] Added detection and waiting capabilities for fetch-based requests to finish before continuing with the next action.
    * [Smart Wait] Added Edge Chromium compatibility for Smart Wait. See [[WebUI] Smart Wait Function](https://docs.katalon.com/katalon-studio/docs/webui-smartwait.html).
* [Katalon Studio Enterprise] Introduced Idle Timeout Bypass Limit to automatically log out licensed users due to timeout. See [Configure Idle Timeout](https://docs.katalon.com/katalon-studio/docs/license-idle-timeout.html).
* [BDD] Added BDD testing onboarding flow.
* [Jira Integration] Only displayed the _Bug_ icon in Final test results.
* [Console Log] Enhanced Plugin loading information in the console log of Katalon Studio Enterprise and Katalon Runtime Engine.
* [Katalon Runtime Engine] Removed the "Offline activation failed" message in the execution log.
* [DDT] Specified the input data of iterations in the Data-driven Testing report.

### Fixes

* Bug: [CSV Report] Incorrect status for skipped Test Suite in CSV Report.
* Bug: Unable to recognize namespace in SOAP Envelope Body.
* Bug: [BDD] Failed feature file from the second run when calling custom keywords.
* Bug: null.null Katalon version in the Report Viewer when deactivating the current account and activating a new one.
* Bug: Incorrect information of test case in Log Report Viewer.
* Bug: Not matching between the Elapsed time of execution in Katalon Studio and the generated report.
* Bug: [Jira Integration] Could not interact with embedded Jira page. Fixed with changes to Jira Integration version 1.0.22. Download here: [Jira Integration](https://store.katalon.com/product/3/Jira-Integration#overview-content).
* Bug: [Jira Integration] Jira-linked tickets had no step in the description.
* Bug: [WebUI] Could not generate test steps when using `replace, trim, split` function and opening WebUI Recorder.
* Bug: Incorrect Copyright and Version information for Katalon Studio and Katalon Runtime Engine packages on macOS.

## Version 8.1.0

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
* Bug: When continuing to record scripts with an existing test case returned error messages incorrectly.
* Bug: An issue of deleting script when using customized keywords with incorrect values.
* Bug: Could not link an existing Window Object to Window built-in keyword.
* Bug: Could not activate Katalon Studio by providing email with extra spacing.
* Bug: Browser-based recorder could not record videos for the second test case if reusing an open browser.
* Bug: Explorer Configuration in Project Settings was not working as intended.

### Known issues

* Bug: [Windows OS] Import error of some javax classes: "Groovy:unable to resolve class javax.*". More details on this forum post: [Katalon 8 custom keywords groovy import error](https://forum.katalon.com/t/katalon-8-customkeywords-groovy-import-error/58225).

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
