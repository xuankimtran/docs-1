---
title: "Create dynamic test suite on the fly with Katalon Runtime Engine" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/dynamic-test-suite-kre.html 
redirect_from:
description:
---

A dynamic test suite is a test suite with multiple test cases added via a search query. You can dynamically add additional test cases while running the test suite. To learn more about the dynamic test suite, you can refer to this document: [Dynamic test suite in Katalon Studio](https://docs.katalon.com/katalon-studio/docs/dynamic-test-suite-ks.html).

From Katalon Studio version 7.8.2 onwards, you can create a dynamic test suite on the fly with Katalon Runtime Engine (KRE). This article guides you on how to do so.

> Requirements:
>
> * Katalon Studio Enterprise version 7.8.2 onwards.
> * Katalon Runtime Engine version 7.8.2 onwards.
> * An active Katalon Runtime Engine license.

> You can download the sample project from our Github repository here: [Dynamic test suite sample](https://github.com/katalon-studio-samples/dynamic-test-suite-sample).

## Enable the query provider

To enable the query provider for the dynamic test suite, install one of the following plugins from the Katalon Store:

* [Basic Search For Dynamic Test Suite](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite)
* [Test case management with tags](https://store.katalon.com/product/6/Test-Case-Management-with-Tags)

Return to Katalon Studio and activate your plugin. To do so, click on the *Profile* icon, then click **Reload Plugin**. 

> Notes:
>
> * To use plugins in console mode, while generating commands, use the API Key of the users who have the plugin installed. Both API key command-line options work, either `-apiKey=<Your_API_Key>` or `-apikey=<Your_API_Key>`.
> * From version 7.7.0 onwards, if you belong to more than one Organization subscribing to Runtime Engine licenses, you can choose which Organization validates your license usage with the following command line: `-orgID=<Katalon_OrgID>`.

## Pass a search query in KRE

To pass a search query in KRE, use the following command-line option:

<table>
	<thead>
		<tr>
			<th>Katalonc Command-line Option</th>
			<th>Description</th>
			<th>Mandatory</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>-testSuiteQuery="&lt;search-query&gt;"</td>
			<td>- Allow overriding the search query of the dynamic test suite from the CLI.<br>-Input <code>&lt;search-query&gt;</code> as the query syntax of the installed plugin.<br>Example: <br><code>-testSuiteQuery="ids=(Test Cases/TC1_Verify Successful Login,Test Cases/TC2_Verify Successful Appointment)"</code></td>
			<td>N</td>
		</tr>
	</tbody>
</table>

> Notes:
>
> * To learn more about supported command-line options in KRE, you can refer to this document: [General commands](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options).

## Create dynamic test suite on the fly with KRE

### Create a new dynamic test suite

To create a new dynamic test suite, in the **Test Explorer** panel, right-click at the **Test Suites** folder > **New** > **Dynamic Test Suite**. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Create-a-new-dynamic-test-suite.png" width="70%" alt="Create a dynamic test suite">

Here, we name the test suite **DTS_Verify Successful Login and Appointment**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-kre/KS-8.2.5-Name-DTS.png" width="70%" alt="Name a dynamic test suite">

### Generate commands with Command Builder

You can use Command Builder in Katalon Studio (KS) to generate commands quickly and precisely.

Follow these steps:

1. Click on the *Build CMD* button in the main toolbar. The **Generate Command for Console Mode** dialog appears.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/comand-builder-icon.png" alt="Build CMD" width=50% alt="build cmd button">

2. Configure your execution as follows:

	2.1. **Test Suite**: select the dynamic test suite you want to execute. Here, we want to execute the **DTS_Verify Successful Login and Appointment** dynamic test suite.
	2.2. **Executive Platform**: Click **Edit** in each field to choose the environment and execution profile you want to execute with. Here, we choose Chrome and the **default** execution profile.
    2.3. **Authentication**: the API key is auto-generated.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-kre/KS-8.2.5-Command-builder.png" width=70% alt="generate cmd dialog">

    > Notes:
    >
    > For detailed information on the command builder, see [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).

3. Click **Generate Command**. The **Generated Command** dialog appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-kre/KS-8.2.5-Generated-command.png" width=70% alt="generate cmd dialog">

	For example, the sample command is:

	```groovy
	./katalonc -noSplash -runMode=console -projectPath="/Users/HTK/Downloads/dynamic-test-suite-sample-main/test.prj" -retry=0 -testSuitePath="Test Suites/DTS_Verify Successful Login and Appointment" -browserType="Chrome" -executionProfile="default" -apiKey="<api-key>" --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true
	```

4. Click **Copy to Clipboard**. Open the KRE folder in the cmd or terminal, then paste the generated command to your cmd/terminal.
### Pass a search query to the CLI for dynamic test suite execution

To pass the search query to the CLI for the dynamic test suite execution, add the `-testSuiteQuery` parameter to the generated command. For example, we want to execute the **TC1_Verify Successful Login** and **TC2_Verify Successful Appointment** test cases in the dynamic test suite, we add the `-testSuiteQuery` parameter as follows:

``` groovy
./katalonc -noSplash -runMode=console -projectPath="/Users/HTK/Downloads/dynamic-test-suite-sample-main/test.prj" -retry=0 -testSuitePath="Test Suites/DTS_Verify Successful Login and Appointment" -browserType="Chrome" -executionProfile="default" -apiKey="<api-key>" --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -testSuiteQuery="ids=(Test Cases/TC1_Verify Successful Login,Test Cases/TC2_Verify Successful Appointment)"
```

With this parameter, KRE overrides the current search query of the dynamic test suite and execute the stated search query in the CLI instead.

> Notes:
>
> * You can search one or more test cases by the test case IDs, separate them by commas.
> * You can only search for one keyword at a time when searching by tag, description, or comment.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-kre/KS-8.2.5-Command-line-terminal.png" width=70% alt="generate cmd dialog">

### Execute the dynamic test suite in KRE

After generating your commands, hit **Enter** to execute the dynamic test suite.

> Notes:
> * Make sure to update the browser by clicking **Tools > Update WebDrivers > Choose browser**. You can learn more about updating webdrivers here: [Update or Downgrade WebDrivers](https://docs.katalon.com/katalon-studio/docs/update-or-downgrade-webdrivers.html).

## Test reports

After the test suite execution, to view your test reports, go to the **Reports** folder in the **Test Explorer** panel.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-kre/KS-8.2.5-view-reports.png" width=100% alt="View reports">

Alternatively, you can also view your reports and details in `<your-project-folder>/Reports`. Katalon Studio supports exporting test reports into different formats, such as HTML, CSV, PDF, and JUnit. You can learn more about exporting reports here: [Generate reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html#report-history).

> Notes:
> 
> * For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).




