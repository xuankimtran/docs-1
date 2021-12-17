---
title: "Sample WebUI tests project with data-driven testing (Shopping Cart sample)" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/shopping-cart-prj.html 
---

This sample demonstrates WebUI testing with data-driven testing in Katalon Studio. This sample also shows you an extensive use of custom keywords in the test case.

The Application Under Test (AUT) is the Katalon shop website: `http://cms.demo.katalon.com`. You can learn more about WebUI testing in this document: [Introduction to WebUI testing](https://docs.katalon.com/katalon-studio/docs/introduction-to-web-testing.html#before-you-begin).

## Open the Shopping Cart sample project

To open the Shopping Cart sample project, in Katalon Studio, go to **File > New Sample Project > Sample Web UI Tests Project (Shopping Cart)**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Open-sample-shopping-cart.png" width="70%" alt="Open Shopping cart sample in Studio">

Alternatively, you can download the Shopping Cart sample project from our Github repository: [Shopping Cart sample](https://github.com/katalon-studio-samples/shopping-cart-tests).

## Shopping Cart sample project components

### Profiles

To open the execution profile, go to **Profiles > default**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Execution-profiles.png" width="70%" alt="Default profile in the Shopping Cart sample">

You can create and save all global variables in the execution profile. They can be used across test cases in your project. To learn more about execution profiles and global variables, you can refer to this document: [Execution profile and global variables](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html).

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

To view our sample custom keywords, in the **Test Explorer** panel, go to **Keywords > sample**. Double-click one of the following .groovy files:

<table>
<thead>
  <tr>
    <th>Custom-keyword files</th>
    <th>Description</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>BlockUIDismissed.groovy</td>
    <td>This file contains a custom keyword that waits for the overlay in the <strong>Checkout</strong> page to disappear.</td>
  </tr>
  <tr>
    <td>Checkout.groovy</td>
    <td>This file contains custom keywords that perform checkout actions.</td>
  </tr>
  <tr>
    <td>Login.groovy</td>
    <td>This file contains custom keywords that perform login actions.</td>
  </tr>
  <tr>
    <td>Select2.groovy</td>
    <td>This file contains custom keywords that perform selecting actions.</td>
  </tr>
  <tr>
    <td>Shop.groovy</td>
    <td>This file contains custom keywords that perform adding-to-the-cart actions.</td>
  </tr>
  <tr>
    <td>Utils.groovy</td>
    <td>This file contains keywords that assist the keywords in the <code>Select2.groovy</code> file.</td>
  </tr>
</tbody>
</table>


<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Open-custom-keywords.png" width="70%" alt="Custom keywords in the Shopping Cart sample">

Custom keywords can be reused many times in test cases to perform different actions such as logging in, adding items to the cart, and checking out. You can see the use of custom keywords in our sample test cases as below: [Test cases](https://docs.katalon.com/katalon-studio/docs/shopping-cart-prj.html#test-cases).
### Test cases

1. Custom-keyword samples test cases

  To view the **Custom-keyword samples** test cases in this project, in the **Test Explorer** panel, go to **Test Cases > Custom-keyword samples**. Double-click to open one of the following test cases:

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-custom-keywords-Test-case.png" width="70%" alt="Custom-keyword test cases">

  - The test case: **Order and check out a single product** adds a single product to the shopping cart, and checks out. The flow in this test case is as follows:

    1. We use the `loginIntoApplicationWithGlobalVariable` custom keyword to:

        - Open the `http://cms.demo.katalon.com` website with maximized windows.
        - Log in with the username and password defined as the global variables in the execution profile.
    
    2. We go to the **Shop** page.
    3. Next, we use the `addToCartWithGlobalVariable` custom keyword to:

        - Add the product to the cart. The product is defined as a global variable in the execution profile.
        - Go to the **Cart** page.
        - Click **Proceed to checkout** to go to the **Checkout** page.

    4. For the checkout step, we use the `CheckoutShop` custom keyword to:
      
        - Click the **Checkout** page.
        - Fill in checkout information. The checkout information is defined as test case variables in the **Variables** tab.
        
          <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-test-case-variables.png" width="70%" alt="Order and check out a single product">

    5. Finally, we use the `logoutFromApplication` custom keyword to:

        - Go to the **My account** page.
        - Click **Log out**.

          <a class="pop">
          <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-TC1.gif" width="70%" alt="Order and check out a single product using coupon">
          </a>
          <p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>

          **<details><summary>Click to view the test script</summary>**

          ```groovy
          import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
          import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
          import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
          import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
          import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
          import com.kms.katalon.core.cucumber.keyword.CucumberBuiltinKeywords as CucumberKW
          import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
          import com.kms.katalon.core.model.FailureHandling as FailureHandling
          import com.kms.katalon.core.testcase.TestCase as TestCase
          import com.kms.katalon.core.testdata.TestData as TestData
          import com.kms.katalon.core.testobject.TestObject as TestObject
          import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
          import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
          import internal.GlobalVariable as GlobalVariable

          CustomKeywords.'sample.Login.loginIntoApplicationWithGlobalVariable'()

          WebUI.waitForElementPresent(findTestObject('Pages/Shop page/lnkShop'), GlobalVariable.waitPresentTimeout)

          WebUI.click(findTestObject('Pages/Shop page/lnkShop'))

          CustomKeywords.'sample.Shop.addToCartWithGlobalVariable'()

          CustomKeywords.'sample.Checkout.CheckoutShop'(firstName,lastName,companyName, country, address, city, postCode, Phone)

          CustomKeywords.'sample.Login.logoutFromApplication'()

          WebUI.closeBrowser()
          ```
          </details>

  - The test case: **Order and check out a single product using coupon** adds a single product to the shopping cart, applies a 50% off coupon, then checks out. The flow in this test case is as follows:

    1. We use the `loginIntoApplicationWithGlobalVariable` custom keyword to:

        - Open the `http://cms.demo.katalon.com` website with maximized windows.
        - Log in with the username and password defined as the global variables in the execution profile.
    
    2. We go to the **Shop** page.
    3. Next, we use the `applyCouponAndAddToCartWithGlobalVariable` custom keyword to:

        - Add the product to the cart. The product is defined as a global variable in the execution profile.
        - Go to the **Cart** page.
        - Fill in the coupon code defined as a global variable.

    4. For the checkout step, we use the `CheckoutShopWithGlobalVariable` custom keyword to: 
      
        - Click the **Checkout** page.
        - Fill in checkout information. The checkout information is defined as global variables in the execution profile.
        
    5. Finally, we use the `logoutFromApplication` custom keyword to:

        - Go to the **My account** page.
        - Click **Log out**.

            <a class="pop">
            <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-TC2.gif" width="70%" alt="Order and check out a single product using coupon">
            </a>
            <p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>
            
            **<details><summary>Click to view the test script</summary>**
                        
            ```groovy
            import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
            import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
            import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
            import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
            import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
            import com.kms.katalon.core.cucumber.keyword.CucumberBuiltinKeywords as CucumberKW
            import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
            import com.kms.katalon.core.model.FailureHandling as FailureHandling
            import com.kms.katalon.core.testcase.TestCase as TestCase
            import com.kms.katalon.core.testdata.TestData as TestData
            import com.kms.katalon.core.testobject.TestObject as TestObject
            import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
            import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
            import internal.GlobalVariable as GlobalVariable

            CustomKeywords.'sample.Login.loginIntoApplicationWithGlobalVariable'()

            WebUI.waitForElementPresent(findTestObject('Pages/Shop page/lnkShop'), GlobalVariable.waitPresentTimeout)

            WebUI.click(findTestObject('Pages/Shop page/lnkShop'))

            CustomKeywords.'sample.Shop.applyCouponAndAddToCartWithGlobalVariable'()

            CustomKeywords.'sample.Checkout.CheckoutShopWithGlobalVariable'()

            CustomKeywords.'sample.Login.logoutFromApplication'()

            WebUI.closeBrowser()
            ```
            </details>


2. Data-driven samples test cases

  To view the **Data-driven samples** test cases in this project, in the **Test Explorer** panel, go to **Test Cases > Data-driven samples > Order and check out multiple products**.

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-DDT-Test-case.png" width="70%" alt="DDT test cases">

  The test case: **Order and check out multiple products** adds products from the product list to the shopping cart, and checks out. The flow in this test case is as follows:

  1. We use the `loginIntoApplicationWithGlobalVariable` custom keyword to:

      - Open the `http://cms.demo.katalon.com` website with maximized windows.
      - Log in with the username and password defined as the global variables in the execution profile.
    
  2. We go to the **Shop** page.
  3. Next, we want the test case to read the data files. To do so, we use the `getAllData()` keyword to extract product names from the product list as follows:

      ```groovy
      TestData product = findTestData(GlobalVariable.dataFile)
      List<String> productList = product.getAllData().stream()
      .map{data -> data[0]}/*get first column of each row in data file */
      .collect(Collectors.toList())/*add collect and parse to list*/
      ```

  4. Then, we use the `addToCart` custom keyword to add extracted product names to the cart.

      ```groovy
      for(def productName : productList){
      CustomKeywords.'sample.Shop.addToCart'(productName.toString(), GlobalVariable.urlProduct)
      }
      ```
  5. Finally, we use the `CheckoutShopWithGlobalVariable` custom keyword to:

      - Click the **Checkout** page.
      - Fill in checkout information. The checkout information is defined as global variables in the execution profile.

          <a class="pop">
          <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-TC3.gif" width="70%" alt="Order and check out multiple products">
          </a>
          <p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>

          **<details><summary>Click to view the test script</summary>**

          ```groovy
          import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
          import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
          import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
          import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

          import java.util.stream.Collectors

          import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
          import com.kms.katalon.core.cucumber.keyword.CucumberBuiltinKeywords as CucumberKW
          import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
          import com.kms.katalon.core.model.FailureHandling as FailureHandling
          import com.kms.katalon.core.testcase.TestCase as TestCase
          import com.kms.katalon.core.testdata.TestData as TestData
          import com.kms.katalon.core.testobject.TestObject as TestObject
          import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
          import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
          import internal.GlobalVariable as GlobalVariable

          CustomKeywords.'sample.Login.loginIntoApplicationWithGlobalVariable'()

          WebUI.waitForElementPresent(findTestObject('Pages/Shop page/lnkShop'), GlobalVariable.waitPresentTimeout)

          WebUI.click(findTestObject('Pages/Shop page/lnkShop'))

          TestData product = findTestData(GlobalVariable.dataFile)
          List<String> productList = product.getAllData().stream()
                        .map{data -> data[0]}/*get first column of each row in data file */
                        .collect(Collectors.toList())/*add collect and parse to list*/

          for(def productName : productList){
            CustomKeywords.'sample.Shop.addToCart'(productName.toString(), GlobalVariable.urlProduct)
          }
          CustomKeywords.'sample.Checkout.CheckoutShopWithGlobalVariable'()
          WebUI.closeBrowser()
          ```
          </details>

### Data Files

To view the data files in this sample project, in the **Test Explorer** panel, go to **Data Files > Product List/Multiple Checkout**.

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Data-files.png" width="70%" alt="Data files in the Shopping Cart sample">

Alternatively, you can go to `<your-project-folder>\Data Files` and choose the file you want to open:

- `Constants.xlsx` contains `Product List` and `Multiple Checkout` sheets.
- `Product List.dat` is a list of products you want to add to the shopping cart.
- `Multiple Checkout.dat` is a list of the customer's personal information needed for shipping on the **Checkout** page.

### Test Suites

The sample test suites demonstrate the data-driven testing in Katalon Studio. To view sample test suites, go to the **Test Suite** folder in the **Test Explorer** panel. Double-click to open one of the three following test suites:

1. The test suite **Order and check out a single product multiple times** demonstrates data-driven testing by data-binding.

    This test suite binds the test case **Order and check out a single product** with the **Multiple Checkout** data file. After opening the **Test Suite**, click **Show Data Binding** to see the binding data. 

    To learn more about binding data, you can refer to the following document: [Data Binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding).

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Test-suites-data-binding.png" width="70%" alt="Order and check out a single product multiple times">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

2. The test suite **Order and check out multiple products** test suite demonstrates data-driven testing by Groovy script.

    This test suite calls the test case **Order and check out multiple products** . This test case reads the **Product list** test data file by using the Groovy script. 
    In the script mode of the test case **Order and check out multiple products**, you can see the following sample code:

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

3. The test suite **Order and check out with Global Variable** demonstrates data-driven testing by global variables.

    In **Order and check out with Global Variable** test suite, we call the **Custom-keywords samples** test cases. These test cases use custom keywords with global variables.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/shopping-cart-samples/KS-SHOPPING-Test-suite-global-variables.png" width="70%" alt="Order and check out multiple products">
    
### Test suite collection

The test suite collection **Shopping-cart-tests - Run All Test Suites** combines the three test suites shown above with different testing environments. 

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


    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/healthcare-samples/KS-SAMPLES-View-results-in-log-viewer.png" width="70%" alt="Observe results in the log Viewer">

    > Notes:
    > * You can view test results in the **Result** tab at the test suite or test suite collection level. The test results can be Passed, Failed, Error, or Incomplete.
    > * After executing test suites or test suite collections, you can view your reports and details in `<your-project-folder>/Reports`. Katalon Studio also supports exporting test reports into different formats, such as HTML, CSV, PDF, and JUnit.
    > * For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

## See also

 * [Create test cases using Record & Playback](https://docs.katalon.com/katalon-studio/tutorials/webui-create-test-case.html#create-and-run-your-first-web-ui-test-case)
