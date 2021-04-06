---
title: "[WebUI] Create and Run WebUI Test Case using Record and Playback"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/webui-create-test-case.html
description: Create and Run WebUI Test Case 
---

This tutorial demonstrates how to create iOS tests with Katalon Studio using **Record** and **Playback**.

Go throught the scenario "Sign in and purchase a tank top" to get familiar with this feature. The basic steps are:

1. Create a new project to store recorded actions.
2. Interact with the web page.
    - Sign in.
    - Purchase a tank top.
3. Stop recording and Save scripts.

> Shopping Cart sample project is available [here](https://github.com/katalon-studio-samples/shopping-cart-tests).

## Create and Run your first WebUI test case

### Create New Project

1. In the **Test Explorer** on the sidebar > click **New Project**.

2. In the displayed **New Project** dialog:

   - Enter project **Name**.
   - In project **Type** > select **Web**.
   - In **Project** > select **Sample Web UI...(Shopping Cart)**, the **Repository URL** is filled automatically.
   - Browse a **Location** to store your project > click **OK**.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/recording-webui-test/new-project.png" width=70%>

### Record

1. From the main toolbar, click on **Web Recorder Utility** icon to open the Web Recorder.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/recording-webui-test/web-record-icon.png" width=30%>

2. In the displayed **Web Recorder**:
    - Enter URL: https://demo-store.katalon.com.
    - Select a browser to start recording (Chrome is recommended).

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/recording-webui-test/selectb-browser.png" width=70%>

3. Wait until the browser is launched and ready to interact.

     When you hover an element, the browser highlights and displays that element's correspondent XPath on the top of the page.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/recording-webui-test/xpath.png" width=70%>

    > Tip: You can use hotkey to capture objects (pressing the combination of <Command + back quote>). The captured object will be highlighted with a green border.

4. Interact with the web page. In this scenario, we will sign in and purchase a tank top.

    During your recording, **Katalon Web Recorder** captures all the objects that you have interacted with. When you enter in the **Password** field, **Katalon Web Recorder** uses '[Set Encrypted Text](https://docs.katalon.com/display/KD/%5BWebUI%5D+Set+Encrypted+Text)' keyword automatically. This input value will be encrypted to ensure security.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/recording-webui-test/recorded-actions.png" width=70%>

5. Once you finish purchasing > click **Save script** to stop recording and save the captured objects. **Katalon Web Recorder** exports a list of objects used in the test case.

     Create a new folder or select an existing one in **Object Repository** > click **OK**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/recording-webui-test/select-repo.png" width=70%>

    > Katalon Studio allows you to continue recording using the existing test case to reduce your effort on modifying existing ones. [Learn more](https://docs.katalon.com/katalon-studio/docs/record-web-utility.html#record-using-existing-test-case)
    >
    > <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/recording-webui-test/test-case-modifying.png" width=70%>

### Playback

To playback the recorded scenario:

1. Select the test case where you saved the recorded actions.
2. From the main toolbar, select any browser on the drop-down list next to **Run** to execute the test case. 

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/recording-webui-test/select-browser-to-playback.png" width=30%>

    Katalon Studio executes the test case with the recorded steps accordingly.

**<details><summary>View the test case in Script mode.</summary>**

```groovy
import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import static com.kms.katalon.core.testobject.ObjectRepository.findWindowsObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
import com.kms.katalon.core.cucumber.keyword.CucumberBuiltinKeywords as CucumberKW
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testng.keyword.TestNGBuiltinKeywords as TestNGKW
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.windows.keyword.WindowsBuiltinKeywords as Windows
import internal.GlobalVariable as GlobalVariable
import org.openqa.selenium.Keys as Keys

WebUI.openBrowser('')

WebUI.navigateToUrl('https://demo-store.katalon.com/')

WebUI.click(findTestObject('Object Repository/shoppingCart/Page_Zack Market/svg_Zack Market_svg-inline--fa fa-user fa-w-14'))

WebUI.setText(findTestObject('Object Repository/shoppingCart/Page_Zack Market/input_Email_email'), 'thuy.ngo@katalon.com')

WebUI.setEncryptedText(findTestObject('Object Repository/shoppingCart/Page_Zack Market/input_Password_password'), 'GklqZBguAPQ=')

WebUI.click(findTestObject('Object Repository/shoppingCart/Page_Zack Market/input_Password_button_btn__2lzmo'))

WebUI.click(findTestObject('Object Repository/shoppingCart/Page_Zack Market/div_All Products_search_auto__TZ-uB'))

WebUI.setText(findTestObject('Object Repository/shoppingCart/Page_Zack Market/input_All Products_auto_input__2ud9e'), 'tank top')

WebUI.click(findTestObject('Object Repository/shoppingCart/Page_Zack Market/span_Tank Top'))

WebUI.click(findTestObject('Object Repository/shoppingCart/Page_Zack Market/img_Clear All_card-img-top'))

WebUI.click(findTestObject('Object Repository/shoppingCart/Page_Zack Market/img'))

WebUI.click(findTestObject('Object Repository/shoppingCart/Page_Zack Market/span_Buy Now'))

WebUI.click(findTestObject('Object Repository/shoppingCart/Page_Zack Market/span_Confirm checkout'))

WebUI.closeBrowser()
```
</details>

Next: [Execute and Debug a Test Case](https://docs.katalon.com/katalon-studio/docs/execute-a-test-case-or-a-test-suite.html).

   See also:
   * [Troubleshoot automated web testing](https://docs.katalon.com/katalon-studio/docs/troubleshoot-common-execution-exceptions-web-test.html).