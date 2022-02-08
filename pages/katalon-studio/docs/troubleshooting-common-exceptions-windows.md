---
title: "Troubleshoot common exceptions when executing Windows tests"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/troubleshoot-common-execution-exceptions-windows.html
redirect_from:
---

> Tips
>
> * To find the exceptions and errors you encountered, use **Ctrl+F**.
> * If you cannot find the exceptions or error message you encountered, you can leave a comment below for further support.

<table>
	<thead>
		<tr>
			<th>Issue</th>
			<th>Solution</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Handling Splash screen</td>
			<td>
				<ul>
					<li>If your app has splash screens, do as follows:<br>
						- Install WinAppDriver version 1.2 onwards. You can download the latest WinAppDriver version from the WinAppDriver Github project here: <a title="https://github.com/microsoft/WinAppDriver" href="https://github.com/microsoft/WinAppDriver" data-renderer-mark="true">WinAppDriver</a>.<br>
						- Install Appium version 1.16.0 onwards. Follow the instruction in the Appium document to install the latest Appium version: <a title="http://appium.io/docs/en/about-appium/getting-started/#installing-appium" href="http://appium.io/docs/en/about-appium/getting-started/#installing-appium" data-renderer-mark="true">Getting started</a>.<br>
						- In Katalon Studio, go to <strong>Project Settings &gt; Desired capabilities &gt; Windows</strong>&nbsp;and add this desired capability: <code>"ms:waitForAppLaunch": "25"</code></li>
				</ul>
				<ul>
					<li>If your app does not have splash screens, in the <strong>Application Title</strong> field, add the application title and start again.</li>
					<li>To record your actions more easily, consider using&nbsp;<strong>Native Windows Recorder</strong>.</li>
				</ul>
			</td>
		</tr>
		<tr>
			<td>Timeout when launching Windows application</td>
			<td>1. Close all unneeded apps and opened folders. Open Katalon Studio only.
				<p>2. Remove unused shortcuts on your desktop and your taskbar.</p>
				<p>3. Use&nbsp;<strong>Windows.startApplication(&hellip;)</strong>&nbsp;instead of&nbsp;<strong>Windows.startApplicationWithTitle(&hellip;)</strong>&nbsp;</p>
				<pre><code>Windows.startApplication('C:\\Users\\katalon\\Desktop\\Demo\\WindowsFormsApp.exe') Windows.switchToWindowTitle('Main App Title') // Replace this by your main window title</code></pre>
			</td>
		</tr>
		<tr>
			<td>WinAppDriver could not sendKeys with correctly text when the default setting is German keyboard&nbsp;</td>
			<td>Clone or download our demo project at our repository: <a href="https://github.com/duyluonganh/kat-german-windows-test">German Windows test</a>.&nbsp;</td>
		</tr>
		<tr>
			<td>
				<p data-renderer-start-pos="757">Unable to Start Application</p>
			</td>
			<td>
				<ul>
					<li>Use this keyword to start the application:&nbsp;<a tabindex="0" href="https://docs.katalon.com/katalon-studio/docs/windows-kw-start-app-title.html" data-testid="inline-card-resolved-view">[Windows] Start Application with Title</a>.</li>
				</ul>
				<ul data-indent-level="1">
					<li>
						<p data-renderer-start-pos="137">Or: Use capability <a title="https://github.com/microsoft/WinAppDriver/releases/tag/v1.2-RC" href="https://github.com/microsoft/WinAppDriver/releases/tag/v1.2-RC" data-renderer-mark="true"><strong data-renderer-mark="true">ms:waitForAppLaunch</strong></a> to wait longer for the app to open.</p>
					</li>
				</ul>
			</td>
		</tr>
	</tbody>
</table>

> The exception you are looking for is not on this page?
>
> Leave a comment below.
