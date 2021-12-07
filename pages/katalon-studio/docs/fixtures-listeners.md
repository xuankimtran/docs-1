---
title: "Test Fixtures and Test Listeners (Test Hooks)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/fixtures-listeners.html
redirect_from:
    - "/x/E4C9/"
    - "/katalon-studio/docs/setupteardown-for-test-suite-and-test-case.html"
    - "/x/7zhO/"
    - "/katalon-studio/docs/test-listeners-test-hooks/"
    - "/katalon-studio/docs/test-listeners-test-hooks.html"
description:
---

To extend your current testing flow, the test fixtures (setUp/tearDown methods) and test listeners might be useful for prerequisite and clean-up configurations for all the tests.

With the prerequisite configuration, the test engine must take specific actions before starting test execution. For clean-up configuration, the test engine must carry out some actions after the test execution finishes.

The infographic below visualizes how Katalon Studio executes your automated test projects with the test fixtures and test listeners methods.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/execution-flow.png" alt="test execution lifecycle" width="100%">

> Test listeners are always triggered first if you define both test listeners and activate setUp/tearDown methods simultaneously.

This document guides you through how to configure the setUp/tearDown methods and the test listeners in Katalon Studio.

## setUp() and tearDown() for Test Suite and Test Case

In Katalon Studio, you can specify prerequisite and clean-up configurations for your test cases using the setUp and tearDown methods. 

Here are some common usages of the setUp and tearDown methods:

<table width=100%>
	<thead>
		<tr>
			<th>Method</th>
			<th>Common usage</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>setUp</td>
			<td>
				<ul>
					<li>Prepare a testing environment, such as:
						<ul>
							<li>Starting new browser with clean cookies</li>
							<li>Creating temporary and proxy databases, directories</li>
							<li>tarting a server process</li>
						</ul>
					</li>
					<li>Call required test cases for the executed test suite</li>
				</ul>
			</td>
		</tr>
		<tr>
			<td>tearDown</td>
			<td>
				<ul>
					<li>Clean-up testing environment, such as:
						<ul>
							<li>Closing connections to browsers</li>
							<li>Disconnecting from databases or server</li>
						</ul>
					</li>
					<li>Call tearDown test cases for the executed test suite</li>
				</ul>
			</td>
		</tr>
	</tbody>
</table>

The table below describes the trigger conditions of these methods:

<table width=100%>
	<thead>
		<tr>
			<th>Method</th>
			<th>Description</th>
			<th>Trigger Condition</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>setUp</td>
			<td>Setup test suite environment</td>
			<td>Before executed test suites</td>
		</tr>
		<tr>
			<td>setUpTestCase</td>
			<td>Run before each test case starts</td>
			<td>Before executed test cases</td>
		</tr>
		<tr>
			<td>tearDown</td>
			<td>Clean test suites environment</td>
			<td>After executed test suites</td>
		</tr>
		<tr>
			<td>tearDownTestCase</td>
			<td>Run after each test case ends</td>
			<td>After executed test cases</td>
		</tr>
	</tbody>
</table>

### Activate setUp and tearDown in a test suite

In the test suite editor, switch to the **Script** tab to view the setUp and tearDown methods template.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/setup-teardown-template.png" alt="script view of test suite" width="100%">

By default, the setUp and tearDown methods are not triggered even if they match with provided trigger condition as shown in the below code sample:

``` groovy
/**
 * Setup test suite environment.
 */
@SetUp(skipped = true) // Please change skipped to be false to activate this method.
def setUp() {
	// Put your code here.
}
```

To activate the **setUp** and **tearDown** methods, you need to set the **skipped** value to **false**. For example: 
``` groovy 
@SetUp(skipped = false)
```

> Notes:
>
> * Execution progress from these methods still has execution logs as usual, and they are stored in the execution logs files of Katalon Studio.
> * You cannot see setUp and tearDown executed reports from generated Test Suite report. You can only see **setUpTestCase** and **tearDownTestCase** in generated Test Suite report.
>
> 	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/setupteardown-for-test-suite-and-test-case/Screen-Shot-2018-01-05-at-14.24.23.png" alt="sample before test suite" width=100%>

### Add setUp and tearDown in manual view of a test case

In the manual view of a test case, you can add the setUp and tearDown method by following these steps:

