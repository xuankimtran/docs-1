---
title: "Data Driven Testing at Test Case level"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/data-driven-testing-at-test-case-level.html
---

> **Important**
>
> * This Proof of Concept (PoC) is not ready for production use. We recommend using this PoC for evaluation purposes only.
> * Download Katalon Studio version [8.1.2.alpha](url).

<INTRODUCTION>

Katalon Studio offers data-driven testing at test case level. 

This is useful if you want to:
- Bind each test case to a fixed set of data.
- Run a test case with different test data combinations.

> **Requirements**
>
> * An active Katalon Studio Enterprise license.
> * A Katalon Runtime Engine License. To learn more about Katalon licenses here: [Katalon licensing](https://docs.katalon.com/katalon-studio/docs/license.html).

In this article, we demonstrate how to manage data binding at test case level and execute them in a test suite.

## Data-driven testing at test case level

In the following example, we configure a data-driven testing at test case level with the following statement:

``` groovy
println "${employee} - ${department}"
```
Do as follows:

### Create a new Test Data

Katalon allows you to use external or internal data sources for test execution. To learn more about creating new data files, you can refer to this document: [Manage Test Data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html#create-an-excel-test-data)
### Create a new Test Case 

  1. Create a new test case. Go to **File > New > Test Case**. 
  2. In the new test case, switch to the the **Variables & Data** tab. There are two sections in this tab:

  - **Variables** section: Support defining variables populated in the **Variables Binding** table.
  - **Data Binding** section: You can add predefined test data files and manage variable binding for your test case execution.

<img src="url" alt="Variables & Data section" width=70%>

### Manage Variables section

In the **Variables** section of the **Variables & Data** tab, to add test case variables, click **Add**. Input variables in the newly added row.

  For example:

  <img src="url" alt="Input Variables" width=70%>

### Manage Data Binding section

In the **Data Binding** section, there are two tables:

- **Test Data**: Specify here data files for your test execution.
- **Variable Binding**: This displays all variables from the  **Variables** section. See also [Test case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html#view-and-declare-variables-in-script-mode).

  1. In the **Test Data** table:

     - Click **Add** to add data file(s). A **Test Data Browser** dialog opens.
  
      <img src="url" width="70%" alt="Add data files">

     - Select the data file(s) you wish to use for variable binding in the **Test Data Browser** dialog. Click **OK**. The selected test data file(s) appear in the **Test Data** table.

      <img src="url" width="70%" alt="Test Data Browser">
      <img src="url" width="70%" alt="Results after adding data files">

      > Note:
      > 
      > In case you are adding a combination of data files, by default, Katalon defines the relationship of multiple data sources at test case level as One - One. You can learn more about the relationship of multiple data file here: [Manage test data relationship](https://docs.katalon.com/katalon-studio/docs/combine-multiple-data-sources.html#manage-test-data-relationship).

      - To specify the data range, double-click on the cell under the **Data Iteration** column of each data files. You can learn more about specifying data iteration here: [Modify data range](https://docs.katalon.com/katalon-studio/docs/combine-multiple-data-sources.html#modify-data-range).

  2. In the **Variable Binding** table, it displays all variables from the **Variables** section of the test.
   
      - Katalon Studio allows users to **Set Type** for variables all at once if the variables have the **same type**. 
        In the following example, the **Employee** and **Department** variables have the same type as *Data Column*. Highlight both rows, click **Set Type > Data Column**.  

        <img src="url" width="70%" alt="Set Data Type">

      - In the **Test Data** column, click on each row to choose the test data files for execution.
       
        <img src="url" width="70%" alt="Choose Test data for Data Type">
      
      - In the **Value** column, click on each row to specify the data field in the selected data file.

        <img src="url" width="70%" alt="Choose Value for Data Type">

      > Note:
      > 
      > In case the variables and the data field in the selected data files share the **same name**, you can quickly map all the variables with its data field in the data file by clicking **Auto Map**. For example, the 'Employee' and 'Department' variables automatically maps with the 'Employee' and 'Department' columns of the test data.

      - Save the test case and run it. To view the the results of your test, go to the **Log Viewer** tab.

        <img src="url" width="70%" alt="Results in Log Viewer">

## Execute Test Suite with Associated Test Case


### Dynamic Test Suite


### Data-binding Test Suite

> **What is a Suite Test Case?**
>
> A Suite Test Case is a test case added to a test suite.


Katalon allows you to select Data Binding options between Test Case level and Suite Test Case level.
