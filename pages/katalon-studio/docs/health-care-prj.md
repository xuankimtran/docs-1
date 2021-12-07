---
title: "Web UI testing (Healthcare sample)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/health-care-prj.html
---

This sample demonstrates fundamental WebUI testing in Katalon Studio. The application under test (AUT) is the CURA Healthcare Service website: `https://katalon-demo-cura.herokuapp.com/`. You can learn more about WebUI testing in this document: [Introduction to WebUI testing](https://docs.katalon.com/katalon-studio/docs/introduction-to-web-testing.html#before-you-begin).
## Open Healthcare sample project

To open Healthcare sample project, in Katalon Studio, go to **File > New Sample Project > Sample Web UI Tests Project (Healthcare)**.

<img src="url" width="70%" alt="Open Healthcare sample in Studio">

Alternatively, you can download the Healthcare sample project from our Github repository here: [Healthcare sample](https://github.com/katalon-studio-samples/healthcare-tests).
## Healthcare sample project components
### Profiles

To open the excution profile, go to **Profiles > default**.

<img src="url" width="70%" alt="Default profile in the Healthcare sample">


You can create and save all global variables in the execution profile. They can be used across test cases in your project. To learn more about execution profile and global variables, you can refer to this document: [Execution Profile and Global Variables](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html).

Here, Katalon creates 3 global variables in this sample project:

<table>
<thead>
  <tr>
    <th>Name</th>
    <th>Value</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>G_Timeout</td>
    <td>10</td>
  </tr>
  <tr>
    <td>G_SiteURL</td>
    <td>http://demoaut.katalon.com</td>
  </tr>
  <tr>
    <td>G_ShortTimeOut</td>
    <td>5</td>
  </tr>
</tbody>
</table>

### Custom keywords

Katalon also creates three custom keywords in this sample project. To learn more about custom keywords, you can refer to this document: [Introduction to custom keywords](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html). 

To see the custom keywords, in the **Test Explorer** panel, go to **Keywords > com.example > WebUICustomKeywords**

<details><summary> <code>isElementPresent</code> </summary>

### Description

This keyword is to check if an element presents in a definite amount of time.
### Parameters

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
    <td>to</td>
    <td>TestObject<br></td>
    <td>Yes</td>
    <td>A Katalon test object</td>
  </tr>
  <tr>
    <td>timeout</td>
    <td>int</td>
    <td>Yes</td>
    <td>The timeout to wait for the element to appear (in seconds).</td>
  </tr>
</tbody>
</table>

</details>

<details><summary> <code>getHtmlTableColumns</code> </summary>

### Description

This keyword gets all rows of an HTML table.
### Parameters

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
    <td>table</td>
    <td>TestObject<br></td>
    <td>Yes</td>
    <td>A Katalon test object represents an HTML table.</td>
  </tr>
  <tr>
    <td>outerTagName</td>
    <td>string</td>
    <td>Yes</td>
    <td>The outer tagname of <code>tr</code> tag, usually <code>tbody</code></td>
  </tr>
</tbody>
</table>

</details>

<details><summary> <code>getHtmlTableColumns</code> </summary>

### Description

This keyword gets all cells of a row of an HTML table .
### Parameters

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
    <td>table</td>
    <td>WebElement</td>
    <td>Yes</td>
    <td>A WebElement represents a row of an HTML table</td>
  </tr>
  <tr>
    <td>tagName</td>
    <td>string</td>
    <td>Yes</td>
    <td>The HTML column tagname, usually <code>td/th</code></td>
  </tr>
</tbody>
</table>

</details>

### Test cases

To get access to the main test cases in this project, in the **Test Explorer** panel, go to **Test Cases > Main Test Cases**.

<img src="url" width="70%" alt="Main test cases">

There are three test cases for different purposes: 

1. **TC1_Verify Successful Login** is to verify if a person can log in successfully with a valid account. The flow in this test case is as follows:

    - Go to the CURA Healthcare Service website: `https://katalon-demo-cura.herokuapp.com/`. Here, we use the `G_SiteURL` global variables.
    - Click the **Make Appointment** button.
    - Fill in the **Username** and **Password**. Here, we set the value type of **Username** and **Password** as **Variable**. You can change the **Username** and **Password** value in the **Variable** tab. To learn more about test case variables, you can refer to this document: [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html).
    - Click the **Login** button.
    - Verify if the account is logged in successfully. Here, we use the `G_Timeout` variables. If the page **Appointment** appears within 10 seconds, the login is successful.
    - Close browser.

    <img src="url" width="70%" alt="Test Case 1 - Verify successful login">

2. **TC2_Verify Successful Appointment** is to verify if that person can successfully make an appointment after logging in. The flow in this test case is as follows:

    - Go to the CURA Healthcare Service website: `https://katalon-demo-cura.herokuapp.com/` and login. Here, to speed up the login process, we call the test case from **Common Test Cases/Login**. To learn more about calling test cases, you can refer to this document: [Call test cases](https://docs.katalon.com/katalon-studio/docs/call-test-case.html#call-test-case-in-manual-view).
    - To make an appointment, fill in the valid value for **Facility**, **Healthcare Program** and **Visit Date**. Click the **Book Appointment** button.
    - Verify if the appointment is successfully confirmed. Here, we consider a appointment is successfully confirmed when the **Appointment Confirmation** text appears.
    - Verify if the booking information is matched with the confirmation information.
    - Take screenshot. 

    > Notes:
    > * You can only see the screenshot after executing a test suite. See below: [Test suite and test suite collection](https://docs.katalon.com/katalon-studio/docs/health-care-prj.html#test-suite-and-test-suite-collection).

    <img src="url" width="70%" alt="Test Case 2 - Verify successful appointment">

3. **TC3_Visual Testing Example** utilizes the **Visual Testing** feature in Katalon TestOps to compare images captured during test executions. You can see the instructions for this feature here: [Visual Testing in Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/ks-visual-testing.html#set-up-visual-testing).

    <img src="url" width="70%" alt="Test Case 3 - Visual Testing example">

### Test suite and test suite collection

There are two test suites in this project. To get access to them, in the **Test Explorer** panel, go to **Test Suites**.

<img src="url" width="70%" alt="Main test suites">

1. **Healthcare-tests - TS_RegressionTest**: This sample test suite is a combination of three above test cases.

<img src="url" width="70%" alt="Healthcare-tests - TS_RegressionTest">

2. **Healthcare-tests - TS_RegressionTestCollection**: This sample test suite collection is a combination of two **Healthcare-tests - TS_RegressionTest** test suites with different testing environments. In this project, we run the test suites with Firefox and Chrome.

<img src="url" width="70%" alt="Healthcare-tests - TS_RegressionTestCollection">

### Execute selected test case or test suite/test suite collection

To execute a test case or a test suite/test suite collection in the sample project:

1. Select the test case/test suite/test suite collection you want to execute.
2. Click **Run** or press Ctrl + Shift + A (macOS: Cmd+Shift+A).

You can choose different browsers to execute your test in the dropdown list next to **Run**. 

<img src="url" width="70%" alt="Run the test case">

3. Observe the test result in the **Log Viewer** tab.

<img src="url" width="70%" alt="Oservice results in the log Viewer">


> Notes:
> * In the test suite or test suite collection level, you can view test results in the **Result** tab. The test results can be Passed, Failed, Error or Incomplete.
> * After executing test suites or test suite collections, you can view your reports and details in `<your-project-folder>/Reports`. Katalon Studio also supports exporting test reports into different formats, such as HTML, CSV, PDF, and JUnit.
> * For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).



