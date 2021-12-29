---
title: "How to extract and verify textual patterns in a test case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/how-to-extract-and-verify-textual-patterns-in-a-test-case.html
description: "In this tutorial, we use Katalon Recorder to extract and verify texts through pattern matching (regex)."
---

In a test project, you might want to verify that the application under test (AUT) displays information in the correct pattern, such as email, phone number, or price tag pattern. Katalon Recorder supports this pattern matching process with several commands. Specifically, commands in Katalon Recorder can take patterns as input to verify several data types on an AUT.

This tutorial shows you how to extract and verify displayed text on an AUT. The pattern used in our case is a *regular expression* (regex): a sequence of characters that specifies a search pattern.

In our example, we have a scenario "extract and verify item price," which consists of these steps:

1. Sign in to the AUT - Katalon Zack Market: `https://demo-store.katalon.com/signin`.
2. Navigate to the homepage: `https://demo-store.katalon.com`.
3. On the homepage, select an item.
4. On the item details page, extract the item price.
5. Verify that the item price is in the correct pattern: a currency symbol (`$`) followed by a numeric value.

After we follow the first three steps of the scenario, the item details page displays the price text as follows:

<a class="pop">
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/extract-and-verify-textual-patterns/KR-AUT-overview.png" width=100% alt="Katalon Recorder AUT overview">
</a>
<p style="text-align: center;"><em>Click the image to enlarge</em></p>

We can see that the price text consists of the item price (`$25.99`) and the currency code (`CAD`).

## Extract and verify textual patterns

To complete the last two steps of the scenario, we create a test case to extract only the price from the displayed price text. Then, we verify that the price is in the correct pattern using a regex.

Follow these steps:

1. Get the XPath of the displayed price text. On the item details page, right-click on the displayed price text, then select **Inspect**.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/extract-and-verify-textual-patterns/KR-AUT-inspect.png" width=70% alt="Katalon Recorder AUT inspect">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge</em></p>

    In the opened inspector window, right-click on the `<div>` tag associated with the price text, and select **Copy > Copy XPath**.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/extract-and-verify-textual-patterns/KR-AUT-copy-xpath.png" width=70% alt="Katalon Recorder AUT Copy XPath">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge</em></p>

2. In Katalon Recorder, create a new test case.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/extract-and-verify-textual-patterns/KR-new-test-case.png" width=70% alt="Katalon Recorder new test case">

3. Store the displayed price text.

    With XPath copied in *step 1*, we use the `storeText` command to store the displayed price text into a variable.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/extract-and-verify-textual-patterns/KR-storeText-command.png" width=70% alt="Katalon Recorder storeText command">

    In our case, the XPath of the text is `//*[@id="root"]/div/div/div[1]/div[2]/div/div[2]/div/div[3]`.

4. Extract the item price.

    We use the `storeEval` command to extract the item price `$25.99` (the first six characters) from the text.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/extract-and-verify-textual-patterns/KR-storeEval-substring.png" width=70% alt="Katalon Recorder storeEval command with a Javascript expression">

    The `storeEval` command evaluates a Javascript expression, then stores the result into a variable. In our example, the target Javascript expression is `"${displayedPrice}".substring(0, 6)`. Here, `substring()` is a method that extracts characters from a string, given two indices.

    The expression evaluates the `displayedPrice` variable into its value. Then it extracts and stores the first six characters into the `itemPrice`.

5. Verify the item price with regex.

    We use the `verifyEval` command with a regex in the **Value** field. This command verifies that the item price is displayed in the correct price pattern.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/extract-and-verify-textual-patterns/KR-verifyEval.png" width=70% alt="Katalon Recorder verifyEval command with a Javascript expression and regular expression">

    To input a regex as a value, we prefix the expression with `regexp:`. For our purpose, we use the regex `^[$](\d+\.\d+)` that checks if the item price starts with a dollar sign and ends with a numeric value.

6. Play the test case and verify the results in the **Log** view.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/extract-and-verify-textual-patterns/KR-Log-view-results.png" width=70% alt="Katalon Recorder Log view results">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge</em></p>