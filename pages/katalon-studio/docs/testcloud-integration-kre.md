---
title: "Run TestCloud with Katalon Runtime Engine" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/testcloud-integration-kre.html
---

Katalon TestCloud is a cloud-based test execution environment where you can automate test scripts across the most common and updated browsers and/or operating systems (OS) and/or a combination of both. See: [TestCloud Overview](https://docs.katalon.com/katalon-testcloud/docs/testcloud-overview.html).

From version 8.2.5 onwards, you can run Test Suite/Test Suite Collection (TS/TSC) with TestCloud in Katalon Runtime Engine (KRE).

You can also configure TestCloud Tunnel to run tests in private domains. For detailed information on TestCloud Tunnel and how to utilize it, see [TestCloud Tunnel](https://docs.katalon.com/katalon-testcloud/docs/testcloud-tunnel.html).

> Requirements:
>
> You have installed KRE. See: [Install Runtime Engine](https://docs.katalon.com/katalon-studio/docs/install-RE.html).

## Run Test Suite/Test Suite Collection with TestCloud in Katalon Runtime Engine

To integrate TestCloud with KRE and configure TestCloud Tunnel, use the following Katalonc command-line options:

<table>
	<tbody>
		<tr>
			<td>
				<p><strong>Katalonc Command-line Option</strong></p>
			</td>
			<td>
				<p><strong>Description</strong></p>
			</td>
			<td>
				<p><strong>Data type</strong></p>
			</td>
			<td>
				<p><strong>Mandatory</strong></p>
			</td>
		</tr>
		<tr>
			<td>
				<p>1</p>
			</td>
			<td>
				<p>-testcloudEnvironmentId</p>
			</td>
			<td>
				<p>The ID of the environment which corresponds to a combination of OS, browser type and browser version to execute.</p>
				<p><em>Note: This parameter already contains the information about browser type. So the browserType parameter is not generated in this integration.</em></p>
			</td>
			<td>
				<p>Text</p>
			</td>
			<td>
				<p>Y</p>
			</td>
		</tr>
		<tr>
			<td>
				<p>2</p>
			</td>
			<td>
				<p>-testcloudTunnel</p>
			</td>
			<td>
				<p>Allow the execution to be performed via a tunnel.</p>
			</td>
			<td>
				<p>Boolean (case-insensitive)</p>
			</td>
			<td>
				<p>N</p>
			</td>
		</tr>
	</tbody>
</table>

## Override with Command Builder

You can use Command Builder to generate commands quickly and precisely.

Follow these steps:

1. Open KS and click on the *Build CMD* button in the main toolbar.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/console-mode-execution/Screenshot-at-Jun-20-15-42-46.png" alt="Build CMD" width=50% alt="build cmd button">

	The **Generate Command for Console Mode** appears as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/TestCloud-KRE.png" width=100% alt="generate cmd dialog">

2. Configure your execution as follows:

	* **Test Suite**: select TS/TSC you want to execute.
	* **Executive Platform**: choose TestCloud for the test environment in **Run with** and select the execution profile in **Profile**.
    * **Override the execution profile and environment**: specify `-BrowserType` in the command to override the browser type and run tests with TestCloud.
	
		> Notes:
		>
		>  This function is available from version 7.6.0 onwards.

   * **Authentication**: enter your API key.

> Notes:
>
> For detailed information on Command Builder, see [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).

3. Click **Generate Command**.

	The **Generated Command** dialog appears. 
4. Click **Copy to Clipboard** and paste the command to your cmd/terminal for execution.
