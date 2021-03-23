---
title: "Azure DevOps Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/azure-devops-integration.html
description:
---

**Azure DevOps Integration** is a built-in integration in Katalon Studio. It supports the connection between Katalon Studio and Azure DevOps (ADO) to deliver the following advanced capabilities:

- Map test cases between Katalon Studio and ADO.
- In ADO, you can send and view Test Results of both Test Suites and Test Cases executed in Katalon Studio.
- In Katalon Studio, you can query Test Runs of ADO in [Dynamic Test Suite](https://docs.katalon.com/katalon-studio/docs/dynamic-test-suite.html).

**Prerequisite**

- An active Katalon Studio Enterprise license.

## Enable the intergration and Authenticate 

You need to enable ADO integration and authenticate to your Azure DevOps Organization to retrieve and map test artifacts between two systems and submit test results to ADO. Do as follow:

In Katalon Studion, go to **Project > Settings > Integrations > Azure DevOps**:

1. Select **Enable Intergration** to enable **Authentication** section for editting.

2. Enter the required credentials for **Authentication**. Your credentials are encrypted by default for security.

    - **Server URL**: `https://dev.azure.com/{yourorganization}`
    - **Personal Access Token**: your Personal Access Token. [Learn more](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page)

3. Click **Connect** to verify whether ADO is connected successfully.

## Configure the Integration

After successfully authenticating with ADO, all relevant ADO Projects will be retrieved and displayed in the drop-down list of **Project**.

To configure the intergration, do as follows:

### 1. Select a project for submitting the test run

- Select a project in the **Project** drop-down list for submitting the test run. 

- The **Test Artifacts Mapping** and **Submission Option** fieldsets are expanded automatically. You can customize the settings in each section. 

    > **Note**
    >
    > If you want to fetch the lastest list of projects > click **Fetch Project**.

### 2. Conduct Test Artifacts Mapping

What is Test Point?

- Test cases by themselves are not executable. When you add a test case to a test suite then test point(s) are generated. A test point is a unique combination of test case, test suite, configuration, and tester. 

- If you have a test case as "Test login functionality" and you add 2 configurations to it as Edge and Chrome then this results in 2 test points. Now these test points can be executed. On execution, test results are generated. Through the test results view (execution history) you can see all executions of a test point. The latest execution for the test point is what you see in the execute tab.

- Hence, test cases are reusable entities. By including them in a test plan or suite, test points are generated. By executing test points, you determine the quality of the product or service being developed. 

What is Test Configuration?

- A test configuration is a combination of configuration variable values. Your configuration variables could be, for example, operating system, browser, CPU type, database. A configuration might be "Windows 8 + 32-bit CPU" or "Windows 10 + 64-bit CPU." 
 
To conduct, go to the **Test Artifacts Mapping** to customize the **Execution Status Mapping** and the **Test Configuration Mapping**.

- Execute the status mapping in the **Execution Status Mapping**, map Katalon Studio's Execution Status to ADO test status.

- In the **Test Configuration Mapping**, you can also **Add** or **Remove** an item to customize the settings. 

### 3. Config Submission Options

- Select a test plan in the drop-down list to submit the test run.

> **Note**
>
> If you want to fetch the lastest list of test plans > click **Fetch Test Plans**.

- Select **Automatically submit test run**.
- Enter the **Test Run Name** and **Build Number** to 

## Map test cases between Katalon Studio and Azure DevOps 

### In Katalon Studio

1. Double-click on a Test Case to open the test case view.
2. Select **Integrations** tab > specify the Test Case's ID(s) of ADO.
3. Click **Verify** to check whether the test case is valid > **Save**.

## Add test results to Azure DevOps
