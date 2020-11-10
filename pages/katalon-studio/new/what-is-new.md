---
title: "What's new in Katalon Studio 7.8" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/what-is-new.html
redirect_from:
    - "/katalon-studio/new/"
    - "/display/KD/Release+Notes/"
    - "/display/KD/Release%20Notes/"
description: What's new in Katalon Studio 7.8
---

Katalon Studio 7.8 has been released with new capabilities aimed at efficient debugging and maintaining test scripts and integrations with qTest, Kobiton, Jira or Katalon TestOps. The following section describes the highlighted new features and enhancements available in Katalon Studio 7.8

For a detailed list of enhancements and bug fixes packed in this release, please see its [changelog](https://docs.katalon.com/katalon-studio/new/version-70.html).

### Time Capsule for saving effort in maintaining test objects  

To reduce the manual effort of re-capturing a broken test object when test fails, Katalon Studio 7.8 supports restoring the AUT to the state on failure due to locators not finding Web UI objects. This robust capability equip you with a "time capsule" for fixing broken objects, reducing reproduction effort, and cutting off time spent on troubleshooting and maintaining your test scripts. [Learn more](https://docs.katalon.com/katalon-studio/docs/time-capsule.html).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/time-capsule/test-suite-fail.gif">

### Support browser-based video recorder

With Screen-based Recorder, you can capture what's visible on the screen while with [the Browser-based Video Recorder](https://docs.katalon.com/katalon-studio/docs/screenshots-videos.html#browser-based-video-recorder), you can:

* Record video of a browser window only (even it's hidden behind another window)
* Record video of Headless browser
* Record videos of multiple browsers simultaneously, for instance, parallel execution of Test Suite Collection.

### Windows testing: Coordinates-based recording

With coordinates-based recording, Katalon Studio records an element's relative coordinates in addition to its selector to identify the exact location to perform a click/right-click action during runtime.

See also:

* [Click Element Offset](https://docs.katalon.com/katalon-studio/docs/windows-kw-click-element-offset.html) 
* [Right-click Element Offset](https://docs.katalon.com/katalon-studio/docs/windows-kw-rightclick-element-offset.html)
* [Windows Recorder](https://docs.katalon.com/katalon-studio/docs/windows-recorder-tutorials.html) 
* [Native Windows Recorder](https://docs.katalon.com/katalon-studio/docs/windows-native-record.html)

### Improve ALM & Cloud device provider integrations

**Kobiton**: Support SSO for authentication

**Jira Cloud**: Support BDD custom field for Jira cloud

**qTest**: This version enhances the integration between qTest and Katalon Studio with the following new features:

* qTest - Katalon Studio parity report in HTML is generated for each test execution, helping users quickly check if the integration between test cases of two systems is up-to-date. (Turn on this setting in Project/Settings/Plugins/qTest)
* In the integrated Katalon Studio Test Case, you can view the qTest Test Case version information and check if there is a newer version on the qTest server. Open a test case editor, select the Integration tab.
* Retrieve the latest version and test steps content of the integrated qTest Test Case from qTest Server for multiple selected test cases at once. Learn more
* Send Skipped test results to qTest Server

### Import your web services from SoapUI and WSDL

In addition to [importing RESTful requests from SoapUI](https://docs.katalon.com/katalon-studio/docs/import-soapui.html) (shipped in 7.6), now you can import SOAP test requests from SoapUI as well. Also, to make it even more convenient, Katalon Studio supports adding SOAP requests from a WSDL file having no service endpoint (Right-click on Object Repository > select Import> select one of the supported sources of test requests).

### Start Page and Test Explorer

We've updated Start Page with a fresh look and more information about the license and subscription tailored to each user. [Let us know what you think](mailto:jass@katalon.com).

### Security and Intellectual Property Compliance

For security and Intellectual Property compliance, from this version, we start to provide Checksum for each Katalon Studio package named `all-packages.sha256`
and Open source libraries's license scanning report in HTML named `KatalonStudio-openSourceReport.html`. Go to [our GitHub Repository](https://github.com/katalon-studio/katalon-studio/releases), for each release from 7.8 onwards, download those files in each build's Assets.

### Enhance Katalon Studio - Katalon TestOps (Beta) Integration

In this release, we have improved the integration with Katalon TestOps (Beta) in multiple areas. 

* You now can generate command for TestOps CI right in the Command Builder of Katalon Studio. 
* You can also decide which TestOps Project to feed your execution result when executing with Katalon Runtime Engine by overriding the Test Project ID via command line. 
* In Katalon Studio, you can see the Releases retrieved from Katalon TestOps while on Katalon TestOps, you can view BDD reports generated from Katalon Studio, which requires you to do some configurations beforehand. [Learn more](https://docs.katalon.com/katalon-analytics/docs/bdd-test-results.html).




