---
title: "[WebUI] View and Analyze Test Suite Reports"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports.html
description: 
---

After Test Suite execution, Katalon Studio generates Test Suite reports that organize the execution logs of the respective Test Cases contained within the suite. You can view Test Suite reports to monitor test coverage and troubleshoot errors quickly.

This tutorial walks you through the steps to view and analyze a Test Suite report.

Here we use a Test Suite that consists of Test Cases with the scenario "Order and check out a single product multiple times." With the Test Suite report generated, we use the interface provided by Katalon Studio to analyze the Test Suite report and pinpoint some errors.

> You can download the sample project here: [Shopping Cart Tests](https://github.com/katalon-studio-samples/shopping-cart-tests).

## Analyze a Test Suite Report

After executing the Test Suite, we view the report directly within Katalon Studio.

Follow these steps:

1. To open the Report History section, go to **Test Explorer > Reports**.

    The Report History section organizes Test Suite Reports into separate folders with execution dates in the format *YYYYMMDD_HHmmss*.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Reports-Section-overview.png" width=30% alt="Test Explorer/Report History">

    Here we view the latest execution report by expanding the folder.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Reports-Section-expand-folder.png" width=30% alt="Test Explorer/Report History expanded">

2. To open the report, double-click on it.

    In our example, the report is displayed as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Displayed-Test-Suite-reports.png" width=70% alt="Test Suite report overview">

    Katalon Studio lists the Test Cases in the **Test Cases Table** with different execution statuses: *Passed*, *Failed*, *Error*, *Incomplete*, and *Skipped*.

    Here we have one Test Case with the *Error* status.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Test-Cases-Table.png" width=70% alt="Test Cases Table">

    Below the **Test Cases Table** is the Report Summary section.

    The report summary includes some information about the Test Suite, such as the Test Suite ID, execution environment, execution time, and execution status.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Test-Suite-Report-Summary.png" width=70% alt="Test Suite Summary">

3. Open the Test Case Log. Select a Test Case in the **Test Cases Table** and click on the **Show Test Case Details** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Test-Suite-Reports-Show-Test-Cases-Details-button.png" width=30% alt="Show Test Case Details button">

    The execution log of the selected Test Case is displayed as follows:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Test-Suite-Report-Displayed-Test-Case-Log.png" width=70% alt="Test Case's Log section">

    This log section outlines the steps in the Test Case with their execution statuses.

4. To view the detailed log message, double-click on the step. The message is displayed in the **Information** tab below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Test-Suite-Report-Detailed-Log-Message.png" width=70% alt="Detailed Log Message">

    In our example, step 5 contains an error with the exception `com.kms.katalon.core.exception.StepErrorException: org.openqa.selenium.NoSuchElementException`. The log message also provides a useful link to a troubleshooting document.

    > To learn how to troubleshoot common exceptions in Web tests, you can refer to this document: [Troubleshoot common exceptions when executing web tests](https://docs.katalon.com/katalon-studio/docs/troubleshoot-common-execution-exceptions-web-test.html).

> **Notes**:
>
> For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

**See also**:

* [Test Suite and Test Suite Collection Reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html).