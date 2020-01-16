---
title: "Execute and Debug a Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/execute-a-test-case-or-a-test-suite.html
redirect_from:
    - "/display/KD/Execute+a+Test+Case+or+a+Test+Suite/"
    - "/display/KD/Execute%20a%20Test%20Case%20or%20a%20Test%20Suite/"
    - "/x/GAvR/"
    - "/katalon-studio/docs/execute-a-test-case-or-a-test-suite/"
    - "/display/KD/Execute+a+test+suite/"
    - "/katalon-studio/tutorials/executing_test_case.html"
    - "/display/KD/Execute+a+test+case/"
    - "/display/KD/Execute%20a%20test%20case/"
    - "/x/ugAM/"
    - "/katalon-studio/docs/execute-a-test-case/"
    - "/katalon-studio/docs/execute-a-test-case.html"
    - "/display/KD/Execute+test+from+specific+step/"
    - "/katalon-studio/tutorials/execute_debug_certain_steps.html"
    - "/display/KD/Debug+Automation+Test/"
    - "/display/KD/Debug%20Automation%20Test/"
    - "/x/C4Ew/"
    - "/katalon-studio/docs/debug-automation-test/"
    - "/katalon-studio/docs/debug-automation-test.html"
    - "/katalon-studio/tutorials/debugging_test_case.html"
    - "/katalon-studio/docs/debugging_test_case.html/"
    - "/katalon-studio/docs/execute_debug_certain_steps.html"
description:
---
## Execute a Test Case

Katalon Studio allows you to run the entire test suite, or an individual test case. Before executing a test case or a test suite, keep in mind the [supported execution environments](/display/KD/Supported+Environments) by Katalon Studio.

Open a test case/test suite, then select the environment to run the test case from **Run** command of the main toolbar. You can also [execute the test case using console mode](/display/KD/Console+Mode+Execution).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2018-8-2-153A203A44.png)

> If you simply click on the **Run** button, the test case will be executed using the default browser defined in [Execution Settings](/display/KD/Execution+Settings).

### Execution Environments and Instructions

* **Browsers**: Simply select to execute your test on one of the supported browsers (Chrome, Firefox, IE, Safari, Edge)
* **Mobile Browsers**: Simply select to execute your test on one of the supported devices (Android, iOS)
* **Mobile**: Before executing your test, check if you have set up the environment for mobile testing for <a href="/display/KD/Mobile+on+Windows">Windows</a> or for <a href="/display/KD/Mobile+on+macOS">macOS</a>. Select your device among those listed in Katalon Studio.

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2018-1-26-183A543A41.png">

    > Troubleshooting
    >
    >If there is no device listed, please make sure the Developer Mode on the phone is turned on, try to unplug and reconnect several times until you are prompted for accepting/trusting this device.
    >
    > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2018-8-2-153A313A52.png">

* **Remote**: Make sure you have set up default configuration for the remote environment in project settings. Refer to&nbsp;<a href="/display/KD/Introduction+to+Desired+Capabilities">Introduction to Desired Capabilities</a>&nbsp;for more details.

* **Custom**: Make sure you have set up default configuration for the remote environment in project settings. Refer to&nbsp;<a class="external-link" href="/x/cgFO#ExecutionSettings-CustomExecution" rel="nofollow">Custom Execution</a>&nbsp;for more details. When you have set up your custom environment, simply select it from the drop-down list.

### Job Progress

The Job Progress will be triggered automatically to show the progress while your test case/test suite is being executed.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2017-6-30-203A543A25.png)

### Troubleshooting

Some factors can affect your execution:

