---
title: "Skip test cases"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/skip-test-cases.html
redirect_from:
description:
---


In this article, we demonstrate how to skip test cases in a test suite by preconfiguring **Test Listener** with the `TestCaseContext.skipThisTestCase()` method. See also [Test Listeners](https://docs.katalon.com/katalon-studio/docs/fixtures-listeners.html#test-listeners-test-hooks).

## Skip Test Cases

1. In the **Test Explorer** pane, right-click on **Test Listeners**. Select **New > New Test Listener**. 
   
<img src="https://github.com/katalon-studio/docs-images/raw/4edfbc46044bc17f1d039c925c34230ed76357e1/katalon-studio/docs/test-listeners-test-hooks/image2017-12-5-103A353A3.png" width="70%" alt="Create a new test listener">

2. A **New Test Listener** dialog opens. Name it as **Skiptest**. Choose **Generate sample Before Test Case method**. Click **OK**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/skip-test-cases/KS-SKIP-Create-Skiptest-Listener.png" width="70%" alt="Name new test listener">

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
   
Inside the **SkipTest** Test Listener, copy and patse the code under the generated sample template.
This helps check for the desired condition and skip the test case if true.
   
```groovy
if(condition){
testCaseContext.skipThisTestCase()
```

4. Return to your test suite. run the test suite. Check the results in the **Results** tab to see the final status of your tests.


## Example:

In this example, we want to skip Test Case: "Google" in a test suite.
We input the following sample code in the new Test Listener:

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
Check the results after running the Test Suite. The test case: "Google" is succesfully skipped.

<img src="https://github.com/katalon-studio/docs-images/raw/8dc7e1d66cd0fe2719aaeabc91d5040ede4bb2aa/katalon-studio/docs/skip-test-cases/KS-SKIP-Results-after-skipping-test-cases.png" width="70%" alt="Results after skipping test case">