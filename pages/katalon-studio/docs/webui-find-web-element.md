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

