---
title: "Run TestCloud with Katalon Runtime Engine" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/testcloud-integration-kre.html
---

Katalon TestCloud is a cloud-based test execution environment where you can automate test scripts across the most common and updated browsers and/or operating systems (OS) and/or a combination of both. See: [TestCloud Overview](https://docs.katalon.com/katalon-testcloud/docs/testcloud-overview.html).

From version 8.2.5 onwards, you can run test suites/test suite collections (TS/TSC) with TestCloud in Katalon Runtime Engine (KRE).

You can also configure TestCloud Tunnel to run tests in private domains. For detailed information on TestCloud Tunnel and how to utilize it, see [TestCloud Tunnel](https://docs.katalon.com/katalon-testcloud/docs/testcloud-tunnel.html).

> Requirements:
>
> * Katalon Runtime Engine version 8.2.5 onwards.
> * A Katalon Runtime Engine license.

## Run test suites/test suite collections with TestCloud in Katalon Runtime Engine

To integrate TestCloud with KRE and configure TestCloud Tunnel, use the following Katalonc command-line options:

<table>
	<thead>
		<tr>
			<th><br />No.</th>
			<th><br />Katalonc Command-line Option</th>
			<th><br />Description</th>
			<th><br />Data type</th>
			<th><br />Mandatory</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><br />1</td>
			<td><br />-testcloudEnvironmentId</td>
			<td><br />The ID of the environment which corresponds to a combination of OS, browser type and browser version to execute.<br /><br />Note: This parameter already contains the information about the browser type. Therefore, the browserType parameter is not generated in this integration.</td>
			<td><br />Text</td>
			<td><br />Y</td>
		</tr>
		<tr>
			<td><br />2</td>
			<td><br />-testcloudTunnel</td>
			<td><br />Allow the execution to be performed via a tunnel.</td>
			<td><br />Boolean (case-insensitive)</td>
			<td><br />N</td>
		</tr>
	</tbody>
</table>

> Notes:
>
> * To get the TestCloud environment ID, open Katalon Studio and use the command builder. See: [Generate Command with Command Builder](/katalon-studio/docs/testcloud-integration-kre.html#generate-command-with-command-builder).

## Generate Command with Command Builder

You can use Command Builder in Katalon Studio (KS) to generate commands quickly and precisely.

> Requirements:
>
> You have enabled TestCloud integration in KS. See: [Integrate TestCloud with Studio](/katalon-studio/docs/testcloud-integration.html).

Follow these steps:

1. Open KS and click on the *Build CMD* button in the main toolbar.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/comand-builder-icon.png" alt="Build CMD" width=50% alt="build cmd button">

	The **Generate Command for Console Mode** appears as below.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/kre-executive-platform.png" width=70% alt="generate cmd dialog">

2. Configure your execution as follows:

	* **Test Suite**: select the TS/TSC you want to execute.
	* **Executive Platform**:
		* **Run with**: Click *Edit* to display the **Select an environment** dialog, select **TestCloud**, then click **OK**.

		    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/run-tsc-testcloud-as-environment.png" width=50% alt="run config tsc">
		
			The **Run Configuration** option appears after you choose TestCloud as your test environment.
		
		* **Run Configuration**: Click *Edit* to display the **TestCloud Configuration (Beta)** dialog, select your desired remote OS, browser, and browser version.
		
			<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/tunnel-setup-helper-link.png" width=50% alt="tc config dialog">
			
			> Notes:
			>
			> To run tests using the TestCloud tunnel, check the **Execute with Tunnel for private domain testing** box and refer to [Configure TestCloud Tunnel](https://docs.katalon.com/katalon-studio/docs/testcloud-integration.html#configure-testcloud-tunnel) for detailed instruction.
		
   * **Authentication**: the API key is auto-filled.

> Notes:
>
> For detailed information on the command builder, see [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).

3. Click **Generate Command**.

	The **Generated Command** dialog appears as below.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/generated-command-grey-cover.png" width=70% alt="generate cmd dialog">

	> Notes:
	>
	> After configuring your desired remote OS, browser, and browser version, TestCloud generates a TestCloud environment ID accordingly. You can get this ID in the **Generated Command** dialog (e.g. `-testcloudEnvironmentId="38"`).

	For example, the sample command is:

	```groovy
	./katalonc -noSplash -runMode=console -projectPath=“your_project_path” -retry=0 -testSuitePath=“your_test_suite_path” -browserType=“TestCloud” -testcloudEnvironmentId=“your_testcloud_id” -testcloudTunnel=“false” -executionProfile=“default” -apiKey=“your_api_key” -orgID=your_ogrID --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true
	```

4. Click **Copy to Clipboard** and paste the command to your cmd/terminal for execution.

> Known issues:
>
> When executing tests via TestCloud integration and a proxy, the opening browser step might fail because of an error relevant to Transport Layer Security (TLS).
>
> A workaround for this issue is to pass through the TLS with the below domains on your server:
>
> * All the domains corresponding to this regex: `^testcloud\.katalon\.com$`.
> * The domain of the site under test.