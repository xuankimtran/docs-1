---
title: "[WebUI] Analyze Test Suite Reports and Resolve Errors"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports.html
description: 
---

After Test Suite execution, Katalon Studio generates Test Suite reports that organize the execution logs of the respective Test Cases contained within the suite. You can view Test Suite reports to monitor test coverage and troubleshoot errors quickly.

This tutorial walks you through the steps to analyze a Test Suite report and resolve errors.

In our example, the Test Suite contains a Test Case with the scenario "Order and check out a single product multiple times." This Test Suite uses incorrect test data that result in an execution error. With the Test Suite report generated, we use the interface provided by Katalon Studio to analyze the Test Suite report and resolve the error.

> You can download the sample project here: [Shopping Cart Tests](https://github.com/katalon-studio-samples/shopping-cart-tests).

## Analyze a Test Suite Report

After executing the Test Suite, we view the report directly within Katalon Studio.

Follow these steps:

1. Open the Report History section. Go to **Test Explorer > Reports**.

    The Report History section organizes Test Suite Reports into separate folders with execution dates in the format *YYYYMMDD_HHmmss*.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Reports-Section-overview.png" width=30% alt="Test Explorer/Report History">

    Here we view the latest execution report by expanding the folder.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Reports-Section-expand-folder.png" width=30% alt="Test Explorer/Report History expanded">

2. To open the report, double-click on it.

    In our example, the report is displayed as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Displayed-Test-Suite-reports.png" width=70% alt="Test Suite report overview">

    Katalon Studio lists the Test Cases in the **Test Cases Table** with different execution statuses: *Passed*, *Failed*, *Error*, *Incomplete*, and *Skipped*.

    Here we have four Test executions; the second Test execution has an *Error* status.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Test-Cases-Table.png" width=70% alt="Test Cases Table">

    The *Error* status indicates user mistakes in writing Test Cases, such as incorrect syntax, missing test objects, or incorrect test data.

    By contrast, a *Failed* status would indicate that the application under test (AUT) fails to perform a function expected by the Test Case, such as an unexpected change in the Web user interface.

    Below the **Test Cases Table** is the Report Summary section.

    The report summary includes information about the Test Suite, such as the Test Suite ID, execution environment, execution time, and execution status.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Test-Suite-Report-Summary.png" width=70% alt="Test Suite Summary">

3. Open the Test Case Log. Select a Test Case in the **Test Cases Table** and click on the **Show Test Case Details** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Test-Suite-Reports-Show-Test-Cases-Details-button.png" width=30% alt="Show Test Case Details button">

    The execution log of the selected Test Case is displayed as follows:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Test-Suite-Report-Displayed-Test-Case-Log.png" width=70% alt="Test Case's Log section">

    This log section outlines the steps in the Test Case with their execution statuses.

4. To view the detailed log message, double-click on the step. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Test-Suite-Report-Detailed-Log-Message.png" width=70% alt="Detailed Log Message">

    The message is displayed in the **Information** tab below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Test-Report-Log-Message.png" width=70% alt="Detailed Log Message">

    In our example, step 5 of the Test Case contains an error with the exception `com.kms.katalon.core.exception.StepErrorException: org.openqa.selenium.NoSuchElementException`. 
    The keyword `sample.Checkout.CheckoutShop()` in this step failed to locate the element with the XPath `normalize-space(text())='Neverland'`.

    Since the Test Suite contains only one Test Case, we know that the error in the second Test execution is caused by incorrect test data. Specifically, the second Test execution failed to locate a Web element using the text data `'Neverland'`.

    > To learn how to troubleshoot common exceptions in Web tests, you can refer to this document: [Troubleshoot common exceptions when executing web tests](https://docs.katalon.com/katalon-studio/docs/troubleshoot-common-execution-exceptions-web-test.html).

## Resolve the Error

Because the incorrect test data in our example is associated with an external data file (Excel test data), we navigate to the data file and update it.

> To learn more about Test Data management, refer to this guide: [Manage Test Data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html).

Follow these steps:

1. Open the Test Suite, then click on the **Show Data Binding** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Open-Test-Suite.png" width=70% alt="Opened Test Suite">

2. Open the associated data file. In the displayed **Test Data** section, right-click on the data file in use and select **Open *Data File***.

    In our example, we open the data file "Multiple Checkout."

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Data-Binding-Right-Click-on-Data-File.png" width=70% alt="Right-click on Data Fle">

3. Update the data file.

    In the opened data file, we can see the file contains the incorrect test data.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Incorrect-Data-File.png" width=70% alt="Incorrect Test Data">

    We then update the data file with the correct test data.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Correct-Data-File.png" width=70% alt="Corrected Test Data">

4. Run the Test Suite and verify the results in the new Test Report.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/webui-view-and-analyze-test-suite-reports/KS-Displayed-Successful-Test-Suite-reports.png" width=70% alt="Successful Test Report">

> **Notes**:
>
> For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

**See also**:

* [Test Suite and Test Suite Collection Reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html).