---
title: "Call Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/call-test-case.html
redirect_from:
    - "/display/KD/Call+Test+Case/"
    - "/display/KD/Call%20Test%20Case/"
    - "/x/qgAM/"
    - "/katalon-studio/docs/call-test-case/"
description:
---
> For more details on how to apply test cases in Data-driven Testing, refer to [Test Case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html).

When generating test steps in a test case, you can also call another test case as a test step. This article guides you through how to call a test case in manual and script view.

## Call Test Case in Manual view

To call another test case in **Manual** view, do as follows:

1. Open a test case in **Manual** view. Click on the drop-down icon of the **Add** button, then select **Call Test Case**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/call-test-case/call-test-case.png" alt="call test case option" width="70%">

2. The **Test Case Browser** dialog appears. This dialog shows all existing test cases within the project. Select a test case to be called, then click **OK**. You can only call one test case at a time.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/call-test-case/test-case-browser.png" alt="test case browser" width="60%">

3.  A **Call Test Case** step is now added with the selected test case above as its target.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/call-test-case/call-test-case-manual.png" alt="call test case in manual view" alt="70%">

    > Once a test step is added as **Call Test Case**, you cannot change it to another keyword.

## Call Test Case in Script view

In the **Script view**, the `callTestCase` method allows users to call another test case as a test step.

Open a test case in the script view, then refer to the following syntaxes:

```groovy

import com.kms.katalon.core.model.FailureHandling
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI

//Call test case using WebUI Class
WebUI.callTestCase(findTestCase("Test Case ID"), ["key1":"value1", "key2":"value2", … , "keyN":"valueN"], FailureHandling.OPTIONAL)

//Call test case using Mobile Class
Mobile.callTestCase(findTestCase("Test Case ID"), ["key1":"value1", "key2":"value2", … , "keyN":"valueN"], FailureHandling.OPTIONAL)
```

<table>
	<thead>
		<tr>
			<th>Items</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Test Case ID</td>
			<td>
				<p>The ID of the test case to be called. You can find this info in the test case properties. Learn more about test case properties here: <a href="https://docs.katalon.com/katalon-studio/docs/search.html#view-test-artifact-properties">View test artifact properties</a>.</p>
			</td>
		</tr>
		<tr>
			<td>
				<p>Parameters binding:</p>
				<pre><code class="language-groovy">[key1:value1, key2:value2, &hellip; , keyN:valueN]</code></pre>
			</td>
			<td>
				<p>The list of input parameters for that test case, if any:</p>
				<ul>
					<li>Key(s): The defined <a class="external-link" href="https://docs.katalon.com/katalon-studio/docs/variable-types.html#test-case-variables" rel="nofollow">Test Case variables</a> within the called test case.</li>
					<li>Value: the value to be used for the corresponding public variables.</li>
				</ul>
			</td>
		</tr>
		<tr>
			<td>FailureHandling.option</td>
			<td>The failure handling option for the current test step. This parameter is optional. See also: <a href="https://docs.katalon.com/katalon-studio/docs/failure-handling.html">Failure Handling</a>.</td>
		</tr>
	</tbody>
</table>

For example:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/call-test-case/call-test-case-script.png" alt="call test case in script view" width="100%">
