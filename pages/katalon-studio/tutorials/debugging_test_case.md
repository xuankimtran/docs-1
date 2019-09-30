---
title: "Debugging test case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/debugging_test_case.html
redirect_from:
    - "/display/KD/Debug+Automation+Test/"
    - "/display/KD/Debug%20Automation%20Test/"
    - "/x/C4Ew/"
    - "/katalon-studio/docs/debug-automation-test/"
    - "/katalon-studio/docs/debug-automation-test.html"
    - "/katalon-studio/tutorials/debugging_test_case.html"
description: "The debugging mode makes debugging easy to use, allowing users to quickly investigate the issues that cause failure for their automation tests."
---

## Debug a test case

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

## Attach Source Code for debugging

Starting from **Katalon Studio version 7.0.0**, when writing a script or debugging, you can view and interact with the implementation of those components compressed in the `com.kms.katalon.core*` packages, including:

* `com.kms.katalon.core`
* `com.kms.katalon.core.cucumber`
* `com.kms.katalon.core.mobile`
* `com.kms.katalon.core.webservice`
* `com.kms.katalon.core.webui`
* `com.kms.katalon.core.windows`

You can also go to the source code where you set a breakpoint for debugging test scripts.
