---
title: "How to Use Control Flow commands in a Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/how-to-use-conditional-statements-in-a-test-case.html
description:
---

Katalon Recorder allows you to control the flow of Test execution with control flow commands. To learn more about available control flow commands, you can refer to this document: [Handle conditional cases in your tests](https://docs.katalon.com/katalon-recorder/docs/conditional-cases.html).

This tutorial shows you how to use control flow commands in a Test Case.

In our example, we create a Test Case with the scenario "Adding items to the shopping cart". The Test Case consists of these steps:

1. Navigate to the application under test (AUT): `https://cms.demo.katalon.com`.
2. Add all items that have the text `"Add to cart"` to the cart.
3. Verify that, on the right corner of the added item, there’s a text `“View cart”` visible.

Here we use control flow commands to automate the task of selecting and verifying all shopping items; the process is as follows:

1. Record a sample Test Case: we record a sample Test Case by selecting and verifying a few items to get the flow of the Test execution.
2. Identify the control flow: we identify where we can apply the control commands in the Test Case.
3. Apply control flow commands to the Test Case: we modify the Test Case with control flow commands.

## Record a Sample Test Case

Here we record a sample Test Case by adding and verifying three shopping items.

Follow these steps:

1. Create a new Test Case. Open Katalon Recorder and create a new Test Case.

    [KS-Create-a-Test-Case]

2. To start recording the Test Case, click on the **Record** button.

3. Navigate to the AUT. In an active browser tab, navigate to the AUT.

    Here we navigate to the Katalon e-commerce website with the URL: `https://cms.demo.katalon.com`.

4. Add items to the cart.

    Here we hover over the displayed items and select three items with the text `"Add to cart"`.

    [KR-Add-an-item]

    On the top right corner of an added items, there should be a confirmation text: `"View cart"`.

    [KR-Added-items-confirmation-text]

5. Verify that the items are added to the cart successfully.

    On the top right corner of an added item, right-click on the confirmation text `"View cart"` and select **Katalon Recorder > verifyText**.

6. Stop recording the Test Case. In Katalon Recorder, click on the **Stop** button.


## Identify the Control Flow

The recorded Test Case is as follows:

## Apply Control Flow Commands to the Test Case

