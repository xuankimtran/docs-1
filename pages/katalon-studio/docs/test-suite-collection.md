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

This section allows you to manage additional configurations for test suite collection execution. In the new **Test Suite Collection** page, click **Execution Information** to expanding the section:

<img src="url" width=60% alt="Execution Information">

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
<li><strong>Max concurrent instances</strong>: To set the number of test suites executing at the same time.</li>
<li><strong>Delay between instances (in seconds)</strong>: To configure the delay time between each test suite execution. You can set the delay time between 0-999 seconds. This function reduces the risk of CPU spike issues when there are too many concurrent test suite executions.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## Manage Test Suite List

You can add a test suite into a collection by following the steps below:

1.  In the command toolbar, click **Add** to add Test Suite.
   
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/image2017-2-17-133A243A44.png)  
      
    
2.  All test suites in Katalon Studio are displayed in **Test Suite Browser**. Select your test suites to be executed then click **OK**.  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/image2017-2-17-133A283A17.png)  
      
    
3.  The selected test suites will be added to the test suite collection accordingly  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/image2018-5-7-153A373A21.png)  
    where:
    
    <table><thead><tr><th>Field</th><th>Description</th></tr></thead><tbody><tr><td>Run with</td><td><p>The environment to be executed with the Test Suite.</p></td></tr><tr><td>Run configuration</td><td><p>Extra information for executing with the selected environment.</p><p><strong>For example:</strong> Select mobile devices to be executed for Android environment</p><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/image2017-2-17-133A533A7.png"></p></td></tr><tr><td>Profile</td><td><a class="external-link" href="/x/xAHR" rel="nofollow">Execution Profile</a> that contains all variables values for each Test Suite execution.</td></tr><tr><td>Run</td><td>This is checked by default. It means that the test case will be executed when running the collection.</td></tr></tbody></table>
    
      
    
    > You can add one test suite to the collection multiple times. This is particularly helpful when the users want to execute the same suite on different environments.
    

## Execute a Test Suite Collection

1.  To run a Test Suite Collection, click **Execute** at toolbar as illustrated below:  
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-suite-collection/image2018-5-7-163A33A11.png)  
      
    
2.  All test suites will be executed accordingly.
3.  Data of historical execution can be found in Reports. Refer to [Test Suite Collection Report](/display/KD/Test+Suite+Collection+Report) for more details.

## Submit and view test results on Katalon TestOps

You can centralize test results including logs and attachments on [Katalon TestOps](/katalon-studio/docs/katalon-analytics-beta-integration.html). Besides test results management, Katalon TestOps will also provide analytics to improve the quality of your test cases.

## Schedule execution of Test Suite Collections remotely

You can leverage [Katalon TestOps](/katalon-analytics/docs/kt-remote-execution.html) to execute Test Suite Collections on multiple servers. The executions can be scheduled to run periodically e.g. hourly or daily.