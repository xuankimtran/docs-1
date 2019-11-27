---
title: "View Reports"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/project-management-view-reports.html
redirect_from:
    - "/display/KA/View+Reports/"
    - "/display/KA/View%20Reports/"
    - "/x/2RxO/"
    - "/katalon-analytics/docs/project-management-view-reports/"
    - "/katalon-studio/tutorials/viewing_test_execution_reports_katalon_analytics.html"
description:
---
## Access reports

Reports in Katalon TestOps are automatically generated based on one or more datasets of automation test results imported in such different formats as Katalon Studio, Katalon Recorder, and JUnit.

Reports can be viewed in the **Test Result** page. Currently, Katalon TestOps shares with you several reports with different insights and findings including Status and Performance reports; Test Executions table; [Test Execution, Test Suite, and Test Case details](katalon-analytics/docs/view-details.html).

## View reports

**Status Report** gives a visual demonstration of historical test result data according to test status, from which you can easily identify trends and patterns of each status. The status report is created from those values as follows:

* the number of test runs
* the number of test executions
* the status of each test run (Passed, Failed, Error, Incomplete)

**Performance Report** visualizes the length of time one test execution took to finish, illustrating trends of duration over time. Any dramatic change in trend may signify a performance issue of the AUT. The performance report is created from those values as follows:

* the duration of each Test Suite
* the number of executions per Test Suite

**Test Executions Table** gives a comprehensive view of your dataset. Testers can read the comparisons between certain values with ease.

Users can manage their data by viewing, downloading, deleting and re-importing test results.

* **Status**: a test status of each Test Suite
* **ID**: an ordinal number that uniquely identifies each Test Suite in a project
* **Test Suite**: the name of each Test Suite
* **Profile**: default or a user's custom input
* **Started**: when the test suite or test suite collection was executed
* **Duration**: the length of time the test lasted
* **Total**: the total number of test cases in one execution
* **P/F/E and I**: the number of test executions according to each type of test results.
* **By**: the user importing the data.
