---
title: "Skip test cases"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/skip-test-cases.html
redirect_from:
description:
---

In this article, we demonstrate how to skip test cases in a test suite by preconfiguring **Test Listener** with the `TestCaseContext.skipThisTestCase()` method. To learn more about the usage of Test Listeners, go to [Test Listeners (Test Hooks)](https://docs.katalon.com/katalon-studio/docs/fixtures-listeners.html#test-listeners-test-hooks).

## Skip Test Cases

1. In the **Test Explorer** panel, right-click on **Test Listeners**. Select **New > New Test Listener**. 
   
<img src="https://github.com/katalon-studio/docs-images/raw/4edfbc46044bc17f1d039c925c34230ed76357e1/katalon-studio/docs/test-listeners-test-hooks/image2017-12-5-103A353A3.png" width="50%" alt="Create a new test listener">

2. A **New Test Listener** dialog opens. Name it as **Skiptest**. Choose **Generate sample Before Test Case method**. Click **OK**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/skip-test-cases/KS-SKIP-Create-Skiptest-Listener.png" width="50%" alt="Name new test listener">

Katalon Studio generates a sample template with necessary annotations, libraries and supported functions as accordingly:

```groovy
import internal.GlobalVariable as GlobalVariable

import com.kms.katalon.core.annotation.BeforeTestCase
import com.kms.katalon.core.annotation.BeforeTestSuite
import com.kms.katalon.core.annotation.AfterTestCase
import com.kms.katalon.core.annotation.AfterTestSuite
import com.kms.katalon.core.context.TestCaseContext
import com.kms.katalon.core.context.TestSuiteContext

class Skiptest {
	/**
	 * Executes before every test case starts.
	 * @param testCaseContext related information of the executed test case.
	 */
	@BeforeTestCase
	def sampleBeforeTestCase(TestCaseContext testCaseContext) {
	println testCaseContext.getTestCaseId()
	println testCaseContext.getTestCaseVariables()
}
```


3. Use the `TestCaseContext.skipThisTestCase()` method to skip test cases. See also [skipThisTestCase()](https://docs.katalon.com/javadoc/com/kms/katalon/core/context/TestCaseContext.html#skipThisTestCase()).
   
Inside the **Skiptest** Listener, copy and paste the following code under the generated sample template.
   
```groovy

// To check for the desired condition and skip the test case if true.
if(inputyourconditionhere)
{   testCaseContext.skipThisTestCase()
}
```

4. Return to your test suite and run it. Check the results in the **Results** tab to see the final status of your tests.

> Note:
>
> Katalon Studio supports exporting test reports in **HTML**, **CSV**, **PDF** and **JUnit**. You can learn more about exporting reports here: [Generate reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html#automatically-generate-reports).

## Example:

In this example, we want to skip the Test Case named: "Google" in a test suite.
We input the following sample code in the **Skiptest** Listener:

```groovy
class Skiptest {
	/**
	 * Executes before every test case starts.
	 * @param testCaseContext related information of the executed test case.
	 */
	@BeforeTestCase
	def sampleBeforeTestCase(TestCaseContext testCaseContext) {
    println testCaseContext.getTestCaseId()
	println testCaseContext.getTestCaseVariables()
	if ((testCaseContext.getTestCaseId()) == "Test Cases/Google") 
		{	testCaseContext.skipThisTestCase()
		}
}
```
Check the results after running the Test Suite. Katalon successfully skips the test case named: "Google".

<img src="https://github.com/katalon-studio/docs-images/raw/8dc7e1d66cd0fe2719aaeabc91d5040ede4bb2aa/katalon-studio/docs/skip-test-cases/KS-SKIP-Results-after-skipping-test-cases.png" width="70%" alt="Results after skipping test case">