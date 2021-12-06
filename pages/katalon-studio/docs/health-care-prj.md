---
title: "Health Care Sample Project"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/health-care-prj.html
---

This sample demonstrates fundamental WebUI testing in Katalon Studio. The application under test (AUT) is the CURA Healthcare Service website: `https://katalon-demo-cura.herokuapp.com/`. You can learn more about WebUI Testing in this document: [Introduction to Web Testing](https://docs.katalon.com/katalon-studio/docs/introduction-to-web-testing.html#before-you-begin).
## Open Healthcare Sample Project

To open Healthcare sample project, in Katalon Studio, go to **File > New Sample Project > Sample Web UI Tests Project (Healthcare)**.

<img src="url" width="70%" alt="Open Healthcare sample in Studio">

Alternatively, you can download the Healthcare sample project from our Github repository here: [Healthcare Sample](https://github.com/katalon-studio-samples/healthcare-tests).
## Healthcare Sample Project components
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

### Test Cases

To get access to the main test cases in this project, in the **Test Explorer** panel, go to **Test Cases > Main Test Cases**.
There are three test cases for different purposes: 

1. **TC1_Verify Successful Login** is to verify if a person can log in successfully with a valid account. The flow in this test case is as follows:

    - Go to the CURA Healthcare Service website: `https://katalon-demo-cura.herokuapp.com/`. Here, we use the `G_SiteURL` global variables.
    - Click the **Make Appointment** button.
    - Fill in the **Username** and **Password**. Here, we set the value type of **Username** and **Password** as **Variable**. You can change the **Username** and **Password** value in the **Variable** tab. To learn more about test case variables, you can refer to this document: [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html).
    - Click the **Login** button.
    - Verify if the account is logged in successfully. Here, we use the `G_Timeout` variables. If the page **Appointment** appears within 10 seconds, the login is successful.
    - Close browser.

2. **TC2_Verify Successful Appointment** is to verify if that person can successfully make an appointment after logging in. The flow in this test case is as follows:

    - Go to the CURA Healthcare Service website: `https://katalon-demo-cura.herokuapp.com/` and login. Here, to speed up the login process, we call the test case from **Common Test Cases/Login**. To learn more about calling test cases, you can refer to this document: [Call Test Cases](https://docs.katalon.com/katalon-studio/docs/call-test-case.html#call-test-case-in-manual-view).
    - To make an appointment, fill in the valid value for **Facility**, **Healthcare Program** and **Visit Date**. Click the **Book Appointment** button.
    - Verify if the appointment is successfully confirmed. Here, we consider a appointment is successfully confirmed when the **Appointment Confirmation** text appears.
    - Verify if the booking information is matched with the confirmation information.
    - Take screenshot. 

    > Notes:
    > * You can only see the screenshot after executing a test suite. See below: [Test Suite and Test Suite Collection](https://docs.katalon.com/katalon-studio/docs/health-care-prj.html#test-suite-and-test-suite-collection).

3. **TC3_Visual Testing Example** utilizes the **Visual Testing** feature in Katalon TestOps to compare images captured during test executions. You can see the instructions for this feature here: [Visual Testing in Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/ks-visual-testing.html#set-up-visual-testing).

To execute a test case in the sample project:

- Select the Test Case you want to execute.
- Click the arrow icon right next to the **Run** button. In the drop-down list, select your preferred browser. To execute it with the default browser, Windows users can press the key combination of **Ctrl + Shift + A**; Mac users press **Command+Shift+A**.
- Observe the test result on Log Viewer.

### Test Suite and Test Suite Collection

The sample test suite is a combination of both test cases whilst the sample test suite collection is a combination of the same test suite with different testing environments. To be more specific, the test suite is executed in Firefox and Chrome.

To execute a test suite or a test suite collection in the sample project:

- Select the Test Suite or the Test Suite Collection you want to execute.
- Click the arrow icon right next to the **Run** button. In the drop-down list, select your preferred browser. To execute it with the default browser, Windows users can press the key combination of **Ctrl + Shift + A**; Mac users press **Command+Shift+A**.
- Observe the test result on Log Viewer.

> In the test suite or test suite collection level, you can view test results in the **Result** tab. The test results can be Passed, Failed, Error or Incomplete.

> After executing tests, you can view your reports and details in [Katalon TestOps](https://analytics.katalon.com).
>
> - [View Test Reports](https://docs.katalon.com/katalon-analytics/docs/project-management-view-reports.html)
> - [View Test Execution, Test Suite and Test Suite Collection Details](https://docs.katalon.com/katalon-analytics/docs/project-management-view-details.html)

### Custom Keywords

The sample test cases can call [Custom Keywords](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html). The syntax of a custom keyword in Katalon Studio should be as follows:

`@Keyword`\
` def static {return type}{functionname}(parameters,parameters...){`\
`...`\
`}`

Example:

```groovy
/**
 * Get all rows of HTML table
 * @param table Katalon test object represent for HTML table
 * @param outerTagName outer tag name of TR tag, usually is TBODY
 * @return All rows inside HTML table
 */
@Keyword
def List<WebElement> getHtmlTableRows(TestObject table, String outerTagName) {
    WebElement mailList = WebUiBuiltInKeywords.findWebElement(table)
    List<WebElement> selectedRows = mailList.findElements(By.xpath("./" + outerTagName + "/tr"))
    return selectedRows
}
```
