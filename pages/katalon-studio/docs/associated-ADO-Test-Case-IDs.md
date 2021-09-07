---
title: "Parameterize Associated Test Case IDs in Azure Test Plans (PoC)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/enhance-ddt-report-in-ado.html
---

> Important:
>
> * This Proof of Concept (PoC) is not ready for production use. We recommend using this PoC for evaluation purposes only.
> * Download Katalon Studio version [8.1.1.alpha](https://github.com/katalon-studio/katalon-studio/releases/tag/v8.1.1.alpha).

In Katalon Studio, you can enable integration with Azure DevOps (ADO) to allow test runs and test results to be automatically submitted to ADO. See [Integration with Azure DevOps Test Plans](https://docs.katalon.com/katalon-studio/docs/azure-devops-test-plans.html).

However, running a test can generate lots of results when you use the Data-driven Testing method. In this PoC, we enhance the Data-driven test results in Azure Test Plan by supporting you to parameterize associated ADO test case IDs in Katalon Studio. Each test iteration ID in
Katalon Studio can be mapped to an ADO test case ID.

> **What is an iteration?**
>
> A test case executes with a test data row is considered an iteration.

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

Before you execute a test suite containing associated test cases, ensure you already enable ADO integration in Katalon Studio.

**In Azure Test Plans**:

You can view your test case IDs in Azure Test Plan.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ado-id.png" alt="ado ID" width=90%>

**In Katalon Studio**:

1. Open your desired Data-driven test case. To learn more about the test data, see [create your Test Data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html).

2. To add the `ado_id` variable, switch to the **Variables** tab of your test case. You can see a list of variables in that test case. Click **Add** and create a **Number** type variable names `ado_id`, with the **Default value** of your choice. Click **Save**. To learn more about variables, see [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/add%20variable.png" width=90%>

3. To call the `ado_id` variable, switch to the **Integration** tab and select the **Azure** integration. In the **ADO Test Case ID list**, call the variable with the syntax `${ado_id}`.

	You can map one test case ID in Katalon Studio with many test case IDs on ADO, IDs are separated by commas. For example, `${ado_id},123456` or `${ado_id}, ${ado_id_1}`.

    Ensure that your ADO test case ID list has no duplicate value. Duplicate test case IDs will be used one time only.

4. To check if the test case ID is valid, click **Verify**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/verified.png" alt="verify" width=70%>

5. Add your test case to a test suite to generate a test point in ADO. Test cases by themselves are not executable in ADO.

	> **What is Test Point?**
	>
	> A test point is a unique combination of a test case, test suite, configuration, and tester. To learn more about the test point, see Microsoft documentation: [Execute tab](https://docs.microsoft.com/en-us/azure/devops/test/new-test-plans-page?view=azure-devops#execute-tab).

6. To manage **Data Binding**, in the test suite editor, click **Show Data Binding**. The **Test Data** and **Variable Binding** tables appear. See [Manage Data Binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/ks-ddt-ado-binding.png" alt="conduct data binding" width=100%>

7. When you are done with the configuration, hit **Run** and execute your test suite with Data Binding.

	In this example, we have an `ado_id` list as below:

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/test%20data.png" alt="test data" width=50%>

	In ADO, we have two test case IDs: 3 and 7.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/test%20case%20ids.png" alt="ado IDs" width=100%>

	In the **Event Log**, you can find invalid ADO test case IDs.
	
	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/event-log.png" alt="event log" width=100%>

	In Azure Test Plan, you can find a report with a list of test iterations. Each test iteration from Katalon Studio is mapped to an ADO test case.

	<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/associated-ADO-TC-IDs/report%20in%20ADO.png" alt="report in ADO" width=100%>