---
title: "Test Case Preferences" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/test-case-preferences.html 
redirect_from:
description: 
---

With Test Case preferences, you can define the default behaviors related to your test case design. This includes:

* Test Case Calling
* Default Open View
* Default Keyword Type
* Line-wrapping settings

To configure your Test Case preferences, go to **Katalon Studio > Preferences > Katalon > Test Case**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-preferences/test-case-preferences.png" width=100% alt="Test Case Preferences">

### Test Case Calling

The **Test Case Calling** option allows you to specify how Katalon Studio should behave when you call another test case as a test step. To learn more about this function, see [Call Test Case](https://docs.katalon.com/katalon-studio/docs/call-test-case.html).

For example, we call the `TC1_Verify Successful Login` test case, with two variables named `Username` and `Password`. Their variables are displayed in the image below:

<img src="https://github.com/katalon-studio/docs-images/raw/a5d0eb256e48bbfb94008ade2ddd43fd9856ede9/katalon-studio/docs/test-case-preferences/calling-example.png" alt="example" width="80%">

* **Generate variable with default value**: The called test case uses the default value of its variables.

  ``` groovy
  WebUI.callTestCase(findTestCase('Main Test Cases/TC1_Verify Successful Login'), [('Username') : 'John Doe', ('Password') : 'ThisIsNotAPassword'], 
      FailureHandling.STOP_ON_FAILURE)
  ```

* **Generate variable with the same name as the exposed variable of the called test case**: The called test case uses its variable names as variable values.

  ``` groovy
  WebUI.callTestCase(findTestCase('Main Test Cases/TC1_Verify Successful Login'), [('Username') : Username, ('Password') : Password], 
      FailureHandling.STOP_ON_FAILURE)
  ```

  * **Expose variables automatically after choosing the called test case**: At the **Variables** tab, all variables of the called test case are also added to the current test case.

To learn more about supported types of variables in Katalon Studio, refer to this document: [Variable Types](https://docs.katalon.com/katalon-studio/docs/variable-types.html#test-case-variables).

### Default Open View

By default, Katalon Studio opens your test case in the manual view. You can choose to always open your test case in the manual view or the script view.

### Default Keyword Type

* **Default Keyword**: Based on your frequently used types of testing, you can set the **Default Keyword Type** as WebUI, Mobile, Cucumber, Web Service, Windows, or TestNG. For example, you set the default keyword type as `WebUI`. In the test case editor, whenever you click **Add**, a new WebUI keyword is added as a new test step.

In each keyword type, you can also set a default keyword. For example, you set **Accept Alert** as the default keyword for the **WebUI** keyword type. In the test case editor, whenever you click **Add**, the **Accept Alert** is added as a new test step by default.

### Line-wrapping Settings

When you edit in script view, depending on how you want to view your scripts, you can enable/disable the line-wrapping to wrap up the code lines in customized maximum line width.

When switching from the manual mode to the script mode, you can also wrap the code lines by pressing a keyboard combination of **Command+Shift+F** for macOS or **Ctrl+Shift+F** for Windows and Linux.

* Line-wrapping disabled:

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-preferences/wrap.png" width=100% alt="Before the line-wrapping enabled">


* Line-wrapping enabled:

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-case-preferences/wrapped.png" width=100% alt="After the line-wrapping enabled">

**See also**:

- [Katalon Preferences](https://docs.katalon.com/katalon-studio/docs/katalon-studio-preferences.html)
- [Import Preferences](https://docs.katalon.com/katalon-studio/docs/import-preferences.html)
- [Proxy Preferences](https://docs.katalon.com/katalon-studio/docs/proxy-preferences.html)
- [Object Spy Preferences](https://docs.katalon.com/katalon-studio/docs/object-spy-preferences.html)