---
title: "Azure DevOps Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/azure-devops-integration.html
description:
---

**Azure DevOps Integration** is a built-in integration that supports the connection between Katalon Studio and Azure DevOps (ADO) to deliver the following advanced capabilities:

- Map test cases between Katalon Studio and ADO.
- In ADO, you can send and view Test Results of both Test Suites and Test Cases executed in Katalon Studio.

Katalon Studio provides the **Azure DevOps Integration** feature to enhance the integration between Katalon Studio and Azure DevOps Pipeline to run automated tests in CI/CD pipeline.

**Prerequisites**

- Katalon Studio v8.0 onwards.
- An active Katalon Studio Enterprise license.

### Enable the Integration and Authenticate Azure DevOps Organization

You need to enable ADO integration and authenticate your Azure DevOps Organization to retrieve and map test artifacts between two systems and submit test results to ADO. Do as follow:

In Katalon Studion, go to **Project > Settings > Integrations > Azure DevOps**:

1. Select **Enable Intergration** to enable **Authentication** section for editting.

2. Enter the required credentials for **Authentication**. Your credentials are encrypted by default for security.

    - **Server URL**: `https://dev.azure.com/{yourorganization}`
    - **Personal Access Token**: your [Personal Access Token](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page). Learn about the [Permission](https://docs.microsoft.com/en-us/azure/devops/organizations/security/about-permissions?view=azure-devops&tabs=preview-page#permissions)

3. Click **Connect** to verify whether Azure DevOps is connected successfully.

### Configure the Integration

After successfully authenticating with ADO, you can select an ADO project among those you have access to in the drop-down list of **Project**.

To configure the integration, do as follows:

1. Select a Project for submitting the test run.

    - Select a fetched project in the **Project** drop-down list.

    - The **Test Artifacts Mapping** and **Submission Option** fieldsets are expanded automatically. You can customize the settings in each section. 

        > If you want to fetch the latest projects list > click **Fetch Project**.

2. Conduct Test Artifacts Mapping.

    In the **Test Artifacts Mapping**, do as follow for submitting the test run.

    - Map Katalon Studio's Execution Status to ADO test status in the **Execution Status Mapping** to match the test results in Katalon Studio with the test outcomes in ADO.

    - Map testing environment in Katalon Studio to configurations fetched from ADO in the **Test Configuration Mapping** to match the  **Execution OS/Device** and **Execution Browser/App** configured in Katalon Studio to run the tests with the **Test Configurations in Azure DevOps**, you can also **Add** or **Remove** an item to customize the settings.

        > **What is Test Configuration?**
        >
        > **A Test Configuration is a combination of configuration variable values**. Your configuration variables could be, for example, operating system, browser, CPU type, database. A configuration might be "Windows 8 + 32-bit CPU" or "Windows 10 + 64-bit CPU." [Learn more](https://docs.microsoft.com/en-us/azure/devops/test/test-different-configurations?view=azure-devops)

3. Config Submission Options.

    - Select a fetched test plan in the drop-down list, the test run is submitted to ADO automatically.

        > Click **Fetch Test Plans** to fetch the latest test plans list.

    - If you want to create test results for ADO test case ID due to multiple test points returned, select **Send test results when ...** to enable test run details for editing.
        - Enter the required **Test Run Name**.
        - Enter **Build Number** > click **Verify** to check if your number is valid.
    
        > **What is Test Point?**
        > 
        > **A test point is a unique combination of a test case, test suite, configuration, and tester**. Test cases by themselves are not executable. When you add a test case to a test suite, test point(s) are generated. [Learn more](https://docs.microsoft.com/en-us/azure/devops/test/new-test-plans-page?view=azure-devops#execute-tab)

    - Decide when and what to submit test results.

### Map test cases between Katalon Studio and Azure DevOps 

**In Katalon Studio:**

1. Double-click on a Test Case to open the test case view.
2. Select **Integrations** tab > specify the Test Cases ID(s) of ADO.
3. Click **Verify** to check whether the test case is valid > **Save**.

Mo^i~ test case cua KS se ung voi nhieu test cases cua Azure, va ung voi moi Azure test case la nhieu test points

### Submit test run and test results after execution

> Ensure that you have already taken the stated steps.

When the execution finishes, the test run is created, and test results are uploaded automatically to ADO in the format specified as below:

Test case result of each test case should display these fields:
- Outcome = Azure status in Status Mapping.
- Test Case Title = Title of the executed test case in ADO.
- Machine name = Hostname in the report.
- Duration =  The elapsed time of each test case.
- Error message = The test case message whenever the Katalon test case status is FAILED or ERROR.