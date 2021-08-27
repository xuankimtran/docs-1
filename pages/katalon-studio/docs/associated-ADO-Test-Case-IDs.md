---
title: "Enhance Data-Driven Testing with Azure DevOps (POC)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/associated-ADO-test-case-IDs.html
---

> **Important**
>
> This Proof of Concept (POC) is not ready for production use. We recommend using this PoC for evaluation purposes only.

Previously, Katalon Studio provides the Data-Driven Testing method for Test Cases and supports Test IDs mapping at Test Cases level in Azure DevOps (ADO). See [Integration with Azure DevOps Test Plans](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.htm).

However, there are cases you want to do the Test ID mapping from the Test Data file to ADO. In this POC, you can parameterize the Test Case variable in ADO Test Case ID with the syntax `ado_id` and execute a Test Suite containing associated Test Cases. Each Katalon Studio iteration is now mapped to an ADO test case. Katalon Studio supports submitting test results that include test iterations to ADO.

> **What is an iteration?**
>
> A test case executes with a test data row is considered an iteration.

> Download Katalon Studio ... [here]()

## Azure DevOps Test Case Ids Parameter

Use the **ado_id** variable to parameterizes the Test Case variable in ADO Test Case ID.

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
			<p data-renderer-start-pos="2418">ADO Test Case Id(s)</p>
		</td>
	</tr>
</tbody>
</table>

## Execute Test Suite containing Associated Test Cases

Before you execute a Test Suite containing Associated Test Cases, ensure you already [Enable the Integration and Perform Authentication](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html#enable-the-integration-and-perform-authentication) with ADO and [create your Test Data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html).

**In Azure Test Plans**:

View Test Case ID on its URL.

**In Katalon Studio**:

1. Open your desired Test Case.
2. In the **Test Case/Variables** tab, click **Add** and create a **Number** type variable names **ado_id** with the **Default value** of your choice. See [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/KS-associated-ADO-TC-IDs-add-variable.png" alt="add variable" width=80%>

3. In **ADO Test Case ID List**, call the variable with the syntax `${ado_id}`.

    * **One:Many Mapping** is applicable, eg., `${ado_id},123456` or `${ado_id}, ${ado_id_1}`. 
    * Duplicate test case Ids will be used one time only.

    > **Notes**
    >
    > **One:Many mapping** means that one row in a table is mapped to multiple rows in another table.

4. Click **Verify**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/KS-associated-ADO-TC-IDs-verify.png" alt="verify" width=40%>

    * If the test case is valid, the message **Valid Test Case(s)** appears.
    * If the test case is invalid, the message **Invalid test case(s) <ID>** appears.

5. Add your Test Case to a Test Suite. See [Create a new Test Suite with Test Case Variables](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#create-a-new-test-suite-with-test-case-variables).
6. Conduct **Variable Binding**. See [Manage Data Binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/KS-associated-ADO-TC-IDs-conduct.png" alt="conduct variable binding" width=80%>

7. Execute your Test Suite with Data Binding:

    * In the **Event Log**, each row of test case ID is passed to the variable.
    * Each Katalon Studio iteration is mapped to an ADO test case.

<Add Event Log Screenshot>