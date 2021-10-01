---
title: "Test Suite Collection" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/test-suite-collection.html 
redirect_from:
    - "/display/KD/Test+Suite+Collection/"
    - "/display/KD/Test%20Suite%20Collection/"
    - "/x/NgvR/"
    - "/katalon-studio/docs/test-suite-collection/"
    - "/display/KD/Execute+a+test+suite+collection/"
description: 
---
A Test Suite Collection contains a list of test suites to allow users more options for planning their test execution. 

To open a new Test Suite Collection, go to **File > New > Test Suite Collection**.
## Manage Execution Information

This section allows you to manage additional configurations for test suite collection execution. In the new **Test Suite Collection** page, click **Execution Information** to expanding the section.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/KS-TSC-execution-info.png" width=70% alt="Execution Information">

<table>
<thead>
<tr>
<th>Execution mode</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Sequential</strong></p>
</td>
<td>
<p>This mode allows you to&nbsp;execute the test suites one after another.</p>
</td>
</tr>
<tr>
<td>
<p><strong><strong>Parallel</strong></strong></p>
</td>
<td>
<p>This mode allows you to execute the test suites at the same time. With this mode, you can also set:</p>
<ul>
<li><strong>Max concurrent instances</strong>: To set the maximum number of test suites executing at the same time.</li>
<li><strong>Delay between instances (in seconds)</strong>: From Katalon version 8.2.0 onwards, you can set the delay time between each test suite execution from 0-999 seconds. This function reduces the risk of CPU spike issues when there are too many concurrent instances.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## Manage Test Suite List

You can add one or many test suites into a collection by following the steps below:

1.  In the command toolbar, click **Add** to add Test Suite.
   
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/image2017-2-17-133A243A44.png" width=40% alt="Click Add to add test suite">
    
2.  The opened **Test Suite Browser** dialog displays all test suites in Katalon Studio. Select the test suites you wish to execute, then click **OK**.  
    
3.  The selected test suites are added to the test suite collection accordingly.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/KS-TSC-Add-TS-to-TSC.png" width=70% alt="Add test suite into TSC">
    
    <table><thead><tr><th>Field</th><th>Description</th></tr></thead><tbody><tr><td>Run with</td><td><p> To select the environment executed with the Test Suite.</p></td></tr><tr><td>Run configuration</td><td><p>To add extra information to execute with the selected environment.</p><p>For example: Select mobile devices to be executed for Android environment</p><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/image2017-2-17-133A533A7.png"></p></td></tr><tr><td>Profile</td><td>Execution Profile that contains all variables values for each Test Suite execution. To learn more about the execution profile, you can refer to this documention: <a class="external-link" href="https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html" rel="nofollow">Execution Profile</a></td></tr><tr><td>Run</td><td> To choose the test suite you wish to run in the test suite collection. This is checked by default. </td></tr></tbody></table>
    
    > You can add one test suite to the collection multiple times. This capability helps you execute the same test suite in different environments.
## Execute a Test Suite Collection

1.  To run a Test Suite Collection, from the main toolbar, click **Execute**. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/KS-TSC-Execute-TS-to-TSC.png" width=60% alt="Run a test suite collection">

2.  After the test suite collection execution, from the **Test Explorer** panel, go to **Reports** to find test reports. To learn more about generating test reports, you can refer to this document: [Test Suite Collection Report](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html#report-history).

## Submit and view test results in Katalon TestOps

You can centralize test results including logs and attachments in Katalon TestOps. You can learn more about uploading test results to Katalon TestOps in this document: [Upload Test Results to Katalon TestOps from Katalon Studio]([/katalon-studio/docs/katalon-analytics-beta-integration.html](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html#upload-test-results-automatically)). 

## Schedule execution of Test Suite Collections remotely

You can schedule a test suite collection execution on multiple servers with Katalon TestOps. To learn more about planning and monitoring all test activities in Katalon TestOps, you can refer to this document here:
[Schedule Test Runs]([/katalon-analytics/docs/kt-remote-execution.html](https://docs.katalon.com/katalon-analytics/docs/create-plan.html#advanced-settings)).

To quickly schedule a test suite colllection execution on Katalon TestOps from Katalon Studio, in the **Test Suite Collection** page, click **Schedule on Katalon TestOps**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/KS-TSC-Schedule-a-TSC.png" width=60% alt="Schedule on Katalon TestOps">