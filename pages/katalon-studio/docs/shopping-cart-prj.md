---
title: "Sample WebUI tests project with Data-driven testing (Shopping Cart sample)" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/shopping-cart-prj.html 
---

This sample demonstrates WebUI testing with Data-driven testing in Katalon Studio. This sample also shows you an extensive use of custom keywords in the test case.

The Application Under Test (AUT) is the Katalon shop website: `http://cms.demo.katalon.com`. You can learn more about WebUI testing in this document: [Introduction to WebUI testing](https://docs.katalon.com/katalon-studio/docs/introduction-to-web-testing.html#before-you-begin).

## Open the Shopping Cart sample project

To open the Shopping Cart sample project, in Katalon Studio, go to **File > New Sample Project > Sample Web UI Tests Project (Shopping Cart)**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Open-sample-shopping-cart.png" width="70%" alt="Open Shopping cart sample in Studio">

Alternatively, you can download the Shopping Cart sample project from our Github repository here: [Shopping Cart sample](https://github.com/katalon-studio-samples/shopping-cart-tests).

## Shopping Cart sample project components

### Profiles

To open the execution profile, go to **Profiles > default**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Execution-profiles.png" width="70%" alt="Default profile in the Shopping Cart sample">

You can create and save all global variables in the execution profile. They can be used across test cases in your project. To learn more about execution profiles and global variables, you can refer to this document: [Execution Profile and Global Variables](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html).

Katalon creates 19 global variables in this sample project as follows:

<table>
<thead>
  <tr>
    <th>Name</th>
    <th>Value</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>urlLogin</td>
    <td>http://cms.demo.katalon.com/my-account</td>
  </tr>
  <tr>
    <td>username</td>
    <td>customer</td>
  </tr>
  <tr>
    <td>password</td>
    <td>crz7mrb.KNG3yxv1fbn</td>
  </tr>
  <tr>
    <td>waitPresentTimeout</td>
    <td>5</td>
  </tr>
  <tr>
    <td>urlShop</td>
    <td>http://cms.demo.katalon.com</td>
  </tr>
  <tr>
    <td>companyName</td>
    <td>KMS</td>
  </tr>
  <tr>
    <td>address</td>
    <td>119 Nguyen Thi Thap</td>
  </tr>
  <tr>
    <td>city</td>
    <td>HCM</td>
  </tr>
  <tr>
    <td>country</td>
    <td>Vietnam</td>
  </tr>
  <tr>
    <td>postCode</td>
    <td>70000</td>
  </tr>
  <tr>
    <td>Phone</td>
    <td>0359912894</td>
  </tr>
  <tr>
    <td>uploadPlaceOrderTimeout</td>
    <td>60</td>
  </tr>
  <tr>
    <td>dataFile</td>
    <td>Product List</td>
  </tr>
  <tr>
    <td>inputColumHeader</td>
    <td>productName</td>
  </tr>
  <tr>
    <td>urlProduct</td>
    <td>http://cms.demo.katalon.com/product</td>
  </tr>
  <tr>
    <td>productName</td>
    <td>Flying Ninja</td>
  </tr>
  <tr>
    <td>coupon</td>
    <td>KBAW662S</td>
  </tr>
  <tr>
    <td>firstName</td>
    <td>katalon</td>
  </tr>
  <tr>
    <td>lastName</td>
    <td>customer</td>
  </tr>
</tbody>
</table>

### Custom keywords

Katalon also creates sample custom keywords in this sample project. To learn more about custom keywords, you can refer to this document: [Introduction to custom keywords](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html).

To view our sample custom keywords, in the **Test Explorer** panel, go to **Keywords > sample**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Open-custom-keywords.png" width="70%" alt="Custom keywords in the Shopping Cart sample">

Custom keywords can be reused many times in test cases to perform different actions such as login, adding items to cart, checkout. You can see the use of custom keywords in our sample test cases as below: [Test cases](https://docs.katalon.com/katalon-studio/docs/shopping-cart-prj.html#test-cases).
### Test cases

1. **Custom-keyword samples** test cases

  To view the **Custom-keyword samples** test cases in this project, in the **Test Explorer** panel, go to **Test Cases > Custom-keyword samples > Order and check out a single product/Order and check out a single product using coupon**.

  There are two test cases for different purposes:

  - **Order and check out a single product** adds a single product to the shopping cart and check out. The flow in this test case is as follows:

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPNG-Order-and-check-out-a-single-product.png" width="70%" alt="Order and check out a single product">

    - We use the `loginIntoApplicationWithGlobalVariable` custom keyword to:

      1. Open the `http://cms.demo.katalon.com` website with maximized windows.
      2. Log in with the username and password defined as the global variables in the execution profile.
    
    - Go to the **Shop** page.
    - Next, we use the `addToCartWithGlobalVariable` custom keyword to:

      1. Add the product to cart. The product is defined as a global variable in the execution profile.
      2. Go to the **Cart** page.
      3. Click **Proceed to checkout** to go to the **Checkout** page.

    - For the checkout step, we use the `CheckoutShop` custom keyword to:
    
      1. Click the **Checkout** page.
      2. Fill in checkout information. The checkout information is defined as test case variables in the **Variables** tab.
        
          <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-test-case-variables.png" width="70%" alt="Order and check out a single product">

    - Finally, we use the `logoutFromApplication` custom keyword to:

      1. Go to the **My account** page.
      2. Click **Log out**.

          <a class="pop">
          <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-TC1.gif" width="70%" alt="Order and check out a single product using coupon">
          </a>
          <p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>

  - **Order and check out a single product using coupon** adds a single product to the shopping cart, applies a 50% off coupon then check out. The flow in this test case is as follows:

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Order-and-check-out-a-single-product-using%20coupon.png" width="70%" alt="Order and check out a single product using coupon">

    - We use the `loginIntoApplicationWithGlobalVariable` custom keyword to:

      1. Open the `http://cms.demo.katalon.com` website with maximized windows.
      2. Log in with the username and password defined as the global variables in the execution profile.
    
    - Go to the **Shop** page.
    - Next, we use the `applyCouponAndAddToCartWithGlobalVariable` custom keyword to:

      1. Add the product to cart. The product is defined as a global variable in the execution profile.
      2. Go to the **Cart** page.
      3. Fill in the coupon code defined as a global variable.

    - For the checkout step, we use the `CheckoutShopWithGlobalVariable` custom keyword to: 
      
      1. Click the **Checkout** page.
      2. Fill in checkout information. The checkout information is defined as global variables in the execution profile.
        
    - Finally, we use the `logoutFromApplication` custom keyword to:

      1. Go to the **My account** page.
      2. Click **Log out**.

          <a class="pop">
          <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-TC2.gif" width="70%" alt="Order and check out a single product using coupon">
          </a>
          <p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>

2. **Data-driven samples** test cases

  To view the **Data-driven samples** test cases in this project, in the **Test Explorer** panel, go to **Test Cases > Data-driven samples > Order and check out multiple products**.

  **Order and check out multiple products** adds products from the product list to the shopping cart and check out. The flow in this test case is as follows:

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Order-and-check-out-multiple%20products.png" width="70%" alt="Order and check out multiple products">

  - We use the `loginIntoApplicationWithGlobalVariable` custom keyword to:

      1. Open the `http://cms.demo.katalon.com` website with maximized windows.
      2. Log in with the username and password defined as the global variables in the execution profile.
    
  - Go to the **Shop** page.
  - Next, we want the test case to read the data files. To do so, we use the `getAllData()` keyword to extract product names from the product list as follows:

    ```groovy
    TestData product = findTestData(GlobalVariable.dataFile)
    List<String> productList = product.getAllData().stream()
    .map{data -> data[0]}/*get first column of each row in data file */
    .collect(Collectors.toList())/*add collect and parse to list*/
    ```

  - Then, we use the `addToCart` custom keyword to add extracted product names to cart.

    ```groovy
    for(def productName : productList){
    CustomKeywords.'sample.Shop.addToCart'(productName.toString(), GlobalVariable.urlProduct)
    }
    ```
  - Finally, we use the `CheckoutShopWithGlobalVariable` custom keyword to:

      1. Click the **Checkout** page.
      2. Fill in checkout information. The checkout information is defined as global variables in the execution profile.

          <a class="pop">
          <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/multiple-check-out%20(online-video-cutter.com).gif" width="70%" alt="Order and check out multiple products">
          </a>
          <p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>

### Data Files

To view the data files in this sample project, in the **Test Explorer** panel, go to **Data Files > Product List/Multiple Checkout**.

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Data-files.png" width="70%" alt="Data files in the Shopping Cart sample">

Alternatively, you can go to `<your-project-folder>\Data Files` and choose the file you want to open:

- `Constants.xlsx` contains `Product List` and `Multiple Checkout` sheets.
- `Product List.dat`: a list of products you want to add to the shopping cart.
- `Multiple Checkout.dat` : a list of the customer's personal information needed for shipping on the Checkout page.

### Test Suites

The sample test suites demonstrate the data-driven testing in Katalon Studio. To view sample test suites, in the **Test Explorer** panel, go to **Test Suite**.

1. **Order and check out a single product multiple times** test suite demonstrates data-driven testing by data-binding.

  This test suite binds the **Order and check out a single product** test case with the **Multiple Checkout** data file. After opening the **Test Suite**, click **Show Data Binding** to see the binding data. 

  To learn more about binding data, you can refer to the following document: [Data Binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding).

  <a class="pop">
  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Test-suites-data-binding.png" width="70%" alt="Order and check out a single product multiple times">
  </a>
  <p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

2. **Order and check out multiple products** test suite demonstrates data-driven testing by Groovy script.

    This test suite calls the **Order and check out multiple products** test case. This test case reads the **Product list** test data file by using the Groovy script. 
    In the script mode of **Order and check out multiple products** test case, you can see the following sample code:

    ```groovy
    TestData product = findTestData(GlobalVariable.dataFile)
    List<String> productList = product.getAllData().stream()
    .map{data -> data[0]}/*get first column of each row in data file */
    .collect(Collectors.toList())/*add collect and parse to list*/

      /*Add extracted product names to cart*/
    for(def productName : productList){
    CustomKeywords.'sample.Shop.addToCart'(productName.toString(), GlobalVariable.urlProduct)
    }
    ```

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Test-suites-data-testing-goorvy-script.png" width="70%" alt="Order and check out multiple products">

3. **Order and check out with Global Variable** test suite demonstrates data-driven testing by global variables.

    In **Order and check out with Global Variable** test suite, we call the **Custom-keywords samples** test cases. These test cases use the custom keywords with global variables.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Test-suite-global-variables.png" width="70%" alt="Order and check out multiple products">
    
### Test suite collection

**Shopping-cart-tests - Run All Test Suites**: This sample test suite collection combines the three above test suites with different testing environments. 

<a class="pop">
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Test-suite-collection.png" width="70%" alt="Shopping-cart-tests - Run All Test Suites">
</a>
<p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

## Execute selected test case or test suite/test suite collection

To execute a test case or a test suite/test suite collection in the sample project:

1. Select the test case/test suite/test suite collection you want to execute.
2. Click **Run** or press Ctrl + Shift + A (macOS: Cmd+Shift+A).

    You can choose different browsers to execute your test in the dropdown list next to **Run**. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-Sample-Run-with-different-browsers.png" width="30%" alt="Run the test case">

3. Observe the test result in the **Log Viewer** tab.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-View-results-in-log-viewer.png" width="70%" alt="Oservice results in the log Viewer">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

    > Notes:
    > * You can view test results in the **Result** tab in the test suite or test suite collection level. The test results can be Passed, Failed, Error or Incomplete.
    > * After executing test suites or test suite collections, you can view your reports and details in `<your-project-folder>/Reports`. Katalon Studio also supports exporting test reports into different formats, such as HTML, CSV, PDF, and JUnit.
    > * For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

## See also

 * [Create test cases using Record & Playback](https://docs.katalon.com/katalon-studio/tutorials/webui-create-test-case.html#create-and-run-your-first-web-ui-test-case)
