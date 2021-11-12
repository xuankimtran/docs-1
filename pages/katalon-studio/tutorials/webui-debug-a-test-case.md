---
title: "[WebUI] Debug a Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: 
description: 
---

Katalon Studio provides an easy-to-use Debug mode that allows investigating root causes of a failed Test Case quickly.

This tutorial demonstrates how to debug a Test Case in the Debug mode.

> You can download the sample project here: [Shopping Cart Tests](https://github.com/katalon-studio-samples/shopping-cart-tests).

In our example, we analyze the Test execution results of a failed Test Case, locate the possible root causes and run the Test in the Debug mode.

Here the application under test (AUT) is an online shopping platform, and we run the Test Case with the scenario "Sign in shopping page to purchase a tank top". To recreate the Test Case, you can refer to this WebUI tutorial here: [[WebUI] Create and Run Web UI Test Case using Record and Playback](https://docs.katalon.com/katalon-studio/tutorials/webui-create-test-case.html).

## Analyze Test execution results

After running a Test Case, you can view the Test execution results in the **Log Viewer**. The execution status of each step is displayed on the left pane. Select the step you want to investigate and view the detailed logs on the right pane.

In our example, the Test execution results show failures in Step 7, and the root cause is `com.kms.katalon.core.webui.exception.WebElementNotFoundException: Web element with id ... not found`.

    [image]

> To learn more about exceptions.
## Debug the Test Case using Debug mode

After locating the root cause of the failed Test Case, you can use the Debug mode to set breakpoints and follow the Test execution step by step to debug it.

Follow these steps to debug the Test Case in the Debug mode:

1. Open the Test Case and switch to the **Script** view.

    [image]

2. Set a breankpoint. Double-click on the leftmost side of the script editor to set a breakpoint. In the Debug mode, Katalon Studio pauses execution at breakpoints for you to start debugging.

    With our failed Test Case, we set a breakpoint on Step 7.

    [image]

3. To open the Debug mode, in the main toolbar, click on the **Debug** button.

    [image]

    The Debug mode provides users with several utilities to track the debugging process.

    **Debug commands**

    <table>
    <thead>
    <tr>
    <th>Command</th>
    <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Resume-debugging.png" alt=""></td>
    <td>Resume debugging</td>
    </tr>
    <tr>
    <td><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Suspend-debugging.png" alt=""></td>
    <td>Suspend debugging</td>
    </tr>
    <tr>
    <td><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Terminate-debugging.png" alt=""></td>
    <td>Terminate debugging</td>
    </tr>
    <tr>
    <td><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Disconnect.png" alt=""></td>
    <td>Disconnect</td>
    </tr>
    <tr>
    <td><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Step-into-current-code-block.png" alt=""></td>
    <td>Step into the current code block</td>
    </tr>
    <tr>
    <td><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Step-over-current-code-block.png" alt=""></td>
    <td>Step over the current code block</td>
    </tr>
    <tr>
    <td><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Return-from-current-code-block.png" alt=""></td>
    <td>Return from the current code block</td>
    </tr>
    <tr>
    <td><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/tutorials/debugging_test_case/Run-to-specific-line.png" alt=""></td>
    <td>Run to a specific line</td>
    </tr>
    </tbody>
    </table>


    **Script Editor**
    
    Users can set breakpoints and follow the execution of a Test Case.
    
    **Watch Utilities**

    Users can track values of variables in a Test Case.

    <table>
    <thead>
    <tr>
    <th>View</th>
    <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><strong>Variables</strong></td>
    <td>You can view all variables associated with the current debugged action using Variables View, which is similar to Variables View in Eclipse.
    </tr>
    <tr>
    <td><strong>Breakpoints</strong></td>
    <td>You can view all breakpoints using Breakpoints View, which is similar to Breakpoints View in Eclipse.
    </tr>
    <tr>
    <td><strong>Expressions</strong></td>
    <td>You can inspect data using Expressions View, which is similar to Expressions View in Eclipse.
    </tr>
    </tbody>
    </table>


> For more details, refer to this guide on the Eclipse documentation: [Java Views and Editors](https://help.eclipse.org/latest/index.jsp?topic=%2Forg.eclipse.jdt.doc.user%2Freference%2Fviews%2Fexpressions%2Fref-expressions_view.htm).

4. 