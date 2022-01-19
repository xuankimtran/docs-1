---
title: "Sample BDD (Cucumber) test project" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/bdd-samples.html 
---

This sample demonstrates fundamental behavior-driven development (BDD) testing. The application under test (AUT) is the react calculator: `https://katalon-studio-samples.github.io/calculator`. To learn more about BDD testing, you can refer to this document: [BDD Testing Framework (Cucumber integration)](https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html).
## Open the sample BDD test project

To open the BDD sample project, in Katalon Studio, go to **File > New Sample Project > Sample BDD Cucumber Tests Project**.

<img src="url" width="70%" alt="Open BDD sample in Studio">

Alternatively, you can download the sample BDD test project from our Github repository: [Sample BDD tests](https://github.com/katalon-studio-samples/calculator-bdd-tests).
## Sample API project components
### Profiles

To open the execution profile, go to **Profiles > default**.

<img src="url" width="60%" alt="Default profile in the BDD sample">

You can create and save all global variables in the execution profile. They can be used across test cases in your project. To learn more about execution profiles and global variables, you can refer to this document: [Execution profile and global variables](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html).

Katalon creates a global variable in this sample project as follows:

<table>
<thead>
  <tr>
    <th>Name</th>
    <th>Value</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>baseURL</td>
    <td><code>https://katalon-studio-samples.github.io/calculator</code></td>
  </tr>
</tbody>
</table>

### Feature files

To open the sample feature files, go to **Include > features > operations**. Double-click to open one of the following .feature files:

<table>
<thead>
  <tr>
    <th>Feature files</th>
    <th>Description</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Divide.feature</td>
    <td>This file outlines the scenario to perform the dividing actions on the react calculator.</td>
  </tr>
  <tr>
    <td>Minus.feature</td>
    <td>This file outlines the scenario to perform the minus actions on the react calculator.</td>
  </tr>
  <tr>
    <td>Multiply.feature</td>
    <td>This file outlines the scenario to perform the multiplying actions on the react calculator.</td>
  </tr>
  <tr>
    <td>Plus.feature</td>
    <td>This file outlines the scenario to perform the plus actions on the react calculator.</td>
  </tr>
</tbody>
</table>

To learn more about feature files creation and maintanance in Katalon Studio, you can refer to this document: [Create & maintain feature files](https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html#add-feature-files).

### Step definitions

To execute the scenario in the feature files, each Gherkin step needs to be defined as a set of programming code. You can reuse Katalon Studio built-in keywords in step definition files. When Katalon Studio executes any features files in the test case, it looks for the matching step definitions in the source folder.

In this sample test project, you can find the step definitions in **Include > scripts > groovy**. The step denfition files are located in two different packages:

<img src="url" width="60%" alt="Step definitions in the BDD project">

1. The `default` package. 

  - The `default` package contains the `Common.groovy` file that defines the `Given` and `Then` steps for all feature files. 

<img src="url" width="60%" alt="Step definitions in the BDD project">

2. The `operations` package.

  - The `operations` package contains four step definition files, representing four forms of calculation: minus, plus, division and multiplication. These files define the `When` steps in their matching feature files. For example, the `Minus.groovy` file defines the `When` steps in the `Minus.feature` file. 

<img src="url" width="60%" alt="Step definitions in the BDD project">

### Custom keywords

You can use custom keywords in the test case. To learn more about custom keywords, you can refer to this document: [Introduction to custom keywords](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html). 

Katalon creates a custom keyword in this sample project. To see the custom keyword, in the **Test Explorer** panel, go to **Keywords > sample > ClickNumber.groovy**.

<img src="url" width="60%" alt="Custom keywords in the BDD project">

The `ClickNumber.clickNumber` keyword is to convert a given number into an integer, then input the number on the react calculator.

This keyword includes the following parameters:

<table>
<thead>
  <tr>
    <th>Parameter</th>
    <th>Type</th>
    <th>Mandatory</th>
    <th>Description</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>number</td>
    <td>string</td>
    <td>Yes</td>
    <td>The number you want to input in the react calculator.</td>
  </tr>
</tbody>
</table>

### Test cases

To access the main test cases in this project, in the **Test Explorer** panel, go to **Test Cases > operations**.

<img src="url" width="60%" alt="Test cases">

There are four test cases representing four different formulas: minus, plus, division and multiplication. 

Here we will describe the main flow in the test case **Verify Minus**. This test case performs the minus calculation with the given numbers.

> The other test cases flow are similar but perform different formulas.

The test case **Verify Minus** executes the `Minus.feature` files in the following steps:

- The `Given` step calls the test case **The Calculator page is loaded successfully**. This test case opens the react calculator.
- The `When` steps calls the test case **Minus number**. This test case:
  
  - Uses the `ClickNumber.clickNumber` custom keyword to input the given numbers on the react calculator.
  - Click the minus button on the calculator

- The `Then` step calls the test case **Check result**. This test case verifies whether the result appeared on the calculator matches with the result stated in the feature files.

**<details><summary>Click to view the test script</summary>**

```groovy
import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import static com.kms.katalon.core.testobject.ObjectRepository.findWindowsObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
import com.kms.katalon.core.cucumber.keyword.CucumberBuiltinKeywords as CucumberKW
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.windows.keyword.WindowsBuiltinKeywords as Windows
import internal.GlobalVariable as GlobalVariable

CucumberKW.runFeatureFile('Include/features/operations/Minus.feature')
```
</details>
      

### Data Files

To view the data files in this sample project, in the **Test Explorer** panel, go to **Data Files > ListUser**.

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/api-sample-prj/KS-API-Data-files.png" width="60%" alt="Data files in the API sample">

Alternatively, you can go to `<your-project-folder>\Data Files` and choose the file you want to open:

- `ListUser.dat` is the .dat file of the `ListUser.xlsx` file.
- `ListUser.xlsx` is an excel file that contains the user information.

### Test suites

The sample test suite demonstrates the web service testing with data-driven testing. To view sample test suite, in the **Test Explorer** panel, go to **Test Suite > web-service-tests - All Test Cases**.

This test suite includes the **Create a new user** and **Find user by ID** test case.
We bind the **Create a new user** test case with the **ListUser** data file. To view the data binding section, select the **Create a new user** test case, then click **Show Data Binding**. To learn more about binding data, you can refer to the following document: [Data Binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/api-sample-prj/KS-API-Test-suite.png" width="100%" alt="Sample test suites">

## Execute selected test cases or test suites

To execute a test case or a test suite in the sample project:

1. Select the test case/test suite you want to execute.
2. Click **Run** or press Ctrl + Shift + A (macOS: Cmd+Shift+A).

    You can choose different browsers to execute your test in the dropdown list next to **Run**. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/api-sample-prj/KS-API-Execution.png" width="30%" alt="Run the test case">

3. Observe the test result in the **Log Viewer** tab.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/api-sample-prj/KS-API-Log-viewer.png" width="100%" alt="Oservice results in the log Viewer">

    > Notes:
    > * You can view test results of the test suite in the **Result** tab. The test results can be Passed, Failed, Error, or Incomplete.
    > * After executing test suites or test suite collections, you can view your reports and details in `<your-project-folder>/Reports`. Katalon Studio also supports exporting test reports into different formats, such as HTML, CSV, PDF, and JUnit.
    > * For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).
## See also

* [Cucumber Features File](https://docs.katalon.com/katalon-studio/docs/cucumber-features-file.html).

