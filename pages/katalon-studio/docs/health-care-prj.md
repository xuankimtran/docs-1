---
title: "Sample WebUI tests project (Healthcare sample)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/health-care-prj.html
---

This sample demonstrates WebUI testing fundamentals in Katalon Studio. The Application Under Test (AUT) is the CURA Healthcare Service website: `https://katalon-demo-cura.herokuapp.com/`. You can learn more about WebUI testing in this document: [Introduction to WebUI testing](https://docs.katalon.com/katalon-studio/docs/introduction-to-web-testing.html#before-you-begin).
## Open the Healthcare sample project

To open the Healthcare sample project, in Katalon Studio, go to **File > New Sample Project > Sample Web UI Tests Project (Healthcare)**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLE-Open-Healthcare-sample.png" width="70%" alt="Open Healthcare sample in Studio">

Alternatively, you can download the Healthcare sample project from our Github repository: [Healthcare sample](https://github.com/katalon-studio-samples/healthcare-tests).
## Healthcare sample project components
### Profiles

To open the execution profile, go to **Profiles > default**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLE-Open-execution-profiles.png" width="70%" alt="Default profile in the Healthcare sample">


You can create and save all global variables in the execution profile. They can be used across test cases in your project. To learn more about execution profiles and global variables, you can refer to this document: [Execution profile and global variables](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html).

Katalon creates three global variables in this sample project as follows:

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

You can use custom keywords in the test case. To learn more about custom keywords, you can refer to this document: [Introduction to custom keywords](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html). 

Katalon creates three custom keywords in this sample project. To see the custom keywords, in the **Test Explorer** panel, go to **Keywords > com.example > WebUICustomKeywords.groovy**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-custom-keywords.png" width="70%" alt="Custom keywords in the Healthcare project">

<details><summary> <code>com.example.WebUICustomKeywords.isElementPresent</code> </summary>

### Description

This keyword is to check if an element displays within a predefined time limit.
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
    <td>Required</td>
    <td>A Katalon test object</td>
  </tr>
  <tr>
    <td>timeout</td>
    <td>int</td>
    <td>Required</td>
    <td>The timeout to wait for the element to appear (in seconds).</td>
  </tr>
</tbody>
</table>

### Returns

<table>
<thead>
  <tr>
    <th>Param Type</th>
    <th>Type</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>boolean</td>
    <td>- <strong>true</strong>: if the element presents.<br>- <strong>false</strong>: if the element does not present.</td>
  </tr>
</tbody>
</table>

### Example

In this example, we want to check whether the **Make Appointment** button displays within 10 seconds.

```groovy
import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
import internal.GlobalVariable as GlobalVariable
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS

/*Open browser and navigate to the AUT website.*/
WebUI.openBrowser(GlobalVariable.G_SiteURL)

/*Check to see whether the Make Appointment button presents within 10 seconds*/
CustomKeywords.'com.example.WebUICustomKeywords.isElementPresent'(findTestObject('Page_CuraHomepage/btn_MakeAppointment'), 10)

WebUI.closeBrowser()

```

</details>

<details><summary> <code>com.example.WebUICustomKeywords.getHtmlTableRows</code> </summary>

### Description

This keyword retrieves web elements from all rows in an HTML table. To learn more about the HTML element of a table, you can refer to this Mozilla developer document: [HTML table basics](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics).
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
    <td>Required</td>
    <td>A Katalon test object represents an HTML table.</td>
  </tr>
  <tr>
    <td>outerTagName</td>
    <td>string</td>
    <td>Required</td>
    <td>The outer tagname of the <code>tr</code> tag, usually <code>tbody</code></td>
  </tr>
</tbody>
</table>

### Returns

The web elements of all rows in the HTML table.

### Example

In this example, we want to retrieve the web elements of all rows in an HTML table body.

After creating a test object representing the HTML table, apply the `com.example.WebUICustomKeywords.getHtmlTableRows` custom keyword as follows:

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
import com.kms.katalon.core.testng.keyword.TestNGBuiltinKeywords as TestNGKW
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.windows.keyword.WindowsBuiltinKeywords as Windows
import internal.GlobalVariable as GlobalVariable
import org.openqa.selenium.Keys as Keys

/*Open the website contains the table*/
WebUI.openBrowser('https://docs.katalon.com/katalon-studio/docs/webui-click.html')

/*Get web elements of all rows of the table body*/
CustomKeywords.'com.example.WebUICustomKeywords.getHtmlTableRows'(findTestObject('Object Repository/Table/New Test Object'), 'tbody')

WebUI.closeBrowser()

```
</details>



<details><summary> <code>com.example.WebUICustomKeywords.getHtmlTableColumns</code> </summary>

### Description

This keyword retrieves web elements of all cells of a row in an HTML table. To learn more about the HTML element of a table, you can refer to this Mozilla developer document: [HTML table basics](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics).
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
    <td>Required</td>
    <td>A WebElement represents a row of an HTML table</td>
  </tr>
  <tr>
    <td>tagName</td>
    <td>string</td>
    <td>Required</td>
    <td>The HTML column tagname, usually <code>td/th</code></td>
  </tr>
</tbody>
</table>

### Returns

The web elements of all cells of a row in the HTML table.

### Example

In this example, we want to retrieve the web elements of all cells of the first row in the following HTML table body. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-Table-sample.png" width="100%" alt="Sample table">

As shown in the above picture, the row index starts at `0`. Here, to get the first line of the table body, we set paramter as `row[0]` and use the `com.example.WebUICustomKeywords.getHtmlTableRows` custom keyword as follows:

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
import com.kms.katalon.core.testng.keyword.TestNGBuiltinKeywords as TestNGKW
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.windows.keyword.WindowsBuiltinKeywords as Windows
import internal.GlobalVariable as GlobalVariable
import org.openqa.selenium.Keys as Keys

/*Open the website contains the table*/
WebUI.openBrowser('https://docs.katalon.com/katalon-studio/docs/webui-click.html')

/*Get web elements of all rows of the table body*/
Rows = CustomKeywords.'com.example.WebUICustomKeywords.getHtmlTableRows'(findTestObject('Object Repository/Table/New Test Object'), 'tbody')

/*Get web elements of all cells of the first row of the table body*/
TableColumns = CustomKeywords.'com.example.WebUICustomKeywords.getHtmlTableColumns'(Rows[0], 'td')

WebUI.closeBrowser()

```

</details>

### Test cases

To access the main test cases in this project, in the **Test Explorer** panel, go to **Test Cases > Main Test Cases**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-Main-test-cases.png" width="70%" alt="Main test cases">

There are three test cases for different purposes: 

1. The test case **TC1_Verify Successful Login** is to verify if a person can log in successfully with a valid account. The flow in this test case is as follows:

    - Go to the CURA Healthcare Service website: `https://katalon-demo-cura.herokuapp.com/`. Here, we use the `G_SiteURL` global variables.
    - Click the **Make Appointment** button.
    - Fill in the **Username** and **Password**. Here, we set the value type of **Username** and **Password** as **Variable**. You can change the **Username** and **Password** value in the **Variable** tab. To learn more about test case variables, you can refer to this document: [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html).

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-Username-password-variables.png" width="70%" alt="Username and Password Variables">

    - Click the **Login** button.
    - Verify if the account is logged in successfully. Here, we use the `G_Timeout` variables. If the page **Appointment** appears within 10 seconds, the login is successful.
    - Close browser.

      <a class="pop">
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLE-TC1.gif" width="70%" alt="Test Case 1 - Verify successful login">
      </a>
      <p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>

      **<details><summary>Click to view the test script</summary>**

      ```groovy
      import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
      import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
      import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
      import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
      import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
      import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
      import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
      import com.kms.katalon.core.model.FailureHandling as FailureHandling
      import com.kms.katalon.core.testcase.TestCase as TestCase
      import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
      import com.kms.katalon.core.testdata.TestData as TestData
      import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
      import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
      import com.kms.katalon.core.testobject.TestObject as TestObject
      import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
      import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
      import internal.GlobalVariable as GlobalVariable
      import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
      import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
      import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS

      WebUI.comment('Story: Login to CURA system')

      WebUI.comment('Given that the user has the valid login information')

      WebUI.openBrowser(GlobalVariable.G_SiteURL)

      WebUI.click(findTestObject('Page_CuraHomepage/btn_MakeAppointment'))

      WebUI.setText(findTestObject('Page_Login/txt_UserName'), Username)

      WebUI.setText(findTestObject('Page_Login/txt_Password'), Password)

      WebUI.comment('When he logins to CURA system')

      WebUI.click(findTestObject('Page_Login/btn_Login'))

      WebUI.comment('Then he should be able to login successfully')

      landingPage = WebUI.verifyElementPresent(findTestObject('Page_CuraAppointment/div_Appointment'), GlobalVariable.G_Timeout)

      WebUI.closeBrowser()
      ```
      </details>
      
2. The test case **TC2_Verify Successful Appointment** is to verify if that person can successfully make an appointment after logging in. The flow in this test case is as follows:

    - Go to the CURA Healthcare Service website: `https://katalon-demo-cura.herokuapp.com/` and sign in. Instead of re-recording the login steps, we call the **Common Test Cases/Login** test case. To learn more about calling test cases, you can refer to this document: [Call test cases](https://docs.katalon.com/katalon-studio/docs/call-test-case.html#call-test-case-in-manual-view).
    - To make an appointment, fill in the valid value for **Facility**, **Healthcare Program**, and **Visit Date**. Click the **Book Appointment** button.
    - Verify if the appointment is successfully confirmed. Here, we consider an appointment is successfully confirmed when the **Appointment Confirmation** text appears.
    - Verify if the booking information is matched with the confirmation information.
    - Take screenshot. 

    > Notes:
    > * You can only see the screenshot after executing a test suite. See below: [Test suite and test suite collection](https://docs.katalon.com/katalon-studio/docs/health-care-prj.html#test-suite-and-test-suite-collection).

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLE-TC2.gif" width="70%" alt="Test Case 2 - Verify successful appointment">
    </a>
    <p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>

    **<details><summary>Click to view the test script</summary>**

    ```groovy
    import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
    import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
    import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
    import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
    import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
    import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
    import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
    import com.kms.katalon.core.model.FailureHandling as FailureHandling
    import com.kms.katalon.core.testcase.TestCase as TestCase
    import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
    import com.kms.katalon.core.testdata.TestData as TestData
    import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
    import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
    import com.kms.katalon.core.testobject.TestObject as TestObject
    import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
    import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
    import internal.GlobalVariable as GlobalVariable
    import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
    import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
    import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS

    WebUI.comment('Story: Book an appointment')

    WebUI.comment('Given that the user has logged into their account')

    WebUI.openBrowser(GlobalVariable.G_SiteURL)

    WebUI.callTestCase(findTestCase('Common Test Cases/Login'), [('Username') : 'John Doe', ('Password') : 'ThisIsNotAPassword'], 
        FailureHandling.STOP_ON_FAILURE)

    WebUI.comment('And Appointment page is displayed')

    if (true) {
        WebUI.selectOptionByLabel(findTestObject('Page_CuraAppointment/lst_Facility'), 'Hongkong CURA Healthcare Center', false)

        WebUI.check(findTestObject('Page_CuraAppointment/chk_Medicaid'))

        WebUI.check(findTestObject('Page_CuraAppointment/chk_Readmission'))

        WebUI.setText(findTestObject('Page_CuraAppointment/txt_VisitDate'), '27/12/2016')

        WebUI.setText(findTestObject('Page_CuraAppointment/txt_Comment'), 'Please make appointment as soon as possible.')
    }

    WebUI.comment('When he fills in valid information in Appointment page')

    WebUI.click(findTestObject('Page_CuraAppointment/btn_BookAppointment'))

    WebUI.verifyTextPresent('Appointment Confirmation', false)

    WebUI.comment('Then he should be able to book a new appointment')

    if (true) {
        WebUI.verifyMatch('Hongkong CURA Healthcare Center', WebUI.getText(findTestObject('Page_AppointmentConfirmation/lbl_Facility')), 
            false)

        WebUI.verifyMatch('Yes', WebUI.getText(findTestObject('Page_AppointmentConfirmation/lbl_HospitalReadmission')), false)

        WebUI.verifyMatch('Medicaid', WebUI.getText(findTestObject('Page_AppointmentConfirmation/lbl_Program')), false)

        WebUI.verifyMatch('27/12/2016', WebUI.getText(findTestObject('Page_AppointmentConfirmation/lbl_VisitDate')), false)

        WebUI.verifyMatch('Please make appointment as soon as possible.', WebUI.getText(findTestObject('Page_AppointmentConfirmation/lbl_Comment')), 
            false)
    }

    WebUI.takeScreenshot()
    ```
    </details>

3. The test case **TC3_Visual Testing Example** utilizes the **Visual Testing** feature in Katalon TestOps to compare images captured during test executions. You can see the instructions for this feature here: [Visual Testing in Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/ks-visual-testing.html#set-up-visual-testing).
### Test suite and test suite collection

There are two test suites in this project. To access them, in the **Test Explorer** panel, go to **Test Suites**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-sample-test-suites.png" width="70%" alt="Main test suites">

1. The test suite **Healthcare-tests - TS_RegressionTest** combines the three test cases shown above.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-Test-suites-regression.png" width="70%" alt="Healthcare-tests - TS_RegressionTest">

2. The test suite collection **Healthcare-tests - TS_RegressionTestCollection** combines two **Healthcare-tests - TS_RegressionTest** test suites with different testing environments. In this project, we run the test suites with Firefox and Chrome.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-Test-suite-collection.png" width="70%" alt="Healthcare-tests - TS_RegressionTestCollection">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

## Execute selected test case or test suite/test suite collection

To execute a test case or a test suite/test suite collection in the sample project:

1. Select the test case/test suite/test suite collection you want to execute.
2. Click **Run** or press Ctrl + Shift + A (macOS: Cmd+Shift+A).

    You can choose different browsers to execute your test in the dropdown list next to **Run**. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-TOOLBAR-Chrome.png" width="30%" alt="Run the test case">

3. Observe the test result in the **Log Viewer** tab. To learn more about analyzing test execution logs, you can refer to this document: [[WebUI] Analyze Test Execution Logs and Debug the Test Case](https://docs.katalon.com/katalon-studio/tutorials/webui-analyze-test-case-execution-logs-and-resolve-errors.html#analyze-test-execution-logs-in-log-viewer).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-View-results-in-log-viewer.png" width="70%" alt="Oservice results in the log Viewer">

    > Notes:
    > * You can view test results in the **Result** tab at the test suite or test suite collection level. The test results can be Passed, Failed, Error, or Incomplete. To learn more about the test status, you can refer in this document: [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html#view-execution-log).
    > * After executing test suites or test suite collections, you can view your reports and details in `<your-project-folder>/Reports`. Katalon Studio also supports exporting test reports into different formats, such as HTML, CSV, PDF, and JUnit.
    > * For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

## See also

* [Create test cases using Record & Playback](https://docs.katalon.com/katalon-studio/docs/create_test_case_using_record_playback.html#record-test-with-the-record-web-function)

