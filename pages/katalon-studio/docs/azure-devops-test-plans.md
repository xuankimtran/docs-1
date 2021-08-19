---
title: "Integration with Azure DevOps Test Plans"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/azure-devops-test-plans.html
redirect_from:
    - "/katalon-studio/docs/azure-devops-integration.html"

description: 
---

> From version 8.1.0 onwards, you can submit a test run with Release information to Azure.

Katalon Studio can natively integrate with the Azure Test Plans service of Azure DevOps (ADO). This integration helps you:

1. Establish a connection between a Katalon Studio project and an ADO project.
2. Easily map ADO Test Cases to automated Test Cases in Katalon Studio.
3. Automatically submit test runs and results to ADO with execution logs, reports, and images for analysis.

> **Requirements**
>
> * Katalon Studio version 8.0.0 onwards.
> * An active Katalon Studio Enterprise license.
> * Azure Test Plans having already been set up.

## Enable the Integration and Perform Authentication

To retrieve relevant test artifacts and create test runs with test results, you need to integrate and authenticate your project with Azure Server. In Katalon Studio, go to **Project > Settings > Integrations > Azure DevOps**. The **Azure DevOps** dialog appears.

1. To enable the **Authentication** area for editing, select **Enable Integration**.

2. Enter your credentials. Your credentials are encrypted by default.

    - **Server URL**: `https://dev.azure.com/{yourorganization}`
    - **Personal Access Token**: your Personal Access Token. We recommend you create a Personal Access Token with full-access scopes. See Microsoft document: [Use personal access tokens](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page) and [Scopes](https://docs.microsoft.com/en-us/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#scopes).

3. To verify whether the connection to Azure Server is successful, click **Connect**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/authentication.png" alt="Azure DevOps dialog" width=70%>

## Configure the Integration

### Step 1: Select a Project for submitting test run and results

After successfully authenticating your project with Azure Server, in the drop-down list of **Project**, select an ADO project that you have access to.

To retrieve the latest projects list, click **Fetch Project**.

After you select a project, the **Test Artifacts Mapping** and **Submission Option** fieldsets automatically expand.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/expand-both.png" alt="test artifacts mapping" width=70%>

### Step 2: Map Test Artifacts between two systems

You can **Add** or **Remove** items in each section to serve your need.

**In the Execution Status Mapping**: Match test results in Katalon Studio with test outcomes in ADO.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/status-mapping.png" width=70%>

**In the Test Configuration Mapping**: This step reduces the number of test results created for each mapped test case. You need to pair **Execution OS/Device** and **Execution Browser/App** in Katalon Studio with **Test Configurations** retrieved from Azure Test Plans.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/test-configuration-mapping.png" alt="Test configuration mapping" width=70%>

> **What is a Test Point?**
>
> A Test Point is a unique combination of a test case, test suite, configuration, and tester. Test cases by themselves are not executable. When you add a test case to a test suite, a test point is generated. To learn more about the Test Point, see Microsoft document: [Execute tab](https://docs.microsoft.com/en-us/azure/devops/test/new-test-plans-page?view=azure-devops#execute-tab).
>
> **What is a Test Configuration?**
>
> A Test Configuration is a combination of configuration variable values containing operating system information, browser, CPU type, database. For example, **Windows 8 + 32-bit CPU** or **Windows 10 + 64-bit CPU**. To learn more about the Test Configuration, see Microsoft document: [Test different configurations](https://docs.microsoft.com/en-us/azure/devops/test/test-different-configurations?view=azure-devops).

### Step 3. Configure Submission Options

1. Select a test plan for the test run to be submitted. To retrieve the latest test plans list, click **Fetch Test Plans**.

   <img alt="Submission Options 8.1.0" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/Submission-option-8.1.0.png" width=70%>

2. Name the test run.

3. To add Build and Release Information to test runs, specify **Build Definition ID** and **Release Definition ID** respectively (**Release Definition ID** was introduced in 8.1.0).

   During runtime, Katalon Studio uses these pipeline definition IDs to get and pass the latest Build and Release to the corresponding properties of a test run.

   <img alt="Fill Pipeline Defition ID" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/definition-id.png" width=70%>

4. Decide what attachments to be sent together with a test run.

5. With the associated Test Case ID and Test Configurations, more than one Test Point might be returned. These Test Points share the same Test Case ID and Test Configurations, yet are different in Test Suite and Tester. In this case, to decide whether Katalon Studio submits test results regardless of the number of Test Points or not, select **Submit test results for multiple test points with the same test case ID**.

6. To save your settings, click **Apply and Close**.

## Map test cases between Katalon Studio and Azure DevOps

**In Azure Test Plans**:

View Test Case ID on its URL.

**In Katalon Studio**:

1. Open a test case.
2. Select the **Integrations** tab.
3. Input Test Case ID(s) of ADO. When many mappings are supported, separate IDs by a comma.
4. To check whether the test case ID is valid, click **Verify**.
5. **Save** your setting.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/map-ks-test-case-with-ado.png" alt="verify ADO test case" width=70%>

## Auto-Submit test run and test results after execution

After a test suite execution finishes, Katalon Studio automatically adds a new test run and test results to the specified test plan.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/result-on-ado.png" alt="new item" width=70%>

## Dynamically change the information of test run in Command-line Option

You can change the test plan ID, test run name, build and release the definition IDs of a test run by using the following command-line options:

> **Requirements**
>
> * An active Katalon Runtime Engine license.
> * Katalon Runtime Engine version 8.0.0 onwards.
> * To use `-adoReleaseDefID`, Katalon Runtime Engine version 8.1.0 onwards is required.

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
				<p>ID of the test plan used for submitting test run(s).</p>
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
            <td>Check Test Points with ID = ; or allow sending Test Results anyway in Project Settings.</td>
        </tr>
    </tbody>
</table>
