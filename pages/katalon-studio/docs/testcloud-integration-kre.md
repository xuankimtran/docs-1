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
> A KRE version 8.2.5 onwards and a KRE license.

## Run Test Suite/Test Suite Collection with TestCloud in Katalon Runtime Engine

To integrate TestCloud with KRE and configure TestCloud Tunnel, use the following Katalonc command-line options:

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 1684px">
<colgroup>
<col style="width: 118px">
<col style="width: 238px">
<col style="width: 979px">
<col style="width: 260px">
<col style="width: 89px">
</colgroup>
<thead>
  <tr>
    <th class="tg-0lax"> 				<br>Katalonc Command-line Option 			</th>
    <th class="tg-0lax"> 				<br>Description 			</th>
    <th class="tg-0lax"> 				<br>Data type 			</th>
    <th class="tg-0lax" colspan="2"> 				<br>Mandatory 			</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax"> 				<br>1 			</td>
    <td class="tg-0lax"> 				<br>-testcloudEnvironmentId 			</td>
    <td class="tg-0lax"> 				<br>The ID of the environment which corresponds to a combination of OS, browser type and browser version to execute.<br> 				<br>Note: This parameter already contains the information about browser type. So the browserType parameter is not generated in this integration. 			</td>
    <td class="tg-0lax"> 				<br>Text 			</td>
    <td class="tg-0lax"> 				<br>Y 			</td>
  </tr>
  <tr>
    <td class="tg-0lax"> 				<br>2 			</td>
    <td class="tg-0lax"> 				<br>-testcloudTunnel 			</td>
    <td class="tg-0lax"> 				<br>Allow the execution to be performed via a tunnel. 			</td>
    <td class="tg-0lax"> 				<br>Boolean (case-insensitive) 			</td>
    <td class="tg-0lax"> 				<br>N 			</td>
  </tr>
</tbody>
</table>

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

	* **Test Suite**: select TS/TSC you want to execute.
	* **Executive Platform**:
		* **Run with**: Click *Edit* to display the **Select an environment** dialog, select **TestCloud**, then click **OK**. 
		
			The **Run Configuration** option appears after you choose TestCloud for test environment.
		
		* **Run Configuration**: Click *Edit* to display the **TestCloud Configuration (Beta)** dialog, select your desired remote OS, browser, and browser version.
		
		> Notes:
		>
		> To run tests with TestCloud Tunnel, check the **Execute with Tunnel for private domain testing** box and refer to [Configure TestCloud Tunnel](https://docs.katalon.com/katalon-studio/docs/testcloud-integration.html#configure-testcloud-tunnel) for detailed instruction.
		
   * **Authentication**: enter your API key.

> Notes:
>
> For detailed information on Command Builder, see [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).

3. Click **Generate Command**.

	The **Generated Command** dialog appears.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/kre-generate-cmd-dialog.png" width=70% alt="generate cmd dialog">

	The sample command is `./katalonc -noSplash -runMode=console -projectPath="/Users/xuan.tran/Katalon Studio/TW demo TC/test.prj" -retry=0 -testSuitePath="Test Suites/healthcare-tests - TS_RegressionTest" -browserType="TestCloud" -testcloudEnvironmentId="38" -testcloudTunnel="false" -executionProfile="default" -apiKey="your_api_key" -orgID=your_ogrID --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true`

4. Click **Copy to Clipboard** and paste the command to your cmd/terminal for execution.
