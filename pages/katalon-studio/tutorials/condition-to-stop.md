---
title: "Terminate Execution Conditionally"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/terminate-execution-conditionally.html
description: "This article provides the concept of terminating execution conditionally and the tutorial on common use cases."
---
In this article, you will learn how to terminate a test execution automatically by configuring a maximum number of test failures in manual view or via the command-line option, with examples using common use cases.

>**Requirements**
>
>- Katalon Studio **version 8.1.0 onwards**
>- Katalon Runtime Engine **version 8.1.0 onwards**
>- A Katalon Runtime Engine License. See [Katalon licensing](https://docs.katalon.com/katalon-studio/docs/license.html).

Consider using the condition to terminate execution when a set of tests is mature and takes hours to finish. Once a significant number of tests fail, they may fail for the same cause. This feature helps you save time, provide early feedback, and avoid the execution of unnecessary test cases.

## Set a maximum number of test failures

>**What is a test failure?**
>
>A test failure is a failed test case or test iteration in an execution.
>
>- 1 test case fails = 1 test failure
>- 1 retried test case fails = 1 test failure
>- 1 test iteration (test case + data row) fails = 1 test failure
>- 1 retried test iteration fails = 1 test failure

### With Command Builder

>**Notes**:
>
>For detailed instruction on how to run a test execution in Console mode, see [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).

 Go to Katalon Studio and set a maximum number of test failures.
 
 1. In the toolbar, select **Build CMD** (Build Command).

 2. In the **Generate Command for Console Mode > Execution Configurations**, check the box **Terminate the execution once the total number of test failures reaches this threshold**. In the text field, input your desired maximum number of test failures.

 	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/condition%20to%20stop%20-%202.png" alt="command builder" width=80%>

	>**Notes**:
	>
	> The maximum test cases failure must be greater than 0 and a natural number (1, 2, 3...). Otherwise, Katalon Studio will not start the execution.

 3. After you are done with the configuration, click **Generate command**. A command containing the `-maxFailedTests` option is generated.
 
	Copy the generated command to use in Console mode.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/generate%20command%201.png" width=70%>

	You can also execute the test with the property file. To save the property file in the **Execution Configurations** dialog, click **Generate property file > Save**.

### With Command-line option

Use the command-line option: ``-maxFailedTests=T``, where T is the maximum number of test failures.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/Command-line-2.png" width=100%>

See [Katalonc command-line option](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#automatically-updating-webdriver-option) for the list of common command-line options supported.

## Report Incomplete Test Suite

When a test suite has at least 1 test case **Not Run**, the final status of that test suite is marked **Incomplete**.

For test suites marked **Incomplete** or **Not started yet**, Katalon Studio automatically sends attachments to TestOps after execution ends. The reports include the execution logs and JUnit Reports.

Test suites marked **Incomplete** or **Not started yet** and the attachments of the test suite execution cannot be uploaded to 3rd-party tools (qTest, JIRA, Slack, Azure DevOps Test Plans, TestRail).

## Troubleshoot

When a test suite or test suite collection is terminated, you can find the test suite or test suite collection reference ID and the maximum number of test failures in the execution log.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/Execution%20log.png" alt="execution log" width=100%>

This applies to either sequential or parallel mode execution. You can check which test execution was terminated and why. You can also see the report in the manual view of Katalon Studio. See also [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html).

## Common Use Cases

Below are three example use cases to illustrate how the parameter works:

- In the case of a test suite execution.
- In the case of a test suite collection executed in sequential mode.
- In the case of a test suite collection executed in parallel mode.

### Terminate Test Suite Execution

In this section, we outline an example execution of a test suite with this parameter.

- Given that you have a test suite that has 10 test cases.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/Test%20suite%20UC%201.png" alt="Test Suites" width="80%">

- You want to stop the test suite after 4 test failures. Set T = 4.

	**Configure in Command Builder**

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/terminate.png" alt="command builder" width="80%">

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/command%20UC%201.png" alt="execution log" width="70%">

	**Execute in Console Mode**

- The test suite is terminated once the number of failures becomes 4. The execution ends, and the rest test cases do not run.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/Test%20log%20result%20-%20UC%201.png" width="90%" alt="info">

- Katalon Studio generates a report in JUnit, HTML, PDF, and CSV format. The report does not show information for test cases that were not run.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/Test%20Result%20in%20KS%20-%20UC%201.png" width="80%" alt="report in Katalon Studio">

	>See also [Test Suite and Test Suite Collection Reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html#test-suite-report).

### Terminate Test Suite Collection Executed In Sequential Mode

- Given that you have 5 test suites, each test suite has 10 test cases. You want to stop the test suite collection after 20 test failures. Set T = 20.

- The test suite collection executes in sequential mode and is terminated once the number of failures becomes 20. The rest test cases in the terminated test suite and the rest test suite do not run.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/Report%20TSC%20UC2.png" alt="report test suite collection" width=100%>

- Katalon Studio generates a report in JUnit, HTML, PDF, and CSV format. The report does not show information for test cases and test suites that were not run.

	> Learn more about how to create and execute a [Test Suite Collection](https://docs.katalon.com/katalon-studio/docs/test-suite-collection.html#manage-execution-information).

### Terminate Test Suite Collection Executed In Parallel Mode

- Given that you have a test suite collection that has 5 test suites with 3 parallel instances. You want to stop the test suite collection after 20 test failures. Set T = 20.

	>**Notes**:
	>
	>- Instances is the number of test suites you set to run at the same time.
	>
	>- T is the maximum number of test case failures (threshold).

- When the test suite begins execution, the first 3 test suites run at the same time with T = 20 in each test suite.

- The test suite collection is terminated once the total number of failures becomes 20. The rest test cases in the terminated test suite and the rest test suite do not run. However, the currently running test suites will not be terminated.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/Report%20UC%203.png" alt="report test suite collection in parallel mode" width="100%">

- Katalon Studio generates a report in JUnit, HTML, PDF, and CSV format. The report does not show information for test cases and test suites that were not run.