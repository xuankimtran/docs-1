---
title: "Set Associated Test Case IDs Parameter in Azure Test Plans (PoC)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/associated-test-case-ids-ado.html
---

> **Important**
>
> * This Proof of Concept (PoC) is not ready for production use. We recommend using this PoC for evaluation purposes only.
> * Download Katalon Studio version [8.1.1.alpha](https://github.com/katalon-studio/katalon-studio/releases/tag/v8.1.1.alpha).

From version 8.0.0, you can enable integration with Azure DevOps (ADO) to allow test runs and test results to be automatically submitted to ADO. See [Integration with Azure DevOps Test Plans](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html).

However, running a test can generate lots of results when you use the Data-driven Testing method. In this PoC, we provide a solution to set custom test iteration IDs, so that test iterations in Katalon Studio are automatically mapped to the related ADO test cases.

> **What is an iteration?**
>
> An iteration is a test case executed with a test data row.

> **Requirements**
>
> * An active Katalon Studio Enterprise license.
> * Azure Test Plans already configured.

## Set Parameter

Use the `ado_id` variable to set the test case variable parameter in the **ADO test case ID list**.

<table data-number-column="false"><colgroup><col /><col /><col /><col /></colgroup>
<tbody>
	<tr>
		<th colspan="1" rowspan="1" data-colwidth="170">
			<div tabindex="0">
				<p data-renderer-start-pos="2330"><strong data-renderer-mark="true">Variable</strong></p>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="170">
			<div tabindex="0">
				<p data-renderer-start-pos="2342"><strong data-renderer-mark="true">Parameter  Type</strong></p>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="170">
			<div tabindex="0">
				<p data-renderer-start-pos="2356"><strong data-renderer-mark="true">Mandatory</strong></p>
			</div>
		</th>
		<th colspan="1" rowspan="1" data-colwidth="170">
			<div tabindex="0">
				<p data-renderer-start-pos="2369"><strong data-renderer-mark="true">Description</strong></p>
			</div>
		</th>
	</tr>
	<tr>
		<td colspan="1" rowspan="1" data-colwidth="170">
			<p data-renderer-start-pos="2386">ado_id</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="170">
			<p data-renderer-start-pos="2396">Number</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="170">
			<p data-renderer-start-pos="2406">Optional</p>
		</td>
		<td colspan="1" rowspan="1" data-colwidth="170">
			<p data-renderer-start-pos="2418">List of ADO Test Case IDs</p>
		</td>
	</tr>
</tbody>
</table>

**In Azure Test Plans**

You can view your test case IDs in Azure Test Plan.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/test-case-ids.png" alt="ado ID" width=90%>

**In Katalon Studio**

1. Open your desired test case.

2. To add the `ado_id` variable, switch to the **Variables** tab of your test case. Click **Add** to create a variable named `ado_id`. To learn more about variables, see [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html).

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/number-ado_id.png" width=90%>

3. To call the `ado_id` variable, switch to the **Integration** tab and select the **Azure** integration. In the **ADO Test Case ID list**, call the variable with the syntax `${ado_id}`.

	You can map one test case ID in Katalon Studio with many test case IDs on ADO, IDs are separated by commas. Duplicated test case IDs will be used one time only.

4. To check if the test case ID is valid, click **Verify**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/verified.png" alt="verify" width=70%>

## Execute Test Suite containing Associated Test Cases

1. Add the test case above to a test suite.

2. To conduct **Data Binding**, in the test suite editor, click **Show Data Binding**.

	In the **Test Data** table, you can add or check your test data files.
	In the **Variable Binding** table, you can see your variable list with related test data files and values. See [Manage Data Binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-binding.png" alt="conduct data binding" width=100%>

3. When you are done with the configuration, hit **Run** to execute your test suite. Once the test suite finished executing, you can view your test results in ADO. Each test iteration in Katalon Studio is automatically mapped to related ADO test cases. Invalid ADO test case IDs is showed in Katalon Studio **Event Log**.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/event-log.png" alt="event log" width=100%>

	In Azure Test Plan, you can find a report with a list of test iterations.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/event-log-ado.png" alt="report in ADO" width=100%>