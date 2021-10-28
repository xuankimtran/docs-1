---
title: "[WebUI] Click Offset" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-click-offset.html 
redirect_from:
    - "/display/KD/%5BWebUI%5D+Click+Offset/"
    - "/display/KD/%5BWebUI%5D%20Click%20Offset/"
    - "/x/eA5O/"
    - "/katalon-studio/docs/webui-click-offset/"
description: 
---
## Description

Click on the given element with the relative position (x, y) from the top-left corner of that element. From Katalon Studio version 8.2.0 onwards, if the target element is behind a loading overlay, Katalon repeatedly tries clicking the element for a period configured in **Project > Settings > Execution > Default wait for element timeout**.

To learn more about setting the **Default wait for element timeout**, you can refer to this document: [Project settings](https://docs.katalon.com/katalon-studio/docs/execution-settings.html#default-execution-settings).

## Parameters

| Param | Param Type | Mandatory | Description |
| --- | --- | --- | --- |
| to | TestObject | Required | Represent a web element. |
| offsetX | int | Required | x position in relative to the element |
| offsetY | int | Required | y position in relative to the element |
| flowControl | FailureHandling | Optional | Specify failure handling schema to determine whether the execution should be allowed to continue or stop. To learn more about failure handling settings, you can refer to this document: [Failure handling](https://docs.katalon.com/katalon-studio/docs/failure-handling.html#default-failure-handlingbehavior)|

## Example

In this example, we want to click on the top left cell of the Tic Tac Toe board. 
By default, the **Default wait for element timeout** setting is for 30 seconds. If the Tic Tac Toe board is behind a loading overlay, Katalon will try clicking the button for 30 seconds maximum.

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

'Open browser and navigate to Tic Tac Toe site.'
WebUI.openBrowser('https://codepen.io/solartic/full/qEGqNL/')

'Click on the top left cell'
WebUI.clickOffset(findTestObject('Object Repository/Page_CodePen - Tic Tac Toe/canvas_tic-tac-toe-board'), 100, 100)

'Close browser'
WebUI.closeBrowser()
```