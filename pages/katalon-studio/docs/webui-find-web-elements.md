---
title: "[WebUI] Find Web Elements" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-find-web-elements.html 
redirect_from:
description: 
---

## Description

Find web elements by test object.

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

The found web elements or `null` if cannot find any.

## Example

You want to find all social networking icons on the [https://katalon-demo-cura.herokuapp.com/](https://katalon-demo-cura.herokuapp.com/) demo website using a test object.

``` groovy

import com.kms.katalon.core.testobject.ConditionType as ConditionType
import com.kms.katalon.core.util.KeywordUtil
import org.openqa.selenium.WebElement
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.testobject.TestObject as TestObject
​
WebUI.openBrowser('https://katalon-demo-cura.herokuapp.com/')
// Wait for the browser to be stable
WebUI.delay(3)
​
TestObject testObj = findTestObject('icon_Social_networking')
List<WebElement> elements = WebUI.findWebElements(testObj, 10)
for (int i = 0;  i < elements.size(); ++i) {
	KeywordUtil.logInfo(elements.get(i).toString())
}
```

**See also**:
* [[WebUI] Find Web Element](https://docs.katalon.com/katalon-studio/docs/webui-find-web-element.html)