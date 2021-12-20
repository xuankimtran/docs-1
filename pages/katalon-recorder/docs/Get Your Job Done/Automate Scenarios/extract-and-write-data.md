---
title: "How to extract and write data in a test case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/write-and-extract-data.html
description: "How to extract and write data from a website in a test case."
---

When testing a website with Katalon Recorder, you might want to extract data from the website and store the data into an external file. Katalon Recorder facilitates this process of extracting and writing data with several commands.

This tutorial shows you how to use Katalon Recorder to extract data from a website and write the data to a CSV file.

In our example, we follow the scenario "Extract data from the checkout page," which consists of these steps:

1. Navigate to the AUT - the Katalon E-commerce page: `https://cms.demo.katalon.com`.
2. Add a few items to the cart.
3. Navigate to the checkout page of the AUT: `https://cms.demo.katalon.com/checkout/`.
4. On the checkout page, extract the names and prices of the added items.
5. Write the extracted data to a CSV file.

After we follow the first three steps of the presented scenario, the checkout page is displayed as below:

<a class="pop">
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Checkout-Page-Overview.png" width=70% alt="Checkout Page Overview">
</a>
<p style="text-align: center;"><em>Click the image to enlarge</em></p>

Added items are organized in a table with names and prices.

To extract the displayed names and prices, and write the data to a CSV file, the process is as follows:

1. Prepare the CSV file: we create a CSV to store the names and prices.
2. Add the CSV file to the workspace: we add the CSV file to the Katalon Recorder workspace.
3. Extract and write data: we create a test case to extract and write the data 
from the checkout page to the CSV file.

## Prepare the CSV file

Here we create a CSV file with two columns to store names and prices of the added items.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Prepared-CSV-file.png" width=70% alt="Prepared CSV file">

## Add the CSV file to the workspace

Follow these steps:

1. Open Katalon Recorder. In the **Workspace** sidebar, click on the *more* icon in the **Test Data** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Sidebar-TestData.png" width=30% alt="Test Data section">

2. In the displayed file dialog, select the CSV file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-File-Dialog.png" width=70% alt="File dialog">

3. The added CSV file is displayed under the **Test Data** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Added-CSV-file.png" width=30% alt="Added CSV file">

> **Notes**:
>
> As a browser extension, Katalon Recorder cannot write data directly to the user file system; the extension only writes to the version of the data file that is added to the workspace. Therefore, you need to download the data file again to view the extracted data.

## Extract and write the data

After preparing and adding the CSV to the workspace, we locate the items on the checkout page by getting their associated XPath. Using the XPath, we create a test case to iterate over all items, extract the names and prices, and then write the data to the CSV file.
### Get the associated XPath

To locate the items on the checkout page for data extraction, we need three types of XPaths: 

* The XPath of a displayed item.
* The XPath of the name of the item.
* The XPath of the price of the item.

Here we use the browser **Inspector** tool to get the XPaths.

Follow these steps:

1. Get the XPath of an item. On the checkout page, right-click on the displayed table of items, then select **Inspect**.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Inspect-Item-List.png" width=70% alt="Inspect the items">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge</em></p>
    The inspector window shows that the items are organized in an HTML table element, and each item is represented as a table row.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Inspected-Table.png" width=70% alt="Inspected table">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge</em></p>

    To get the XPath of an item, right-click on a `<tr>` tag and select **Copy > Copy XPath**.
    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Copy-Table-XPath.png" width=70% alt="Inspected table row">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge</em></p>

2. Get the XPath of an item name. In the inspector window, right-click on the `<td>` tag associated with the item name and select **Copy > Copy XPath**.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Copy-Name-XPath.png" width=70% alt="Inspected item name">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge</em></p>

3. Get the XPath of an item price. In the inspector window, right-click on the `<td>` tag associated with the item price and select **Copy > Copy XPath**.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Copy-Price-XPath.png" width=70% alt="Inspected item price">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge</em></p>

The three XPaths that we get are as follows:

<table>
    <thead>
        <tr>
            <th>Element</th>
            <th>XPath</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><b>Item</b></td>
            <td><code>//*[@id="order_review"]/table/tbody/tr[1]</code></td>
        </tr>
        <tr>
            <td><b>Name</b></td>
            <td><code>//*[@id="order_review"]/table/tbody/tr[1]/td[1]</code></td>
        </tr>
        <tr>
            <td><b>Price</b></td>
            <td><code>//*[@id="order_review"]/table/tbody/tr[1]/td[2]</code></td>
        </tr>
    </tbody>
</table>

From the XPath of the item element, we can see that each row (`<tr>`) in the table is associated with an ID value. For example, the XPath of the item that we copy contains the ID value `1`. With this ID value, we can quickly iterate over all items in the table to extract the names and prices.

### Extract and write data in a test case

Follow these steps:

1. Open a new Test Case. With the `open` command, navigate to the checkout page of the AUT.

    The URL for the checkout page is `https://cms.demo.katalon.com/checkout/`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Open-command.png" width=70% alt="KR open command">

2. Get the count of rows of the item table. 

    To iterate over all items in the table, we need the total number of rows. Here we use the `storeXpathCount` command with the target `//*[@id="order_review"]/table/tbody/tr` to count the number of rows. We then store the count into the `rowNum` variable.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-storeXPathCount-command.png" width=70% alt="KR storeXpathCount">

3. Iterate over the items.

    Here we use two commands: `store` and `while`. The `store` command creates the `ID` variable to represent the ID value of an item. The `while` command starts a loop to iterate over the items in the table. 

    > To learn more about control flow commands in Katalon Recorder, refer to this guide: [Handle conditional cases in your tests](https://docs.katalon.com/katalon-recorder/docs/conditional-cases.html).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Store-and-While-command.png" width=70% alt="KR store and while commands">

    Here the while command checks if the current ID value is valid using the expression `${ID} < ${rowNum}`.

4. Store the name of an item.

    We use the `storeText` command to store the item name into the `itemName` variable.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-storeText-command.png" width=70% alt="KR storeText command">

    The XPath for the command is `//*[@id="order_review"]/table/tbody/tr[${ID}]/td[1]`.

5. Store the price of an item.

    Here we use the `storeText` command to store the item price into the `itemPrice` variable.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-storeText-command-price.png" width=70% alt="KR storeText command for price">

    The XPath for the command is `//*[@id="order_review"]/table/tbody/tr[${ID}]/td[2]`.

6. Write data to the CSV file.

    We use the `appendToCSV` command to append the extracted name and price to the added CSV file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-appendToCSV-command.png" width=70% alt="KR storeText command for price">

    The **Target** of the command is the name of the added CSV file. The added values to the CSV, item name and price, are separated by commas.

7. Move on to the next item.

    To continue selecting and verifying the next item, we use the `storeEval` command to increment the value of the ID variable.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-storeEval-endWhile-commands.png" width=70% alt="KR storeEval endWhile commands">

    The extracting and writing steps execute the `while` loop. Therefore, we use the `endWhile` command to terminate the loop.

8. Play the test case and download the CSV file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Results.png" width=70% alt="KR results">

9. Open the downloaded CSV file and verify the results.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/write-and-extract-data/KR-Downloaded-CSV.png" width=70% alt="KR downloaded CSV file">