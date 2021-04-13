---
title: "Integration with Azure DevOps Test Plans (Pre-release)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/azure-devops-test-plans.html
description: 
---

> **Important**
>
> This is just a pre-release version that is not ready for production use. You are highly recommended to test its usability only.

In the release of version 8.0.0, expected to be shipped by the end of April, Katalon Studio can be natively integrated with Azure DevOps (ADO) - Test Plans. This integration will help you with the following problems:

<table style="width: 914px;">
	<tbody>
		<tr>
			<td style="width: 417px;">
				<p><strong>Problems</strong></p>
			</td>
			<td style="width: 481px;">
				<p><strong>Solutions</strong></p>
			</td>
		</tr>
		<tr>
			<td style="width: 417px;">
				<p>You want to map manual Test Cases in ADO to a corresponding automated Test Case in Katalon Studio to know which Test Cases are automated.</p>
			</td>
			<td style="width: 481px;">
				<p>Do as follows:</p>
				<ol>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html#enable-the-integration-and-authenticate-azure-devops-organization">Enable the Integration and Authenticate Azure DevOps Organization</a>.</li>
					<li>In <a href="https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html#configure-the-integration">Configure the Integration</a>, <strong>Conduct Test Artifacts Mapping</strong>.</li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html#map-test-cases-between-katalon-studio-and-azure-devops">Map test cases between Katalon Studio and Azure DevOps</a>.</li>
				</ol>
			</td>
		</tr>
		<tr>
			<td style="width: 417px;">
				<p>You want the Test Run in Katalon Studio to be created accordingly with the test execution reports and results uploaded to its corresponding Test Run in ADO to get the test status and have sufficient materials for debugging.</p>
			</td>
			<td style="width: 481px;">
				<p>Do as follows:</p>
				<ol>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html#enable-the-integration-and-authenticate-azure-devops-organization">Enable the Integration and Authenticate Azure DevOps Organization</a>.</li>
					<li>In <a href="https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html#configure-the-integration">Configure the Integration</a>, <strong>Configure Submission Options</strong>.</li>
					<li><a href="https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html#submit-test-run-and-test-results-after-execution">Submit test run and test results after execution</a>.</li>
				</ol>
			</td>
		</tr>
	</tbody>
</table>

> [Download Katalon Studio v8.0.0.rc2](https://github.com/katalon-studio/katalon-studio/releases/tag/v8.0.0.rc2).

The document introduces how the built-in **Azure DevOps Integration** feature looks like and how to use it in Katalon Studio.

**Requirements**

* Katalon Studio version 8.0.
* An active Katalon Studio Enterprise license.
* Set up Azure DevOps.

### Enable the Integration and Authenticate Azure DevOps Organization

You need to enable ADO integration and authenticate your ADO to retrieve and map test artifacts between two systems and submit test results to ADO. Do as follows:

In Katalon Studion, go to **Project > Settings > Integrations > Azure DevOps**:

1. Select **Enable Intergration** to enable **Authentication** section for editting.

2. Enter the required credentials for **Authentication**. Your credentials are encrypted by default for security.

    - **Server URL**: `https://dev.azure.com/{yourorganization}`
    - **Personal Access Token**: your [Personal Access Token](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page). We recommend you to create a Personal Access Token with full-access [scopes](https://docs.microsoft.com/en-us/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops#scopes).

3. Select **Encrypt authentication data** for security assurance.

4. Click **Connect** to verify whether Azure DevOps is connected successfully.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/authentication.png" width=70%>

### Configure the Integration

After successfully authenticating with ADO, you can select an ADO project among those you have access to in the drop-down list of **Project**.

To configure the integration, do as follows:

1. Select a Project for submitting the test run.

    - Select a fetched project in the **Project** drop-down list.

    - The **Test Artifacts Mapping** and **Submission Option** fieldsets are expanded automatically. You can customize the settings in each section. 

        > Click **Fetch Project** to fetch the latest projects list.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/expand-both.png" width=65%>
        
2. Conduct Test Artifacts Mapping

    - In the **Execution Status Mapping**, map **Katalon Studio's status** with **Azure DevOps's status** to match the test results in Katalon Studio with the test outcomes in ADO.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/status-mapping.png" width=70%>

    - In the **Test Configuration Mapping**, map the **Execution OS/Device** and **Execution Browser/App** configured to run the test in Katalon Studio with the **Test Configurations in Azure DevOps**. 

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/test-configuration-mapping.png" width=70%>
    
        Depending on **what OS and platform** using to execute the test, Katalon Studio will get the corresponding **Azure Test Configuration** and use it as a filter for its configured test points for the test run submission.

        You can also **Add** or **Remove** item(s) to customize the settings.

        > **What is Test Configuration?**
        >
        > **A Test Configuration is a combination of configuration variable values**. Your configuration variables could be, for example, operating system, browser, CPU type, database. A configuration might be "Windows 8 + 32-bit CPU" or "Windows 10 + 64-bit CPU." [Learn more](https://docs.microsoft.com/en-us/azure/devops/test/test-different-configurations?view=azure-devops)

        > **What is Test Point?**
        > 
        > **A test point is a unique combination of a test case, test suite, configuration, and tester**. Test cases by themselves are not executable. When you add a test case to a test suite, test point(s) are generated. [Learn more](https://docs.microsoft.com/en-us/azure/devops/test/new-test-plans-page?view=azure-devops#execute-tab)

3. Configure Submission Options

    - Select a fetched test plan in the drop-down list, the test run is submitted to ADO automatically.

        > Click **Fetch Test Plans** to fetch the latest test plans list.

    - If you want to submit test results for ADO test case ID when there are multiple test points returned, select **Send test results when ...** to enable test run details for editing > enter the required **Test Run Name**.

    - Decide when and what to submit test results.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/submission-options.png" width=65%>

4. Click **Apply and Close** to save your settings.

### Map test cases between Katalon Studio and Azure DevOps 

**In Katalon Studio:**

1. Double-click on a Test Case to open the test case view.
2. Select **Integrations** tab > specify the Test Cases ID(s) of ADO (to map to more than one ID, separate them by a comma).
3. Click **Verify** to check whether the test case id exists in ADO for mapping the test case(s) > **Save**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/map-ks-test-case-with-ado.png" width=60%>

### Submit test run and test results after execution

> Ensure that you have already taken the stated steps.

When the execution finishes, the test run is created, and test results are uploaded automatically to ADO in the format specified as below:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/result-on-ado.png" width=70%>

### Dynamically changing test run’s information in CLI

You can change the test plan ID, test run name, and build number of a test run by using the following command-line.

**Requirements**

* An active Katalon Runtime Engine license.
* Katalon Runtime Engine v8.0.

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
				<p>--info -adoBuildNumber="text"</p>
			</td>
			<td data-colwidth="253">
				<p>Pass the build number to Test Run properties on ADO.</p>
			</td>
			<td data-colwidth="253">
				<p>N</p>
			</td>
		</tr>
	</tbody>
</table>

### Known issues

* Both macOS and Windows builds:
   * [Katalon Studio] Moving Katalon Test Cases integrated with ADO to another folder causes the association to be lost. 
   * [Katalon Runtime Engine] Using `-adoPlanId` with **invalid** value causes the execution to stop.
   * Test Results submission is not applicable to a SKIPPED test case.
* macOS build only:
   * You can only set up this integration **ONCE** since there is an issue with switching the project and test plan later.
  
### Troubleshoot common issues

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
