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

Katalon Studio allows you to run the entire test suite or an individual test case. Before executing a test case or a test suite, keep in mind the [supported execution environments](/display/KD/Supported+Environments) by Katalon Studio.

Open a test case/test suite, and select the environment to run the test case from **Run** command of the main toolbar. You can also [execute the test case using console mode](/display/KD/Console+Mode+Execution).

> If you click on the **Run** button, the test case will be executed using the default browser defined in [Execution Settings](/display/KD/Execution+Settings).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/run.png" width=320>

### Test Environments

* **Browsers**: Select to execute your test on one of the supported browsers (Chrome, Firefox, IE, Safari, Edge)
* **Mobile Browsers**: Select to execute your test on one of the supported devices (Android, iOS)
* **Mobile**: Before executing your test, check if you have set up the environment for mobile testing for <a href="/display/KD/Mobile+on+Windows">Windows</a> or for <a href="/display/KD/Mobile+on+macOS">macOS</a>. Select your device among those listed in Katalon Studio.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2018-1-26-183A543A41.png">

   > Troubleshooting
   >
   > If there is no device listed, please make sure the Developer Mode on the phone is turned on, try to unplug, and reconnect several times until you are prompted to accept/trust this device.
   >
   > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/image2018-8-2-153A313A52.png">

* **Remote**: Make sure you have set up a default configuration for the remote environment in project settings. Refer to&nbsp;<a href="/display/KD/Introduction+to+Desired+Capabilities">Introduction to Desired Capabilities</a>&nbsp;for more details.
* **Custom**: Make sure you have set up a default configuration for the remote environment in project settings. Refer to&nbsp;<a class="external-link" href="/x/cgFO#ExecutionSettings-CustomExecution" rel="nofollow">Custom Execution</a>&nbsp;for more details. When you have set up your custom environment, select it from the drop-down list.

### Job Progress

The **Job Progress** is triggered automatically to show the progress while your test case/test suite is being executed.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/progress.png">

### Troubleshooting

Some factors can affect your execution:

