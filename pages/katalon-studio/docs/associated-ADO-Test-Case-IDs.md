---
title: "Parameterize Azure DevOps Test Case ID List (PoC)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/parameterize-ado-test-case-id.html
---

> **Important**
>
> * This Proof of Concept (PoC) is not ready for production use. We recommend using this PoC for evaluation purposes only.
> * Download Katalon Studio version [8.1.1.alpha](https://github.com/katalon-studio/katalon-studio/releases/tag/v8.1.1.alpha).

From version 8.0.0, you can natively integrate with Azure DevOps (ADO) to map ADO test cases to automated test cases in Katalon Studio, and 
automatically submit test runs with results to ADO.

However, running a test can generate lots of results when you use the Data-driven Testing method. In this PoC, we provide a solution to set custom test iteration IDs, so that test iterations in Katalon Studio are automatically mapped to the related ADO test cases.

> **What is an iteration?**
>
> An iteration is a test case executed with a test data row.

> **Requirements**
>
> * An active Katalon Studio Enterprise license.
> * Azure Test Plans is already configured.
> * Azure DevOps integration is already enabled and configured. See [Integration with Azure DevOps Test Plans](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html).

## Set Parameter

In this step, we will guide you through adding and calling a test case variable in the **ADO test case ID list**.

**In Azure Test Plans**

You can view your test case IDs in Azure Test Plan.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/test-case-ids.png" alt="ado ID" width=90%>

**In Katalon Studio**

1. Add a test case variable:

	Open your desired test case and switch to the **Variables** tab. To create a variable, click **Add**. For example, we create a number variable named `ado_id`. To learn more about variables, see [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html).

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/number-ado_id.png" width=90%>

2. Call a variable in the ADO test case ID list:

	Switch to the **Integration** tab and select the **Azure** integration. In the **ADO Test Case ID list**, call the variable with the syntax `${Your_variable_name}`, for example: `${ado_id}`.

	You can map one test case ID in Katalon Studio with many test case IDs on ADO, IDs are separated by commas. Duplicated test case IDs will be used one time only.

	To check if the test case ID is valid, click **Verify**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/verified.png" alt="verify" width=70%>

## Execute Test Suite containing Associated Test Cases

1. Add the test case above to a test suite.

2. To conduct **Data Binding**, in the test suite editor, click **Show Data Binding**.

	In the **Test Data** table, you can add or check your test data files.
	The **Variable Binding** table shows your variable list with related test data files and values. See [Manage Data Binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-binding.png" alt="conduct data binding" width=100%>

3. When you are done with the configuration, hit **Run** to execute your test suite. Once the test suite finished executing, you can view your test results in ADO. Each test iteration in Katalon Studio is automatically mapped to related ADO test cases. Invalid ADO test case IDs are showed in Katalon Studio **Event Log**.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/event-log-ado.png" alt="event log" width=100%>

	In Azure Test Plan, you can find a report with a list of test iterations.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/report%20in%20ADO.png" alt="report in ADO" width=100%>