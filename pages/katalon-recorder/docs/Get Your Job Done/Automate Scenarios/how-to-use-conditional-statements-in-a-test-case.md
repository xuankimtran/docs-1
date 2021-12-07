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
3. Verify that, on the right corner of the selected item, there's a text "View cart" visible.

Here we use control flow commands to automate the task of selecting and verifying all shopping items; the process is as follows:

1. Analyze the control flow: we analyze the Test Case and identify where we can apply the control flow commands.
2. Apply control flow commands to the Test Case: we modify the Test Case with control flow commands.

## Analyze the Control Flow

In our example, the AUT is an e-commerce website that displays 12 shopping items:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-AUT-UI.png" width=100% alt="UI of the AUT">

Items added to the cart have the confirmation text "View cart."

To analyze the control flow, follow these steps:

1. Analyze the Test execution flow.

    The Test Case recorded according to the scenario "Adding items to the shopping cart" is as follows:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-Recorded-Test-Case.png" width=70% alt="Recorded Test Case">

    From the interface of the AUT and the recorded Test Case, we can see the flow of the Test execution consists of these steps:

    1. With the `open` command, navigate to the site `https://cms.demo.katalon.com`.
    2. With the `click` command, hover over an item and click on the text "Add to cart."
    3. With the `verifyText` command, verify that the added item has the confirmation text "View cart."
    4. Repeat step 2 and step 3 with every item on the page.

2. Identify the pattern in the Test Case. 

    Here we can see the `click` and `verifyText` commands are repeatedly used.

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
                <td><code>xpath=//main[@id='main']/div[2]/ul/li[{ID}]/div/a[2]</code></td>
            </tr>
            <tr>
                <td><em>verifyText</em></td>
                <td><code>xpath=//main[@id='main']/div[2]/ul/li[{ID}]/div/a[3]</code></td>
            </tr>
        </tbody>
    </table>

    From the XPath in the **Target** field, we can see that each item has a unique `ID` value. The' ID' value is incremented as the items are selected from the top to the bottom of the page.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/conditional-and-loop-tutorial/KR-Test-Execution-pattern.png" width=70% alt="Repeated commands in the Test Case">



## Apply Control Flow Commands to the Test Case