* [Failure Handling](https://docs.katalon.com/katalon-studio/docs/failure-handling.html)
* [Test Listeners](https://docs.katalon.com/katalon-studio/docs/fixtures-listeners.html#test-listeners-test-hooks)
* [Setup/Teardown Test Case/Suite](https://docs.katalon.com/katalon-studio/docs/fixtures-listeners.html)

You can also refer to this [document](https://docs.katalon.com/katalon-studio/docs/troubleshoot-common-execution-exceptions-web-test.html) for troubleshooting issues relating to web test execution.

## Debug a test case

Creating automation test cases is a repetitive task that requires a lot of editing and re-running test cases. In many automation tools, when a test case fails and you make certain changes to the script, you usually have to execute the whole script all over again to make sure the test is executed as expected.

To save your precious time from tedious repetitive re-running all unnecessary steps for debugging and to make debugging easier, Katalon Studio provides the following utilities:

* Debug: Run from here
* Debug: Enable/Disable steps
* Debug mode
* Debug from here

**Requirements**

* An active Katalon Studio Enterprise license
* Katalon Studio version 7.0+

### Debug: Run from here

With this feature, you can resume the existing execution quickly. Katalon Studio currently supports **Run from here** with **Chrome, Firefox, and Edge Chromium** (Edge Chromium is supported from version 7.3.0+) only. To use it, from the [Manual view](/display/KD/Manual+View) of a test case:

1. Start a browser with the `Open Browser` step, or you must have a currently running browser
2. Make sure this browser's session is NOT terminated when the execution finishes (Go to **Project/Settings/Execution** and uncheck the **Terminate...** options in **Post-Execution Options** based on your testing needs)
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/post-execution.png" width=85%>

3. In the Manual view of the test case, right-click on a step, select **Run from here** and select one of the **currently running** browser instances to execute your test.

   > If there are no running browser instances that are previously launched in Katalon Studio, **Run from here** is disabled.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/debug-from-here.png" width=85%>

### Debug: Enable/Disable steps

Katalon Studio allows you to enable/disable one or more test steps before executing the test case to skip unwanted steps during execution. You can use the provided keyboard shortcuts to perform the actions.

* For Windows:  **Ctrl+D** (disable) and **Ctrl+E** (enable) on selected steps.
* For macOS: **command+/** (disable) and **option+command+/**

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/enable-disable.png" width=85%>

### Debug mode

The Debug mode is designed to make debugging easy to use, allowing investigating the root causes more quickly. The following steps present how to debug a test case:

1. Open a test case and switch to the **Script** view.
   
   ![Script view Katalon Studio](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Script-view.png)

2. Double-click on the leftmost side of the script editor to mark a breakpoint. A breakpoint is where Katalon Studio pauses the test execution for you to start debugging.
   
   ![mark a breakpoint for the step](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/mark-a-breakpoint.png)

3. Choose a browser for **Debug** from the main toolbar.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/debug-browser.png" width=439>

4. Confirm (select **Yes**) when being asked to display the **Debug** perspective.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/confirm-perspective.png" width=514 >

5. The **Debug** perspective provides convenient options for debugging purposes. You can:

   * Navigate execution using commands from the debug toolbar
   
   ![debug toolbar](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Navigate-execution.png)

   Where:

   | Command | Description |
   | --- | --- |
   |  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Resume-debugging.png) | Resume debugging |
   |  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Suspend-debugging.png) | Suspend debugging |
   |  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Terminate-debugging.png) | Terminate debugging |
   |  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Disconnect.png) | Disconnect |
   |  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Step-into-current-code-block.png) | Step into the current code block |
   |  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Step-over-current-code-block.png) | Step over the current code block |
   |  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Return-from-current-code-block.png) | Return from the current code block |
   |  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Run-to-specific-line.png) | Run to a specific line |

   * Track values of variables using Watch utilities.**
   
   ![Watch utilities](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Watch-utilities.png)
   
   Where:

   | View | Description |
   | --- | --- |
   | Variables | You can view all variables associated with the current debugged action using Variables View, which is similar to Variables View in Eclipse. Refer to this [guide](http://help.eclipse.org/luna/index.jsp?topic=%2Forg.eclipse.jdt.doc.user%2Freference%2Fviews%2Fexpressions%2Fref-expressions_view.htm) for more details. |
   | Breakpoints | You can view all breakpoints using Breakpoints View, which is similar to Breakpoints View in Eclipse. Refer to this [guide](http://help.eclipse.org/luna/index.jsp?topic=%2Forg.eclipse.jdt.doc.user%2Freference%2Fviews%2Fexpressions%2Fref-expressions_view.htm) for more details. |
   | Expressions | You can inspect data using Expressions View, which is similar to Expressions View in Eclipse. Refer to this [guide](http://help.eclipse.org/luna/index.jsp?topic=%2Forg.eclipse.jdt.doc.user%2Freference%2Fviews%2Fexpressions%2Fref-expressions_view.htm) for more details. |

### Debug from here

From version **7.5.5**, Katalon Studio provides **Debug from here** with **Chrome, Firefox, and Edge Chromium**. To use it, do as follows:

1. Start a browser with the `Open Browser` step, or you must have a currently running browser
2. Make sure this browser's session is NOT terminated when the execution finishes (Go to **Project/Settings/Execution** and uncheck the **Terminate...** options in **Post-Execution Options** based on your testing needs)

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/post-execution.png" width=85%>

3. Open a test case in its **Script** view and double-click on the leftmost side of the script editor to mark a breakpoint. A breakpoint is where Katalon Studio pauses the test execution for you to debug.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/breakpoint.png" width=85%>

4. Switch to the test case's **Manual** view, right-click on a step, select **Debug from here** and select one of the **currently running** browser instances to execute your test.

   > If there are no running browser instances that are previously launched in Katalon Studio, **Debug from here...** is disabled.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/debug-from-here.png" width=85%>

## Read third-party libraries source code

> From version 7.9.0 onwards, **Decompile class file for debugging** is available for usage. [Learn more](https://docs.katalon.com/katalon-studio/docs/execute-a-test-case-or-a-test-suite.html#decompile-class-file-for-debugging)

Katalon Studio supports reading source code from third-party libraries for debugging. To conduct, follow one of the below utilities:

- Attach source code for debugging
- Decompile class file for debugging

**Requirements**

* Attach source code: Katalon Studio version 7.0+
* Decompile class file: Katalon Studio version 7.9+

### Attach Source Code for debugging

> This is the default feature provided by Eclipse.

From Katalon Studio version 7.0.0, when writing a script or debugging, you can view and interact with the implementation of those components compressed in the `com.kms.katalon.core*` packages, including:

* `com.kms.katalon.core`
* `com.kms.katalon.core.cucumber`
* `com.kms.katalon.core.mobile`
* `com.kms.katalon.core.webservice`
* `com.kms.katalon.core.webui`
* `com.kms.katalon.core.windows`

You can also go to the source code where you set a breakpoint for debugging test scripts.

### Decompile Class File for debugging

From Katalon Studio version 7.9.0, Katalon supports debugging **class file without source code** directly. On debugging a class file, Katalon will find, download, and attach the source code automatically for you. You don't have to perform these steps manually like in the previous versions of Katalon.

   <img alt="decompiler-introduction" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/decompiler-introduction.png" width=85%>

In case Katalon fails to find and attach the source code (e.g. It cannot find the source jar anywhere on the Internet,...), it will decompile the class file and show the decompiled source. Katalon support various algorithms for decompiling, including **Jad, JD, FernFlower, CFR, Procyon**.

#### How to enable/disable the decompiler feature?
Katalon will enable this feature by default. You can double-check by:
1. Go to Windows > Preferences (or Katalon Studio > Preferences on MacOS)
2. Select General > Editors > File Associations
3. For "\*.class" and "\*.class without source": "Katalon Class Decompiler Viewer" is selected by default. In case you want to switch back to the default class file viewer in previous versions, please choose "Class File Viewer" instead.

#### How to configure the decompiler feature?
1. Go to Windows > Preferences (or Katalon Studio > Preferences on MacOS)
2. Select Java > Decompiler
   
   <img alt="decompiler-introduction" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execute-a-test-case-or-a-test-suite/decompiler-config.png" width=85%>
