---
title: "Shopping Cart Samples" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/shopping-cart-prj.html 
---

Shopping Cart sample project is available [here](https://github.com/katalon-studio-samples/shopping-cart-tests).

## Profiles

- In the [default profile](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html), you can create and save all [global variables](https://docs.katalon.com/katalon-studio/docs/global-variables.html). They can be used across Test Cases in your project.

## Test Cases

The sample test cases can call [Custom Keywords](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html) or implement the data-driven testing.

Custom keywords are functions defined to be reused many times, e.g. Login, Shop, Checkout, etc.

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

> After the execution is completed, you can view the test results in [Katalon TestOps](https://https.analytics.katalon.com).
>
> - [View Test Reports](https://docs.katalon.com/katalon-analytics/docs/project-management-view-reports.html)
> - [View Test Case details](https://docs.katalon.com/katalon-analytics/docs/project-management-view-details.html#details-of-each-test-case)


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

> After executing tests, you can view your reports and details in [Katalon TestOps](https://analytics.katalon.com).
>
> - [View Test Reports](https://docs.katalon.com/katalon-analytics/docs/project-management-view-reports.html)
> - [View Test Suite Details](https://docs.katalon.com/katalon-analytics/docs/project-management-view-details.html)


## Data Files

- `Constants.xlsx` contains `Product List` and `Multiple Checkout` sheets.
- `Product List.dat`: a list of products you want to add to the shopping cart.
- `Multiple Checkout.dat` : a list of the customer's personal information needed for shipping on the Checkout page.
