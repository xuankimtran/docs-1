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

A Test Suite Collection (TSC) contains a list of test suites to allow users more options to plan their test execution. 

To open a new Test Suite Collection, go to **File > New > Test Suite Collection**. The new **Test Suite Collection** page opens with two sections:

* **Execution Information**: This section allows you to manage additional configurations for TSC execution. 
* **Test Suite List**: This section allows you to add one or many test suites into a collection.
## Manage Execution Information

After creating a TSC, in the new **Test Suite Collection** page, click **Execution Information** to expand the section.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/KS-TSC-Execute-information-2.png" width=70% alt="Execution Information">

<table style="width: 1027px;">
<thead>
<tr>
<th style="width: 84.5781px; text-align: left;">Execution mode</th>
<th style="width: 925.422px;">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td style="width: 84.5781px;">
<p><strong>Sequential</strong></p>
</td>
<td style="width: 925.422px;">
<p>This mode allows you to&nbsp;execute the test suites one after another.</p>
</td>
</tr>
<tr>
<td style="width: 84.5781px;">
<p><strong><strong>Parallel</strong></strong></p>
</td>
<td style="width: 925.422px;">
<p>This mode allows you to execute the test suites at the same time. With this mode, you can also set:</p>
<ul>
<li><strong>Max concurrent instances</strong>: To set the maximum number of test suites executing at the same time.</li>
<li><strong>Delay between instances (in seconds)</strong>: From Katalon version 8.2.0 onwards, you can set the delay time between each test suite execution from 0-999 seconds. This function reduces the risk of CPU spike issues when there are too many concurrent instances. When a test suite is ready to start, Katalon will print the following message in the <strong>Event Log</strong> tab: <code>Test suite ${testSuiteID} is ready to start at ${currentTimeStamp}</code></li>
</ul>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/KS-TSC-Print-event-log-2.png" alt="Event Log message" width="60%" /></p>
</td>
</tr>
</tbody>
</table>

## Manage Test Suite List

After configuring the **Execution Information** section, to add test suites into a collection, follow the steps below:

1.  In the command toolbar, click **Add** to add a Test Suite.
   
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/image2017-2-17-133A243A44.png" width=40% alt="Click Add to add test suite">
    
2.  The **Test Suite Browser** dialog appears, displaying all your Katalon Studio test suites. Select the test suites you wish to execute, then click **OK**.  
    
3.  The selected test suites are added to the test suite collection accordingly.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/KS-TSC-Add-test-to-TSC-2.png" width=70% alt="Add test suite into TSC">
    
    <table><thead><tr><th>Field</th><th>Description</th></tr></thead><tbody><tr><td>Run with</td><td><p> To select the environment executed with the Test Suite.</p></td></tr><tr><td>Run configuration</td><td><p>To add extra information to execute with the selected environment.</p><p>For example: Select mobile devices to be executed for Android environment</p><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/image2017-2-17-133A533A7.png"></p></td></tr><tr><td>Profile</td><td>Execution Profile that contains all variables values for each Test Suite execution. To learn more about the execution profile, you can refer to this document: <a class="external-link" href="https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html" rel="nofollow">Execution Profile</a></td></tr><tr><td>Run</td><td> To choose the test suite you wish to run in the test suite collection. This is checked by default. </td></tr></tbody></table>
    
    > You can then configure each duplicated test suite individually, for example to run the same test suites in different environments.
## Execute a Test Suite Collection

1.  To run a TSC, from the main toolbar, click **Execute**. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/KS-TCS-Execute-TCS-2.png" width=60% alt="Run a test suite collection">

2.  After the TSC execution, from the **Test Explorer** panel, go to **Reports** to find test reports. To learn more about generating test reports, you can refer to this document: [Test Suite Collection Report](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html#report-history).

## Submit and view test results in Katalon TestOps

You can centralize test results including logs and attachments in Katalon TestOps. You can learn more about uploading test results to Katalon TestOps in this document: [Upload Test Results to Katalon TestOps from Katalon Studio]([/katalon-studio/docs/katalon-analytics-beta-integration.html](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html#upload-test-results-automatically)). 

## Schedule execution of Test Suite Collections remotely

You can schedule a TSC execution on multiple servers with Katalon TestOps. To learn more about planning and monitoring all test activities in Katalon TestOps, you can refer to this document here:
[Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html#schedule-test-runs).

To quickly schedule a TSC execution on Katalon TestOps from Katalon Studio, in the **Test Suite Collection** page, click **Schedule on Katalon TestOps**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/KS-TSC-Schedule-a-TSC-2.png" width=60% alt="Schedule on Katalon TestOps">