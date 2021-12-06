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

To extend your current testing flow, test fixtures and test listeners might be useful. Test fixture is a set of fixed steps used as prerequisite and clean-up configurations for all the tests.

With the prerequisite configuration, the test engine must take specific actions before starting test execution. For clean-up configuration, the test engine must carry out some actions after the test execution finishes.

The infographic bellow visualizes how Katalon Studio executes your automated test projects with test fixtures (setUp/tearDown) and test listeners methods.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/execution-flow.png" alt="test execution lifecycle" width="100%">

> Test listeners is always triggered first if you define both test listeners and activate setUp/tearDown methods simultaneously.

In this document, we will guide you through how to configure the setUp/tearDown methods and the test listeners in Katalon Studio.

## setUp() and tearDown() for Test Suite and Test Case

In Katalon Studio, you can specify prerequisite and clean-up configurations for your test cases by using the setUp and tearDown methods. The table below describes the trigger conditions and common usages of these methods:

<table>
	<thead>
		<tr>
			<th>Method</th>
			<th>Description</th>
			<th>Trigger Condition</th>
			<th>Common Usage</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>setUp</td>
			<td>Setup test suite environment</td>
			<td>Before executed test suites</td>
			<td>
				<ul>
					<li>Prepare a testing environment</li>
					<li>Call required test cases for the executed test suite</li>
				</ul>
			</td>
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
			<td>
				<ul>
					<li>Clean-up testing environment</li>
					<li>Call TearDown test cases for the executed test suite</li>
				</ul>
			</td>
		</tr>
		<tr>
			<td>tearDownTestCase</td>
			<td>Run after each test case ends</td>
			<td>After executed test cases</td>
		</tr>
	</tbody>
</table>

### Activate setUp and tearDown

In the test suite editor, switch to the **Script** tab to view the setUp and tearDown methods template.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/setup-teardown-template.png" alt="script view of test suite" width="100%">

By default, the **SetUp** and **TearDown** methods are not triggered even if they match with provided trigger condition as shown in the below code sample.

``` groovy
/**
 * Setup test suite environment.
 */
@SetUp(skipped = true) // Please change skipped to be false to activate this method.
def setUp() {
	// Put your code here.
}
```

To activate the **setUp** and **tearDown** methods, you need to set the **skipped** value to **false**. For example: `@SetUp(skipped = false)`.

> Notes:
>
> * Execution progress from these methods still has execution logs as usual, and they are stored in the execution logs files of Katalon Studio.
> * You cannot see setUp and tearDown executed reports from generated Test Suite report. You can only see **setUpTestCase** and **tearDownTestCase** in generated Test Suite report.
>
> 	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/setupteardown-for-test-suite-and-test-case/Screen-Shot-2018-01-05-at-14.24.23.png" alt="sample before test suite" width=100%>

### In Manual view

<table>
	<thead>
		<tr>
			<th>Method</th>
			<th>Description</th>
			<th>Common Usage</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Set Up</td>
			<td>This method is always called <strong>first</strong> prior to executing the main test steps.<br><br></td>
			<td><p>Prepare testing environment such as:</p>
				<ul>
					<li>Starting new browser with clean cookies</li>
					<li>Creating temporary &amp; proxy databases, directories</li>
					<li>Starting a server process</li>
					<li>...</li>
				</ul>
			</td>
		</tr>
		<tr>
			<td>Tear Down If Failed</td>
			<td>This method will be called after executing all steps of the test case, <strong>and</strong> one of those steps has <strong>Failed</strong> status.</td>
			<td><p>Clean-up the testing environment such as:</p>
				<ul>
					<li>Closing browsers</li>
					<li>Disclosing opened connections to database or server</li>
					<li>...</li>
				</ul><p>&nbsp;</p>
			</td>
		</tr>
		<tr>
			<td>Tear Down If Passed</td>
			<td>This method will be called after executing all steps of the test case <strong>and</strong> all of those steps have <strong>Pass</strong> status.</td>
		</tr>
		<tr>
			<td>Tear Down If Error</td>
			<td>This method will be called after executing all the test case steps <strong>and</strong> one of those steps has <strong>Error</strong> status.</td>
		</tr>
		<tr>
			<td>Tear Down</td>
			<td>This method will be called <strong>finally</strong>.</td>
		</tr>
	</tbody>
</table>

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/setup-teardown-manual.png" alt="setUp and tearDown in manual view" width="100%">

> The SetUp()/ TearDown() methods might have **Error** status if any issue occurs during their execution. The only exception to this is when **AssertionError** Class is used, or the methods are skipped.

### In Script view

You can declare a method as **setup()** or **teardown()** method using the appropriated annotation above it:

```groovy
@com.kms.katalon.core.annotation.SetUp
@com.kms.katalon.core.annotation.TearDown
@com.kms.katalon.core.annotation.TearDownIfFailed
@com.kms.katalon.core.annotation.TearDownIfPassed
@com.kms.katalon.core.annotation.TearDownIfError
```

For example:

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

Test listeners are test steps created based on your own criterion. Test listeners "listen" to the event defined in the script and behave accordingly. When matching the condition, you can execute test listeners. To start with Test Listeners, follow the guide below.

### Create new Test Listeners

Test Listeners are the same as other test artifacts. You can perform all basic operations such as **create, copy/cut, rename, or delete** with Test Listeners. This section focus on how to **create** new Test Listeners. In the Tests Explorer pane, you can find Test Listeners location. To create new Test Listener:

1. In the **Tests Explorer** section, right-click on **Test Listeners** folder. Select **New > New Test Listener**.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/new-test-listener.png" alt="create new test listener" width=80%>

2. The **New Test Listener** dialog appears with 4 options as below: 

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-listeners-test-hooks/new-test-listener-dialog.png" alt="Test Listeners options" width=80%>

	| Option | Description |
	| --- | --- |
	| Generate sample Before Test Case method | A sample listener will be generated before every test case starts. |
	| Generate sample After Test Case method | A sample listener will be generated after every test case ends. |
	| Generate sample Before Test Suite method | A sample listener will be generated before every test suite starts. |
	| Generate sample After Test Suite method | A sample listener will be generated after every test suite ends. |

	You can select one or multiple options, then click **OK**. Once finished, Katalon Studio generates a sample template accordingly. The template includes necessary annotations, libraries and supported functions.

> Notes:
>
> * There is no limit on Test Listeners. Users can create as many as preferred.
> * If you have more than one Test Listener class, the classes themselves are instantiated in Katalon storage in alphabetical order. Only then are the individual listener methods executed top-down.
> * Execution status of any steps within Test Listers will not affect the overall status of the executed test case. For example, if you have a FAILED output in any of your Test Listeners, but the final status of the executed test case is PASSED, then the test case's status will be PASSED).

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

In this example, we will define multiple environments as different Global Variables by using Test Listeners. For more information, see [Global Variables and Execution Profile](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html#create-a-profile).

Before you execute your test case, change the environment variable to your preferred environment by following the example below:

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
