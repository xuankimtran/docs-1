---
title: "Version History - 7.x" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-70.html
redirect_from:
    - "/katalon-studio/new/all-versions.html"
    - "/katalon-studio/new/version-72.html"
    - "/katalon-studio/new/version-72/"
    - "/katalon-studio/new/version-71/"
    - "/katalon-studio/new/version-71.html"
    - "/katalon-studio/new/version-70/"
    - "/katalon-studio/new/version-48.html"
    - "/katalon-studio/new/version-501.html"
description: Release note 7.x
---

## Official Release - Version 7.8.2

### Improvements
 
* [Katalon TestOps (Beta) Integration] Support detecting Assertions in execution log.
* [Time Capsule] Allow turning on/turning off Time Capsule in Project Settings (Go to Project > Settings > Execution > WebUI). 

### Fixes
   
* Bug: An issue of generating Time Capsule for an error that doesn't cause test execution to fail.
* Bug: An issue of showing "No application is started yet" when test execution already started. Address [here](https://github.com/katalon-studio/katalon-studio/issues/409).
* Bug: Cannot generate execution reports when `WebUI.comment` contains invalid XML characters.

## Version 7.8.0 - 7.8.1

### New features

* Support Time Capsule for optimizing fixing broken Web Test Objects. [Learn more](https://docs.katalon.com/katalon-studio/docs/time-capsule.html)
* [Katalon Studio Enterprise] Support browser-based video recording. [Learn more](https://docs.katalon.com/katalon-studio/docs/screenshots-videos.html#browser-based-video-recorder)
* [Windows Testing] Support coordinates-based recording with [Click Element Offset](https://docs.katalon.com/katalon-studio/docs/windows-kw-click-element-offset.html) and [Right-click Element Offset](https://docs.katalon.com/katalon-studio/docs/windows-kw-rightclick-element-offset.html) keywords on both [Windows Recorder](https://docs.katalon.com/katalon-studio/docs/windows-recorder-tutorials.html) and [Native Windows Recorder](https://docs.katalon.com/katalon-studio/docs/windows-native-record.html).
* Provide Checksum for each Katalon Studio package named `all-packages.sha256`
and Open source libraries's license scanning report in HTML named `KatalonStudio-openSourceReport.html` (Go to [our GitHub Repository](https://github.com/katalon-studio/katalon-studio/releases), download those files in each build's Assets).
* [Katalon Studio Enterprise] Allow replacing a built-in library with an external one for flexible libraries usage in a test project. [Learn more](https://docs.katalon.com/katalon-studio/docs/external-libraries.html#exclude-built-in-libraries)
* [Web Service Testing] Import SOAP requests from SoapUI and WSDLs having no service endpoints. [Learn more](https://docs.katalon.com/katalon-studio/docs/import-soapui.html)
* [Katalon TestOps (Beta) Integration] Export BDD reports generated in Katalon Studio to display in TestOps. [Learn more](https://docs.katalon.com/katalon-analytics/docs/bdd-test-results.html)
* [Katalon TestOps (Beta) Integration] Support generating commands for TestOps CI in Katalon Studio's Command Builder.
* [Katalon TestOps (Beta) Integration] Allow overriding TestOps Project ID via command line.
* [Katalon TestOps (Beta) Integration] View Releases in Katalon Studio's Test Explorer. 
* Provide in-app tutorials for new Katalon users to start testing Web UI, Mobile, Web Service and Windows applications (Go to Help > Tutorials > Select Web UI/Mobile/Web Service/Windows).
* You can create a new project with Desktop type.
* [Katalon Studio Enterprise] Configure idle timeout for license usage management. [Learn more](https://docs.katalon.com/katalon-studio/docs/license-management.html#configure-idle-timeout)

### Improvements

* Support Microsoft Edge (Chromium) 86
* Support Chrome 86
* [qTest Integration]: Generate qTest - Katalon Studio parity report in HTML, sync up qTest test case version and test steps's content, and send Skipped test results to qTest. [Learn more]()
* [Kobiton Integration] Support SSO for authentication and corresponding command options. [Learn more](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#integration-options)
* [Jira Cloud Integration]: Support importing BDD Feature Files. [Learn more](https://docs.katalon.com/katalon-studio/docs/jira-integration.html#jira-cloud-integration)
* [BDD Testing Framework] Allow setting default package for step defenitions. [Learn more](https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html#set-default-package-for-step-definitions).
* [Mobile Testing] Support "Attributes" Selector Strategy and add "Verify and Highlight" feature to Mobile Spy/Recorder.
* [Katalon TestOps (Beta) Integration]: Support automatically retrying uploading Test Projects and Test Reports from Katalon Studio to Katalon TestOps upon failure.
* Replace Katalon Help with Start Page for a new fresh look and more customized information for each user.
* Reduce the size of Katalon Docker Image.
* Discontinued new purchase of Katalon Runtime Engine DevOps license. Read more about [Katalon Runtime Engine DevOps Sunsetting](https://docs.katalon.com/katalon-studio/docs/kre-devops-sunset.html).
* Display SKIP test status in execution reports.

### Fixes

* Bug: An issue of not installing Smart Wait extension automatically on Chrome when running tests.
* Bug: Failed to display items in table and tree views on macOS Big Sur.
* Bug: [Katalon Studio Enterprise - Export Test Artifacts] Cannot export test cases.
* Bug: [Katalon Studio Enterprise] Cannot import API from OpenAPI Specification 3.0.
* Bug: [Katalon Runtime Engine] Cannot execute Dynamic Test Suites.
* Bug: An issue of Katalon Runtime Engine activation failure on Katalon Docker Image.
* Bug: GUI issues on Windows machines when scaling to more than 100% size of text.
* Bug: [Test Object's Editor] Cannot display all object properties in a window screen.
* Bug: API Requests with fileupload body uses a file path instead of a file name.
* Bug: [Katalon TestOps (Beta) Integration]: Cannot display more than 20 projects fetched from Katalon TestOps (Beta).

## Version 7.7.0 - 7.7.1 - 7.7.2

### New features

* [Katalon Record Utility] Support adding verification test steps during recording with Chrome, Edge (Chromium-based), and Firefox. [Learn more](https://docs.katalon.com/katalon-studio/docs/record-web-utility.html#validate-ui-elements).
* [Katalon Studio Enterprise - Web Service Testing] Import RESTful API with OpenAPI Specification 3.0. [Learn more](https://docs.katalon.com/katalon-studio/docs/import-openapi30.html)
* [Web Service Testing] Import RESTful requests from WADLs. [Learn more](https://docs.katalon.com/katalon-studio/docs/import-wadl.html)
* [Windows Testing] Support passing Capabilities including `appArguments` and `appWorkingDir` for Native Windows Recorder. [Learn more](https://docs.katalon.com/katalon-studio/docs/introduction-to-desired-capabilities.html#windows-desktop-app-testing)
* Support using Global Variables in Email Settings. [Learn more](https://docs.katalon.com/katalon-studio/docs/execution-settings.html#support-global-variables-in-email-settings)
* [Katalon Runtime Engine] Allow selecting an Organization for license validation when activating Katalon Runtime Engine. [Learn more](https://docs.katalon.com/katalon-studio/docs/use-online-license.html#katalon-runtime-engine)
* [Katalon TestOps (Beta) Integration] Support integration with Katalon TestOps Vision for visual testing. [Learn more](https://forum.katalon.com/t/early-release-of-katalon-testops-vision-visual-testing-image-comparison)

### Improvements

* Support Microsoft Edge (Chromium) 85
* Support Chrome 85
* Install the Basic Reports plugin automatically for all users
* Publish [API docs version 7.7](https://docs.katalon.com/javadoc/index.html)

### Fixes

* Bug: [Katalon Runtime Engine] An issue of generating reports after execution 
* Bug: [Katalon Runtime Engine] An exception thrown when updating WebDriver automatically in Command Line. Address [here]( https://forum.katalon.com/t/test-collection-are-not-running-from-azure-getting-classnotfoundexception-com-kms-katalon-core-logging-logback-systemoutfilter-cannot-be-found-by-ch-qos-logback-classic-1-2-3-and-lots-of-unable-to-resolve-class-errors/47743)
* Bug: [Katalon Record Utility] Unable to locate Objects during execution if the objects are captured with such options as **Merge objects**, **Duplicate objects**, or **Replace existing objects**
* Bug: [TestNG] Return incorrect test results when using the `runTestNGTestClasses` keyword

## Version 7.6.6

### Improvements

* [qTest Integration] Upload test results of the integrated Test Suites in Test Suite Collection to qTest
* [Katalon TestOps (Beta) Integration] Display TestOps Plans in Tests Explorer. [Learn more](https://docs.katalon.com/katalon-analytics/docs/view-ci-plans.html)
* [Katalon Studio Enterprise] Enhance Self-healing Insights. [Learn more](https://docs.katalon.com/katalon-studio/docs/self-healing.html#understand-self-healing-insights)
* [Katalon Studio Enterprise] Enhance UX of adding test cases to test suites
* Support [troubleshooting activation problems](https://docs.katalon.com/katalon-studio/docs/troubleshoot-activation-problems.html)

### Fixes

* Bug: An issue related to Test Objects' names in Katalon Record Utility
* Bug: [Command Builder] An issue of setting the waiting time to update execution status of the Test Suite
* Bug: [Windows Testing] Test execution failure caused by the default timeout of `switchToWindowTitle`
* Bug: [Web Service Testing] An issue of saving test request's body

## Version 7.6.5

You can download Katalon Studio version 7.6.5 [here](https://github.com/katalon-studio/katalon-studio/releases/tag/v7.6.5).

### Improvements

* [qTest Integration] Include qTest Test Case ID in the name of Katalon Test Cases downloaded from qTest

### Fixes

* Bug: [Web Recorder] Unable to use **Run from here** when recording web with Internet Explorer WebDriver v3.6.0.0
* Bug: [Web Recorder] Unable to capture navigate actions when recording with Internet Explorer WebDriver
* Bug: [Mobile Recorder] Unable to perform any actions on an Android Tab element
* Bug: [Mobile Recorder] Unable to detect elements when spying/recording an iOS app
* Bug: [qTest Integration] Unable to send test reports to qTest automatically
* Bug: [Jira Integration - Katalon BDD] An issue of importing incorrect content of Feature files from Jira
* Bug: [TestRail Integration] TestRail plugin does not support Manual Proxy Configuration
* Bug: [Kobiton Integration] Unable to apply System Proxy configuration when retrieving Kobiton devices and applications
* Bug: [Katalon TestOps (Beta) Integration] Unable to upload test results to Katalon TestOps (Beta)
* Bug: [Report Email] Unable to receive any emails or receive unexpected test suite report emails
* Bug: [Test Listeners] Text field is not visible when renaming a test listener
* Bug: [Katalon Runtime Engine] Unexpected stack trace is displayed at the end of execution

## Version 7.6.2

### New Features

* Katalon TestOps (Beta) Integration: Support associating a test execution in Katalon Studio with Release on Katalon TestOps (Beta) via command-line parameter. [Learn more](https://docs.katalon.com/katalon-studio/docs/execution-release-cli.html)
* Katalon TestOps (Beta) Integration: Display the Executions table in Tests Explorer. [Learn more](https://docs.katalon.com/katalon-studio/docs/view-execution-list.html)

### Fixes

* Bug: [Self-healing mechanism] Null Pointer Exception thrown when XPath/CSS locator is empty

## Version 7.6.0 - 7.6.1

### New features

* [Katalon Studio Enterprise] Support Self-Healing Web tests. [Learn more](https://docs.katalon.com/katalon-studio/docs/self-healing.html)
* [Katalon Studio Enterprise] Support setting timeout and maximum response size for API requests. [Learn more](https://docs.katalon.com/katalon-studio/docs/execution-settings.html#web-service-settings)
* [Katalon Studio Enterprise] Support retrying failed test executions immediately in Test Suite's execution. [Learn more](https://docs.katalon.com/katalon-studio/docs/test-suite.html#retry)
* [Mobile Testing] Fully support Selector Strategies. [Learn more](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html)
* [Mobile Testing] Support App Center Test integration. [Learn more](https://docs.katalon.com/katalon-studio/docs/app-center.html)
* [API Testing] Support importing RESTful requests from SoapUI to Katalon Studio. [Learn more](https://docs.katalon.com/katalon-studio/docs/import-soapui.html)
* [Desktop Testing] Support new Windows keywords, including [setEncryptedText](https://docs.katalon.com/katalon-studio/docs/windows-kw-set-encrypted-text.html), [getAttribute](https://docs.katalon.com/katalon-studio/docs/windows-kw-get-attribute.html), [verifyElementAttributeValue](https://docs.katalon.com/katalon-studio/docs/windows-kw-verify-element-attribute-value.html), [waitForElementAttributeValue](https://docs.katalon.com/katalon-studio/docs/windows-kw-wait-element-attribute-value.html), [verifyElementPresent](https://docs.katalon.com/katalon-studio/docs/windows-kw-verify-element-present.html), [verifyElementNotPresent](https://docs.katalon.com/katalon-studio/docs/windows-kw-verify-element-not-present.html), [waitForElementPresent](https://docs.katalon.com/katalon-studio/docs/windows-kw-wait-element-present.html), and [waitForElementNotPresent](https://docs.katalon.com/katalon-studio/docs/windows-kw-wait-element-not-present.html)
* Allow overriding `Browser Type` and `Execution Profile` of all Test Suites in a Test Suite Collection via command line. [Learn more](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder)
* Support Content Assist function for Custom Keywords in test cases (same as built-in keywords)

### Improvements

* [Katalon Studio Enteprise] Applitools Integration becomes a built-in feature with its libraries updated to the latest versions
* Support updating Microsoft Edge (Chromium) driver in Katalon Studio Tools
* Set Chrome as the default browser

### Fix

* Bug: Log Viewer displays incorrect test results if a test case has Call Test Case steps
* Bug: [Desktop Testing] `setText()` keyword does not clear the current text before setting the given text
* Bug: [qTest Integration] Unable to upload reports to qTest in qTest v10.1.0.0 or later

## Version 7.5.10

### New feature

* Support importing test scripts of Selenium IDE version 3.x. [Learn more](https://docs.katalon.com/katalon-studio/docs/import-selenium-ide.html)

### Improvement

* [WebUI Testing] Support Recorder and Spy with Microsoft Edge (Chromium)

### Fix

* Bug: [Mobile] An issue of missing mobile devices when using Custom Capabilities. Address [#275](https://github.com/katalon-studio/katalon-studio/issues/275)

## Version 7.5.5

### New features

* [Katalon Studio Enterprise] Support "Debug from here". [Learn more](https://docs.katalon.com/katalon-studio/docs/execute-a-test-case-or-a-test-suite.html#debug-from-here)
* [Web Service Testing] Support parameterizing a SOAP request's service endpoint. [Learn more](https://docs.katalon.com/katalon-studio/docs/parameterize-a-web-service-object.html#for-soap-based-request)
* [Web Service Testing] Support defining body content of RESTful API requests with methods other than POST/PUT/PATCH/DELETE

### Improvements

* [Custom Keywords] Organize Custom Keywords in an alphabetical order in Keyword Browser and support categorizing them with `keywordObject`. [Learn more](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html#create-a-custom-keyword)
* Improve Katalon Studio's performance of checking/unchecking test folders containing more than 50 Test Cases
* Log Viewer has a new design: Root cause shown on the top of the stack trace and Test Object ID added to Selenium’s common exceptions for better debugging.
* [Desktop Testing] Increase the default timeout and allow changing this default value when using `switchToWindowTitle` during recording and executing tests. [Learn more](https://docs.katalon.com/katalon-studio/docs/windows-kw-switch-window-title.html#setting-timeout)

### Fixes

* Bug: [Mobile] NullPointerException exception thrown by the `startExistingApplication` keyword when running on a Sauce Labs device
* Bug: [Mobile] Unable to capture objects using Spy Mobile

## Version 7.5.0 - 7.5.2

### New features

* [Katalon Studio Enterprise] Implement Native Windows Recorder (for Windows only). [Learn more](https://docs.katalon.com/katalon-studio/docs/windows-native-record.html)
* [Katalon Studio Enterprise] Send Test Suite Collection's report emails. [Learn more](https://docs.katalon.com/katalon-studio/docs/execution-settings.html#emails-settings)
* [Katalon Studio Enterprise] Support retrying Failed test data only in Test Suite's execution. [Learn more](https://docs.katalon.com/katalon-studio/docs/test-suite.html#modify-execution-information)
* [Web Testing] Support a new WebUI keyword to upload files by drag-and-drop. [Learn more](https://docs.katalon.com/katalon-studio/docs/webui-upload-file-drag-and-drop.html)
* Allow setting a default execution profile at project level. [Learn more](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html#set-default-profile-at-project-level)

### Improvements

* Support Microsoft Edge (Chromium) 83
* Support Chrome 83
* [Katalon Runtime Engine] Improve execution log in CLI mode by printing out applied proxy configurations
* Improve Proxy Settings with two separate types, including **Authentication** and **System** proxies. [Learn more](https://docs.katalon.com/katalon-studio/docs/katalon-studio-preferences.html#proxy-preferences)
* [Web Service] Enhance WSDL importing feature. [Learn more](https://docs.katalon.com/katalon-studio/docs/import-soap-requests-from-wsdl.html).
* [Web Service] Support defining a content type for form-data HTTP Body of RESTful requests. [Learn more](https://docs.katalon.com/katalon-studio/docs/restful.html#request-body)
* Downgrade the MySQL Connector/J, the official JDBC driver for MySQL, from 8.0.17 to 8.0.15
* Upgrade the Microsoft JDBC Driver 6.2 for SQL Server
* Enhance GUI of the following components: Image-based Testing in Tests Explorer, Katalon TestOps (Beta) Integration dialog, Activation dialog, and CAPTCHA error in the Activation dialog

### Fixes

* Bug: An issue of OAUth1.0 Authorization
* Bug: [Mobile Testing] Unable to scroll down to see all test object attributes
* Bug: [Tests Explorer] Unable to open a feature file if it is not under the **Include** folder. Address [#293](https://github.com/katalon-studio/katalon-studio/issues/293)
* Bug: Window Objects' references in Test Case not being updated automatically when Windows Objects are renamed. Address [#289](https://github.com/katalon-studio/katalon-studio/issues/289)
* Bug: Exposing proxy password

## Version 7.4.0

### New features

* Support migrating Selenium/TestNG/JUnit test scripts to Katalon Studio. [Learn more](https://docs.katalon.com/katalon-studio/docs/selenium-testng-junit-migration.html)
* Publish [TestNG/JUnit Keywords](https://store.katalon.com/product/180/TestNG-JUnit-Keywords) plugin
* Support Chrome 81

## Version 7.3.2 - 7.3.3

### Fix

* Bug: Unable to activate Katalon Runtime Engine on Oracle Linux Server 7.6

## Version 7.3.1

### Improvement

* [Katalon Runtime Engine] Improve execution log in CLI mode

### Fixes

* Bug: Unable to activate Katalon Studio
* Bug: Unable to open a containing folder of a package in Tests Explorer
* Bug: [Web Service] An issue of saving HTTP Body content created with `x-www-form-urlencoded` or `form-data` option
* Bug: [Web Service] An issue of handling API response in XML format
* Bug: [Web Service] Unable to send a SOAP request behind proxy
* Bug: [DDT] An issue of Database Connection settings being saved across projects

## Version 7.3.0

### New Features

* Support Microsoft Edge (Chromium) on both Windows and macOS
* [Windows] Support parameterizing Windows test objects. [Learn more](https://docs.katalon.com/katalon-studio/docs/windows-test-objects.html#parameterize-windows-test-objects)
* Add a Notification icon

### Improvements

* Support configuring `Delay Between Actions` in milliseconds in Execution settings
* Enhance UI
* Include the `TestObject` class in [Katalon API Documents](https://docs.katalon.com/javadoc/index.html)

### Fixes

* Bug: [Runtime Engine] An issue of counting the number of execution processes
* Bug: [Windows] An issue of debugging Windows test scripts
* Bug: [Kobiton Integration] An issue of not displaying error message for invalid account
* Bug: [BDD] `runFeatureFolder` throws exception when tests fail
* Bug: An issue of configuring the port of Mail Server in Email settings
* Bug: [API] Unable to send a request in macOS or Linux if its HTTP body uses `form-data` or `file` with relative path on Windows machine

## Version 7.2.7

### Fixes

* Bug: [BDD] `java.lang.NoClassDefFoundError` thrown when running a feature file
* Bug: An issue of Smart Wait preventing request state in XMLHttpRequest from being read

## Version 7.2.6

### Fixes

* Bug: Fail to activate Katalon Studio Enterprise with Katalon accounts registered with unconventional domains such as `.technology`.
* Bug: [Desktop Apps Testing] An issue of losing Windows test objects when users drag and drop their folders.
* Bug: [Desktop Apps Testing] An issue with automatically updating Windows test objects' references in Test Scripts after a drag and drop.
* Bug: [Desktop Apps Testing] Cannot identify Windows test objects by relative path.
* Bug: [Desktop Apps Testing] Cannot create a new item with a right-click on a Windows object.
* Bug: [Desktop Apps Testing] Cannot edit a Windows object's property.
* Bug: [Mobile Testing] A performance issue of the `setSliderValue` keyword when testing with a Sauce Labs device.
* Bug: [Mobile Testing] Fail to recognize iPad device and create a new remote session with iPad simulator.

### Discontinued Support

* Business Support Service

## Version 7.2.5

### New Features

* [Web Service] Support configuring Content Type in HTTP Header separately from HTTP Body. [Learn more](https://docs.katalon.com/katalon-studio/docs/restful.html).

### Improvements

* [Kobiton Integration] Allow customizing Kobiton Server URL in Katalon Studio Preferences.
* Enhance Smart Wait's performance during test executions.

### Fixes

* Bug: An issue related to a failure of Swagger's importing multiple requests without operation ID.
* Bug: An issue where Click step passes but no actual action is performed.

## Version 7.2.4

### New Features

* Support editing JVM parameters in Execution Settings. [Learn more](https://docs.katalon.com/katalon-studio/docs/execution-settings.html#execution-settings).

## Version 7.2.3

### Fixes

* Bug: Cannot send SOAP Request due to failure in parsing WSDL definition

## Version 7.2.2

### New Features

* [Web Testing] Support image-based object recognition. [Learn more](https://docs.katalon.com/katalon-studio/docs/manage-web-test-object.html#visual-object-recognition)

## Version 7.2.0 - 7.2.1

### New Features

* New Windows keywords:
  * [`getElementPosition`](https://docs.katalon.com/katalon-studio/docs/windows-kw-get-element-position.html)
  * [`getElementRect`](https://docs.katalon.com/katalon-studio/docs/windows-kw-get-element-rect.html)
  * [`startApplicationWithTitle`](https://docs.katalon.com/katalon-studio/docs/windows-kw-start-app-title.html)
  * [`switchToWindow`](https://docs.katalon.com/katalon-studio/docs/windows-kw-switch-window.html)
  * [`switchToWindowTitle`](https://docs.katalon.com/katalon-studio/docs/windows-kw-switch-window-title.html)
* New Mobile keywords:
  * [`executeMobileCommand`](https://docs.katalon.com/katalon-studio/docs/mobile-execute-command.html)
  * [`doubleTap`](https://docs.katalon.com/katalon-studio/docs/mobile-double-tap.html)
  * [`longPress`](https://docs.katalon.com/katalon-studio/docs/mobile-long-press.html)
  * [`setEncryptedText`](https://docs.katalon.com/katalon-studio/docs/mobile-set-encrypted-text.html)
* Support adding [Proxy Exceptions](https://docs.katalon.com/katalon-studio/docs/proxy-preferences.html) in Proxy Preferences and `-proxy.excludes` option in console mode.
* [Mobile Recorder] Implement the following actions: Get Text, Swipe, and Scroll To Text.

### Changes and Improvements

* Support ChromeDriver version 79.
* Add **Profiles** to Test Suite Collection Report.
* [Mobile- iOS] Support **Install Dependencies** and **Install WebDriverAgent** tools on the main menu. Please be noted that you have to install [homebrew](https://brew.sh/) manually.
* [Command Syntax] Support both `-serverUrl` and `-serverURL` arguments.
* Make the `DriverFactory.changeWebDriver()` method a public method.
* Support **Open containing folder** for Folders in Tests Explorer.

### Fixes

* Bug: [Windows] An issue related to creating a project.
* Bug: An issue related to saving Web Service Message.
* Bug: Empty result tab after a Test Suite execution.
* Bug: Test Script lost parens in method call after editing some steps.
* Bug: [KRE] an issue related to the `retry` option.
* Bug: [Web] Cannot set a timeout in **Wait for options**.
* Bug: [Web Service Request] an issue related to saving HTTP Header.

## Version 7.1.0-7.1.1

### New Features

* [Katalon TestOps (Beta)] Support Billing Manager role for being in charge of subscription. [Learn more](https://docs.katalon.com/katalon-analytics/docs/kt-user-role-permission.html).
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

## Version 7.0.0- 7.0.10

### New Features

* Support **Close and Clean up** item in Project menu for closing the project and removing the following items: `.classpath`, and  `.project` files; `bin`, `Libs`, and `.settings` folders.
* Support manually uploading Test Suite Collections' results to Katalon TestOps (Beta).
* Support connecting to Git with SSH. [Learn more](https://docs.katalon.com/katalon-studio/docs/git-integration.html)
* Allow configuring the usage tracked by Katalon Studio. [Learn more](https://docs.katalon.com/katalon-studio/docs/katalon-studio-preferences.html).
* Support data-driven testing with additional database sources. [Learn more](https://docs.katalon.com/katalon-studio/docs/database-settings.html).
* Support attaching Katalon Studio's source code for debugging. [Learn more](https://docs.katalon.com/katalon-studio/docs/debugging_test_case.html).
* Support customizing Tests Explorer. [Learn more](https://docs.katalon.com/katalon-studio/docs/toolbars-and-views.html#tests-explorer-view).
* Support Test Objects refactoring. [Learn more](https://docs.katalon.com/katalon-studio/docs/test-objects-refactoring.html).
* Support Custom Keywords refactoring. [Learn more](https://docs.katalon.com/katalon-studio/docs/custom-keywords-refactor.html).
* Support private plugins. [Learn more](https://docs.katalon.com/katalon-studio/docs/private-plugins.html).
* Support Windows 10 desktop application testing. See [Windows Desktop Apps Test Design](https://docs.katalon.com/katalon-studio/docs/introduction-desktop-app-testing.html).
* Support sharing test artifacts across projects. [Learn more](https://docs.katalon.com/katalon-studio/docs/import-export-test-artifact.html).
* Support Smart Wait function in a script and a project. See [[WebUI] Smart Wait Function](https://docs.katalon.com/katalon-studio/docs/webui-smartwait.html).
* Support [the WinAppDriver installation](https://docs.katalon.com/katalon-studio/docs/setup-winappdriver.html) and [`Terminate running WebDrivers`](https://docs.katalon.com/katalon-studio/docs/handle-webdrivers.html) options in Katalon Studio Tools.
* Support WebDriver event listeners. [Learn more](https://docs.katalon.com/katalon-studio/docs/webdriver-event-listeners.html).
* Support customizing the Console log. [Learn more](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html).
* Support Cucumber keywords executing one or multiple feature files with tags. Learn more about [runFeatureFileWithTags](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-feature-file-tag.html) and [runFeatureFolderWithTags](https://docs.katalon.com/katalon-studio/docs/cucumber-kw-run-feature-folder-tag.html).

### Changes and Improvements

* [Web Service] Encode special characters in query parameters.
* Revert **IEDriverServer** from 3.141.59 to 3.6.0.
* [Console mode] The `katalon` launcher is replaced by `katalonc` and there is a separate app named **Katalon Studio Runtime Engine** for executing Katalon Studio in console mode. Click [here](https://www.katalon.com/download/) to download.
* Convert **qTest** and **Kobiton** built-in integrations into plugins.
* Display errors of test scripts in the **Problems** view.
* Support ChromeDriver version 77 and IEDriverServer version 3.141.59.
* Show a full stack trace of an exception thrown by custom classes in Test Hooks.
* Support manually uploading test suite collections' results to Katalon TestOps (Beta).
* [Web Service] Support passing proxy details through the script. [Learn more](https://docs.katalon.com/katalon-studio/docs/proxy-preferences.html#pass-proxy-details-through-the-script).
* Update documents of [Katalon Studio API Specification](https://docs.katalon.com/javadoc/index.html) to version 7.0.0.
* Upgrade Apache POI to version 3.17.
* Dynamic Querying Test Suite is renamed Dynamic Test Suite.
* Add plugins reloading options to the Project Settings.
* Support parsing the Request Message's template from the associated `XSD` file when importing test objects from WSDL.
* Support adding the Organisation ID parameter to the Command Generator.
* Support selecting a Katalon TestOps (Beta)'s organization on the activation.
* Enhancement: Add some JVM options to reduce Katalon Studio's memory consumption.
* Support a hotkey of Spy Utility in Web Recorder to capture objects. [Learn more](https://docs.katalon.com/katalon-studio/docs/record-web-utility.html).
* Update **Quick Start** in Katalon Studio after activation.
* Support adding `.gitignore` and `build.gradle` files when creating a project.
* Support uploading reports with pdf, HTML, CSV formats (generated by Basic Report plugin) to Katalon TestOps (Beta). [Learn more](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).
* Support submitting test run results with captured videos to Katalon TestOps (Beta). [Learn more](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).
* Support uploading the `*.rp` file to Katalon TestOps (Beta) to parse more information on test results.
* Support creating a test plan right from the test suite collection screen in Katalon Studio to enhance the integration of Katalon Studio with Katalon TestOps (Beta). [Learn more](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).
* Support uploading Project Code from Katalon Studio to Katalon TestOps (Beta). [Learn more](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).
* Update the integration mechanism with Katalon TestOps (Beta). [Learn more](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).
* Update the integration configurations with Katalon TestOps (Beta) when a new project is created.
* Support auto-filling the input of [Katalon API Key](https://docs.katalon.com/katalon-studio/docs/katalon-apikey-70.html) in the command-line generator.
* Support generating test results in JUnit format.
* Support uploading reports of test suite collections to Katalon TestOps (Beta).
* Remove unnecessary information in the console log when users execute in the console mode for the first time.
* Support passing more information to the console mode execution with `--info -buildLabel="text" -buildURL="text"`. See [General Options ](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options) in Console Mode Execution.
* Upgrade the activation mechanism in Katalon Studio to seamlessly integrate with Katalon TestOps (Beta). See [Activate Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-studio-activation-since-70.html).
* Merge the Plugins menu into the Tools menu.
* Support MySQL Database version **8.0.17**.
* Support automatically reloading plugins when opening a project.

### Fixes

* Bug: [DDT] Cannot get values from data files with database type in a test case.
* Bug: Cannot log in to Katalon Studio with passwords containing special characters.
* Bug: [Web Service] SOAP response has an empty header.
* Bug: Cannot reload plugins with credentials containing special characters.
* Bug: The **Results** tab of Test Suites/Test Suite Collection fails to automatically refresh after the first execution.
* Bug: **Show references** of test objects fails to display the objects' references in global variables and test case variables.
* Bug: Cannot send SOAP requests when **WSDL** files contain the relative `xsi:schemaLocation`.
* Bug: [WebUI Keyword] The `WebUI.clickImage` keyword fails to perform.
* Bug: [Web Service] `getCurrentRequest()` always gets default values instead of a variable's values passed from test case.
* Bug: Incorrectly return code when **Follow redirects** is disabled in Web Service Request. [More details](https://forum.katalon.com/t/followreridects-does-not-work/33800).
* Bug: Cannot save modifications in the configuration tab of the Web Service Request.
* Bug: Cannot detect mobile test objects having parameterized global variables in their properties.
* Bug: [Console Mode] To retry executing failed test cases in Test Suite Collection fails to return the correct exit code.
* Bug: [Data Binding] An issue causes binding Variables to Test Data to fail.
* Bug: [WebService] Verification Editor doesn't keep Unicode characters.
* Bug: [Mobile Testing] Cannot retry executing failed test cases.
* Bug: Web service response displays garbled text as non-Latin characters.
* Bug: [Basic Report Plugin] CSV Report status is always Incomplete.
* Bug: The Log Viewer’s cursor incorrectly renders when selecting a log message.
* Bug: Newly added variables disappear after a switch from the Variable tab to another tab.
* Bug: An issue related to Variable binding when the data contains special characters.
* Bug: The Delay keyword doesn't work when the passing data is BigDecimal.
* Bug: Har files disappear after having been opened for the first time with the current Web Service object.
* Bug: [Custom Keyword] an issue related to the default package name when users create a keyword without entering a package name.
* Bug: [Katalon TestOps (Beta)] Cannot navigate to the URL configured by users in View Execution History.
* Bug: [Katalon TestOps (Beta)] an issue related to the error message when users create a new project for the invited team without permission.
* Bug: [GlobalVariable] Cannot execute a script with a profile that has a Global Variable with invalid syntax.
* Bug: [WebUI Keywords]  The `verifyElementPresent()` and `verifyElementNotPresent()` keywords should return `false` instead of throwing an exception when the verified elements do not exist.
* Bug: The `Delay between actions` fails to perform as configured.
* Bug: An issue causes `callTestCase` to fail.
* Bug: `findWebElements` fails when the `Default wait for element timeout` is set to 0 in the Execution Settings.
* Bug: [Web Recorder] An issue related to the `Cannot save entity: file path length limit exceeded.` error when saving test objects.
* Bug: Custom Keywords are not displayed in the Recent keywords after being used.
* Bug: An issue related to renaming a folder with uppercase or lowercase characters. [More details](https://github.com/katalon-studio/katalon-studio/issues/189).
