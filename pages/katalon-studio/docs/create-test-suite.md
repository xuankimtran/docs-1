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

### From menu

The most simple way is to go to File > New > Test Suite.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/test-suite-1.png)

Fill in the name of the test suite and the description (optional).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/New-test-suite-window.png)

### From a Test Case

Here's another way to create a test suite: Navigate to the **Add to test suite** button after you have finished scripting a test case.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/create-test-suite/Test-suite-2.png)

There are two options to add test cases:
- Add to an existing test suite (for you to locate the test cases in an existing test suite)
- Add to a new test suite (for you to locate the test cases in a new test suite)

## Modify Execution Information

You can manage additional configurations for test suite execution by expanding the **Execution Information** section, as below:

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-2-15-143A493A29.png)

<table>
   <thead>
      <tr>
         <th>Field</th>
         <th>Description</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>
            <p>Page load timeout:</p>
            <p>&nbsp;<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-2-15-143A563A48.png"></p>
         </td>
         <td>
            <p>The timeout period allowed to wait for a page to be loaded. You can choose among the following options:</p>
            <ul>
               <li><strong>Use default</strong>: the default value defined will be used. Refer to <a href="/pages/viewpage.action?pageId=3179873">Execution Preferences (Version 5.0 and below)</a> for more details.</li>
               <li><strong>User-defined value</strong>: the entered timeout value (in seconds) will be used.</li>
            </ul>
            <p>&nbsp;</p>
         </td>
      </tr>
      <tr>
         <td>
            <p>Retry:</p>
            <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/retry.png"></p>
         </td>
         <td>
            <p>The <strong>maximum</strong> number of retries for execution until it is successfully passed. You can opt to retry only <strong>failed</strong> test cases and/or <strong>failed</strong> test data. Please note that Retrying Failed Test Data Only is supported in <strong>version 7.5+</strong>.</p>
            <p>&nbsp;</p>
         </td>
      </tr>
      <tr>
         <td>
            <p>Mail Recipients</p>
            <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-2-15-153A123A46.png"></p>
         </td>
         <td>
            <p>The list of recipients who would receive the execution report once the test suite finishes its execution.</p>
            <blockquote class="important">
               <p>There's also another list of recipients who will be receiving all the reports from Katalon by default. Refer to <a href="/display/KD/Emails+Settings">Emails Settings</a> for more details.</p>
            </blockquote>
         </td>
      </tr>
      <tr>
         <td>
            <p>Last run:</p>
            <p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-2-15-153A143A55.png"></p>
         </td>
         <td>
            <p>The datetime when the test suite was last executed. You can quickly open the report of this execution by clicking on the <strong>Last run</strong> hyperlink.</p>
            <p>&nbsp;</p>
         </td>
      </tr>
   </tbody>
</table>

## Manage Test Case List

There are several ways to add Test Cases into Test Suites. You can drag and drop the Test Case into Test Suites or using the Test Suite editor to manually add the test case.

>_Note: Test Cases can be duplicated in the same Test Suite._

Open a test suite, then select option to add **Add Test Case** from command toolbar.  
![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-2-15-143A333A40.png)

All test cases in Katalon Studio are displayed in the **Test Case Browser** dialog for you to select your preferred options. The selected test cases will be added in the test case list accordingly.  


> The checkbox at the end of test case row is checked by default. It means that the test case will be executed when running a test suite.

## Dynamic Test Suite (Dynamic Test Cases List)

**Dynamic Test Suite** is a test suite in which a collection of multiple test cases are added to NOT in a manual way but via [search query](https://docs.katalon.com/katalon-studio/docs/search.html). This feature only works when you have already installed the plugin that defines the querying syntax. In case there is no installed plugin, the Query Provider is set to “No query provider available.” by default.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-querying-test-suite/dynamic-ts.png" width="1041" height="289">

Currently, there are three plugins from Katalon Store, which enable this feature by providing query search function and returning any matched test cases or test suites of the query statement.

* [Basic Search For Dynamic Test Suite](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite).
* [Test Case Management with Tags](https://store.katalon.com/product/6/Test-Case-Management-with-Tags). [Learn more](https://store.katalon.com/product/13/TestRail-Integration).
* [TestRail Integration](https://store.katalon.com/product/13/TestRail-Integration). [Learn more](https://docs.katalon.com/katalon-studio/docs/testrail-integration.html).

After installing one of those plugins, go to Katalon Studio and click **Reload Plugins**. [Learn more about how to reload plugins](https://docs.katalon.com/katalon-store/docs/user/access-store-in-KS.html#reload-plugins).

**Query Provider**: the query syntax standard of a plugin that is currently applied. For example, when you successfully install the *Basic Search For Dynamic Test Suite* plugin, the query syntax standard becomes "Built-in".

**Query**: this search box allows you to input the query syntax manually. For example:
`id=(Test Cases/Simple Examples/Katalon Shop/Custom-keyword samples/Order and check out a single product)`.

**Query Builder** provides a convenient way to create and run query in Katalon Studio.

- **Id**: to search by the exact IDs of a test artifact.
- **Name**: to search by the name of a test artifact.
- **Tag**: to search by the tag linked to test artifacts.
- **Comment**: to search by the comments attached to test artifacts.
- **Description**: to search by the description associated with test artifacts.

*Note*: Search criteria are applied to all test artifacts including test case, test suite, folder, and etc.

**Preview**: to view the results after having the searching query.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-querying-test-suite/result.png" width="1039" height="346">

## Execute a Test Suite

Open a test case/test suite, then select the environment to run the test case from **Run** command of the main toolbar. You can also [execute the test case using console mode](/display/KD/Console+Mode+Execution). 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2018-8-2-153A203A44.png)

> If you simply click on the **Run** button, the test case will be executed using the default browser defined in [Execution Settings](/display/KD/Execution+Settings).

<table><thead><tr><th>Execution Environment</th><th>Execution Guide</th></tr></thead><tbody><tr><td><strong>Browsers</strong></td><td>Simply select to execute your test on one of the supported browsers (Chrome, Firefox, IE, Safari, Edge)</td></tr><tr><td><strong>Mobile Browsers</strong></td><td>Simply select to execute your test on one of the supported devices (Android, iOS)</td></tr><tr><td><strong>Mobile</strong></td><td><p>Before executing your test, check if you have set up the environment for mobile testing for <a href="/display/KD/Mobile+on+Windows">Windows</a> or for <a href="/display/KD/Mobile+on+macOS">macOS</a>. Select your device among those listed in Katalon Studio.</p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2018-1-26-183A543A41.png"><p>&nbsp;</p><blockquote class="important"><p class="title">Troubleshooting</p><p>If there is no device listed, please make sure the Developer Mode on the phone is turned on, try to unplug and reconnect several times until you are prompted for accepting/trusting this device.</p><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2018-8-2-153A313A52.png"></p></blockquote></td></tr><tr><td><strong>Remote</strong></td><td>Make sure you have set up default configuration for the remote environment in project settings. Refer to&nbsp;<a href="/display/KD/Introduction+to+Desired+Capabilities">Introduction to Desired Capabilities</a>&nbsp;for more details.</td></tr><tr><td><strong>Custom</strong></td><td>Make sure you have set up default configuration for the remote environment in project settings. Refer to&nbsp;<a class="external-link" href="/x/cgFO#ExecutionSettings-CustomExecution" rel="nofollow">Custom Execution</a>&nbsp;for more details. When you have set up your custom environment, simply select it from the drop-down list.</td></tr></tbody></table>

The Job Progress will be triggered automatically to show the progress while your test case/test suite is being executed.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2017-6-30-203A543A25.png)