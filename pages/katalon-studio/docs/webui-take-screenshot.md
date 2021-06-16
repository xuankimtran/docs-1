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

## Parameters

Here are the parameters for the WebUI keywords.

| Parameter |  Type | Mandatory | Description |
| --- | --- | --- | --- |
| fileName | String | Optional | A String that represents the path to the saved image. The path can be an absolute or relative path. |
| flowControl | FailureHandling | Optional | Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop. |
| screenshotOptions | Map | Optional | A String representing the information to be printed on the captured screenshot. This string should be limited to 100 characters and size. |

>Notes: ScreenshotOptions is available for Katalon Studio version 8.0.5 onwards.

### ScreenshotOptions parameters

 The screenshotOptions parameter has the following properties:

| Parameter | Type | Mandatory | Description |
| --- | --- | --- | ---|
| Text | String | Must not be null or empty | This string determines the information to be printed on the captured screenshot. This string should be limited to 100 characters. |
| x | Integer | Optional | x pixels from the left side of image. Default is 0.|
| y | Integer | Optional | y pixels from the top of the image. Default is 0. |
| font | String | Optional | Font name. Default is Arial. |
| fontSize | Integer | Optional | Size of font. Default is 12, maximum is 50. |
| fontColor | String | Optional | Hex string of color. Default is "#000000" (black).|
| fontStyle | FontStyle | Optional | fontStyle can be Plain, Italic or Bold. Default is Plain. |

For further information on standard map literal syntax, go to: [The Groovy Development Kit - Collections-Maps](https://groovy-lang.org/groovy-dev-kit.html#Collections-Maps)

>Notes: Supported fonts are OS system fonts. You can find a list of font names for your operating system here:
>
> * Windows: [How to Change the Default System Font on Windows 10](https://www.howtogeek.com/716407/how-to-change-the-default-system-font-on-windows-10/#:~:text=Windows%2010's%20default%20system%20font,on%20your%20Windows%2010%20PC.)
> * macOS: [Fonts - Apple Developer](https://developer.apple.com/fonts/#:~:text=SF%20Pro,and%20includes%20a%20rounded%20variant.)

## Example uses of WebUI keywords

In this section, we demonstrate example uses of the WebUI keywords for screenshots.

### Take a screenshot of your current browser after logging in

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

By default, your screenshots are saved to your temp folder.

### Store your screenshot in a custom location

 The following example also takes a screenshot of your current browser after logging in. But here, the screenshot is saved to a custom location.

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

Same as above, but here the screenshot is stored in the same location as your current project, using relative paths.

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

### Print text on your screenshots

> Requirements: Katalon Studio 8.0.5

The following examples illustrate different configurations to print the information you require on your screenshots.

* Add current timestamp to your screenshot:

```groovy
def timestamp = new Date().format("YYYY-MM-dd HH:mm:ss")
WebUI.takeScreenshot(["text" : timestamp])
```

* Add text "Katalon Studio" at position (10, 20):

```groovy
WebUI.takeScreenshot(["text" : "Katalon Studio", "x" : 10, "y" : 20])
```

* Add text Katalon Studio at position (10, 20) with font Courier, size 24, and gray color:

```groovy
WebUI.takeScreenshot(["text" : "Katalon Studio", "x" : 10, "y" : 20, "font" : "Courier", "fontSize" : "24", "fontColor": "#808080"])
```

* Take a screenshot, save it at D://Document. Add text "Katalon Studio" at position (10, 20) with font Courier, size 24 in gray:

```groovy
WebUI.takeScreenshot("D://Document", ["text" : "Katalon Studio", "x" : 10, "y" : 20, "font" : "Courier", "fontSize" : "24", "fontColor": "#808080"])
```
