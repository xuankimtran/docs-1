---
title: "Test Artifacts Sharing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/import-export-test-artifact.html 
description: Instruction of how to export and import test artifacts
---
> This feature is available starting from [version 7.0.0](https://docs.katalon.com/katalon-studio/new/version-70.html).

Test artifacts sharing allows you to import and export test artifacts across Katalon Studio projects. These test artifacts include test cases, test objects, profiles, and custom keywords.

> **Note**: You can only import test artifacts exported from Katalon Studio. The format of the exported file name is `shared-[timestamp].zip`.

## Export test artifacts

1. From the main menu, **Tools > Utility > Export Test Artifact**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-export-test-artifact/Export-test-artifact.png" width="528" height="150">

2. In the **Export Test Artifacts** window:

* Add the test cases, test objects, profiles, and/or custom keywords that you'd like to export.
* Under **Export Location**, select the destination folder for the exported file(s).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-export-test-artifact/export-test-artifacts.png" width="497" height="797">

3. Click **OK** to export the selected test artifacts.

## Import test artifacts

The test artifacts you'd like to import must be exported from a Katalon Studio project.

1. From the main menu, **Tools > Utility > Import Test Artifact**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-export-test-artifact/Import-test-artifacts.png" width="521" height="153">

2. In the **Import Test Artifacts** window, choose your desired file to import, test case import location, and test object import location.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/import-export-test-artifact/import-test-artifact.png" width="496" height="171"> 

3. Click **OK**. Refresh the test explorer by right-clicking > **Refresh** to view them in the specified locations.


