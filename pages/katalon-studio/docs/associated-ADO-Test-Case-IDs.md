---
title: "Enhance Data-driven Testing Report in Azure DevOps (POC)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/associated-ado-test-case-ids.html
---

> **Important**
>
> This Proof of Concept (POC) is not ready for production use. We recommend using this POC for evaluation purposes only.

Previously, Katalon Studio provides the Data-Driven Testing method for test cases and supports test IDs mapping at test cases level in Azure DevOps (ADO). See [Integration with Azure DevOps Test Plans](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html).

Katalon Studio also supports submitting test results that include test iterations to ADO. However, running automated tests with Data-Driven Testing generates lots of results, especially when you run it with a large test data file. In that case, you might want to do the test ID mapping from the test data file to ADO so that you can quickly identify false lines in your test data.

In this POC, you can parameterize the test case variable in the ADO test case ID with the syntax `ado_id` and execute a test suite containing associated test cases. Each Katalon Studio iteration is now mapped to an ADO test case.

> **What is an iteration?**
>
> A test case executes with a test data row is considered an iteration.

> Download Katalon Studio ... [here]()

## Azure DevOps Test Case Ids Parameter

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

Before you execute a test suite containing associated test cases, ensure you already [Enable the Integration and Perform Authentication](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html#enable-the-integration-and-perform-authentication) with ADO and [create your Test Data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html).

**In Azure Test Plans**:

View test case ID on its URL.

**In Katalon Studio**:

1. Open your desired test case.
2. In the **Test Case/Variables** tab, click **Add** and create a **Number** type variable names `ado_id` with the **Default value** of your choice. See [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-ado-id.png" alt="add variable" width=60%>

3. In **ADO Test Case ID List**, call the variable with the syntax `${ado_id}`.

    * You can map one test case ID in Katalon Studio with many test case IDs on ADO, for example, `${ado_id},123456` or `${ado_id}, ${ado_id_1}`. 
    * Duplicate test case IDs will be used one time only.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-data.png" alt="test data" width=40%>

4. To check if the test case ID is valid, click **Verify**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-verify.png" alt="verify" width=40%>

5. Add your test case to a test suite.
6. Conduct **Variable Binding**. See [Run Test Case with an external data source](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-binding.png" alt="conduct variable binding" width=100%>

7. Execute your test suite with Data Binding:

    * Each Katalon Studio iteration is mapped to an ADO test case.
	* In the **Event Log**, you can find the invalid ADO test case ID.
	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-event-log.png" alt="event log" width=100%>