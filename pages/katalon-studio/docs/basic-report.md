---
title: "Basic Report"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/basic-report.html
description: Guide on how to use Basic Report plugin
---
Basic Report Plugin is a Custom Keyword that replaces the current Report feature of Katalon Studio. Starting from [version 6.1.5](https://docs.katalon.com/katalon-studio/new/version-615.html), the Report feature has been migrated to the Basic Report plugin.  You need to install this plugin to generate reports of Test Suite execution with HTML, CSV, and PDF formats.

> [Install Basic Report](https://store.katalon.com/product/59/Basic-Report)

Starting from version 7.0, Katalon Studio automatically generates junit report for both Test Suite and Test Suite Collection.

## Automatically generate reports

1. In **Project > Settings > Plugins > Report**, select the formats of reports that will be automatically generated after each Test Suite execution.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Basic%20Report/report-settings.png" width="546" height="318">

2. Execute a Test Suite and observe the *Log Viewer* after the test execution completes. The generated reports will be the same as the settings you've configured above.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Basic%20Report/log-viewer.png" width="391" height="87">

   You can view the generated reports in **<project_folder>\\Reports\\<execution_folder>** after the test execution finishes.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Basic%20Report/report-folder.png" width="" height="">

## Manually export reports

Open the **Result** view of a Test Suite or a Test Suite Collection > on the top right corner, select **Export report** > choose a format to export.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/Basic%20Report/report%201.png" width="1030" height="181">

> For Test Suite Collection, you can export to HTML format only.
