---
title: "Shopping Cart Project" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/shopping-cart-prj.html 
---

## Profiles

- In the [default profile](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html), you can create and save all [global variables](https://docs.katalon.com/katalon-studio/docs/global-variables.html). You can use them anywhere in your Test Case.

## Test Cases

The sample test cases can call [Custom Keywords](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html) or implement the data-driven testing.

In the test cases calling custom keywords:

- Some functions are defined to be reused many times. Ex: Login, Shop, Checkout...
- Syntax of a custom keyword:\
        `@Keyword
        def static {return type}{functionname}(parameters,parameters...){`\
        `...`\
        `}`

In the test cases implementing the data-driven testing: The `getAllData()` function is used for getting all rows and the first column of each row in the data file. Then they're added to the collection and parsed to the product list.

```groovy
TestData product = findTestData(GlobalVariable.dataFile)
List<String> productList = product.getAllData().stream()
.map{data -> data[0]}/*get first column of each row in data file */
.collect(Collectors.toList())/*add collect and parse to list*/
```

There are three test cases for different purposes in this project:

- Test Case 1: Add a single product to the shopping cart and check out.
- Test Case 2: Add a single product to the shopping cart, apply a 50% off coupon and then check out.
- Test Case 3: Add several products to the shopping cart and check out.

To run a test case in the sample project:

- Select the Test Case you want to execute.
- Click the **Run** button or Windows users can press the key combination of **Ctrl + Shift + A**; Mac users press **Command+Shift+A**.
- Observe the test result on Log Viewer.

## Test Suites

The sample test suites are to demonstrate the data-driven testing in Katalon Studio.

1. Data-driven testing by Data-binding

[Data Binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#create-a-new-test-suite-with-test-case-variables) is used to run a test case with an external data source.

- On the selected Test Suite, click **Show Data Binding** on the right corner of the Test Suite view.
- Select a Test Case.
- In the **Test Data table** -> click the **Add** button -> Select your preferred **Test Data** and click **OK**.
- In the **Variable Binding** table-> Click **Set Type** > **Data Column** -> Click **Set Test Data** > Select the preferred Test Data; then bind the Variables of the Test Case with the corresponding columns of data.

2. Data-driven testing by Groovy script

Test data can be read right in your test case by using the Groovy script. Find the test data and the stream list of products; then get all rows and the first column of each row in the data file to add them to the collection and parse them to the product list.
In the script mode of **Order and check out multiple products** test case, you can see:

```groovy
TestData product = findTestData(GlobalVariable.dataFile)
List<String> productList = product.getAllData().stream()
.map{data -> data[0]}/*get first column of each row in data file */
.collect(Collectors.toList())/*add collect and parse to list*/
```

3. Data-driven testing by Global Variables

In **Order and check out with Global Variable** test suite, call the Custom Keywords in a Test Case with parameterized Global Variables.

To run a test suite in the sample project:

- Select the Test Suite you want to execute.
- Click the **Run** button or Windows users can press the key combination of **Ctrl + Shift + A**; Mac users press **Command+Shift+A**.
- Observe the test result on Log Viewer.

## Data Files

- `Constants.xlsx` contains `Product List` and `Multiple Checkout` sheets.
- `Product List.dat`: a list of products you want to add to the shopping cart.
- `Multiple Checkout.dat` : a list of the customer's personal information needed for shipping on the Checkout page.
