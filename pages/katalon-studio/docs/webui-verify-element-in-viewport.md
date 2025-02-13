---
title: "[WebUI] Verify Element In Viewport" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-verify-element-in-viewport.html 
redirect_from:
    - "/display/KD/%5BWebUI%5D+Verify+Element+Visible+In+Viewport/"
    - "/display/KD/%5BWebUI%5D%20Verify%20Element%20Visible%20In%20Viewport/"
    - "/x/7ooY/"
    - "/katalon-studio/docs/webui-verify-element-visible-in-viewport/"
    - "/katalon-studio/docs/webui-verify-element-visible-in-viewport.html"
description: 
---
Description
-----------

Verify if the web element is visible in current [viewport](https://www.w3schools.com/css/css_rwd_viewport.asp)

Parameters
----------

| Param | Param Type | Mandatory | Description |
| --- | --- | --- | --- |
| to | TestObject | Required | Represent a web element. |
| timeOut  | int  | Required | Maximum period of time (in seconds) that system will wait to return the result. |
| flowControl | FailureHandling | Optional | Specify [failure handling](/x/qAAM) schema to determine whether the execution should be allowed to continue or stop. |

Returns
-------

<table><thead><tr><th>Param Type</th><th>Description</th></tr></thead><tbody><tr><td>Boolean</td><td><ul><li><strong>true:</strong>&nbsp;the element is visible in current viewport.</li><li><strong>false:</strong> the element is NOT visible in current viewport.</li></ul></td></tr></tbody></table>

Example
-------

Within the next 10 seconds, you want to verify that the 'btn_Login' button is visible in the current viewport.

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

// Open browser and navigate to website that contains the element to wait for
WebUI.openBrowser(GlobalVariable.G_SiteURL)

// Wait for btn_Login to be visible in 10s
WebUI.verifyElementInViewport(findTestObject('Page_Login/btn_Login'), 10)

// Close browser
WebUI.closeBrowser()
```