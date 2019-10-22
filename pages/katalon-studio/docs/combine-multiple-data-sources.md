---
title: "Combine multiple data sources" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/combine-multiple-data-sources.html 
description: 
---

This section shows how to execute your automation test using predefined test data from multiple sources.

In the test suite editor, click **Show Data Binding** to add predefined test data files and manage variable binding for your test case execution.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/1-databinding.png" width="695" height="238">

Katalon Studio expands the Data Binding section with **Test Data** and **Variable Binding** tables.

* [Test Data](/display/KD/Manage+Test+Data): You can specify data files used for data binding.
* Variable Binding: If there's any [public variable](/display/KD/Variable+Types#VariableTypes-Publicvariables) defined in your test case, you can manage variable binding by specifying which value would be used for which variables during test execution.

## Test Data

1. In the **Test Data** table, click **Add** to add data file(s).

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-6-30-213A473A37.png)

2. In **Test Data Browser**, select a combination of data files you prefer to use for variable binding. The selected test data files are added to the table accordingly.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/data-browser.png" width="385" height="404"> 

5. Double-click on the **Data Iteration** to specify the data range to be used for execution.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/data-iteration.png" width="341" height="200"> 

    Where:

    <table><thead><tr><th>Option</th><th>Description</th></tr></thead><tbody><tr><td>Run all rows</td><td>All the data rows in the data file will be used during test execution.</td></tr><tr><td>Run from row ... to row ...</td><td>The data range from a particular row to another particular row in the data file will be used during test execution.</td></tr><tr><td>Run with specific rows</td><td><p>The data rows which are specified here will be used during test execution. You can use <strong>comma</strong> and <strong>hyphen</strong> characters to define the rows.</p><p>For example:</p><ul><li>to use three data rows (row 1, row 2, row 3), enter: 1,2,3</li><li>to use six data rows (row 1, row 2, row 3, row 4, row 5, row 9), enter: 1-5,9</li></ul></td></tr></tbody></table>

6. Click **Type** to toggle between *One* and *Many*, which represents the test data relationship of multiple test data sources.

### Manage test data relationship

If you are specifying multiple test data, you can further define the relationship among them to decide how the final data set used in the test execution will be. There are two types of relationship supported in Katalon Studio:

| Relationship Type | Description |
| --- | --- |
| One | The data set will be indicated as 'One' in the relationship with other data set. |
| Many | The data set will be indicated as 'Many' in the relationship with other data set. |

Therefore, we have the following combinations of data sets:

<table><thead><tr><th>Relationship</th><th>Example</th></tr></thead><tbody><tr><td>One to One</td><td><p>Given there are two data sets as below:</p><p><img width=170 src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/one-one.png"></p><p>Then the final data set used for test execution will be:</p><ul><li>John Marketing</li><li>Joe Sales</li></ul></td></tr><tr><td>Many to Many</td><td><p>Given there are two data sets as below:</p><p><img width=170 src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/many-many.png"></p><p>Then the final data set used for test execution will be:</p><ul><li>John Marketing</li><li>John Sales</li><li>Joe Marketing</li><li>Joe Sales</li><li>Mary Marketing</li><li>Mary Sales</li></ul></td></tr><tr><td>One to Many</td><td><p>Given there are two data sets as below:</p><p><img width=170 src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/one-many.png"></p><p>Then the final data set used for test execution will be:</p><ul><li>John Marketing</li><li>Joe Marketing</li><li>Mary Marketing</li><li>Emily Marketing</li><li>John Sales</li><li>Joe Sales</li><li>Mary Sales</li><li>Emily Sales</li></ul></td></tr><tr><td>One to One to Many</td><td><p>Given there are three data sets as below:</p><p><img width=220 src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/one-one-many.png"></p><p>Then the final data set used for test execution will be:</p><ul><li>John Marketing Executive</li><li>John Marketing Director</li><li>Joe Sales Executive</li><li>Joe Sales Director</li></ul></td></tr></tbody></table>

## Variable Binding

In the **Variable Binding** table, all the public variables defined in that test case are displayed for being bound to the configured test data.

1. Katalon Studio allows users to **Set Type** for variables all at once if the variables have the **same type**. In this case, Username and Password have the same type as *Data Column*. Highlight both rows, click **Set Type** and select **Data Column**:  
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/set-type.png" width="548" height="141">
      
2. Click on each cell of the **Test Data** column to decide which test data from the list to be passed into this variable during execution.
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/bind-test-data.png" width="553" height="263"> 

3. Click on each cell of the **Value** column to specify the data field to be used during execution. Select one of the headers of the selected test data; the selected header will be specified accordingly.
    
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/bind-value.png" width="551" height="236">

4. Save the test suite when you're done.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/binding.png" width="707" height="120">
    
    During execution, the _username_ variable looks for the _Username_ column of the _valid-accounts_ excel file while the _password_ variable searches for the _Password_ column of the _valid-accounts_ CSV file.

### Bind to Scripting value

This option allows you to associate the variables with other scripting value.

1.  Highlight rows No. 1 and No.2 > click **Set Type** > select **Script Variable**.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-8-31-153A193A20.png)

2.  Specify the data to be used in the **Value** cell. This value is  used during execution.

    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-8-31-153A213A10.png)