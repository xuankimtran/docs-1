---
title: "Create dynamic test suite at runtime" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/dynamic-test-suite-kre.html 
redirect_from:
description:
---

A dynamic test suite is a test suite with multiple test cases added via a search query. You can dynamically add additional test cases while running the test suite. To learn more about dynamic test suites in Katalon Studio, you can refer to this document: [Dynamic test suite in Katalon Studio](https://docs.katalon.com/katalon-studio/docs/dynamic-test-suite-ks.html).

From Katalon Studio version 7.8.2 onwards, you can create a dynamic test suite at runtime with Katalon Runtime Engine (KRE). This article guides you on how to do so.

> Requirements:
>
> * Katalon Studio Enterprise version 7.8.2 onwards.
> * Katalon Runtime Engine version 7.8.2 onwards.
> * An active Katalon Runtime Engine license.

> You can download the sample project from our Github repository: [Dynamic test suite sample](https://github.com/katalon-studio-samples/dynamic-test-suite-sample).

## Enable the Query Provider

The **Query Provider** is to provide the query syntax to search test artifacts within the dynamic test suite.
When you implement the dynamic test suite for the first time, the **Query Provider** is set to **No query provider available** by default.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-querying-test-suite/dynamic-ts.png" width="100%" alt="The default state of the query provider">

To enable the query provider for the dynamic test suite, install one of the following plugins from the Katalon Store:

* [Basic Search For Dynamic Test Suite](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite)
* [Test case management with tags](https://store.katalon.com/product/6/Test-Case-Management-with-Tags)

Return to Katalon Studio and activate your plugin. To do so, click on the *Profile* icon, then click **Reload Plugin**. 

> Notes:
>
> * To use plugins in console mode, while generating commands, use the API Key of the users who have the plugin installed. Both API key command-line options work, either `-apiKey=<Your_API_Key>` or `-apikey=<Your_API_Key>`.
> * From version 7.7.0 onwards, if you belong to more than one Organization subscribing to Runtime Engine licenses, you can choose which Organization validates your license usage with the following command line: `-orgID=<Katalon_OrgID>`.

After you successfully activate the plugin, the **Query Provider** automatically applies the query syntax of the installed plugin. For example, after activating the **Test Case Management with Tags** plugin, the **Query Provider** is set to **Advanced Tag Search**. You can now add test cases for dynamic test suite execution.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-kre/KS-8.2.5-The-query-provider.png" width="100%" alt="The query provider in the dynamic test suite">

## Create dynamic test suite at runtime with KRE
### Create a new dynamic test suite

Open Katalon Studio and create a new dynamic test suite. In the **Test Explorer** panel, right-click at the **Test Suites** folder > **New** > **Dynamic Test Suite**. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-ks/KS-DYNAMIC-Create-a-new-dynamic-test-suite.png" width="70%" alt="Create a dynamic test suite">

The **New** dialog opens. Name the dynamic test suite. Here, we name the test suite **DTS_Verify Successful Login and Appointment**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-kre/KS-8.2.5-Name-DTS.png" width="70%" alt="Name a dynamic test suite">

### Generate commands with the command builder

You can use the command builder in Katalon Studio (KS) to generate commands quickly and precisely.

Follow these steps:

1. Click on the *Build CMD* button in the main toolbar. The **Generate Command for Console Mode** dialog appears.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/studio-integration/comand-builder-icon.png" alt="Build CMD" width=50% alt="build cmd button">

2. Configure your execution as follows:

	2.1. **Test Suite**: select the dynamic test suite you want to execute. Here, we want to execute the **DTS_Verify Successful Login and Appointment** dynamic test suite.
	
	2.2. **Executive Platform**: Click **Edit** in each field to choose the environment and execution profile you want to execute with. Here, we select Chrome and the **default** execution profile.
    
	2.3. **Authentication**: 
	
	- **Katalon API key**: the API key is auto-generated. 
	- **Katalon Organization**: Select the Organization that validates your license usage.

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

4. Click **Copy to Clipboard**. Open the KRE folder in the command prompt or terminal, then paste the generated command to your cmd/terminal.

### Pass the search query to the CLI for dynamic test suite execution

To pass the search query to the CLI for the dynamic test suite execution, add the `-testSuiteQuery` parameter to the generated command. You can learn more about the `-testSuiteQuery` parameter in this document: [General commands](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options).

For example, we want to execute the **TC1_Verify Successful Login** and **TC2_Verify Successful Appointment** test cases in the dynamic test suite, we add the `-testSuiteQuery` parameter as follows:

``` groovy
./katalonc -noSplash -runMode=console -projectPath="/Users/HTK/Downloads/dynamic-test-suite-sample-main/test.prj" -retry=0 -testSuitePath="Test Suites/DTS_Verify Successful Login and Appointment" -browserType="Chrome" -executionProfile="default" -apiKey="<api-key>" --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -testSuiteQuery="ids=(Test Cases/TC1_Verify Successful Login,Test Cases/TC2_Verify Successful Appointment)"
```

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-kre/KS-8.2.5-Command-line-terminal.png" width=70% alt="generate cmd dialog">

> Notes:
>
> * Suppose the associated dynamic test suite has an existing search query. In that case, the `-testSuiteQuery` parameter overrides the current search query and executes the dynamic test suite with the stated search query in the CLI instead.
> * You can add one or more test cases via the search query by test case IDs and separate them by commas.
> * You can only search for one keyword at a time when searching by tag, description, or comment.

### Execute the dynamic test suite in KRE

After finalizing parameters in your command, hit **Enter** to execute the dynamic test suite.

> Notes:
> * Make sure to update the browser by clicking **Tools > Update WebDrivers > Choose browser**. You can learn more about updating webdrivers here: [Update or Downgrade WebDrivers](https://docs.katalon.com/katalon-studio/docs/update-or-downgrade-webdrivers.html).

## Test reports

After the test suite execution, to view your test reports, go to the **Reports** folder in the **Test Explorer** panel.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/dynamic-test-suite-kre/KS-8.2.5-view-reports.png" width=100% alt="View reports">

Alternatively, you can also view your reports and details in `<your-project-folder>/Reports`. Katalon Studio supports exporting test reports into different formats, such as HTML, CSV, PDF, and JUnit. You can learn more about exporting reports here: [Generate reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html#report-history).

> Notes:
> 
> * For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).




