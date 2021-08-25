---
title: "Integration with Azure DevOps Test Plans"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/azure-devops-test-plans.html
redirect_from:
    - "/katalon-studio/docs/azure-devops-integration.html"

description: 
---

> In 8.1.0+, you can submit test run with Release information to Azure.

Katalon Studio can be natively integrated with Azure Test Plans service of Azure DevOps (ADO). This integration will help you:

1. Establish a connection between a Katalon Studio project and ADO project.
2. Easily map ADO Test Cases to automated Test Cases in Katalon Studio.
3. Automatically submit test run and test results to ADO with execution logs, reports, and images for analysis.

**Requirements**

* Katalon Studio version 8.0.0.
* An active Katalon Studio Enterprise license.
* Azure Test Plans having already been set up.

## Enable the Integration and Perform Authentication

In Project Settings, you need to enable the integration and authenticate your project with Azure Server to allow retrieving relevant test artifacts and creating test runs and results. Go to **Project > Settings > Integrations > Azure DevOps**:

1. Select **Enable Intergration** to enable **Authentication** area for editting.

2. Enter your credentials. Your credentials are encrypted by default.

    - **Server URL**: `https://dev.azure.com/{yourorganization}`
    - **Personal Access Token**: your [Personal Access Token](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page). We recommend you to create a Personal Access Token with full-access [scopes](https://docs.microsoft.com/en-us/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#scopes).

3. Click **Connect** to verify whether the connection to Azure Server is successful.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/authentication.png" width=70%>

## Configure the Integration

### Step 1: Select a Project for submitting test run and results

After successfully authenticating your project with Azure Server, select an ADO project among those you have access to in the drop-down list of **Project**.

Hit **Fetch Project** to retrieve the latest projects list.

The **Test Artifacts Mapping** and **Submission Option** fieldsets are expanded automatically after you select a project.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/expand-both.png" width=70%>

### Step 2: Map Test Artifacts between two systems

You can **Add** or **Remove** item(s) in each section to serve your need.

**In the Execution Status Mapping**: Match test results in Katalon Studio with test outcomes in ADO.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/status-mapping.png" width=70%>

**In the Test Configuration Mapping**: This step is to help reducing the number of Test Results created for each mapped test case. You need to pair **Execution OS/Device** and **Execution Browser/App** in Katalon Studio with Test Configurations retrieved from Azure Test Plans.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/test-configuration-mapping.png" width=70%>

> **What is Test Point?**
>
> A test point is **a unique combination of a test case, test suite, configuration, and tester**. Test cases by themselves are not executable. When you add a test case to a test suite, test point(s) are generated. [Learn more](https://docs.microsoft.com/en-us/azure/devops/test/new-test-plans-page?view=azure-devops#execute-tab)
>
> **What is Test Configuration?**
>
> A Test Configuration is **a combination of configuration variable values**, containing information of operating system, browser, CPU type, database. For example: "Windows 8 + 32-bit CPU" or "Windows 10 + 64-bit CPU." [Learn more](https://docs.microsoft.com/en-us/azure/devops/test/test-different-configurations?view=azure-devops)

### Step 3. Configure Submission Options

1. Select a test plan for test run to be submitted. Hit **Fetch Test Plans** to retrieve latest test plans list.

   <img alt="Submission Options 8.1.0" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/Submission-option-8.1.0.png" width=70%>

2. Name test run.

3. If you want to add Build and Release Information to test runs, specify **Build Definition ID** and **Release Definition ID** respectively (*Release Definition ID* was introduced since 8.1.0). 

   During runtime, Katalon Studio uses these pipeline definition IDs to get the latest Build and Release, and pass them to the corresponding properties of a test run.

   <img alt="Fill Pipeline Defition ID" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/definition-id.png" width=70%>

4. Decide what attachments to be sent together with a test run.

5. With the associated Test Case ID and Test Configurations, there may be more than one Test Point returned. These Test Points share the same Test Case ID and Test Configurations, yet different in terms of Test Suite and Tester. In this case, you can decide whether Katalon Studio submits test results regardless of the number of Test Points or not. Select **Submit test results for multiple test points with the same test case ID**.

6. Click **Apply and Close** to save your settings.

## Map test cases between Katalon Studio and Azure DevOps

**In Azure Test Plans**:

View Test Case ID on its URL.

**In Katalon Studio**:

1. Open a test case.
2. Select **Integrations** tab.
3. Input Test Case ID(s) of ADO. One:Many mapping is supported, separate IDs by comma.
4. Click **Verify** to check whether the test case ID is valid.
5. **Save** your setting.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/map-ks-test-case-with-ado.png" width=70%>

## Auto-Submit test run and test results after execution

After a test suite execution finishes, Katalon Studio adds a new test run and test results to the specified test plan automatically.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/result-on-ado.png" width=70%>

## Dynamically change test run’s information in CLI

You can change test plan ID, test run name, build and release definition IDs of a test run by using the following command-line options:

**Requirements**

* An active Katalon Runtime Engine license.
* Katalon Runtime Engine v8.0.0+
* To use `-adoReleaseDefID`, Katalon Runtime Engine 8.1.0 is required.

<table data-number-column="false" data-layout="default" data-autosize="false" data-pm-slice="1 1 []">
	<tbody>
		<tr>
			<th data-colwidth="254">
				<p>Katalonc Command-line Option</p>
			</th>
			<th data-colwidth="253">
				<p>Description</p>
			</th>
			<th data-colwidth="253">
				<p>Mandatory?</p>
			</th>
		</tr>
		<tr>
			<td data-colwidth="254">
				<p>-adoPlanId=&lt;testplan id&gt;</p>
			</td>
			<td data-colwidth="253">
				<p>Id of the test plan used for submitting test run(s).</p>
			</td>
			<td data-colwidth="253">
				<p>N</p>
			</td>
		</tr>
		<tr>
			<td data-colwidth="254">
				<p>-adoTestRunName="text"</p>
			</td>
			<td data-colwidth="253">
				<p>Create test run(s) on ADO with the specified name.</p>
			</td>
			<td data-colwidth="253">
				<p>N</p>
			</td>
		</tr>
		<tr>
			<td data-colwidth="254">
				<p>--info -adoBuildDefId =&lt;Definition ID of Build Pipeline&gt;</p>
			</td>
			<td data-colwidth="253">
				<p>Get the latest completed Build ID of the specified Build Definition ID and pass it to the corresponding Test Run property on ADO.</p>
			</td>
			<td data-colwidth="253">
				<p>N</p>
			</td>
		</tr>
		<tr>
			<td data-colwidth="254">
				<p>--info -adoReleaseDefID=&lt;Definition ID of Release Pipeline&gt;</p>
			</td>
			<td data-colwidth="253">
				<p>Get the latest Release ID and its stage based on the specified Definition ID of Release Pipeline and pass them to the corresponding Test Run properties on ADO. (Runtime Engine 8.1.0+ is required)</p>
			</td>
			<td data-colwidth="253">
				<p>N</p>
			</td>
		</tr>
	</tbody>
</table>

## Troubleshoot common issues

<table>
    <thead>
        <tr>
            <th>Error</th>
            <th>Solution</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Cannot create Test Results for Azure DevOps Test Case ID= due to multiple Test Points returned.</td>
            <td>Please check Test Points with Id = ; or allow sending Test Results anyway in Project Settings.</td>
        </tr>
    </tbody>
</table>
