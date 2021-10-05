---
title: "[WS] Set HAR File Generation" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/ws-set-har-file-generation.html 
redirect_from:
description: 
---

## Description

Katalon Studio generates HAR files for each Web Service request by default. From version 8.2.0 onwards, you can use the `setHarFileGeneration` keyword to enable or disable HAR file generation globally.

## Parameters

<table data-number-column="false">
	<tbody>
		<tr>
			<th colspan="1" rowspan="1">
				<p data-renderer-start-pos="874"><strong data-renderer-mark="true">Parameter</strong></p>
			</th>
			<th colspan="1" rowspan="1">
				<p data-renderer-start-pos="897"><strong data-renderer-mark="true">Parameter Type</strong></p>
			</th>
			<th colspan="1" rowspan="1">
				<p data-renderer-start-pos="905"><strong data-renderer-mark="true">Mandatory</strong></p>
			</th>
			<th>
				<p data-renderer-start-pos="905"><strong data-renderer-mark="true">Description</strong></p>
			</th>
		</tr>
		<tr>
			<td colspan="1" rowspan="1">
				<p data-renderer-start-pos="921"><strong data-renderer-mark="true">enable</strong></p>
			</td>
			<td colspan="1" rowspan="1">
				<p data-renderer-start-pos="988">boolean</p>
			</td>
			<td colspan="1" rowspan="1">
				<p data-renderer-start-pos="999">Required</p>
			</td>
			<td>Enable or disable HAR file generation.</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="1">
				<p data-renderer-start-pos="1008"><strong data-renderer-mark="true">flowControl</strong></p>
			</td>
			<td colspan="1" rowspan="1">
				<p data-renderer-start-pos="1074">FailureHandling</p>
			</td>
			<td colspan="1" rowspan="1">
				<p data-renderer-start-pos="1093">Optional</p>
			</td>
			<td>Specify <a href="https://docs.katalon.com/katalon-studio/docs/failure-handling.html">failure handling</a> schema to determine whether the execution should be allowed to continue or stop.</td>
		</tr>
	</tbody>
</table>

> Exception:
>
> If Katalon Studio could not save the setting, throw: **StepFailedException**.

### Returns

<table data-number-column="false">
	<tbody>
		<tr>
			<th colspan="1" rowspan="1" data-colwidth="480">
				<div tabindex="0">
					<p data-renderer-start-pos="2146"><strong data-renderer-mark="true">Parameter Type</strong></p>
				</div>
			</th>
			<th colspan="1" rowspan="1" data-colwidth="480">
				<div tabindex="0">
					<p data-renderer-start-pos="2164"><strong data-renderer-mark="true">Description</strong></p>
				</div>
			</th>
		</tr>
		<tr>
			<td colspan="1" rowspan="1" data-colwidth="480">
				<p data-renderer-start-pos="2181">boolean</p>
			</td>
			<td colspan="1" rowspan="1" data-colwidth="480">
				<ul data-indent-level="1">
					<li><code data-renderer-mark="true">true</code><strong data-renderer-mark="true">:</strong>&nbsp;enable HAR file generation.</li>
				</ul>
				<ul data-indent-level="1">
					<li>
						<p data-renderer-start-pos="2256"><code data-renderer-mark="true">false</code><strong data-renderer-mark="true">:&nbsp;</strong>disable HAR file generation.</p>
					</li>
				</ul>
			</td>
		</tr>
	</tbody>
</table>

### Example

* Disable HAR file generation:

```groovy
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS

'Do not generate har file when sending a request.'
WS.setHarFileGeneration(false)
```

* Enable HAR file generation:

``` groovy
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS

'Generating har file when sending a request. This is the default setting.'
WS.setHarFileGeneration(true)
```

To check whether the HAR file generation option is enabled or not, see [[WS] Get HAR File Generation](https://docs.katalon.com/katalon-studio/docs/ws-get-HAR-file-generation.html).