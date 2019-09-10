---
title: "Health Care Project"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/health-care-prj.html
---
The Health care sample project is available [here](https://github.com/katalon-studio-samples/healthcare-tests).

This sample is to demonstrate very fundamental [web testing](https://docs.katalon.com/katalon-studio/docs/introduction-to-web-testing.html#before-you-begin) in Katalon Studio. The application under test (AUT) is the [CURA Healthcare Service website](https://katalon-demo-cura.herokuapp.com/).

## Profiles

In the [default profile](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html), you can create and save all [global variables](https://docs.katalon.com/katalon-studio/docs/global-variables.html). They can be used across Test Cases in your project.

## Test Cases

There are two test cases for different purposes in this project:

- Test Case 1 is to verify if a person can log in successfully with a valid account.
- Test Case 2 is to verify if that person can successfully make an appointment after logging in.

To execute a test case in the sample project:

- Select the Test Case you want to execute.
- Click the arrow icon right next to the **Run** button. In the drop-down list, select your preferred browser. To execute it with the default browser, Windows users can press the key combination of **Ctrl + Shift + A**; Mac users press **Command+Shift+A**.
- Observe the test result on Log Viewer.

## Test Suite and Test Suite Collection

The sample test suite is a combination of both test cases whilst the sample test suite collection is a combination of the same test suite with different testing environments. To be more specific, the test suite is executed in Firefox and Chrome.

To execute a test suite or a test suite collection in the sample project:

- Select the Test Suite or the Test Suite Collection you want to execute.
- Click the arrow icon right next to the **Run** button. In the drop-down list, select your preferred browser. To execute it with the default browser, Windows users can press the key combination of **Ctrl + Shift + A**; Mac users press **Command+Shift+A**.
- Observe the test result on Log Viewer.

> In the test suite or test suite collection level, you can view test results in the **Result** tab. The test results can be Passed, Failed, Error or Incomplete.

## Custom Keywords

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
