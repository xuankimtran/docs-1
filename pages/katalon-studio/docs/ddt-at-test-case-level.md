---
title: "Data-driven testing at test case level"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/ddt-at-test-case-level.html
---

> **Important**
>
> * This Proof of Concept (PoC) is not ready for production use. We recommend using this PoC for evaluation purposes only.
> * Download Katalon Studio version [8.1.2.alpha](url).

Data-driven testing (DDT) at the test case level allows you to add one or more data files and manage variable binding at the test case level. 

This function is useful if you want to:
- Bind each test case to a fixed set of data.
- Run a test case with different test data combinations.
- When executing a test suite containing associated test cases, you can see the results of each test iteration with the mapped test data.

> **What is an iteration?**
>
> An iteration is a test case executed with a test data row.

> **Requirements:**
>
> * An active Katalon Studio Enterprise license.
> * An active Katalon Runtime Engine license. To learn more about Katalon licenses, you can refer to this document here: [Katalon licensing](https://docs.katalon.com/katalon-studio/docs/license.html).

In this article, we demonstrate how to manage data binding at the test case level and execute them in a test suite.

## Conduct data binding at the test case level
### Create a new test data

To create a new data file, go to **File > New > Test Data**. Katalon allows you to use external or internal data sources for test execution. To learn more about creating new data files, you can refer to this document: [Manage Test Data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html#create-an-excel-test-data).

### Create test case variables

1. Create a new test case. Go to **File > New > Test Case**. Here, we name the test case **DDT at TC level**.
2. In the new test case, switch to the **Variables & Data** tab. In the **Variables** section, to add test case variables, click **Add**. Input variables in the newly added row. 
    Values input here will automatically appear in the **Variable Binding** section.

      <img src="url" alt="Input variables appear in the variable binding section" width=70%>

### Manage data binding

In the **Data Binding** section, there are two tables:

- **Test Data**: Specify here the data files for your test execution.
- **Variable Binding**: This displays all variables input in the **Variables** section.

1. In the **Test Data** table:

  - Click **Add** to add one or more data files. A **Test Data Browser** dialog opens.
  
      <img src="url" width="70%" alt="Add data files">

  - Select the data files you wish to use for variable binding in the **Test Data Browser** dialog. Click **OK**. The selected test data files appear in the **Test Data** table.

      <img src="url" width="70%" alt="Test Data Browser"><br>
      
      <img src="url" width="70%" alt="Results after adding data files">

      > Note:
      > 
      > If you are adding a combination of data files, by default, Katalon defines the relationship of multiple data sources at the test case level as **One** - **One**. You can learn more about the relationship between multiple data files here: [Manage test data relationship](https://docs.katalon.com/katalon-studio/docs/combine-multiple-data-sources.html#manage-test-data-relationship).

  - To specify the data range, double-click on the cell under the **Data Iteration** column of each data files. You can learn more about types of data iteration here: [Modify data range](https://docs.katalon.com/katalon-studio/docs/combine-multiple-data-sources.html#modify-data-range).

2. In the **Variable Binding** table:
   
  - Katalon Studio allows users to **Set Type** for variables all at once if the variables have the same type.  
    In the following example, the **Employee** and **Department** variables have the same type as **Data Column**. Highlight both rows, click **Set Type > Data Column**.  

      <img src="url" width="70%" alt="Set Data Type">

  - In the **Test Data** column, click on each row to choose the test data files for execution.
       
      <img src="url" width="70%" alt="Choose Test data for Data Type">
      
  - In the **Value** column, click on each row to specify the data field in the selected data file.

      <img src="url" width="70%" alt="Choose Value for Data Type">

      > Note:
      > 
      > If the variables and the data field in the selected data files share the same name, you can quickly map all the variables with the data fields in the data file by clicking **Auto Map**. For example, with this function, the 'Employee' and the 'Department' variables automatically map with the 'Employee' and 'Department' columns of the test data.

  - Save the test case and run it. To view the results of your test, go to the **Log Viewer** tab.

      <img src="url" width="70%" alt="Results in Log Viewer">

## Execute test suites containing associated test cases

In this section, we demonstrate how to execute the associated test cases in:

- A dynamic test suite
- A suite test case
### Dynamic test suite 

Dynamic test suite is a test suite with multiple test cases added via a search query. You can dynamically add additional test cases while running the test suite. 
To learn more about the dynamic test suite, you can refer to this document: [Dynamic test suite](https://docs.katalon.com/katalon-studio/docs/create-test-suite.html#dynamic-test-suite-dynamic-test-cases-list).

1. To implement this function, install one of the plugins from the Katalon Store:
    * [Basic search For dynamic test suite.](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite)
    * [Test case management with tags.](https://store.katalon.com/product/6/Test-Case-Management-with-Tags)
    * [TestRail integration.](https://store.katalon.com/product/13/TestRail-Integration)

  - To activate the installed plugin, navigate to Account Settings in Katalon Studio and click **Reload Plugin**.
  
2. In the **Test Explorer** panel, right-click on **Test Suite**. Select **New > Dynamic Test Suite**.
3. To add test cases via search query, input the search condition into the **Query** box. Then hit **Preview** to query out the matching test cases. To learn more about the search query function, you can refer to this document: [Search test cases](https://docs.katalon.com/katalon-studio/docs/search.html).  
  For example: To add the associated test case into this dynamic test suite, you can input `id=(Test Cases/DDT at TC level)` into the **Query** box. The matched test case appears in the test suite.

    <img src="url" width="70%" alt="Results after searching query">
    
4. Hit **Run** to execute the test suite.  

  Alternatively, you can run the test suite in console mode. For detailed instructions on running a test execution in console mode, you can refer to this document: [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).
### Conduct data binding in a suite test case

> What is a suite test case?
>
> A suite test case is a test case in a test suite.

  1. Add the above test case to a test suite.
  2. To conduct **Data Binding**, in the test suite editor, click **Show Data Binding**. By default, this section shows the **Data binding** section from the test case added in Step 1.
      
      <img src="url" width="70%" alt="Default data binding section">
      
  3. Select the data binding level. Katalon allows you to select the data binding level at the test case (TC) level or the suite test case (STC) level.

      <img src="url" width="70%" alt="Data Binding Options">


      <table>
      <thead>
        <tr>
          <th>Use Test Case level </th>
          <th>Use Suite Test Case level</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>With this option:<br>- Data in the <strong>Test Data</strong> and <strong>Variable Binding</strong> tables are from the test case added in Step 1.<br>- You can edit these sections at the TC level.</td>
          <td>With this option:<br>- Data in the <strong>Test Data</strong> and <strong>Variable Binding</strong> tables are from the STC.<br>- You can edit these sections at the STC level. To learn more about binding data at the STC level, you can refer to this document:<br><a href="https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding" target="_blank" rel="noopener noreferrer">Manage Data Binding</a>.</td>
        </tr>
      </tbody>
      </table>
      
      > Note:
      >
      > In case your test suite has existing data configurations, switching to the **Use Test Case level** option does not remove the preconfigured data in the suite test case.

  4. When you are done with the configuration, hit **Run** to execute your test suite. 
### Test Reports

After the test suite execution, to view your test reports, in the **Test Explorer** panel, right-click at **Test Report > Open containing folder**. In the report, you can view:
  -  The final status of your test and test steps.
  -  The mapped data file of each test iteration.
      
  <img src="url" width="70%" alt="Reports">

> Note:
>
> Katalon Studio supports exporting test reports in **HTML**, **CSV**, **PDF** and **JUnit**. You can learn more about exporting reports here: [Generate reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html#automatically-generate-reports).