---
title: "[WebUI] Click" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-click.html 
redirect_from:
    - "/display/KD/%5BWebUI%5D+Click/"
    - "/display/KD/%5BWebUI%5D%20Click/"
    - "/x/MYkY/"
    - "/katalon-studio/docs/webui-click/"
description: 
---
## Description

Click on the given element.

## Set the default wait for element timeout

From Katalon Studio version 8.2.0 onwards, you can set the timeout for Katalon to click an element behind an overlay. With this configuration, Katalon repeatedly tries clicking the target element until the predefined time is used up.

To set the timeout, go to **Project > Settings > Execution**, then manually input the desired waiting time in the **Default wait for element timeout** setting.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/wait-for-element-timeout/KS-OVERLAY-Set-the-default-wait-for-element-timeout.png" width=70% alt="The Default wait for element timeout setting">

## Parameters

| Param | Param Type | Mandatory | Description |
| --- | --- | --- | --- |
| to | TestObject | Required | Represent a web element. |
| flowControl | FailureHandling | Optional | Specify failure handling schema to determine whether the execution should be allowed to continue or stop. To learn more about failure handling setting, you can refer to this document: [Failure handling](https://docs.katalon.com/katalon-studio/docs/failure-handling.html#default-failure-handlingbehavior) |

## Example

You want to click on the **Make Appointment** button. By default, the **Default wait for element timeout** setting is for 30 seconds. If the **Make Appointment** button is behind a loading overlay, Katalon will try clicking the button for 30 seconds in maximum.

```groovy
import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
import internal.GlobalVariable as GlobalVariable
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS

'Open browser and navigate to demo AUT site.'
WebUI.openBrowser(GlobalVariable.G_SiteURL)

'Click on \'Book Appointment\' button'
WebUI.click(findTestObject('Page_CuraHomepage/btn_MakeAppointment'))

'Close browser'
WebUI.closeBrowser()
```