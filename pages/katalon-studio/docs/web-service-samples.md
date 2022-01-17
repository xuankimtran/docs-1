---
title: "Sample API/Web Service test project" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/web-service-samples.html 
---

This sample demonstrates fundamental API Testing with RESTful requests. The sample uses the following base URL: `https://sample-web-service-aut.herokuapp.com`. To learn more about API testing, you can refer to this document: [Introduction to API testing](https://docs.katalon.com/katalon-studio/docs/introduction_api_testing.html).
## Open the sample API test project

To open the API sample project, in Katalon Studio, go to **File > New Sample Project > Sample API Tests Project**.

<img src="url" width="70%" alt="Open API sample in Studio">

Alternatively, you can download the sample API test project from our Github repository: [Web Service tests](https://github.com/katalon-studio-samples/web-service-tests).
## Sample API project components
### Profiles

To open the execution profile, go to **Profiles > default**.

<img src="url" width="70%" alt="Default profile in the API sample">


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
    <td>baseURL</td>
    <td>https://sample-web-service-aut.herokuapp.com</td>
  </tr>
  <tr>
    <td>successCode</td>
    <td>200</td>
  </tr>
  <tr>
    <td>globalid</td>
    <td>0</td>
  </tr>
</tbody>
</table>

### RESTful requests

To access the sample RESTful requests in this project, in the **Test Explorer** panel, go to the **Object Repository** folder.

1. The **POST a new user** object:

<img src="url" width="70%" alt="Sample POST request">

**(1) Request method**

Katalon allows you to choose one of these following methods for your request test: GET, POST, PUT, DELETE, PATCH, HEAD, CONNECT, OPTIONS, TRACE. The method needs to match with the API endpoint to have a valid request. Here, we are creating a POST request to send the user information to the server to create an account. The server will return us with a new userID as a response.

**(2) Request URL**

Along with the request method, request URL is to tell the web server which API is utilized under test. Any mismatch between method and URL leads to an invalid request exception at runtime or wrong data response. For the POST request, we specify the API endpoint as follows: `${GlobalVariable.baseUrl}/api/users/json`, with the base URL is listed as a global variable, see above: [Profiles](https://docs.katalon.com/katalon-studio/docs/web-service-samples.html#profiles).

**(3) Authorization**

Authorization is an essential part of an API. It is used to get the correct data under permission (unless the data is public). To learn more about authorization, you can refer to this document: [Authorization](https://docs.katalon.com/katalon-studio/docs/authorization.html).

We don't specify any authorization for this POST request.

**(4) HTTP Header**

**(5) HTTP Body**


2. The **GET user by id** object:

<img src="url" width="70%" alt="Sample GET request">


### Custom keywords

You can use custom keywords in the test case. To learn more about custom keywords, you can refer to this document: [Introduction to custom keywords](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html). 

Katalon creates two custom keywords in this sample project. To see the custom keywords, in the **Test Explorer** panel, go to **Keywords > sample > Common.groovy**.

<img src="url" width="70%" alt="Custom keywords in the API project">

<details><summary> <code>sample.Common.createNewUser</code> </summary>

### Description

This keyword is to use the POST request to send the user information including username, password, age, gender, and avatar to the server to create an account, then extract the new user ID from the response.
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
    <td>age</td>
    <td>int</td>
    <td>Yes</td>
    <td>The age of the user</td>
  </tr>
  <tr>
    <td>username</td>
    <td>String</td>
    <td>Yes</td>
    <td>The username for the user account</td>
  </tr>
  <tr>
    <td>password</td>
    <td>String</td>
    <td>Yes</td>
    <td>The password for the user account</td>
  </tr>
  <tr>
    <td>gender</td>
    <td>String</td>
    <td>Yes</td>
    <td>The gender for the user</td>
  </tr>
  <tr>
    <td>expectedStatus</td>
    <td>int</td>
    <td>Yes</td>
    <td>The expected status code of the request</td>
  </tr>
</tbody>
</table>

</details>

<details><summary> <code>sample.Common.findUserById</code> </summary>

### Description

This keyword is to use the GET response to retrieve and verify the user information by the userID.
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
    <td>id </td>
    <td>int</td>
    <td>Yes</td>
    <td>The id of the new user</td>
  </tr>
  <tr>
    <td>age</td>
    <td>int</td>
    <td>Yes</td>
    <td>The age of the user</td>
  </tr>
  <tr>
    <td>username</td>
    <td>String</td>
    <td>Yes</td>
    <td>The username for the user account</td>
  </tr>
  <tr>
    <td>password</td>
    <td>String</td>
    <td>Yes</td>
    <td>The password for the user account</td>
  </tr>
  <tr>
    <td>gender</td>
    <td>String</td>
    <td>Yes</td>
    <td>The gender for the user</td>
  </tr>
  <tr>
    <td>expectedStatus</td>
    <td>int</td>
    <td>Yes</td>
    <td>The expected status code of the request</td>
  </tr>
</tbody>
</table>

</details>

### Test cases

To access the sample test cases in this project, in the **Test Explorer** panel, go to the **Test Cases** folder.

<img src="url" width="70%" alt="Test cases">

There are two test cases for different purposes: 

1. **Create a new user** uses the `sample.Common.createNewUser` keyword to send the user information including username, password, age, gender, and avatar to the server to create an account, then extract the new user ID from the response.

    <img src="url" width="70%" alt="">

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
      
2. **TC2_Verify Successful Appointment** is to verify if that person can successfully make an appointment after logging in. The flow in this test case is as follows:

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

3. **TC3_Visual Testing Example** utilizes the **Visual Testing** feature in Katalon TestOps to compare images captured during test executions. You can see the instructions for this feature here: [Visual Testing in Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/ks-visual-testing.html#set-up-visual-testing).
### Test suite and test suite collection

There are two test suites in this project. To access them, in the **Test Explorer** panel, go to **Test Suites**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-sample-test-suites.png" width="70%" alt="Main test suites">

1. **Healthcare-tests - TS_RegressionTest**: This sample test suite combines the three above test cases.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-Test-suites-regression.png" width="70%" alt="Healthcare-tests - TS_RegressionTest">

2. **Healthcare-tests - TS_RegressionTestCollection**: This sample test suite collection combines two **Healthcare-tests - TS_RegressionTest** test suites with different testing environments. In this project, we run the test suites with Firefox and Chrome.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-Test-suite-collection.png" width="70%" alt="Healthcare-tests - TS_RegressionTestCollection">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

## Execute selected test case or test suite/test suite collection

To execute a test case or a test suite/test suite collection in the sample project:

1. Select the test case/test suite/test suite collection you want to execute.
2. Click **Run** or press Ctrl + Shift + A (macOS: Cmd+Shift+A).

    You can choose different browsers to execute your test in the dropdown list next to **Run**. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-Sample-Run-with-different-browsers.png" width="30%" alt="Run the test case">

3. Observe the test result in the **Log Viewer** tab.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-View-results-in-log-viewer.png" width="70%" alt="Oservice results in the log Viewer">

    > Notes:
    > * You can view test results in the **Result** tab in the test suite or test suite collection level. The test results can be Passed, Failed, Error, or Incomplete.
    > * After executing test suites or test suite collections, you can view your reports and details in `<your-project-folder>/Reports`. Katalon Studio also supports exporting test reports into different formats, such as HTML, CSV, PDF, and JUnit.
    > * For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).
## See also

* [Create your first API test with Katalon Studio](hhttps://docs.katalon.com/katalon-studio/docs/create_first_api_test_katalon_studio.html#introduction)
* [Verification Snippets](https://docs.katalon.com/katalon-studio/docs/verification-snippets.html).