1. Click on the drop-down button of the **Add** icon and choose **Method**. To learn more about the method statement, see [Define Method](https://docs.katalon.com/katalon-studio/docs/statements.html#define-method).
2. The **Method builder** dialog appears. Enter your method's name and its return value, then choose one of the options below:

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/method-builder.png" alt="method builder" width="100%">

<table>
	<thead>
		<tr>
			<th>Method</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Set Up</td>
			<td>This method is always called first, before executing the main test steps.<br><br></td>
		</tr>
		<tr>
			<td>Tear Down If Failed</td>
			<td>This method is called after executing all steps of the test case, if one of those steps is marked as <strong>Failed</strong>.</td>
		</tr>
		<tr>
			<td>Tear Down If Passed</td>
			<td>This method is called after executing all steps of the test case, if all of those steps are marked as <strong>Pass</strong>.</td>
		</tr>
		<tr>
			<td>Tear Down If Error</td>
			<td>This method is called after executing all the test case steps, if one of those steps is marked as <strong>Error</strong>.</td>
		</tr>
		<tr>
			<td>Tear Down</td>
			<td>This method is called at the end of an execution.</td>
		</tr>
	</tbody>
</table>

3. To add a test step under a method, choose the line of that method, then click **Add**. A new keyword is added under that method.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/setup-teardown-manual.png" alt="setUp and tearDown in manual view" width="100%">

> The setUp/tearDown methods might be marked as **Error** if any issue occurs during their execution. The possible exception is when the **AssertionError** class is used, or if the methods are skipped.

### Add setUp and tearDown in the script view of a test case

In the script view of a test case, you can declare a method as setUp/tearDown methods using the matching annotation above them. For example:

```groovy
@com.kms.katalon.core.annotation.SetUp
def setup(def param1, def param2) {
}
@com.kms.katalon.core.annotation.TearDownIfFailed
def teardownIfFailed(def param1, def param2) {
}
@com.kms.katalon.core.annotation.TearDownIfPassed
def teardownIfPassed(def param1, def param2) {
}
@com.kms.katalon.core.annotation.TearDownIfError
def teardownIfError(def param1, def para2) {
}
@com.kms.katalon.core.annotation.TearDown
def teardown(def param1, def param2) {
}
```

## Test Listeners (Test Hooks)

Test listeners are test steps created to "listen" to the event defined in the script and behave accordingly. In this section, you will learn how to create a test listener.

### Create new Test Listeners

Test listeners are test artifacts. You can perform all basic operations such as create, copy/cut, rename, or delete with test listeners. To create a new test listener, do as follows:

1. In the **Tests Explorer** section, right-click on the **Test Listeners** folder. Select **New > New Test Listener**.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/new-test-listener.png" alt="create new test listener" width=80%>

2. The **New Test Listener** dialog appears with four options as below: 

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/new-test-listener-dialog.png" alt="Test Listeners options" width=80%>

	| Option | Description |
	| --- | --- |
	| Generate sample Before Test Case method | Create a sample test listener executed before every test case starts. |
	| Generate sample After Test Case method | Create a sample test listener executed after every test case ends. |
	| Generate sample Before Test Suite method | Create a sample test listener executed before every test suite starts. |
	| Generate sample After Test Suite method | Create a sample test listener executed after every test suite ends. |

	You can select one or multiple options, then click **OK**. Once finished, Katalon Studio generates a sample template accordingly. The template includes necessary annotations, libraries, and supported functions.

> Notes:
>
> * You can create multiple test listeners.
> * If you have more than one test listener class, the classes themselves are instantiated in Katalon storage in alphabetical order. Only then are the individual listener methods executed top-down.
> * The execution status of any steps within test listers does not affect the overall status of the executed test case. For example, if you have a FAILED output in any of your test listeners, but the final status of the executed test case is PASSED, then the test case's status is PASSED.

You can view the test listener template here:

```groovy
import internal.GlobalVariable as GlobalVariable

import com.kms.katalon.core.annotation.BeforeTestCase
import com.kms.katalon.core.annotation.BeforeTestSuite
import com.kms.katalon.core.annotation.AfterTestCase
import com.kms.katalon.core.annotation.AfterTestSuite
import com.kms.katalon.core.context.TestCaseContext
import com.kms.katalon.core.context.TestSuiteContext

class NewTestListener {
	/**
	 * Executes before every test case starts.
	 * @param testCaseContext related information of the executed test case.
	 */
	@BeforeTestCase
	def sampleBeforeTestCase(TestCaseContext testCaseContext) {
		println testCaseContext.getTestCaseId()
		println testCaseContext.getTestCaseVariables()
	}

	/**
	 * Executes after every test case ends.
	 * @param testCaseContext related information of the executed test case.
	 */
	@AfterTestCase
	def sampleAfterTestCase(TestCaseContext testCaseContext) {
		println testCaseContext.getTestCaseId()
		println testCaseContext.getTestCaseStatus()
	}

	/**
	 * Executes before every test suite starts.
	 * @param testSuiteContext: related information of the executed test suite.
	 */
	@BeforeTestSuite
	def sampleBeforeTestSuite(TestSuiteContext testSuiteContext) {
		println testSuiteContext.getTestSuiteId()
	}
	/**
	 * Executes after every test suite ends.
	 * @param testSuiteContext: related information of the executed test suite.
	 */
	@AfterTestSuite
	def sampleAfterTestSuite(TestSuiteContext testSuiteContext) {
		println testSuiteContext.getTestSuiteId()
	}
}
```

### Example

In this example, we will define multiple environments as different Global Variables by using test listeners. For more information, see [Global Variables and Execution Profile](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html#create-a-profile).

Before you execute your test case, change the environment variable to your preferred environment by following the script below:

```groovy
import internal.GlobalVariable as GlobalVariable

import com.kms.katalon.core.annotation.BeforeTestCase
import com.kms.katalon.core.annotation.BeforeTestSuite
import com.kms.katalon.core.annotation.AfterTestCase
import com.kms.katalon.core.annotation.AfterTestSuite
import com.kms.katalon.core.context.TestCaseContext
import com.kms.katalon.core.context.TestSuiteContext

/**
 * Executes before every test case starts.
 * @param testCaseContext related information of the executed test case.
 */

@BeforeTestCase
def sampleBeforeTestCase(TestCaseContext testCaseContext) {
    if (GlobalVariable.gl_Environment == 'Local') {
        GlobalVariable.gl_Url = 'localhost'
    } else if (GlobalVariable.gl_Environment == 'Staging') {
        GlobalVariable.gl_Url = 'staging'
    }
}
```
