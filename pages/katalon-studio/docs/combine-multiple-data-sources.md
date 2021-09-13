---
title: "Combine multiple data sources" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/combine-multiple-data-sources.html 
description: 
---

This article shows you how to execute your automation test using predefined test data from multiple sources.

Go to your test suite, click **Show Data Binding** to expand the **Data Binding** section. This feature binds the predefined test data files and manage variable binding with the Test Suite you want to run.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/1-databinding.png" width="70%" alt="Expand data binding section">

In the extending **Data Binding** section, there are two tables:

- **Test Data**: Support specifying data files for your test execution.
- **Variable Binding**: Display all variables of the selected test case. See also [Test case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html#view-and-declare-variables-in-script-mode).

## Test Data Table
### Adding data sources  

1. In the **Test Data** table, click **Add** to add data file(s). A **Test Data Browser** dialog opens.
   
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-6-30-213A473A37.png" width="50%" alt="Add data files">


2. Select a combination of data files you wish to use for variable binding in the **Test Data Browser** dialog. Click **OK**. The selected test data files appear in the **Test Data** table.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/data-browser.png" width="50%" alt="Test Data Browser"> 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/KS-MULTIPLE-add-data-files.png" width="70%" alt="Results after adding data files"> 

### Modify data range

To specify the data range, double-click on the cell under the **Data Iteration** column of each data files.  

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/data-iteration.png" width="50%" alt="Data Iteration"> 


<table><thead><tr><th>Option</th><th>Description</th></tr></thead><tbody><tr><td>Run all rows</td><td>To use all the data rows in the data file in the test execution.</td></tr><tr><td>Run from row ... to row ...</td><td>To use the data range from a particular row to another particular row in the data file during the test execution.</td></tr><tr><td>Run with specific rows</td><td><p>To use the specific data rows in the data file during test execution. You can use <strong>comma</strong> and <strong>hyphen</strong> characters to define the rows.</p><p>For example:</p><ul><li>to use three data rows (row 1, row 2, row 3), enter: 1,2,3</li><li>to use six data rows (row 1, row 2, row 3, row 4, row 5, row 9), enter: 1-5,9</li></ul></td></tr></tbody></table>

### Manage test data relationship

To toggle between *One* and *Many*, click on the cell under the **Type** column of each data files. These types represent the relationship of multiple test data sources. 

You can also further define the relationship among them as below:

| Relationship Type | Description |
| --- | --- |
| One | To indicate the data set as 'One' in the relationship with the other data set. |
| Many | To indicate the data set as 'Many' in the relationship with the other data set. |

Therefore, we have the following combinations of data sets:

<table><thead><tr><th>Relationship</th><th>Example</th></tr></thead><tbody><tr><td>One to One</td><td><p>Given there are two data sets as below:</p><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/KS-MULTIPLE-Managa-data-relationship-One-One.png" width="70%" alt="Manage Data Relationships One One"><img width=170 src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/one-one.png"></p><p>Then the final data set used for test execution will be:</p><ul><li>John Marketing</li><li>Joe Sales</li></ul></td></tr><tr><td>Many to Many</td><td><p>Given there are two data sets as below:</p><p>
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/KS-MULTIPLE-Manage-data-relationships-Many-Many.png" width="70%" alt="Manage Data Relationship One Many"><img width=170 src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/many-many.png"></p><p>Then the final data set used for test execution will be:</p><ul><li>John Marketing</li><li>John Sales</li><li>Joe Marketing</li><li>Joe Sales</li><li>Mary Marketing</li><li>Mary Sales</li></ul></td></tr><tr><td>One to Many</td><td><p>Given there are two data sets as below:</p><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/KS-MULTIPLE-Manage-data-relationship-One-Many.png" width="70%" alt="Manage Data Relationship Many Many"><img width=170 src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/one-many.png"></p><p>Then the final data set used for test execution will be:</p><ul><li>John Marketing</li><li>Joe Marketing</li><li>Mary Marketing</li><li>Emily Marketing</li><li>John Sales</li><li>Joe Sales</li><li>Mary Sales</li><li>Emily Sales</li></ul></td></tr><tr><td>One to One to Many</td><td><p>Given there are three data sets as below:</p><p><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/KS-MULTIPLE-Manage-data-relationships-One-One-Many.png" width="70%" alt="Manage Data Relationships One One Many"><img width=220 src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/one-one-many.png"></p><p>Then the final data set used for test execution will be:</p><ul><li>John Marketing Executive</li><li>John Marketing Director</li><li>Joe Sales Executive</li><li>Joe Sales Director</li></ul></td></tr></tbody></table>

## Variable Binding Table

After adding the test case into the test suite, Katalon automatically imports all variables of the selected test case into the **Variable Binding** table.

1. Katalon Studio allows users to **Set Type** for variables all at once if the variables have the **same type**. In this case, Username and Password have the same type as *Data Column*. Highlight both rows, click **Set Type > Data Column**.  
    
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/set-type.png" width="70%" alt="Set Data Type">

2. In the **Test Data** column, click on each row to choose the test data files for execution.
    
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/bind-test-data.png" width="70%" alt="Choose Test data for Data Type"> 

3. In the **Value** column, click on each row to specify the data field in the selected data file.
    
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/bind-value.png" width="70%" alt="Choose Value for Data Type">

4. Save the test suite when you finish.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/combine-multiple-data-sources/binding.png" width="70%" alt="Final result">
    
During execution, the _username_ variable looks for the _Username_ column of the _valid-accounts_ excel file while the _password_ variable searches for the _Password_ column of the _valid-accounts_ CSV file.
### Bind to Scripting value

This option allows you to associate the variables with other scripting values.

1.  Highlight rows No. 1 and No.2 > click **Set Type** > select **Script Variable**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-8-31-153A193A20.png" width="70%" alt="Script Variable Option"> 

2.  Specify the data used in the **Value** cell.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/design-a-test-suite/image2017-8-31-153A213A10.png" width="70%" alt="Secify Value in Script Variable"> 

