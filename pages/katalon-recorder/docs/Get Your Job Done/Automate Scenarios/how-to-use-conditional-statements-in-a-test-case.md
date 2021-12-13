---
title: "How to Use Control Flow commands in a Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/how-to-use-conditional-statements-in-a-test-case.html
description:
---

Katalon Recorder allows you to control Test execution flow with control flow commands. To learn more about available control flow commands, you can refer to this document: [Handle conditional cases in your tests](https://docs.katalon.com/katalon-recorder/docs/conditional-cases.html).

This tutorial shows you how to use control flow commands in a Test Case.

In our example, we have a Test Case with the scenario "Adding items to the shopping cart," which consists of these steps:

1. Navigate to the application under test (AUT): `https://cms.demo.katalon.com`.
2. Select all items with the text "Add to cart."
3. Verify that, on the right corner of the selected item, there's a confirmation text "View cart" visible.

Here we use control flow commands to automate the task of selecting and verifying all shopping items; the process is as follows:

1. Record the Test Case: we record the Test Case to manually select and verify all items.
2. Modify the Test Case using control flow commands: we analyze the Test execution flow and modify the Test Case using control flow commands.
## Record the Test Case

Here we record the Test Case according to the scenario "Adding items to the shopping cart."

Follow these steps:

1. In Katalon Recorder, create a new Test Case, then click on the **Record** button to start recording.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-New-Test-Case.png" width=70% alt="KR New Test Case">

2. Navigate to the AUT. In an active browser tab, navigate to the AUT.

    Here the URL for the AUT is `https://cms.demo.katalon.com`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-AUT.png" width=70% alt="KR Application Under Test">

3. Add items to the cart. In the opened page, hover over the displayed items and select the item with the text "Add to cart."

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-Select-item.png" width=70% alt="KR Select an item to add to cart">

4. Verify that the item is added to the cart successfully. Right-click on the confirmation text `"View cart"` and select **Katalon Recorder > verifyText**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-Verify-item.png" width=70% alt="KR Select an item to add to cart">

5. Repeat *step 3* and *step 4* for every item on the page.

The recorded Test Case is as follows:

<a class="pop">
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-Recorded-Test-Case.png" width=70% alt="Recorded Test Case">
</a>
<p style="text-align: center;"><em>Click the image to enlarge</em></p>


## Modify the Test Case using Control Flow Commands

### Analyze the Test Execution Flow

We first analyze the recorded Test Case to identify where we can apply control flow commands.

The recorded Test Case shows that the `click` and `verifyText` commands are repeatedly used.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-Test-Case-Repeated-Step.png" width=70% alt="Repeated commands in the Test Case">

The **Target** fields of the `click` and `verifyText` commands are:

<table>
    <thead>
        <tr>
            <th>Command</th>
            <th>Target</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><em>click</em></td>
            <td><code>xpath=//main[@id='main']/div[2]/ul/li[{ID-value}]/div/a[2]</code></td>
        </tr>
        <tr>
            <td><em>verifyText</em></td>
            <td><code>xpath=//main[@id='main']/div[2]/ul/li[{ID-value}]/div/a[3]</code></td>
        </tr>
    </tbody>
</table>

From the XPath in the **Target** field, we can see that each item has a unique *ID* value. Because the items are selected from the top to the bottom of the page, the associated *ID* value is incremented.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-Test-Execution-pattern.png" width=70% alt="Repeated commands in the Test Case">

Knowing that each item is associated with one *ID* value, we can use control flow commands to automatically iterate over, select, and verify all 12 items. 
### Apply Control Flow Commands to the Test Case

Here we propose the following control flow:

<a class="pop">
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-Control-Flow.png" width=70% alt="Proposed flowchar">
</a>
<p style="text-align: center;"><em>Click the image to enlarge</em></p>

The specific steps in the proposed control flow are:

1. Open the AUT.
2. Get the *ID* value of the current item.
3. Check if the *ID* is valid; otherwise, the Test Case ends.
4. On the item, if there's a text "Add to cart" visible, click on the text; otherwise, skip to *step 6*.
5. Verify that the added item has the text "View cart" visible.
6. Move on to the next item, and continue with *step 2*.

To apply control flow commands, follow these steps:

1. Open a new Test Case. With the `open` command, navigate to the AUT.

    The URL for the AUT is `https://cms.demo.katalon.com`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-Open-command.png" width=70% alt="KR open command">

2. Get the *ID* value of the current item.

    Here we represent the *ID* value with the variable `ID` and use the `store` command to set the first value for the variable.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-store-command.png" width=70% alt="KR store command">

3. Check if the *ID* is valid.

    Since we want to iterate over all 12 items on the page, we use the `while` control flow command to start a loop. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-while-command.png" width=70% alt="KR while command">


    Here the `while` command checks if the *ID* is valid using the expression `${ID} < 12`. The placeholder syntax `${ID}` expands the `ID` variable into its value.

4. Check if there's a text "Add to cart" visible, then click on the text.

    Here we use the three following commands:
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-storeText-if-click-commands.png" width=70% alt="KR storeText, if, click commands">
    
    We first use the `storeText` command to store the displayed text of the item into a variable. Then we use the `if` conditional command to check if the stored text equals "Add to cart." If the `if` command evaluates to `true`, we use the `click` command to select the text.

    Here XPath for the text "Add to cart" is `xpath=//main[@id='main']/div[2]/ul/li[${ID}]/div/a[2]`.

5. Verify that the added item has the text "View cart" visible.

    Here we use the `verifyText` command.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-verifyText-command.png" width=70% alt="KR verifyText command">

    The XPath for the text "View cart" is `xpath=//main[@id='main']/div[2]/ul/li[${ID}]/div/a[3]`.

    The `click` and `verifyText` command execute only when the `if` command evaluates to `true`. Therefore, we use the `endIf` command to terminate the conditional.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-endIf-command.png" width=70% alt="KR endIf command">

6. Move on to the next item.

    To continue selecting and verifying the next item, we use the `storeEval` command to increment the value of the `ID` variable.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-storeEval-command.png" width=70% alt="KR storeEval command">

    The **Target** of the `storeEval` command is the expression `${ID} + 1`. This expression increments the value of the `ID` variable by 1. As a result, the execution flow continues with the next item on the page.

    The clicking and verifying steps execute inside the `while` loop. Therefore, we use the `endWhile` command to terminate the loop.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-endWhile-command.png" width=70% alt="KR endWhile command">

7. Play the Test Case and verify the results in the **Log** section.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-Test-Execution-results.png" width=70% alt="KR execution results">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge</em></p>
