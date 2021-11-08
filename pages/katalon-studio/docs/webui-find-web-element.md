---
title: "[WebUI] Find Web Element" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-find-web-element.html 
redirect_from:
description: 
---

## Description

Find web element by test object.

## Parameters

<table>
	<thead>
		<tr>
			<th>Param</th>
			<th>Param Type</th>
			<th>Mandatory</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>to</td>
			<td>TestObject</td>
			<td>Required</td>
			<td>Represent a web element.</td>
		</tr>
		<tr>
			<td>timeout</td>
			<td>int</td>
			<td>Required</td>
			<td>Maximum period of time (in seconds) that system will wait to return a result.</td>
		</tr>
		<tr>
			<td>flowControl</td>
			<td>FailureHandling</td>
			<td>Optional</td>
			<td>Specify&nbsp;<a href="https://docs.katalon.com/katalon-studio/docs/failure-handling.html">failure handling</a>&nbsp;schema to determine whether the execution should be allowed to continue or stop.</td>
		</tr>
	</tbody>
</table>

## Returns

The found web element or `null` if cannot find any.

## Example

You want to find the Facebook icon on the [https://katalon-demo-cura.herokuapp.com/](https://katalon-demo-cura.herokuapp.com/) demo website using a test object.

``` groovy

import com.kms.katalon.core.testobject.ConditionType as ConditionType
import com.kms.katalon.core.util.KeywordUtil
import org.openqa.selenium.WebElement
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.testobject.TestObject as TestObject
​
WebUI.openBrowser('https://katalon-demo-cura.herokuapp.com/')
// Wait until the brower's stable
WebUI.delay(3)
​
// Create a test object. This is the Facebook icon on the demo website
TestObject testObj = findTestObject('icon_Facebook')
WebElement anElement = WebUI.findWebElement(testObj, 5)
KeywordUtil.logInfo(anElement.toString())
```

**See also**:
* [[WebUI] Find Web Elements](https://docs.katalon.com/katalon-studio/docs/webui-find-web-elements.html)