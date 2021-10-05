---
title: "[WS] Get HAR File Generation" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/ws-get-har-file-generation.html 
redirect_from:
description: 
---

## Description

With this keyword, you can check whether HAR file generation is enabled or disabled.

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
> If Katalon Studio could not get the setting, throw: **StepFailedException**.

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
					<li><code data-renderer-mark="true">true</code>: HAR file generation is enabled.</li>
				</ul>
				<ul data-indent-level="1">
					<li>
						<p data-renderer-start-pos="2256"><code data-renderer-mark="true">false</code>: HAR file generation is disabled.</p>
					</li>
				</ul>
			</td>
		</tr>
	</tbody>
</table>

### Example

```groovy
boolean isHarFileGenerationEnabled = WS.getHarFileGeneration()
println isHarFileGenerationEnabled
```

To enable or disable HAR file generations on demand, see [[WS] Set HAR File Generation](https://docs.katalon.com/katalon-studio/docs/ws-set-HAR-file-generation.html).