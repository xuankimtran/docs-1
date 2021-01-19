---
title: "What's new in v7.8?" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/what-is-new-78.html
description: What's new in Katalon Studio 7.8
---

Katalon Studio 7.8 has been released with new capabilities aimed at efficient debugging and maintaining test scripts and enhanced integrations with qTest, Kobiton, Jira, or Katalon TestOps. The following section describes the highlighted new features and enhancements available in Katalon Studio 7.8.

For a detailed list of enhancements and bug fixes packed in this release, please see its [release notes](https://docs.katalon.com/katalon-studio/new/version-70.html).

### Time Capsule for saving effort in maintaining test objects  

To reduce the manual effort of re-capturing a broken test object when a test fails, Katalon Studio 7.8 supports restoring the AUT to the state on failure due to locators not finding Web UI objects. This robust capability equips you with a "time capsule" for fixing broken objects, reducing reproduction effort, and cutting off time spent on troubleshooting and maintaining your test scripts. [Learn more](https://docs.katalon.com/katalon-studio/docs/time-capsule.html).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/time-capsule/test-suite-fail.gif">

### Brand-new browser-based video recorder for Headless Execution

With Screen-based Recorder, you can capture what's visible on the screen, while with [the Browser-based Video Recorder](https://docs.katalon.com/katalon-studio/docs/screenshots-videos.html#browser-based-video-recorder), you can record videos of **Headless** browser. You can also record video of a browser window only (even it's hidden behind another window) or videos of multiple browsers simultaneously in parallel execution.

### Increased accuracy in locating Windows objects with coordinates-based recording

With coordinates-based recording for Windows testing, Katalon Studio captures an element's relative coordinates in addition to its selector during recording to identify the exact location to perform a click/right-click action during runtime.

Fail to select a Windows object:

<img alt="Native Windows Recorder without coordinates" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/native-windows-recorder-without-coordinates.gif" width=100%>

Select a Windows object successfully thanks to coodinates:

<img alt="Native Windows Recorder with coordinates" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/native-windows-recorder/native-windows-recorder-with-coordinates.gif" width=100%>

See also:

* [Click Element Offset](https://docs.katalon.com/katalon-studio/docs/windows-kw-click-element-offset.html) 
* [Right-click Element Offset](https://docs.katalon.com/katalon-studio/docs/windows-kw-rightclick-element-offset.html)
* [Windows Recorder](https://docs.katalon.com/katalon-studio/docs/windows-recorder-tutorials.html) 
* [Native Windows Recorder](https://docs.katalon.com/katalon-studio/docs/windows-native-record.html)

### Improve ALM & Cloud device provider integrations

In this major release, we shipped some important enhancements to improve the integration of Katalon Studio with Kobiton, Jira Cloud, and especially qTest. 

**Kobiton Integration**: When configuring Kobiton integration in your project, you can use your Kobiton's API Key to authenticate with the Kobiton Server. New command options for this enhancement is supported accordingly. [Learn more](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#integration-options)

**Jira Cloud Integration**: In this version and later, you can now import the BDD Feature Files from Jira Cloud Server after establishing a connection with a BDD custom field in Project Settings. [Learn more](https://docs.katalon.com/katalon-studio/docs/jira-integration.html#jira-cloud-integration)

**qTest**: This version enhances the integration between qTest and Katalon Studio with the following new features:

* Generate the qTest - Katalon Studio parity report in HTML for each test execution, which helps you quickly check if the integration between two systems' test cases is up-to-date (Turn on this setting in Project/Settings/Plugins/qTest and read more [here](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#qtest---katalon-studio-parity-report)).
* In the integrated Katalon Studio Test Case, you can view the qTest Test Case version information and check if there is a newer version on the qTest server. Open a test case editor, select the **Integration** tab.
* Retrieve the latest version and test steps content of the integrated qTest Test Case from qTest Server for multiple selected test cases at once. [Learn more](https://docs.katalon.com/katalon-studio/docs/qtest-integration.html#qtest-test-cases-version-control-and-synchronization)
* Send Skipped test results to qTest Server.

The following gif shows how to check which integrated Test Cases in Katalon Studio need updating based on the integrated qTest Test Cases:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/enable-qtest-integration/qtest-version-checking-in-bulk.gif" width=100%>

### Import your web services from SoapUI and WSDL

In addition to [importing RESTful requests from SoapUI](https://docs.katalon.com/katalon-studio/docs/import-soapui.html) (shipped in 7.6), now you can import SOAP test requests from SoapUI as well. Also, you can import SOAP requests from a WSDL file having no service endpoint.

### Provide In-app Tutorials for new users 

If you're in the transition from manual testing to automated testing, it may be overwhelming in the beginning. One of the core values we propose to our users is to make Katalon Studio easy to use. Keeping this in mind, we provide automated test beginners with in-app tutorials of all technologies we currently support, including Web UI, Mobile, Web Service, and Desktop. In future releases, we expect to provide tutorials of advanced features as well.

### Start Page and Test Explorer Makeovers

We've updated Start Page with a fresh look and more information about the license and subscription tailored to each user. [Let us know what you think!](mailto:jass@katalon.com).

### Security and Intellectual Property Compliance

For security and Intellectual Property compliance, from this version, we start to provide Checksum in `all-packages.sha256` for each Katalon Studio package
and Open-source libraries' license scanning report in HTML (`KatalonStudio-openSourceReport.html`). Go to [our GitHub Repository](https://github.com/katalon-studio/katalon-studio/releases), for each release from 7.8 onwards, download those files in each build's Assets.

### Enhance Katalon Studio - Katalon TestOps (Beta) Integration

In this release, we have improved the integration with Katalon TestOps (Beta) in multiple areas. 

* You can now generate a command for TestOps CI right in the Command Builder of Katalon Studio. 
* You can also decide which TestOps Project to feed your execution result when executing with Katalon Runtime Engine by overriding the Test Project ID via command line. 
* Katalon will automatically retry uploading Test Projects and Test Reports to Katalon TestOps upon failure.
* In Katalon Studio, you can view Releases and download execution reports retrieved from your TestOps project, which enhances your team's collaboration substantially when you can view execution reports pushed to TestOps by your teammates. While on Katalon TestOps, you can view BDD reports generated from Katalon Studio, which requires you to do some configurations beforehand. [Learn more here](https://docs.katalon.com/katalon-analytics/docs/bdd-test-results.html).




