---
title: "How to extract and verify textual patterns in a test case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/how-to-extract-and-verify-textual-patterns-in-a-test-case.html
description: "In this tutorial, we use Katalon Recorder to extract and verify texts through pattern matching (regex)"
---

In a test project, you might want to verify that the application under test (AUT) displays information in correct pattern, such as email, phone number, or price tag pattern. Katalon Recorder supports this pattern matching process with several commands. Specifically, commands in Katalon Recorder can take patterns as parameters, which enable you to verify several data types on the AUT, including displayed UI text, link, or web elements.

This tutorial shows you how to extract and verify displayed text on an AUT through pattern matching.

In our example, we have a test case with the scenario "check out and verify the price tag," which consists of these steps:

1. Sign in to the AUT - Katalon Zack Market: `https://demo-store.katalon.com/signin`.
2. Select and buy an item.
3. Navigate to the checkout page of the AUT: `https://demo-store.katalon.com/checkout`.
4. On the checkout page, verify that the total price is displayed in the correct price tag format: a dollar sign (`$`) followed by a numeric value.
5. Extract the numeric part from the displayed price tag.

To implement a test case according to the presented scenario, we propose the following process:

1. Record the test case: we record the test case to buy an item and nagivate to the checkout page.
2. Extract and verify the textual pattern: we append the recorded test case with commands that extract and verify textual pattern of the price tag.

## Record the test case

Here we record a test case according to the first three steps of the introduced scenario.

Follow these steps:

1. Sign up for a new account. Navigate to the sign-up page of the AUT and create a new account.

    The URL for the sign-up page is `https://demo-store.katalon.com/signup`.

2. In Katalon Recorder, create a new test case, then click on the **Record** button to start recording.

    [KR-create-a-new-test-case]

3. In an active browser tab, navigate to the sign-in page of the AUT.

    Here the URL for the sign-in page is `https://demo-store.katalon.com/signin`.

    [KR-AUT-signin-page]

4. Type in your username and password, then click **Sign In**.

    [KR-AUT-sign-in]

5. In the main page of the AUT, select and buy a product.

    Here we select the top-left product ("Basic Top").

    [KR-AUT-select-a-product]

    In the product page, select **Buy Now**.

    [KR-AUT-buy-now]

6. After you're nagivated to the checkout page, stop the test recording.

    [KR-AUT-checkout-page]

The recorded test case is as follows:

[]

