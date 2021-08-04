---
title: "Terminate Execution Conditionally"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/terminate-execution-conditionally.html
description: "This article provides the concept of terminating execution conditionally and the tutorial on common use cases."
---
From version 8.1.0 onwards, you can set a maximum number of test failures before your test execution automatically ends. You can set this condition via the command-line option. The ability to terminate an execution helps you save time and provide early feedback instead of waiting for the testing process to finish.

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

- You have a high number of failed test cases in a given test execution.
- You have a mature set of tests, and it takes hours to finish execution.
- You have a new code committed or a new build available, where a high number of test failures might reflect the quality of the new build.

In this article, you will learn how to configure a maximum number of test failures, with examples using common use cases.

You can use this feature to:

- Terminate a test suite.
 	- Terminate a test suite with configured retry after executing all.
	- Terminate a test suite with configured retry failed executions immediately.
	- Terminate a test suite with Data-driven testing.
	- Terminate a test suite with Data-driven testing and configured retry after executing all.
	- Terminate a test suite with Data-driven testing with configured retry failed executions immediately.
- Terminate a test suite collection executed in sequential mode.
- Terminate a test suite collection executed in parallel mode.

## Set a maximum number of test failures

>**Requirements**
>
>- A test suite or test suite collection. See [Create a test suite](https://docs.katalon.com/katalium-framework/docs/katalium-framework-create-test-suite.html).
>- Katalon Studio **version 8.1.0 onwards**.
>- A Katalon Studio Enterprise and Katalon Runtime Engine License. See [Katalon licensing](https://docs.katalon.com/katalon-studio/docs/license.html).

### With Command Builder

 To set a maximum number of test failures before terminating execution, go to Katalon Studio. In the toolbar, select **Build CMD** (Build Command).

 <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/build%20cmd.png" alt="build cmd" width=40%>

 In the **Generate Command for Console Mode > Execution Configurations**, check the box **Terminate the execution once the total number of test failures reaches this threshold**. In the text field, input your desired maximum number of test failures.

 <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/condition%20to%20stop%20-%202.png" alt="command builder" width=70%>

 >**Notes**:
 >
 > The number of maximum test cases failure must be greater than 0 and a natural number (1,2,3...). Otherwise, Katalon Studio will not start the execution.

 After you're done with the configuration, click **Generate command**. Copy the generated command to use in Console mode.

 <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/generate%20command%200.png" alt="generate command" width=70%>

You can also run execution with the property file. To save the property file in the **Execution Configurations** dialog, click **Generate property file > Save**.

 >**Notes**: For detailed instruction on how to run a test execution in Console mode, see [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).

### With Command-line option

Use the command-line option: ``-maxFailedTests=T``, where T is the maximum number of test failures.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/command-line.png" alt="command line" width=100%>

See [Katalonc command-line option](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#automatically-updating-webdriver-option) for the list of common command-line options supported.

## 3rd-Party Integrations

The final status of a terminated test suite is marked **Incomplete**. When a test suite has at least 1 test case not run, the status of this test suite is **Incomplete**.

**Incomplete** and **Not started yet** test suite and its test cases' results are not uploaded to 3rd-party tools (qTest, JIRA, Slack, Azure DevOps Test Plans, TestRail) except for TestOps, since TestOps parses the execution log.

Katalon Studio sends **Incomplete** test suite execution’s attachments, including execution log and JUnit Report to TestOps. This action ends the incomplete execution on TestOps.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/TestOps%20report.png" alt="TestOps report" width="100%">

## Common Use Cases

We outline below three example use cases using this parameter:

1. Terminate test suite execution.
2. Terminate test suite collection executed in sequential mode.
3. Terminate test suite collection executed in parallel mode.

### Terminate Test Suite Execution

Given that you have a test suite that has 6 test cases. You set the ``maxFailedTests=4``. (T = 4).

>**Notes**:
>
> - T is the number of maximum failure test cases (threshold).
> - x is the number of test case failures in the test suite.

When you click **Execute**, the test suite runs with T = 4.

- If test case 1 passed, the number of the test case failures in this test suite is 0 (x = 0).
- If test case 2 failed, then x = 1.
- If test case 3 failed, then x = 2.
- If test case 4 failed, then x = 3.
- If test case 5 failed, then x = 4. Since x = 4 = T, the test suite is terminated, and test case 6 does not trigger to run.

Below is the final status of each test case in the test suite.

<table data-number-column="false"><colgroup><col /><col /><col /><col /></colgroup>
<tbody>
 <tr>
  <th colspan="1" rowspan="1" data-colwidth="226">
   <p data-renderer-start-pos="11924"><strong data-renderer-mark="true">Test Suite</strong></p>
   <figure></figure>
  </th>
  <th colspan="1" rowspan="1" data-colwidth="201">
   <div data-="">
    <p data-renderer-start-pos="11938"><strong data-renderer-mark="true">Run Status</strong></p>
   </div>
   <figure></figure>
  </th>
  <th colspan="1" rowspan="1" data-colwidth="124">
   <div data-="">
    <p data-renderer-start-pos="11952"><strong data-renderer-mark="true">Final </strong></p>
   </div>
   <figure></figure>
  </th>
  <th colspan="1" rowspan="1" data-colwidth="208">
   <div data-="">
    <p data-renderer-start-pos="11962"><strong data-renderer-mark="true">Condition to Terminate </strong></p>
   </div>
   <div data-="">
    <p data-renderer-start-pos="22063"> T = 4</strong></p>
   </div>
   <figure></figure>
  </th>
 </tr>
 <tr>
  <td colspan="1" rowspan="1" data-colwidth="226">
   <p data-renderer-start-pos="11985">Test Case 1</p>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="201">
   <div data-="">
    <p data-renderer-start-pos="12001">Passed</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="124">
   <div data-="">
    <p data-renderer-start-pos="12011"><span data-emoji-id="2714" data-emoji-short-name=":heavy_check_mark:" data-emoji-text="✔">&radic;</span></p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="208">
   <div data-="">
    <p data-renderer-start-pos="12017">x = 0</p>
   </div>
  </td>
 </tr>
 <tr>
  <td colspan="1" rowspan="1" data-colwidth="226">
   <p data-renderer-start-pos="12026">Test Case 2</p>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="201">
   <div data-="">
    <p data-renderer-start-pos="12041">Failed</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="124">
   <div data-="">
    <div data-="">
     <p data-renderer-start-pos="12052">&radic;</p>
    </div>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="208">
   <div data-="">
    <p data-renderer-start-pos="12057">x = 1</p>
   </div>
  </td>
 </tr>
 <tr>
  <td colspan="1" rowspan="1" data-colwidth="226">
   <p data-renderer-start-pos="12066">Test Case 3</p>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="201">
   <div data-="">
    <p data-renderer-start-pos="12081">Failed</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="124">
   <div data-="">&radic;</div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="208">
   <div data-="">
    <p data-renderer-start-pos="12097">x = 2</p>
   </div>
  </td>
 </tr>
 <tr>
  <td colspan="1" rowspan="1" data-colwidth="226">
   <p data-renderer-start-pos="12106">Test Case 4</p>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="201">
   <div data-="">
    <p data-renderer-start-pos="12121">Failed</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="124">
   <div data-="">&radic;&nbsp;</div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="208">
   <div data-="">
    <p data-renderer-start-pos="12136">x = 3</p>
   </div>
  </td>
 </tr>
 <tr>
  <td colspan="1" rowspan="1" data-colwidth="226">
   <p data-renderer-start-pos="12145">Test Case 5</p>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="201">
   <div data-="">
    <p data-renderer-start-pos="12160">Failed</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="124">
   <div data-="">&radic;</div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="208">
   <div data-="">
    <p data-renderer-start-pos="12175">x = 4 = T</p>
   </div>
  </td>
 </tr>
 <tr>
  <td colspan="1" rowspan="1" data-colwidth="226">
   <p data-renderer-start-pos="12186">Test Case 6</p>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="201">
   <div data-="">
    <p data-renderer-start-pos="12201"><strong data-renderer-mark="true">Not Run</strong></p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="124">&nbsp;</td>
  <td colspan="1" rowspan="1" data-colwidth="208">
   <div data-="">
    <p data-renderer-start-pos="12216">Stop</p>
   </div>
  </td>
 </tr>
</tbody>
</table>

>**Notes**:
>
>In the **Execution log**, the report shows information of the executed test cases only, which is 5 test cases in this example. Katalon Studio auto-generates the report of 5 executed test case results in JUnit, HTML, PDF, and CSV format. See also [Test Suite and Test Suite Collection Reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html#test-suite-report).

You can also apply the terminate execution conditionally with **Retry all**, **Retry immediately**, and **Data-driven testing**. These cases follow the same logic with this example, following the definition of a test failure mentioned.

### Terminate Test Suite Collection Executed In Sequential Mode

Given that you have 5 test suites, each test suite has 10 test cases. You set the ``maxFailedTests=20`` (T = 20).

 >**Notes**:
 >
 >- T is the threshold of the first test suite.
 >
 >- x is the total number of test failures counted in those previous test suites that finish running.
 >
 >- T - x (x < T) is the new threshold of the next test suite.

When you click **Execute**, test suite 1 runs with T = 20.

- If test suite 1 finishes running and has 4 test failures (x = 4), the new threshold of the next test suite is 16 (T - x = 16). Therefore, test suite 2 is triggered to run with T = 16.
- If test suite 2 finishes running and has 3 test failures (x = 4 + 3), the new threshold of the next test suite is 13 (T - x = 13). Therefore, test suite 3 is triggered to run with T = 13.
- If test suite 3 finishes running and has 5 test failures (x = 4 + 3 + 5), the new threshold of the next test suite is 8 (T - x = 8). Therefore, test suite 4 is triggered to run with T = 8.
- If test suite 4 finishes running with 8 test failures and stops, the total number of test failures counted in test suites 1, 2, 3, and 4 is 20 (x = 4 + 3 + 5 + 8). Since x = T = 20, the test suite collection stops triggering test suite 5.

Below is the final status of each test suite in the test suite collection.

<table data-number-column="false"><colgroup><col /><col /><col /><col /></colgroup>
<tbody>
 <tr>
  <th colspan="1" rowspan="1" data-colwidth="286">
   <p data-renderer-start-pos="21994"><strong data-renderer-mark="true">Test Suite Collection</strong></p>
   <figure></figure>
  </th>
  <th colspan="1" rowspan="1" data-colwidth="168">
   <div data-="">
    <p data-renderer-start-pos="22019"><strong data-renderer-mark="true">Total Failed/Total Test Case</strong></p>
   </div>
   <figure></figure>
  </th>
  <th colspan="1" rowspan="1" data-colwidth="166">
   <div data-="">
    <p data-renderer-start-pos="22044"><strong data-renderer-mark="true">Condition to Terminate</strong></p>
   </div>
   <div data-="">
    <p data-renderer-start-pos="22063">T = 20</p>
   </div>
   <figure></figure>
  </th>
  <th colspan="1" rowspan="1" data-colwidth="140">
   <p data-renderer-start-pos="22071"><strong data-renderer-mark="true">3rd-Party Integration</strong></p>
   <figure></figure>
  </th>
 </tr>
 <tr>
  <td colspan="1" rowspan="1" data-colwidth="286">
   <p data-renderer-start-pos="22098">Test Suite Collection - Test Suite 1</p>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="168">
   <div data-="">
    <p data-renderer-start-pos="22138">4/10</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="166">
   <div data-="">
    <p data-renderer-start-pos="22147">x = 4</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="140">
   <p data-renderer-start-pos="22154">Applies</p>
  </td>
 </tr>
 <tr>
  <td colspan="1" rowspan="1" data-colwidth="286">
   <p data-renderer-start-pos="22167">Test Suite Collection - Test Suite 2</p>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="168">
   <div data-="">
    <p data-renderer-start-pos="22207">3/10</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="166">
   <div data-="">
    <p data-renderer-start-pos="22215">x = 7</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="140">
   <p data-renderer-start-pos="22222">Applies</p>
  </td>
 </tr>
 <tr>
  <td colspan="1" rowspan="1" data-colwidth="286">
   <p data-renderer-start-pos="22235">Test Suite Collection - Test Suite 3</p>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="168">
   <div data-="">
    <p data-renderer-start-pos="22275">5/10</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="166">
   <div data-="">
    <p data-renderer-start-pos="22283">x = 12</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="140">
   <p data-renderer-start-pos="22291">Applies</p>
  </td>
 </tr>
 <tr>
  <td colspan="1" rowspan="1" data-colwidth="286">
   <p data-renderer-start-pos="22304">Test Suite Collection - Test Suite 4</p>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="168">
   <div data-="">
    <p data-renderer-start-pos="22344">8/10</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="166">
   <div data-="">
    <p data-renderer-start-pos="22352">x = 20 = T</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="140">
   <p data-renderer-start-pos="22360">Applies</p>
  </td>
 </tr>
 <tr>
  <td colspan="1" rowspan="1" data-colwidth="286">
   <p data-renderer-start-pos="22373">Test Suite Collection - Test Suite 5</p>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="168">
   <div data-="">
    <p data-renderer-start-pos="22413"><strong data-renderer-mark="true">Not Started Yet</strong></p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="166">
   <div data-="">
    <p data-renderer-start-pos="22432">Stop</p>
   </div>
  </td>
  <td colspan="1" rowspan="1" data-colwidth="140">
   <p data-renderer-start-pos="22440">N/A</p>
  </td>
 </tr>
</tbody>
</table>

Katalon Studio auto-generates JUnit reports with all executed test cases in test suites 1, 2, 3, and 4.

> Learn more about how to create and execute a test suite collection in [Test Suite Collection](https://docs.katalon.com/katalon-studio/docs/test-suite-collection.html#manage-execution-information)

### Terminate Test Suite Collection Executed In Parallel Mode

Given that you have a test suite collection that has 10 test suites with 3 parallel instances. You set the ``maxFailedTests=100`` (T = 100).

>**Notes**:
>
>- Instances is the number of test suites you set to run at the same time.
>
>- T is the threshold of those test suites in the first execution batch.
>
>- x  is the total number of test failures counted in test suites having finished running.
>
>- T - x (x < T) is the new threshold of the next test suite.

When you click **Execute**, the first 3 test suites run at the same time with T = 100 in each test suite. 

- If test suite 1 finishes running and has 50 failures, the new threshold of the next test suite is 50 (T - x = 50). Therefore, test suite 4 is triggered to run with T = 50.
- If test suite 2 finishes running and has 40 failures, the new threshold of the next test suite is 10 (T - x = 10). Therefore, test suite 5 is triggered to run with T = 10.
- If test suite 3 has 100 failures and stops, the total number of test failures counted in test suites 1, 2, and 3 is 190 (x = 50 + 40 + 100). Since x > T, the test suite collection stops triggering test suites 6, 7, 8, 9, and 10. The currently running test suites 4 and 5 will not be terminated.

Below is the final status of each test suite in the test suite collection.

<table>
	<tbody>
		<tr>
			<th colspan="1" rowspan="1">
				<p><strong>Test Suite Collection</strong></p>
			</th>
			<th colspan="1" rowspan="1">
				<p><strong>Threshold</strong>&nbsp;</p>
			</th>
			<th colspan="1" rowspan="1">
				<div>
					<p><strong>Total Failed/Total Test Case</strong></p>
				</div>
			</th>
			<th colspan="1" rowspan="1">
				<div>
					<p><strong>Condition to Terminate</strong></p>
				</div>
				<div>
					<p>T = 100&nbsp;</p>
				</div>
			</th>
			<th colspan="1" rowspan="1">
				<p><strong>Execution log and Report</strong>&nbsp;</p>
			</th>
			<th>
				<p><strong>3rd-Party Integration</strong></p>
			</th>
		</tr>
		<tr>
			<td colspan="1" rowspan="1">
				<p>Test Suite 1</p>
			</td>
			<td colspan="1" rowspan="1">
				<p>T = 100</p>
			</td>
			<td colspan="1" rowspan="1">
				<div>
					<p>50</p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<div>
					<p>x1 = 50</p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<p>Same as a normal test suite</p>
			</td>
			<td>&nbsp;Applies</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="1">
				<p>Test Suite 2</p>
			</td>
			<td colspan="1" rowspan="1">
				<p>T = 100</p>
			</td>
			<td colspan="1" rowspan="1">
				<div>
					<p>40</p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<div>
					<p>x2 = x1 + 40 = 90</p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<p>Same as a normal test suite</p>
			</td>
			<td>&nbsp;Applies</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="1">
				<p>Test Suite 3</p>
			</td>
			<td colspan="1" rowspan="1">
				<p>T = 100</p>
			</td>
			<td colspan="1" rowspan="1">
				<div>
					<p>100</p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<div>
					<p><strong>x3 = 90 + 100 &gt; T</strong></p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<p>Same as a normal test suite</p>
			</td>
			<td>&nbsp;Applies</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="1">
				<p>Test Suite 4</p>
			</td>
			<td colspan="1" rowspan="1">
				<p>T - x1 = 50</p>
			</td>
			<td colspan="1" rowspan="1">
				<div>
					<p>5</p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<p>Same as a normal test suite</p>
			</td>
			<td colspan="1" rowspan="1">
				<p>Applies</p>
			</td>
			<td>&nbsp;N/A</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="1">
				<p>Test Suite 5</p>
			</td>
			<td colspan="1" rowspan="1">
				<p>T - x2 = 10</p>
			</td>
			<td colspan="1" rowspan="1">
				<div>
					<p>2</p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<p>Same as a normal test suite</p>
			</td>
			<td colspan="1" rowspan="1">
				<p>Applies</p>
			</td>
			<td>&nbsp;N/A</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="1">
				<p>Test Suite 6</p>
			</td>
			<td colspan="1" rowspan="1">N/A</td>
			<td colspan="1" rowspan="1">
				<div>
					<p><strong>Not Started Yet</strong></p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<p>N/A</p>
			</td>
			<td colspan="1" rowspan="1">N/A</td>
			<td>&nbsp;N/A</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="1">
				<p>Test Suite 7</p>
			</td>
			<td colspan="1" rowspan="1">N/A</td>
			<td colspan="1" rowspan="1">
				<div>
					<p><strong>Not Started Yet</strong></p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<p>N/A</p>
			</td>
			<td colspan="1" rowspan="1">N/A&nbsp;</td>
			<td>&nbsp;N/A</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="1">
				<p>Test Suite 8</p>
			</td>
			<td colspan="1" rowspan="1">N/A&nbsp;</td>
			<td colspan="1" rowspan="1">
				<div>
					<p><strong>Not Started Yet</strong></p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<p>N/A</p>
			</td>
			<td colspan="1" rowspan="1">N/A</td>
			<td>&nbsp;N/A</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="1">
				<p>Test Suite 9</p>
			</td>
			<td colspan="1" rowspan="1">N/A</td>
			<td colspan="1" rowspan="1">
				<div>
					<p><strong>Not Started Yet</strong></p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<p>N/A</p>
			</td>
			<td colspan="1" rowspan="1">N/A</td>
			<td>&nbsp;N/A&nbsp;</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="1">
				<p>Test Suite 10</p>
			</td>
			<td colspan="1" rowspan="1">N/A</td>
			<td colspan="1" rowspan="1">
				<div>
					<p><strong>Not Started Yet</strong></p>
				</div>
			</td>
			<td colspan="1" rowspan="1">
				<p>N/A</p>
			</td>
			<td colspan="1" rowspan="1">N/A</td>
			<td>&nbsp;N/A</td>
		</tr>
	</tbody>
</table>

Katalon Studio auto-generates JUnit reports with all test cases in test suites 1, 2, 3, 4, and 5.

## Troubleshoot testing

When a test suite or test suite collection is terminated, in the execution log, Katalon Studio prints out information about the test suite or test suite collection reference ID and the maximum number of test failures allowed.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/condition-to-stop/execution%20log.png" alt="execution log" width=100%>

This applies to either sequential or parallel mode execution. You can check which and why the test execution is terminated. See also [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html).
