---
title: "[Mobile] Wait For Element Not Present" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-wait-for-element-not-present.html 
redirect_from:
description: 
---
From version 8.1.0 onwards, Katalon Studio provides the conditional waiting keyword for Mobile testing as in WebUI. See [[WebUI] Wait For Element Not Present](https://docs.katalon.com/katalon-studio/docs/webui-wait-for-element-not-present.html).

To set conditional waiting when executing the Mobile test in script, use the keyword ``waitForElementNotPresent``.

## Description

<table data-number-column="false"><colgroup><col /><col /></colgroup>
<tbody>
	<tr>
		<th colspan="1" rowspan="1" data-colwidth="565">
			<div tabindex="0">
				<p data-renderer-start-pos="1344"><strong data-renderer-mark="true">Syntax</strong></p>
				<figure></figure>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="395">
			<div tabindex="0">
				<p data-renderer-start-pos="1354"><strong data-renderer-mark="true">Description</strong></p>
				<figure></figure>
			</div>
		</th>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="565">
			<p data-renderer-start-pos="1371"><code data-renderer-mark="true">Mobile.waitForElementNotPresent(to, timeout, flowControl) boolean</code></p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="395">
			<p data-renderer-start-pos="1440">Wait for the given element to <strong data-renderer-mark="true">NOT</strong> present (appear)&nbsp;within&nbsp;the given time (in seconds).&nbsp;</p>
		</td>
	</tr>
</tbody>
</table>

## Parameters

<table data-number-column="false"><colgroup><col /><col /><col /><col /></colgroup>
<tbody>
	<tr>
		<th colspan="1" rowspan="1" data-colwidth="176">
			<div tabindex="0">
				<p data-renderer-start-pos="1550"><strong data-renderer-mark="true">Parameter</strong></p>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="174">
			<div tabindex="0">
				<p data-renderer-start-pos="1563"><strong data-renderer-mark="true">Parameter Type</strong></p>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="133">
			<div tabindex="0">
				<p data-renderer-start-pos="1581"><strong data-renderer-mark="true">Mandatory</strong></p>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="477">
			<div tabindex="0">
				<p data-renderer-start-pos="1594"><strong data-renderer-mark="true">Description</strong></p>
			</div>
		</th>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="176">
			<p data-renderer-start-pos="1611"><code data-renderer-mark="true">to</code></p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="174">
			<p data-renderer-start-pos="1617">TestObject</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="133">
			<p data-renderer-start-pos="1631">Required</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="477">
			<p data-renderer-start-pos="1638">Represent a mobile element.</p>
		</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="176">
			<p data-renderer-start-pos="1671"><code data-renderer-mark="true">timeout</code></p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="174">
			<p data-renderer-start-pos="1682">Integer</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="133">
			<p data-renderer-start-pos="1693">Required</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="477">
			<p data-renderer-start-pos="1700">The maximum period of time in <strong data-renderer-mark="true">seconds</strong> that system will wait to return a result.</p>
			<ul data-indent-level="1">
				<li>
					<p data-renderer-start-pos="1783">If timeout &gt; 0 KS wait <code data-renderer-mark="true">timeout</code> to return a result.</p>
				</li>
				<li>
					<p data-renderer-start-pos="1837">If timeout = 0, KS uses the default wait for element timeout in Project Settings.</p>
				</li>
				<li>
					<p data-renderer-start-pos="1922">If timeout &lt; 0, KS throws <code data-renderer-mark="true">IllegalArgumentException</code>.</p>
				</li>
			</ul>
		</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="176">
			<p data-renderer-start-pos="1981"><code data-renderer-mark="true">flowControl</code></p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="174">
			<p data-renderer-start-pos="1996">FailureHandling</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="133">
			<p data-renderer-start-pos="2015">Optional</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="477">
			<div>
				<div><strong>Notes</strong>: Failure handling is currently not supported for this mobile keyword.</div>
			</div>
			<p data-renderer-start-pos="2021">Specify&nbsp;<a title="https://docs.katalon.com/x/qAAM" href="https://docs.katalon.com/x/qAAM" data-renderer-mark="true">failure handling</a>&nbsp;schema to determine whether the execution should be allowed to continue or stop.</p>
		</td>
	</tr>
</tbody>
</table>

## Returns

<table data-number-column="false"><colgroup><col /><col /></colgroup>
<tbody>
	<tr>
		<th colspan="1" rowspan="1" data-colwidth="480">
			<div tabindex="0">
				<p data-renderer-start-pos="2146"><strong data-renderer-mark="true">Parameter Type</strong></p>
				<figure></figure>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="480">
			<div tabindex="0">
				<p data-renderer-start-pos="2164"><strong data-renderer-mark="true">Description</strong></p>
				<figure></figure>
			</div>
		</th>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="480">
			<p data-renderer-start-pos="2181">boolean</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="480">
			<ul data-indent-level="1">
				<li>
					<p data-renderer-start-pos="2194"><code data-renderer-mark="true">true</code><strong data-renderer-mark="true">:</strong>&nbsp;the element is <strong data-renderer-mark="true">NOT</strong> present within the given timeout.</p>
				</li>
				<li>
					<p data-renderer-start-pos="2256"><code data-renderer-mark="true">false</code><strong data-renderer-mark="true">:&nbsp;</strong>the element is present within the given timeout.</p>
				</li>
			</ul>
		</td>
	</tr>
</tbody>
</table>

## Example

You want to wait for 'App' control to not be present in 10 seconds timeout.

```groovy

import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import internal.GlobalVariable as GlobalVariable

'Start application on current selected android\'s device'
Mobile.startApplication(GlobalVariable.G_AndroidApp, false)

'Wait for app control to not be present in 10 seconds timeout'
Mobile.waitForElementNotPresent(findTestObject('Object Repository/Application/android.widget.TextView - App'), 10)

'Close application on current selected android\'s device'
Mobile.closeApplication()
```
