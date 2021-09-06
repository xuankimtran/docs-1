---
title: "Enhance Data-driven Testing Report in Azure Test Plans (PoC)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/enhance-ddt-report-in-ado.html
---

> Important:
>
> * This Proof of Concept (PoC) is not ready for production use. We recommend using this PoC for evaluation purposes only.
> * Download Katalon Studio version [8.1.1.alpha](https://github.com/katalon-studio/katalon-studio/releases/tag/v8.1.1.alpha).

In Katalon Studio, you can enable an integration with Azure DevOps (ADO) to allow test runs and test results automatically being submitted to ADO. See [Integration with Azure DevOps Test Plans](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html).

However, running a test in Katalon Studio can generate lots of results when you use the Data-driven Testing method. In that case, you might want to quickly identify data rows related to false test iterations.

> **What is an iteration?**
>
> A test case executes with a test data row is considered an iteration.

In this PoC, we enhance the Data-driven Testing Report in ADO by support you to parameterize associated ADO test case IDs in Katalon Studio.

## Azure DevOps Test Case IDs Parameter

Use the `ado_id` variable to parameterize the test case variable in ADO test case ID.

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

## Execute Test Suite containing Associated Test Cases

Before you execute a test suite containing associated test cases, ensure you already enable ADO integration.

**In Azure Test Plans**:

View test case ID on its URL.

**In Katalon Studio**:

1. Open your desired Data-driven test case. To learn more about the test data, see [create your Test Data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html).
2. In the **Test Case/Variables** tab, click **Add** and create a **Number** type variable names `ado_id` with the **Default value** of your choice. See [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-ado-id.png" alt="add variable" width=70%>

3. In **ADO Test Case ID List**, call the variable with the syntax `${ado_id}`.

    * You can map one test case ID in Katalon Studio with many test case IDs on ADO, IDs are separated by commas. For example, `${ado_id},123456` or `${ado_id}, ${ado_id_1}`.
    * Duplicate test case IDs will be used one time only.

		<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-data.png" alt="test data" width=50%>

4. To check if the test case ID is valid, click **Verify**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-verify.png" alt="verify" width=50%>

5. Add your test case to a test suite.
6. Conduct **Data Binding**. See [Manage Data Binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding)

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-binding.png" alt="conduct variable binding" width=100%>

7. Execute your test suite with Data Binding:

    * Each Katalon Studio iteration is mapped to an ADO test case.
	* In the **Event Log**, you can find the invalid ADO test case ID.
		<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-event-log.png" alt="event log" width=100%>