* [Failure Handling](/display/KD/Failure+Handling)
* [Test Listeners](https://docs.katalon.com/katalon-studio/docs/test-listeners-test-hooks.html)  
* [Setup/Teardown Test Case/Suite](https://docs.katalon.com/katalon-studio/docs/setupteardown-for-test-suite-and-test-case.html)

You can also refer to this [guide](/display/KD/Troubleshooting+common+issues+related+to+interacting+with+an+element) to troubleshoot problems relating to test execution.

## Debug a test case

### Debug: Execute from a Selected Step

Creating automation test cases is a repetitive task that requires a lot of editing and rerunning test cases. In many automation tools, when the test case fails and users makes certain changes to the script, they usually have to execute the whole script all over again to make sure the test is executed as expected. To save users from the trouble of having to re-run all unnecessary steps, Katalon Studio provides two ways so that users can start the test at their preferred steps:

* Debug: Execute from selected step
* Enable/Disable steps

From the [Manual view](/display/KD/Manual+View) of the test case:

1\. Start a browser in Katalon script using 'Open Browser' step. Else, you must have a current session running.

2. Ensure this browser's session is NOT terminated (Go to **Project > Settings > Executions > Post-Execution > Terminate...** options are unchecked based on your testing needs).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/post-execution.png" width="" height="">

3\. Right-click on one of the step you want to execute from, and execute the sesssion.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2017-8-18-113A343A23.png)

From the Manual view of the test case, right-click on a step and select **Execute from here…**. Once this option is selected, all **_currently running and supported Chrome instances_** are displayed so that you can select to run the script from the selected step.

If there is no running Chrome browser instances that are previously launched in Katalon Studio, **Execute from here...** is disabled.

### Enable/Disable steps

Katalon Studio also allows users to enable/disable one or more test steps before executing the test case as shown in the screenshot below. Using the shortcuts  **Ctrl + D** (disable) and **Ctrl + E** (enable) on selected steps, users can skip unwanted steps when executing the test case.

![Enable/Disable steps](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/execute_debug_certain_steps/Enable_Disable-steps.png)

As described above, users have two methods to specify steps to be executed. The first method allows users to quickly resume the existing execution, but it only supports Chrome sessions that are launched by Katalon Studio. On the other hand, the "enable/disable steps" method does not have this restriction but users may not be able to execute on specific context as wanted.

### Debug mode

Katalon Studio provides the capability for debugging test scripts. Its Debug mode is designed to make debugging easy to use, allowing quickly investigating the issues that cause failure for their automation tests.

The following steps present how to debug a test case:

1\. Open a test case and switch to the **Script** view.
![Script view Katalon Studio](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Script-view.png)

2\. Double-click on the leftmost side of the script editor to mark a breakpoint for the step from which you want to start debugging.
![mark a breakpoint for the step](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/mark-a-breakpoint.png)

3\. Choose the browser for **Debug** from the main toolbar.
![Choose the browser for Debugging test case](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/the-browser.png)

4\. Confirm (select **Yes**) when asked to show the **Debug** perspective.
![the Debug perspective.](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Debug-perspective.png)

5\. The **Debug** perspective provides convenient options for debugging purposes. You can:

**Navigate execution using commands from the debug toolbar.**
![debug toolbar](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Navigate-execution.png)

Where:

| Command | Description |
| --- | --- |
|  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Resume-debugging.png) | Resume debugging |
|  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Suspend-debugging.png) | Suspend debugging |
|  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Terminate-debugging.png) | Terminate debugging |
|  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Disconnect.png) | Disconnect |
|  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Step-into-current-code-block.png) | Step into current code block |
|  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Step-over-current-code-block.png) | Step over current code block |
|  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Return-from-current-code-block.png) | Return from current code block |
|  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Run-to-specific-line.png) | Run to specific line |

**Track values of variables using Watch utilities.**
![Watch utilities](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Watch-utilities.png)Where:

| View | Description |
| --- | --- |
| Variables | You can view all variables associated with the current debugged action using Variables View which is similar to Variables View in Eclipse. Refer to this [guide](http://help.eclipse.org/luna/index.jsp?topic=%2Forg.eclipse.jdt.doc.user%2Freference%2Fviews%2Fexpressions%2Fref-expressions_view.htm) for more details. |
| Breakpoints | You can view all breakpoints using Breakpoints View which is similar to Breakpoints View in Eclipse. Refer to this [guide](http://help.eclipse.org/luna/index.jsp?topic=%2Forg.eclipse.jdt.doc.user%2Freference%2Fviews%2Fexpressions%2Fref-expressions_view.htm) for more details. |
| Expressions | You can inspect data using Expressions View which is similar to Expressions View in Eclipse. Refer to this [guide](http://help.eclipse.org/luna/index.jsp?topic=%2Forg.eclipse.jdt.doc.user%2Freference%2Fviews%2Fexpressions%2Fref-expressions_view.htm) for more details. |

6\. Stop execution when you complete debugging.
Although the debugging mode in Katalon Studio is very similar to that of the popular Eclipse IDE, we manage to retain just enough function to keep the UI clean while providing all the required options to investigate issues when needed. If you have any suggestions or need any support, please send your request [here](https://www.katalon.com/#submit-ticket).

### Attach Source Code for debugging

Starting from **Katalon Studio version 7.0.0**, when writing a script or debugging, you can view and interact with the implementation of those components compressed in the `com.kms.katalon.core*` packages, including:

* `com.kms.katalon.core`
* `com.kms.katalon.core.cucumber`
* `com.kms.katalon.core.mobile`
* `com.kms.katalon.core.webservice`
* `com.kms.katalon.core.webui`
* `com.kms.katalon.core.windows`

You can also go to the source code where you set a breakpoint for debugging test scripts.