---
title: "[Mobile] Wait For Element Not Present" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-wait-for-element-not-present.html 
redirect_from:
description: 
---
## Description

Wait for the given element to NOT be present within the given time (in seconds).

>**Requirements**:
>
> Katalon Studio version 8.1.0 onwards.

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
					<p data-renderer-start-pos="1783">If timeout &gt; 0, Katalon Studio waits <code data-renderer-mark="true">timeout</code> to return a result.</p>
				</li>
				<li>
					<p data-renderer-start-pos="1837">If timeout = 0, Katalon Studio uses the default wait for element timeout in Project Settings.</p>
				</li>
				<li>
					<p data-renderer-start-pos="1922">If timeout &lt; 0, Katalon Studio throws <code data-renderer-mark="true">IllegalArgumentException</code>.</p>
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
				<div>Failure handling is currently not supported for this mobile keyword.</div>
			</div>
			<p data-renderer-start-pos="2021">Specify&nbsp;<a title="https://docs.katalon.com/x/qAAM" href="https://docs.katalon.com/x/qAAM" data-renderer-mark="true">failure handling</a>&nbsp;schema to determine whether the execution should be allowed to continue or stop.</p>
		</td>
	</tr>
</tbody>
</table>

> See also: [Understand waiting keywords](https://docs.katalon.com/katalon-studio/docs/understand-waiting-keywords.html)
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

In this example, for 10 seconds or until true, wait for the Accessibility element to be gone, then continue testing. If the Accessibility element is still present, mark as failed and continue.

```groovy
//Start Application
Mobile.startApplication(GlobalVariable.G_AndroidApp, false)
// Wait for the first element to present 
Mobile.waitForElementPresent(findTestObject('Application/android.widget.TextView - Accessibility'), 10)
// Verify if the element's text is correct
Mobile.verifyElementText(findTestObject('Application/android.widget.TextView - Accessibility'), 'Accessibility', FailureHandling.CONTINUE_ON_FAILURE)
//Tap on OS
Mobile.tap(findTestObject('Object Repository/Application/android.widget.TextView - OS'), 0)
//Wait for the Accessibility element to be gone on the next screen
Mobile.waitForElementNotPresent(findTestObject('Application/android.widget.TextView - Accessibility'), 10)
//Then tap on MMS Messaging element
Mobile.tap(findTestObject('Object Repository/Application/android.widget.TextView - MMS Messaging '), 0)
```
