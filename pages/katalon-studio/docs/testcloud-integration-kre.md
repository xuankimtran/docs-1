---
title: "Run TestCloud with Katalon Runtime Engine" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/testcloud-integration-kre.html
---

To run Test Suite/Test Suite Collection (TS/TSC) with TestCloud in Katalon Runtime Engine (KRE), use the following Katalonc Command-line options:

<table data-number-column="true"><colgroup><col /><col /><col /><col /><col /></colgroup>
<tbody>
	<tr>
		<th colspan="1" rowspan="1" data-colwidth="236">
			<div tabindex="0">
				<p data-renderer-start-pos="22683"><strong data-renderer-mark="true">Katalonc Command-line Option</strong></p>
				<figure></figure>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="432">
			<div tabindex="0">
				<p data-renderer-start-pos="22715"><strong data-renderer-mark="true">Description</strong></p>
				<figure></figure>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="139">
			<div tabindex="0">
				<p data-renderer-start-pos="22730"><strong data-renderer-mark="true">Data type</strong></p>
				<figure></figure>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="111">
			<div tabindex="0">
				<p data-renderer-start-pos="22743"><strong data-renderer-mark="true">Mandatory</strong></p>
				<figure></figure>
			</div>
		</th>
	</tr>
	<tr>
		<td>1</td>
		<td colspan="1" rowspan="1" data-colwidth="236">
			<p data-renderer-start-pos="22758">-testcloudEnvironmentId</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="432">
			<p data-renderer-start-pos="22785">ID of the environment which is corresponding to a combination of OS, browser type and browser version to execute.</p>
			<p data-renderer-start-pos="22900"><em data-renderer-mark="true">Notes: This parameter already contains the information about browser type. So browserType parameter is not generated in this integration.</em></p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="139">
			<p data-renderer-start-pos="23041">Text</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="111">
			<p data-renderer-start-pos="23049">Y</p>
		</td>
	</tr>
	<tr>
		<td>2</td>
		<td colspan="1" rowspan="1" data-colwidth="236">
			<p data-renderer-start-pos="23056">-testcloudTunnel</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="432">
			<p data-renderer-start-pos="23076">Allow to the execution is performed via Tunnel.</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="139">
			<p data-renderer-start-pos="23127">Boolean (case-insensitive)</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="111">
			<p data-renderer-start-pos="23157">N</p>
		</td>
	</tr>
</tbody>
</table>

## Override...?