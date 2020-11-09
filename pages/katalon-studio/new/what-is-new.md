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

Optimize the workflow of fixing broken test objects after execution by capturing the HTML page source upon failure

Significantly cut off test maintenance time 

Save team effort on test result investigation

### Support browser-based video recorder

Address the unserved needs of the following use cases

Record Headless browsers

Record the browser instance instead of the screen

Record multiple testing browser instances simultaneously

### Windows testing: Coordinates-based recording 

record an element's relative coordinates in addition to its selector to identify the exact location to perform a click/right-click action during runtime.

### Improve ALM & Cloud device provider integration

* Kobiton: Support SSO for authentication

* Studio-qTest integration with the following features 

Synchronise qTest Test Case version and test steps content

Support Studio-qTest Parity Report in HTML  for TS/TSC execution

Update skipped status for qTest test cases

This version enhances the integration between qTest and Katalon Studio with the following new features:

qTest - Katalon Studio parity report is generated for each test execution, helping users quickly check if the integration between test cases of two systems is up-to-date. (Turn on this setting in Project/Settings/Plugins/qTest)
In the integrated Katalon Studio Test Case, you can view the qTest Test Case version information and check if there is a newer version on the qTest server. Open a test case editor, select the Integration tab.
Retrieve the latest version and test steps content of the integrated qTest Test Case from qTest Server for multiple selected test cases at once. Learn more

* [Jira Integration] Support BDD custom field for Jira cloud

### Import your web services from SoapUI and WSDL

Migrate SOAP request objects from SoapUI to Katalon Studio

Allow importing SOAP WSDL without service endpoint (already supported by SoapUI)

### Start Page and Test Explorer

We've updated Start Page with a fresh look and more information about the license and subscription of each user. [Let us know what you think](mailto:jass@katalon.com).

### Security and Intellectual Property Compliance

* Checksum
* Provide a report of Open Source License scanning


### Enhance Katalon Studio - Katalon TestOps Integration

Generate command for TestOps CI 

Export BDD reports in Katalon Studio to be displayed in TestOps 

Allow overriding TestOps project ID in CLI

Display Releases in Test Explorer



