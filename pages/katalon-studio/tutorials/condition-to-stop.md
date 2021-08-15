---
title: "Terminate Execution Conditionally"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/terminate-execution-conditionally.html
description: "This article provides the concept of terminating execution conditionally and the tutorial on common use cases."
---
In this article, you will learn how to terminate an automation execution by configuring a maximum number of test failures, with examples using common use cases.

>**Requirements**
>
>- Katalon Studio **version 8.1.0 onwards**.
>- A Katalon Runtime Engine License. See [Katalon licensing](https://docs.katalon.com/katalon-studio/docs/license.html).

From version 8.1.0 onwards, you can terminate an execution after T test failures number (T is the failure threshold value). Reaching the threshold value immediately stops the entire test run. You can set this condition via the command-line option.

The ability to terminate execution when reaching its failure threshold value helps you save time, provide early feedback, and avoid the execution of unnecessary automation test cases.

>**What is a test failure?**
>
>A test failure is a failed test case or test iteration in an execution.
>
>- 1 test case fails = 1 test failure
>- 1 retried test case fails = 1 test failure
>- 1 test iteration (test case + data row) fails = 1 test failure
>- 1 retried test iteration fails = 1 test failure
>
> The number of maximum test cases failure must be greater than 0 and a natural number (1,2,3...). Otherwise, Katalon Studio will not start the execution.

Consider using this parameter when:

- You have a high number of failed test cases in given test execution.
- You have a mature set of tests, and it takes hours to finish execution.
- You have a new code committed or a new build available, where a high number of test failures might reflect the quality of the new build.

You can use this feature to:

- Terminate a test suite.
 	- Terminate a test suite with configured Retry after executing all.
	- Terminate a test suite with configured Retry failed executions immediately.
	- Terminate a test suite with Data-driven testing.
	- Terminate a test suite with Data-driven testing and configured Retry after executing all.
	- Terminate a test suite with Data-driven testing with configured Retry failed executions immediately.
- Terminate a test suite collection executed in sequential mode.
- Terminate a test suite collection executed in parallel mode.

## Set a maximum number of test failures

### With Command Builder

>**Notes**: For detailed instruction on how to run a test execution in Console mode, see [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).

 To terminate test execution after T test failures, go to Katalon Studio and set a maximum number of test failures.
 
 1. In the toolbar, select **Build CMD** (Build Command).

 <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/build%20cmd.png" alt="build cmd" width=40%>

 2. In the **Generate Command for Console Mode > Execution Configurations**, check the box **Terminate the execution once the total number of test failures reaches this threshold**. In the text field, input your desired maximum number of test failures.

 <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/condition%20to%20stop%20-%202.png" alt="command builder" width=70%>

 >**Notes**:
 >
 > The maximum test cases failure must be greater than 0 and a natural number (1,2,3...). Otherwise, Katalon Studio will not start the execution.

 3. After you're done with the configuration, click **Generate command**. A command contains the `maxFailedTests` option is generated.
 
 Copy the generated command to use in Console mode.

 <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/generate%20command%201.png" width=70%>

You can also run execution with the property file. To save the property file in the **Execution Configurations** dialog, click **Generate property file > Save**.

### With Command-line option

Use the command-line option: ``-maxFailedTests=T``, where T is the maximum number of test failures.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/Command-line-2.png" width=100%>

See [Katalonc command-line option](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#automatically-updating-webdriver-option) for the list of common command-line options supported.

## Reporting Incomplete Test Suite

When a test suite has at least 01 test case **Not Run**, the final status of that test suite is marked **Incomplete**.

Katalon Studio sends **Incomplete** or **Not started yet** test suite and the attachments of the test suite execution, including execution log and JUnit Report to TestOps.

However, **Incomplete** or **Not started yet** test suite and the attachments of the test suite execution are not uploaded to 3rd-party tools (qTest, JIRA, Slack, Azure DevOps Test Plans, TestRail).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/TestOps%20report%202.png" alt="TestOps report" width="100%">

## Troubleshoot testing

When a test suite or test suite collection is terminated, in the execution log, Katalon Studio prints out information about the test suite or test suite collection reference ID and the maximum number of test failures allowed.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/Execution%20log.png" alt="execution log" width=100%>

This applies to either sequential or parallel mode execution. You can check which and why the test execution is terminated. See also [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html).

You can also see the report in Katalon Studio IDE.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/reports%20in%20IDE.png" alt="report in IDE" width="100%">

## Common Use Cases

Below are three example use cases to illustrate how the parameter works:

- In the case of a test suite execution.
- In the case of a test suite collection executed in sequential mode.
- In the case of a test suite collection executed in parallel mode.

### Terminate Test Suite Execution

In this section, we outline an example execution of a test suite with this parameter. This example works for all test types, such as **Retry all**, **Retry immediately**, and **Data-driven testing**.

Given that you have a test suite that has 6 test cases.

You want to stop the test suite after 4 test failures and the maximum number of failures set to 4.

The test suite is terminated once the number of failures becomes 4. The execution ends, and the rest test cases do not run.

Katalon Studio generates a report in JUnit, HTML, PDF, and CSV format. The report does not show information for test cases that were not run. See also [Test Suite and Test Suite Collection Reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html#test-suite-report).

### Terminate Test Suite Collection Executed In Sequential Mode

Given that you have 5 test suites, each test suite has 10 test cases. You want to stop the test suite collection after 20 test failures and the maximum number of failures set to 20.

The test suite collection executes in sequential mode and is terminated once the number of failures becomes 20. The rest test cases in the terminated test suite and the rest test suite do not run.

Katalon Studio generates a report in JUnit, HTML, PDF, and CSV format. The report does not show information for test cases and test suites that were not run.

> Learn more about how to create and execute a test suite collection in [Test Suite Collection](https://docs.katalon.com/katalon-studio/docs/test-suite-collection.html#manage-execution-information)

### Terminate Test Suite Collection Executed In Parallel Mode

Given that you have a test suite collection that has 10 test suites with 3 parallel instances. You want to stop the test suite collection after 100 test failures and the maximum number of failures set to 100.

>**Notes**:
>
>- Instances is the number of test suites you set to run at the same time.
>
>- T is the maximum number of test case failures (threshold).

When the test suite begins execution, the first 3 test suites run at the same time with T = 100 in each test suite.

The test suite collection is terminated once the total number of failures becomes 100. The rest test cases in the terminated test suite and the rest test suite do not run. However, the currently running test suites will not be terminated.

Katalon Studio generates a report in JUnit, HTML, PDF, and CSV format. The report does not show information for test cases and test suites that were not run.