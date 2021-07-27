---
title: "Terminate Execution Additionally"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/condition-to-stop.html
description: "This article provides the concept of terminating execution additionally and the tutorial on common use cases."
---
Available from **version 8.1.0 onwards**, you can terminate test suite and test suite collection execution additionally based on the number of test failures. This article provides the concept of terminate execution additionally and the tutorial on common use cases.

## Terminate execution additionally
You can terminate a test suite and test suite collection execution additionally via the command line to save time spent waiting for the execution to finish. The addition to terminate execution is based on the maximum number of test failures allowed during runtime.

Terminate execution additionally is useful when a set of tests is mature, and it takes hours to finish execution. A significant number of test failures in execution can reflect the tested build’s quality. By terminating the execution, you can have earlier feedback instead of waiting for the execution to finish.

Defining a threshold that sets the maximum number of test failures in an execution helps you save time and enhance testing efficiency, especially on new code committed or a new build available. A reasonable threshold is subject to the acceptance level of each software team.

## Common ways to terminate execution additionally

### Prerequisites
- A test suite/test suite collection and a defined number of maximum failure test cases. See [Create a test suite](https://docs.katalon.com/katalium-framework/docs/katalium-framework-create-test-suite.html).
- Katalon Studio **version 8.1.0 onwards**. Install the [latest Katalon Studio version](https://www.katalon.com/download/).
- Katalon Studio Enterprise and Katalon Runtime Engine License. See [Katalon licensing](https://docs.katalon.com/katalon-studio/docs/license.html).

### Definition of a test failure
A test failure is a failed test case or test data execution in a test suite.
- 1 test case fails = 1 test failure
- 1 retried test case fails = 1 test failure
- 1 test iteration (test case + data row) fails = 1 test failure
- 1 retried test iteration fails = 1 test failure

> **Note**:
>
> The number of maximum failure test cases must be a positive integer. Input invalid argument in command-line option or command builder, Katalon Studio cannot start the execution.

### In Command Builder
To enable terminate execution additionally, in Katalon Studio, go to **Build CMD** on the toolbar.

In the **Generate Command for Console Mode** dialog, see the **Execution Configurations** section. Select the checkbox: **Terminate the execution once the total number of test failures reaches this threshold** and fill in the text field with the maximum test failures number.

After you're done with the setting, you can **Generate command** or **Generate property file to run with Console mode. See [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder) for detailed instruction on how to run a test execution in Console mode.

### Commond-line option
You can use the command-line option for setting addition to terminate test suite/ test suite collection execution. Given T as the maximum number of test failures allowed. Setting the maximum number of test failures allowed in the execution by using this command-line option: **-maxFailedTests= T**.

See [Katalonc Command-line option](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#automatically-updating-webdriver-option) for the list of command-line options supported.

## Comman Use Case
You can apply the terminate execute additionally in many different situations. Below are the three most common use cases:
### Use Case 1: Test suite execution
Given that you have a test suite that has 6 test cases. You set the maxFailedTests = 4.
For example, the test suite has the result describes in the table below:

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
				<p data-renderer-start-pos="11962"><strong data-renderer-mark="true">Condition to Stop</strong></p>
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
				<p data-renderer-start-pos="12017">x=0</p>
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
				<p data-renderer-start-pos="12057">x=1</p>
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
				<p data-renderer-start-pos="12097">x=2</p>
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
				<p data-renderer-start-pos="12136">x=3</p>
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
				<p data-renderer-start-pos="12175">x=4=T</p>
			</div>
		</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="226">
			<p data-renderer-start-pos="12186">Test Case 6</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="201">
			<div data-="">
				<p data-renderer-start-pos="12201">Not Run</p>
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

When the test suite reaches 4 test failures, the execution stops immediately. In the **Execution log**, the report shows full information of the test cases executed only, which is 5 test cases in this example. Katalon Studio auto-generates the report of the executed test case (in this example: 5 test cases result) to JUnit, HTML, PDF, and CSV.

You can also apply the terminate execution additionally together with **Retry all**, **Retry immediately**, and **Data-driven testing**. These cases follow the same algorithm with this example, following the definition of a test failure mentioned.
### Use Case 2: Test suite collection in Sequential Mode
Given that you have 5 test suites, each test suite has 10 test cases. You set the maxFailedTests = 20. For example, the test suite has the result describes in the table below:
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
				<p data-renderer-start-pos="22044"><strong data-renderer-mark="true">Condition to Stop</strong></p>
			</div>
			<div data-="">
				<p data-renderer-start-pos="22063">T=20</p>
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
				<p data-renderer-start-pos="22147">x=4</p>
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
				<p data-renderer-start-pos="22215">x=7</p>
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
				<p data-renderer-start-pos="22283">x=12</p>
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
				<p data-renderer-start-pos="22352">x=20</p>
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

Katalon Studio auto-generates JUnit report with all test cases in test suite 1,2,3,4.

> Learn more about how to create and execute a test suite collection in [Test Suite Collection](https://docs.katalon.com/katalon-studio/docs/test-suite-collection.html#manage-execution-information)

### Use Case 3: Test suite collection in Parallel Mode
Given that you have a test suite collection that has 10 test suites, Instances = 3. You set the maxFailedTests = 100.

The flow of this example is explained as below:

1. Click **Execute**
2. 3 test suites run at the same time with maxFailedTests=100 in each test suite. 
3. Test suite 1 finishes running and has 50 failures => T-x=50.
4. Test suite 4 is triggered to run with maxFailedTests=50.
5. Test suite 2 finishes running and has 40 failures => T-x=10
6. Test suite 5 is triggered to run with maxFailedTests=10.
7. Test suite 3 has 100 failures and stops. => x=50+40+100.
8. x>T, Test suite collection stops triggering test suite 6,7,8,9,10.
9. Currently running test suite 4,5 will not be terminated due to the condition in step 7.

For example, the test suite has the result describes in the table below:

<table data-number-column="false"><colgroup><col /><col /><col /><col /><col /><col /></colgroup>
<tbody>
	<tr>
		<th colspan="1" rowspan="1" data-colwidth="126">
			<p data-renderer-start-pos="23230"><strong data-renderer-mark="true">Test Suite Collection</strong></p>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="120">
			<p data-renderer-start-pos="23255"><strong data-renderer-mark="true">Threshold</strong>&nbsp;</p>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="160">
			<div data-="">
				<p data-renderer-start-pos="23270"><strong data-renderer-mark="true">Total Failed/Total Test Case</strong></p>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="150">
			<div data-="">
				<p data-renderer-start-pos="23295"><strong data-renderer-mark="true">Condition to Stop</strong></p>
			</div>
			<div data-="">
				<p data-renderer-start-pos="23314">T=100&nbsp;</p>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="112">
			<p data-renderer-start-pos="23323"><strong data-renderer-mark="true">Execution log and Report</strong>&nbsp;</p>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="92">
			<p data-renderer-start-pos="23351"><strong data-renderer-mark="true">3rd-Party Integration</strong></p>
		</th>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="126">
			<p data-renderer-start-pos="23378">Test Suite 1</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="120">
			<p data-renderer-start-pos="23394">T=100</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="160">
			<div data-="">
				<p data-renderer-start-pos="23403">50</p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="150">
			<div data-="">
				<p data-renderer-start-pos="23410">x1=50</p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="112">
			<p data-renderer-start-pos="23419">Same as a normal test suite</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="92">
			<p data-renderer-start-pos="23440">Applies</p>
		</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="126">
			<p data-renderer-start-pos="23453">Test Suite 2</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="120">
			<p data-renderer-start-pos="23469">T=100</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="160">
			<div data-="">
				<p data-renderer-start-pos="23478">40</p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="150">
			<div data-="">
				<p data-renderer-start-pos="23484">x2=x1+40=90</p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="112">
			<p data-renderer-start-pos="23499">Same as a normal test suite</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="92">
			<p data-renderer-start-pos="23520">Applies</p>
		</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="126">
			<p data-renderer-start-pos="23533">Test Suite 3</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="120">
			<p data-renderer-start-pos="23549">T=100</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="160">
			<div data-="">
				<p data-renderer-start-pos="23558">100</p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="150">
			<div data-="">
				<p data-renderer-start-pos="23565"><strong data-renderer-mark="true">x3=90+100 &gt; T</strong></p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="112">
			<p data-renderer-start-pos="23582">Same as a normal test suite</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="92">
			<p data-renderer-start-pos="23603">Applies</p>
		</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="126">
			<p data-renderer-start-pos="23616">Test Suite 4</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="120">
			<p data-renderer-start-pos="23632">T-x1=50</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="160">
			<div data-="">
				<p data-renderer-start-pos="23643">5</p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="150">&nbsp;</td>
		<td colspan="1" rowspan="1" data-colwidth="112">
			<p data-renderer-start-pos="23652">Same as a normal test suite</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="92">
			<p data-renderer-start-pos="23673">Applies</p>
		</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="126">
			<p data-renderer-start-pos="23686">Test Suite 5</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="120">
			<p data-renderer-start-pos="23702">T-x2=10</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="160">
			<div data-="">
				<p data-renderer-start-pos="23713">2</p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="150">&nbsp;</td>
		<td colspan="1" rowspan="1" data-colwidth="112">
			<p data-renderer-start-pos="23722">Same as a normal test suite</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="92">
			<p data-renderer-start-pos="23743">Applies</p>
		</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="126">
			<p data-renderer-start-pos="23756">Test Suite 6</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="120">&nbsp;</td>
		<td colspan="1" rowspan="1" data-colwidth="160">
			<div data-="">
				<p data-renderer-start-pos="23776"><strong data-renderer-mark="true">Not Started Yet</strong></p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="150">&nbsp;</td>
		<td colspan="1" rowspan="1" data-colwidth="112">
			<p data-renderer-start-pos="23799">N/A</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="92">&nbsp;</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="126">
			<p data-renderer-start-pos="23812">Test Suite 7</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="120">&nbsp;</td>
		<td colspan="1" rowspan="1" data-colwidth="160">
			<div data-="">
				<p data-renderer-start-pos="23832"><strong data-renderer-mark="true">Not Started Yet</strong></p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="150">&nbsp;</td>
		<td colspan="1" rowspan="1" data-colwidth="112">
			<p data-renderer-start-pos="23855">N/A</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="92">&nbsp;</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="126">
			<p data-renderer-start-pos="23868">Test Suite 8</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="120">&nbsp;</td>
		<td colspan="1" rowspan="1" data-colwidth="160">
			<div data-="">
				<p data-renderer-start-pos="23888"><strong data-renderer-mark="true">Not Started Yet</strong></p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="150">&nbsp;</td>
		<td colspan="1" rowspan="1" data-colwidth="112">
			<p data-renderer-start-pos="23911">N/A</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="92">&nbsp;</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="126">
			<p data-renderer-start-pos="23924">Test Suite 9</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="120">&nbsp;</td>
		<td colspan="1" rowspan="1" data-colwidth="160">
			<div data-="">
				<p data-renderer-start-pos="23944"><strong data-renderer-mark="true">Not Started Yet</strong></p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="150">&nbsp;</td>
		<td colspan="1" rowspan="1" data-colwidth="112">
			<p data-renderer-start-pos="23967">N/A</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="92">&nbsp;</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="126">
			<p data-renderer-start-pos="23980">Test Suite 10</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="120">&nbsp;</td>
		<td colspan="1" rowspan="1" data-colwidth="160">
			<div data-="">
				<p data-renderer-start-pos="24001"><strong data-renderer-mark="true">Not Started Yet</strong></p>
			</div>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="150">&nbsp;</td>
		<td colspan="1" rowspan="1" data-colwidth="112">
			<p data-renderer-start-pos="24024">N/A</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="92">&nbsp;</td>
	</tr>
</tbody>
</table>

Katalon Studio auto-generates JUnit report with all test cases in test suite 1,2,3,4,5.

## Troubleshoot testing termination

When a test suite/test suite collection is terminated, in the execution log, Katalon Studio prints out information about the test suite/test suite collection reference ID and the maximum number of test failures allowed.

This applies to either sequential or parallel mode execution. You can be able to check which test execution is terminated and their reason why.

## Terminated Execution and 3rd-party Integrations
The final status of a terminated test suite is marked **Incomplete**.

**Incomplete** test suite and its test cases' results are not uploaded to 3rd-party tools (qTest, JIRA, Slack, Azure DevOps Test Plans, TestRail) except for TestOps, since TestOps parses the execution log.

Katalon Studio sends **Incomplete** test suite execution’s attachments, including execution log and JUnit Report to TestOps. This action ends the incomplete execution on TestOps.
