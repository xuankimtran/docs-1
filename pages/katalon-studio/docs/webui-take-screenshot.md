---
title: "[WebUI] Take Screenshot" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-take-screenshot.html 
redirect_from:
    - "/display/KD/%5BWebUI%5D+Take+Screenshot/"
    - "/display/KD/%5BWebUI%5D%20Take%20Screenshot/"
    - "/x/2IoY/"
    - "/katalon-studio/docs/webui-take-screenshot/"
description: 
---
In this section, you will find key example uses of WebUI keywords. Those examples demonstrate how to take screenshots using WebUI keywords, as well as optional settings and triggers.

## Parameters  

| Parameter |  Type | Mandatory | Description |
| --- | --- | --- | --- |
| fileName | String | Optional | A String that represents the path to the saved image. The path can be an absolute or relative path. |
| flowControl | FailureHandling | Optional | Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop. |

## Use cases

### Taking a screenshot of your current browser after logging in

```groovy
import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import internal.GlobalVariable as GlobalVariable

'Open browser and navigate to AUT'
WebUI.openBrowser(GlobalVariable.G_SiteURL)

'Input username'
WebUI.setText(findTestObject('Page_Login/txt_UserName'), Username)

'Input password'
WebUI.setText(findTestObject('Page_Login/txt_Password'), Password)

'Click on new_btn'
WebUI.click(findTestObject('Page_Login/btn_Login'))

'Take screenshot after logging in'
WebUI.takeScreenshot()

'Close browser'
WebUI.closeBrowser()
```
By default, your screenshot will be saved to your temp folder.

### Store your screenshot in a custom location

 The following example also takes a screenshot of your current browser after logging in. Here, the screenshot is saved to a custom location.

```groovy
import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import internal.GlobalVariable as GlobalVariable

'Open browser and navigate to AUT'
WebUI.openBrowser(GlobalVariable.G_SiteURL)

'Input username'
WebUI.setText(findTestObject('Page_Login/txt_UserName'), Username)

'Input password'
WebUI.setText(findTestObject('Page_Login/txt_Password'), Password)

'Click on new_btn'
WebUI.click(findTestObject('Page_Login/btn_Login'))

'Take screenshot after logging in'
WebUI.takeScreenshot('E:\\screenshot.png')

'Close browser'
WebUI.closeBrowser()
```

### Sort and store screenshots by projects using relative paths

Same as above, but here the screenshot is stored with your current project.

```groovy
 import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import internal.GlobalVariable as GlobalVariable

'Open browser and navigate to AUT'
WebUI.openBrowser(GlobalVariable.G_SiteURL)

'Input username'
WebUI.setText(findTestObject('Page_Login/txt_UserName'), Username)

'Input password'
WebUI.setText(findTestObject('Page_Login/txt_Password'), Password)

'Click on new_btn'
WebUI.click(findTestObject('Page_Login/btn_Login'))

'Take screenshot after logging in'
WebUI.takeScreenshot('Test/Demo.png')
 
'Close browser'
WebUI.closeBrowser()
```

## Add timestamps to your screenshots

> Requirements: Katalon Studio 8.0.5

The following parameter allows you to set automatic timestamps as per your preference.

| Parameter | Type | Mandatory | Description |
| --- | --- | --- | --- |
| screenshotOptions | Map | Optional | A String representing the information to be printed on the captured screenshot. This string should be limited to 100 characters and size. |

For further information on standard map literal syntax, go to: [Apache Groovy programming language - The Groovy Development Kit](https://groovy-lang.org/groovy-dev-kit.html#Collections-Maps)

The screenshotOptions parameter has the following properties:

| Parameter | Type | Mandatory | Description |
| --- | --- | --- | ---|
| Text | String | Must not be null or empty | This string determines the information to be printed on the captured screenshot. This string should be limited to 100 characters. |
| x | Integer | Optional | x pixels from the left side of image. Default is 0.|
| y | Integer | Optional | y pixels from the top of the image. Default is 0. |
| font | String | Optional | Font name. Default is Arial. |
| fontSize | Integer | Optional | Size of font. Default is 12, maximum is 50. |
| fontColor | String | Optional | Hex string of color. Default is “#000000“ (black).|
| fontStyle | FontStyle | Optional | fontStyle can be Plain, Italic or Bold. Default is Plain. |
 
### Example uses of screenshotOptions

The following examples illustrate different configurations to print the information you require on your screenshots.

#### Add current timestamp to your screenshot:
```
def timestamp = new Date().format("YYYY-MM-dd HH:mm:ss")
WebUI.takeScreenshot(["text" : timestamp])
```

#### Add text "Katalon Studio" at position (10, 20):

```
WebUI.takeScreenshot(["text" : "Katalon Studio", "x" : 10, "y" : 20])
```

#### Add text Katalon Studio at position (10, 20) with font Courier, size 24, and gray color

```
WebUI.takeScreenshot(["text" : "Katalon Studio", "x" : 10, "y" : 20, "font" : "Courier", "fontSize" : "24", "fontColor": "#808080"])
```

#### Take screenshot at D://Document and add text Katalon Studio at position (10, 20) with font Courier, size 24 and gray color

```
WebUI.takeScreenshot("D://Document", ["text" : "Katalon Studio", "x" : 10, "y" : 20, "font" : "Courier", "fontSize" : "24", "fontColor": "#808080"])
```

Placeholder: information on OS fonts