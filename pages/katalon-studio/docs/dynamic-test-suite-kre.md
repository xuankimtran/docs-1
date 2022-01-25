---
title: "Execute dynamic test suite on the fly with KRE" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/dynamic-test-suite-kre.html 
redirect_from:
description:
---

A dynamic test suite is a test suite with multiple test cases added via a search query. You can dynamically add additional test cases while running the test suite. You can learn more about the dynamic test suite in this document: [Dynamic test suite in Katalon Studio](https://docs.katalon.com/katalon-studio/docs/dynamic-test-suite-ks.html).

> Requirements:
>
> * Katalon Studio Enterprise version 7.8.2 onwards.
> * Katalon Runtime Engine version 7.8.2 onwards.
> * An active Katalon Runtime Engine license.

> You can download the sample project from our Github repository here: [Dynamic test suite sample](https://github.com/katalon-studio-samples/dynamic-test-suite-sample).

This article shows you how to pass test cases dynamically to a dynamic test suite in Katalon Runtime Engine execution.

## Install the query provider plugin

To enable the query provider for the dynamic test suite, install one of the following plugins from the Katalon Store:

* [Basic Search For Dynamic Test Suite](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite)
* [Test case management with tags](https://store.katalon.com/product/6/Test-Case-Management-with-Tags)

Return to Katalon Studio and activate your plugin. To do so, click on the *Profile* icon, then click **Reload Plugin**. If you want to use the plugin in console mode, refer to this document: [Use Plugins in Console Mode](https://docs.katalon.com/katalon-studio/docs/kse-use-plugins.html#use-plugins-in-console-mode).

## Dynamic test suite parameter

To pass test cases dynamically to a dynamic test suite in Katalon Runtime Engine execution, use the following command-line option:

<table>
	<thead>
		<tr>
			<th><br />Katalonc Command-line Option</th>
			<th><br />Description</th>
			<th><br />Data type</th>
			<th><br />Mandatory</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><br />-testSuiteQuery</td>
			<td><br />Allow overriding the search query of Dynamic Test Suite from CLI.</td>
			<td><br />Text</td>
			<td><br />N</td>
		</tr>
	</tbody>
</table>

> Notes:
>
> * To learn more about supported command-line options, you can refer to this document: [General command-line options](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options).



2. In the **Test Explorer** panel, right-click on **Test Suite**. Select **New > Dynamic Test Suite**.
3. To add test cases via search query, input the search condition into the **Query** box. Then hit **Preview** to query out the matching test cases. To learn more about the search query function, you can refer to this document: [Search test cases](https://docs.katalon.com/katalon-studio/docs/search.html).  
  For example: To add the associated test case into this dynamic test suite, you can input `id=(Test Cases/DDT at TC level)` into the **Query** box. The matched test case appears in the test suite.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Dynamic-Test-suite.png" width="100%" alt="Results after searching query">


## Generate Command with Command Builder

You can use Command Builder in Katalon Studio (KS) to generate commands quickly and precisely.

Follow these steps:

1. Open KS and click on the *Build CMD* button in the main toolbar.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/comand-builder-icon.png" alt="Build CMD" width=50% alt="build cmd button">

	The **Generate Command for Console Mode** appears as below.

   <img src="url" width=70% alt="generate cmd dialog">

2. Configure your execution as follows:

	* **Test Suite**: select the TS/TSC you want to execute.
	* **Executive Platform**:
		* **Run with**: Click *Edit* to display the **Select an environment** dialog, select **TestCloud**, then click **OK**.

		    <img src="url" width=50% alt="run config tsc">

			The **Run Configuration** option appears after you choose TestCloud as your test environment.
		
   * **Authentication**: the API key is auto-filled.

> Notes:
>
> For detailed information on the command builder, see [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).

3. Click **Generate Command**.

	The **Generated Command** dialog appears as below.

    <img src="url" width=70% alt="generate cmd dialog">

	For example, the sample command is:

	```groovy
	./katalonc -noSplash -runMode=console -projectPath="/Users/yen.nguyen/Downloads/dynamic-test-suite-sample-main/test.prj" -retry=0 -testSuitePath="Test Suites/DTS_Verify Successful Login and Appointment" -browserType="Chrome" -executionProfile="default" -apiKey="<api-key>" --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true
	```

4. Click **Copy to Clipboard** and paste the command to your cmd/terminal for execution.


