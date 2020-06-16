---
title: "Test Suite" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/test-suite.html 
redirect_from:
    - "/katalon-studio/docs/create-test-suite/"
    - "/katalon-studio/docs/design-a-test-suite.html"
    - "/display/KD/Design+a+Test+Suite/"
    - "/display/KD/Design%20a%20Test%20Suite/"
    - "/x/mAvR/"
    - "/katalon-studio/docs/design-a-test-suite/"
    - "/katalon-studio/docs/dynamic-test-suite.html"
    - "/katalon-studio/docs/dynamic-querying-test-suite/"
    - "/katalon-studio/docs/dynamic+querying+test+suite/"
    - "/katalon-studio/docs/dynamic%20querying%20test%20suite/"
description: 
---
A test suite is a collection of multiple different or duplicate test cases.

## Create a new Test Suite

To create a new Test Suite, do as follows:

1. From the menu bar, select **File > New > Test Suite**
  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/test-suite-1.png)

2. Fill in the name of the test suite and the description (optional).

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/New-test-suite-window.png)

3. Click **OK** when you are done.

Here is another way to create a new Test Suite. In a Test Case, click  **Add to test suite** button after you have finished creating a test case.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/Test-suite-2.png)

You can choose to add that test case to an **existing** or a **new** test suite.

## Modify Execution Information

You can specify additional configurations for test suite execution by expanding the **Execution Information** section, as below:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-2-15-143A493A29.png)

### Implicit timeout

In **Implicit timeout**, you can decide the timeout period that Katalon waits for a page to be loaded by choosing one of the following options:
<ul>
   <li><strong>Use default</strong>: Use the predefined default value</li>
   <li><strong>User define</strong>: Use the specified value (in seconds)</li>
</ul>

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-2-15-143A563A48.png">

### Retry

You can configure when and how many times Katalon retries an execution of a Test Suite until the Test Suite passes successfully.

**From version 7.6 onwards**

> To significantly shorten the execution time, Katalon Studio supports retrying failed test execution **immediately**.

Select one of the following options to decide when and which execution Katalon Studio will retry:

* **failed executions immediately** (only available for Katalon Studio Enterprise users): Retry a failed execution of a test case or test data immediately.
* **all executions**: Retry all executions when the Test Suite fails.
* **failed executions only**: Retry only failed executions when the Test Suite fails.

**From version 7.6 backwards**

You can opt to retry only <strong>failed</strong> test cases and/or <strong>failed</strong> test data.

> Retrying **Failed Test Data Only** is available for **Katalon Studio Enterprise** users from version **7.5+**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/retry-750.png">

### Mail Recipients

You can add a list of recipients who will receive execution reports via email once the test suite finishes its execution.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-2-15-153A123A46.png">

There's also another list of recipients who will receive all the reports from Katalon by default. Refer to [Emails Settings](https://docs.katalon.com/katalon-studio/docs/execution-settings.html#emails-settings) for more details.

## Manage Test Case List

There are several ways to add Test Cases into Test Suites. You can drag and drop the Test Case into Test Suites or using the Test Suite editor to manually add the test case.

> Test Cases can be duplicated in the same Test Suite.

Open a test suite, then select the option to add **Add Test Case** from the command toolbar.  
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-2-15-143A333A40.png)

All test cases in Katalon Studio are displayed in the **Test Case Browser** dialog for you to select your preferred options. The selected test cases are added to the test case list accordingly.  

> The checkbox at the end of the test case row is checked by default. It means that the test case is executed when you run a test suite.

## Dynamic Test Suite (Dynamic Test Cases List)

**Dynamic Test Suite** is a test suite in which a collection of multiple test cases are added to NOT in a manual way but via a [search query](https://docs.katalon.com/katalon-studio/docs/search.html). This feature only works when you have already installed the plugin that defines the querying syntax. In case there is no installed plugin, the Query Provider is set to “No query provider available.” by default.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-querying-test-suite/dynamic-ts.png" width="1041" height="289">

Currently, there are three plugins from Katalon Store, which enable this feature by providing query search function and returning any matched test cases or test suites of the query statement.

* [Basic Search For Dynamic Test Suite](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite).
* [Test Case Management with Tags](https://store.katalon.com/product/6/Test-Case-Management-with-Tags). [Learn more](https://store.katalon.com/product/13/TestRail-Integration).
* [TestRail Integration](https://store.katalon.com/product/13/TestRail-Integration). [Learn more](https://docs.katalon.com/katalon-studio/docs/testrail-integration.html).

After installing one of those plugins, go to Katalon Studio and click **Reload Plugins**. [Learn more about how to reload plugins](https://docs.katalon.com/katalon-store/docs/user/access-store-in-KS.html#reload-plugins).

**Query Provider**: The query syntax standard of a plugin that is currently applied. For example, when you successfully install the *Basic Search For Dynamic Test Suite* plugin, the query syntax standard becomes "Built-in".

**Query**: This search box allows you to input the query syntax manually. For example,
`id=(Test Cases/Simple Examples/Katalon Shop/Custom-keyword samples/Order and check out a single product)`.

**Query Builder** provides a convenient way to create and run a query in Katalon Studio.

- **Id**: to search by the exact IDs of a test artifact.
- **Name**: to search by the name of a test artifact.
- **Tag**: to search by the tag linked to test artifacts.
- **Comment**: to search by the comments attached to test artifacts.
- **Description**: to search by the description associated with test artifacts.

*Note*: Search criteria are applied to all test artifacts, including test case, test suite, folder, and etc.

**Preview**: View the results after having the searching query.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-querying-test-suite/result.png" width="1039" height="346">

## Execute a Test Suite

Open a test case/test suite, then select an environment to run the test case from **Run** command of the main toolbar.

> If you click on the **Run** button, the test case is executed using the default browser defined in [Execution Settings](/display/KD/Execution+Settings).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/environment.png" width=310>

* **Browsers**: Select one of the supported browsers, including Chrome, Firefox, IE (for Windows only), Safari, or Edge Chromium, Chrome (headless), and Firefox (headless).
* **Mobile Devices**: Select one of the listed devices (Android or iOS).

  Before executing your test, check if you have set up the environment for mobile testing for <a href="/display/KD/Mobile+on+Windows">Windows</a> or for <a href="/display/KD/Mobile+on+macOS">macOS</a>.

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2018-1-26-183A543A41.png">

  > Troubleshooting
  >
  > If there is no device listed, please make sure the Developer Mode on the phone is turned on, try to unplug, and reconnect several times until you are prompted to accept/trust this device.
  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2018-8-2-153A313A52.png">

* **Windows**: Select this option if you are executing tests on a desktop application.
* **Remote**: Make sure you have set up the default configuration for the remote environment in project settings. Refer to&nbsp;<a href="/display/KD/Introduction+to+Desired+Capabilities">Introduction to Desired Capabilities</a>&nbsp;for more details.
* **Custom**: Make sure you have set up the default configuration for the remote environment in project settings. Refer to&nbsp;<a class="external-link" href="/x/cgFO#ExecutionSettings-CustomExecution" rel="nofollow">Custom Execution</a>&nbsp;for more details. When you have set up your custom environment, select it from the drop-down list.

The Job Progress is triggered automatically to show the progress while your test case/test suite is being executed.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2017-6-30-203A543A25.png)

> You can also [execute the test case using console mode](/display/KD/Console+Mode+Execution).
