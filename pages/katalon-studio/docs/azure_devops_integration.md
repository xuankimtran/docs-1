---
title: "Integration with Azure DevOps Test Plans (Prerelease)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/azure-devops-test-plans.html
description: 
---

> **Important**
>
> This is just a prerelease version, not ready for production use.

In the next major release, v8.0, expected to be shipped by the end of April, Katalon Studio can be natively integrated with Azure DevOps (ADO) - Test Plans. This feature will support you:

- When you have manual Test Cases in ADO and you want to map to a corresponding automated Test Case in Katalon Studio to know which Test Cases are automated.

- When you execute the integrated Test Cases in Katalon Studio, you want the Test Run to be created accordingly with the test execution reports and results uploaded to its corresponding Test Run in ADO so that you can get the test status and have sufficient materials for debugging.

To be specific, in terms of the feature, you can do the following things:

- Enable, Authenticate and Configure the integration in Project Settings.
- Associate Test Cases between two systems.
- When a Test Suite/ Test Suite Collection execution finishes, Katalon will create Test Run and submit Test Results to ADO.
- Dynamically change test plan ID, test run name, and build number of a test run via CLI.

This document introduces what built-in **Azure DevOps Intergration** feature looks like and how to use it in Katalon Studio.

> Download Katalon Studio v8.0.0.rc [here](https://github.com/katalon-studio/katalon-studio/releases/tag/v8.0.0.rc).

**Requirements**

* Katalon Studio version 8.0.
* An active Katalon Studio Enterprise license.
* Set up Azure DevOps.

### Enable the Integration and Authenticate Azure DevOps Organization

You need to enable ADO integration and authenticate your Azure DevOps Organization to retrieve and map test artifacts between two systems and submit test results to ADO. Do as follow:

In Katalon Studion, go to **Project > Settings > Integrations > Azure DevOps**:

1. Select **Enable Intergration** to enable **Authentication** section for editting.

2. Enter the required credentials for **Authentication**. Your credentials are encrypted by default for security.

    - **Server URL**: `https://dev.azure.com/{yourorganization}`
    - **Personal Access Token**: your [Personal Access Token](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page). Learn about the [Permission](https://docs.microsoft.com/en-us/azure/devops/organizations/security/about-permissions?view=azure-devops&tabs=preview-page#permissions)

3. Click **Connect** to verify whether Azure DevOps is connected successfully.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/authentication.png" width=70%>

### Configure the Integration

After successfully authenticating with ADO, you can select an ADO project among those you have access to in the drop-down list of **Project**.

To configure the integration, do as follows:

1. Select a Project for submitting the test run.

    - Select a fetched project in the **Project** drop-down list.

    - The **Test Artifacts Mapping** and **Submission Option** fieldsets are expanded automatically. You can customize the settings in each section. 

        > If you want to fetch the latest projects list > click **Fetch Project**.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/expand-both.png" width=65%>
        
2. Conduct Test Artifacts Mapping.

    In the **Test Artifacts Mapping**, do as follows for submitting the test run:

    - Map Katalon Studio's Execution Status to ADO test status in the **Execution Status Mapping** to match the test results in Katalon Studio with the test outcomes in ADO.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/status-mapping.png" width=70%>

    - Map testing environment in Katalon Studio to configurations fetched from ADO in the **Test Configuration Mapping** to match the  **Execution OS/Device**, and **Execution Browser/App** configured in Katalon Studio to run the tests with the **Test Configurations in Azure DevOps**.  

	    You can also **Add** or **Remove** item(s) to customize the settings.

        > **What is Test Configuration?**
        >
        > **A Test Configuration is a combination of configuration variable values**. Your configuration variables could be, for example, operating system, browser, CPU type, database. A configuration might be "Windows 8 + 32-bit CPU" or "Windows 10 + 64-bit CPU." [Learn more](https://docs.microsoft.com/en-us/azure/devops/test/test-different-configurations?view=azure-devops)

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/environment-mapping.png" width=70%>

3. Config Submission Options.

    - Select a fetched test plan in the drop-down list, the test run is submitted to ADO automatically.

        > Click **Fetch Test Plans** to fetch the latest test plans list.

    - If you want to create test results for ADO test case ID due to multiple test points returned, select **Send test results when ...** to enable test run details for editing.
        - Enter the required **Test Run Name**.
        - Enter **Build Number** > click **Verify** to check if your number is valid (to map to more than one number, separate them by a comma). 
    
        > **What is Test Point?**
        > 
        > **A test point is a unique combination of a test case, test suite, configuration, and tester**. Test cases by themselves are not executable. When you add a test case to a test suite, test point(s) are generated. [Learn more](https://docs.microsoft.com/en-us/azure/devops/test/new-test-plans-page?view=azure-devops#execute-tab)

    - Decide when and what to submit test results.

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/submission-options.png" width=65%>

3. Click **Apply and Close** to save your settings.

### Map test cases between Katalon Studio and Azure DevOps 

**In Katalon Studio:**

1. Double-click on a Test Case to open the test case view.
2. Select **Integrations** tab > specify the Test Cases ID(s) of ADO (to map to more than one ID, separate them by a comma).
3. Click **Verify** to check whether the test case is valid > **Save**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/map-ks-test-case-with-ado.png" width=60%>

### Submit test run and test results after execution

> Ensure that you have already taken the stated steps.

When the execution finishes, the test run is created, and test results are uploaded automatically to ADO in the format specified as below:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-intergration/result-on-ado.png" width=70%>

### Change test run information in Command-line

You can dynamically change test plan ID, test run name, and build number of a test run by using the following command-line.

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