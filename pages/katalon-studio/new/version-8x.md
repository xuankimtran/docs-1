---
title: "Official Release - Version 8.0.0" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/new/version-8x.html
redirect_from:
    - "/katalon-studio/new/all-versions.html"
description: Release notes 8.0
---

### New Features

* [Katalon Studio Enterprise] Support native integration with Azure DevOps Test Plans. [Learn more](/katalon-studio/docs/azure-devops-test-plans.html)
* [Katalon Studio Enterprise] Import/Export desired capabilities. [Learn more](/katalon-studio/docs/import-export-desired-capabilities.html)
* [Katalon Runtime Engine License] Add a parameter to release the previous execution session before checking license. [Learn more]()
* Product Tours for new Web UI and Web Service users.

### Improvements

* Improve Performance: Load large projects faster and consume less memory during execution.
* Edge Chromium is now the default **embedded browser** (used to be Internet Explorer).
* Web Testing: Update the embedded GeckoDriver to the latest version.
* [Windows OS] Replace embedded Oracle JRE 8 with Azul Zulu OpenJDK 8.
* Enhance Katalon TestOps Integration:
    * [Katalon Runtime Engine] Support query for Test Suite Collection. [Learn more]()
    * [Katalon Runtime Engine] Support new parameters for new Build concept. [Learn more]()
* [Katalon Runtime Engine] Pass HashMap for Global Variables from CLI.
* [Katalon Runtime Engine] Add an option to Command Builder for updating WebDriver automatically.
* [Enhanced Report] Add profile details to the email reports.

### Changes

* Katalon accounts registered with personal email are eligible for Katalon Studio Enterprise and Katalon Runtime Engine trial licenses for 30 days.
* MySQL becomes an external library. To continue using it, follow [this guide](/katalon-studio/tutorials/how-to-implement-ddt-mysql.html) to configure MySQL database connection.

### Fixes

* Bug: Fix all blocker & critical security vulnerabilities reported by SonarQube in static code analysis and 3rd-party libraries scanning tools. 
* Bug: [Katalon Runtime Engine] Lacking of tracking event for activation.
* Bug: An issue of not displaying an error message when removing MySQL driver.
* Bug: [Katalon Studio Enterprise] [Windows] An issue of generating PDF reports.
* Bug: [Windows] Missing Network connection Preference.
* Bug: [Chorme 86] Recorder function is not working.
* Bug: Cannot import Swagger JSON files.
* Bug: [Katalon Studio Enterprise] Cannot clone an existing project from GIT.
* Bug: The Bypass Certificate validation option is not working.
* Bug: [Katalon Runtime Engine] An issue of not sending emails.
* Bug: [Windows Testing] Test Suite Collection does not execute the 2nd Test Suite.
* Bug: An issue of deleting scripts when renaming folder name.
* Bug: [Chrome 87] An error thrown in the HTML execution result.
* Bug: Cannot drag and drop a custom keyword from Keyword Browser.
* Bug: An issue of not updating References of Called Test Cases in Test Listeners when the test cases are moved by drag and drop or cut and paste.
