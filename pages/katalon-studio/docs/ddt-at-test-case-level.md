---
title: "Data-driven testing at test case level (PoC)"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/ddt-at-test-case-level.html
---

> Important:
> * This Proof of Concept (PoC) is not ready for production use. We recommend using this PoC for evaluation purposes only.
> * Download Katalon Studio version [8.1.2.alpha](https://github.com/katalon-studio/katalon-studio/releases/tag/v8.1.2.alpha).

Data-driven testing (DDT) at the test case level allows you to add one or more data files and manage data binding at the test case level. 

This function is useful if you want to:
- Bind each test case to a fixed set of data.
- Run a test case with different test data combinations.
- When executing a test suite containing associated test cases, you can either reuse data binding at the test case level or conduct new data binding in a test suite.

> Requirements:
> * An active Katalon Studio Enterprise license.
> * An active Katalon Runtime Engine license. To learn more about activating your license, you can refer to this document here: [Activate Katalon license](https://docs.katalon.com/katalon-studio/docs/activate-license.html#activate-a-license-with-internet-access).

In this article, we demonstrate how to manage data binding at the test case level and execute them in a test suite.

## Conduct data binding at the test case level
### Create a new test data

To create a new data file, go to **File > New > Test Data**. Katalon allows you to use external or internal data sources for test execution. To learn more about creating new data files, you can refer to this document: [Manage Test Data](https://docs.katalon.com/katalon-studio/docs/manage-test-data.html#create-an-excel-test-data).

### Create test case variables

1. Create a new test case. Go to **File > New > Test Case**. Here, we name the test case **DDT at TC level**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-New-test-case.png" alt="New test case" width=100%>

2. In the new test case, switch to the **Variables & Data Binding** tab. In the **Variables** section, to add test case variables, click **Add**. Input variables in the newly added row. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Variables-binding-tab.png" alt="The variable & data binding tab" width=100%>

    Values input here will automatically appear in the **Variable Binding** section.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Binding-variables-at-TC-level.png" alt="Input variables appear in the variable binding section" width=100%>

### Manage data binding

> What is an iteration?
>
> An iteration is a test case executed with a test data row.

In the **Data Binding** section, there are two tables:

- **Test Data**: Specify here the data files for your test execution.
- **Variable Binding**: This displays all variables input in the **Variables** section.

1. In the **Test Data** table:

  - Click **Add** to add one or more data files. A **Test Data Browser** dialog opens.
  
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Add-data-files.png" width="70%" alt="Add data files">

  - Select the data files you wish to use for variable binding in the **Test Data Browser** dialog. Click **OK**. The selected test data files appear in the **Test Data** table.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Test-data-browser-2.png" width="50%" alt="Test Data Browser"><br>
      
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Results-after-adding-data.png" width="100%" alt="Results after adding data files">

      > Notes:
      > 
      > If you are adding a combination of data files, by default, Katalon defines the relationship of multiple data sources at the test case level as One-to-One relationship. You can learn more about the relationship between multiple data files here: [Manage test data relationship](https://docs.katalon.com/katalon-studio/docs/combine-multiple-data-sources.html#manage-test-data-relationship).

  - To specify the data range, double-click on the cell under the **Data Iteration** column of each data file. You can learn more about types of data iteration here: [Modify data range](https://docs.katalon.com/katalon-studio/docs/combine-multiple-data-sources.html#modify-data-range).

2. In the **Variable Binding** table:
   
  - Katalon Studio allows users to **Set Type** for variables all at once if the variables have the same type.  
    In the following example, the **Employee** and **Department** variables have the same type as **Data Column**. Highlight both rows, click **Set Type > Data Column**.  

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Set-data-type.png" width="70%" alt="Set Data Type">

  - In the **Test Data** column, click on each row to choose the test data files for execution.
       
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Choose-test-data-for-data-type.png" width="70%" alt="Choose Test data for Data Type">
      
  - In the **Value** column, click on each row to specify the data field in the selected data file.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Choose-value-for-data-type.png" width="70%" alt="Choose Value for Data Type">

      > Notes:
      > 
      > If the variables and the data field in the selected data files share the same name, you can quickly map all the variables with the data fields in the data file by clicking **Map All**. For example, with this function, the 'Employee' and the 'Department' variables automatically map with the 'Employee' and 'Department' columns of the test data.

  - Save the test case and run it. To view the results of your test, go to the **Log Viewer** tab.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Test-case-results.png" width="70%" alt="Results in Log Viewer">

## Execute test suites containing associated test cases

> What is a suite test case?
>
> A suite test case is a test case in a test suite.

In this section, we demonstrate how to execute the associated test cases in:

- A suite test case
- A dynamic test suite
### Conduct data binding at the suite test case level

1. Add the above test case to a test suite.
2. To conduct **Data Binding**, in the test suite editor, click **Show Data Binding**. 
      
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Show-data-binding-2.png" width="100%" alt="Data binding section in the test suite">
      
3. Select the data binding level. Katalon allows you to select the data binding level at the test case (TC) level or the suite test case (STC) level. By default, the **Use Variables and Binding at Suite Test Case** option is selected.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Data-binding-options.png" width="100%" alt="Data Binding Options">


    <table>
    <thead>
      <tr>
      <th>Options</th>
      <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
      <td>Use Variables and Binding at Test Case</td>
      <td>With this option:<br>- Katalon executes the associated test case with the data binding at the test case level.<br>- To edit the data binding at the test case level, click the <strong>Test Case</strong> hyperlink. By doing so, the users are transitted to the <strong>Variables & Data Binding</strong> tab of the associated test case.<br><p style="text-align: center;"><a class="pop"><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Click-TC-hyperlink.gif" width="70%" alt="Choose the Use Variables and Binding at Test Case option"></a><br><em>Click the gif to enlarge it.</em></p><br>- While selecting the <strong>Use Variables and Binding at Test Case</strong> option, the data binding at the suite test case level is disabled.<br><p style="text-align: center;"><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Warning-at-TC-level.png" width="70%" alt="Choose the Use Variables and Binding at Test Case option"></p></td>
      </tr>
      <tr>
      <td>Use Variables and Binding at Suite Test Case</td>
      <td>With this option:<br>- Katalon executes the associated test case with the data binding at the suite test case level.<br>- You can edit the <strong>Test Data</strong> and <strong>Variable Binding</strong> tables at the STC level. To learn more about binding data at the STC level, you can refer to this document: <a href="https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html#manage-data-binding" target="_blank" rel="noopener noreferrer">Manage Data Binding</a>.<br><p style="text-align: center;"><a class="pop"><img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Binding-suite-test-case-2.png" width="70%" alt="Choose the Use Variables and Binding at Suite Test Case option"></a><br><em>Click the image to enlarge it.</em></p></td>
      </tr>
    </tbody>
    </table>
        
    > Notes:
    > * In case your test suite has existing data configurations, switching to the **Use Variables and Binding at Test Case** option does not remove the preconfigured data in the suite test case.

4. When you are done with the configuration, hit **Run** to execute your test suite. 
### Dynamic test suite 

A dynamic test suite is a test suite with multiple test cases added via a search query. You can dynamically add additional test cases while running the test suite. 
To learn more about dynamic test suites, you can refer to this document: [Dynamic test suite](https://docs.katalon.com/katalon-studio/docs/create-test-suite.html#dynamic-test-suite-dynamic-test-cases-list).

1. To implement this function, install one of the plugins from the Katalon Store:
    * [Basic Search For Dynamic Test Suite](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite)
    * [Test case management with tags](https://store.katalon.com/product/6/Test-Case-Management-with-Tags)
    * [TestRail integration](https://store.katalon.com/product/13/TestRail-Integration)

  - To activate the installed plugin, navigate to Account Settings in Katalon Studio and click **Reload Plugin**.
  
2. In the **Test Explorer** panel, right-click on **Test Suite**. Select **New > Dynamic Test Suite**.
3. To add test cases via search query, input the search condition into the **Query** box. Then hit **Preview** to query out the matching test cases. To learn more about the search query function, you can refer to this document: [Search test cases](https://docs.katalon.com/katalon-studio/docs/search.html).  
  For example: To add the associated test case into this dynamic test suite, you can input `id=(Test Cases/DDT at TC level)` into the **Query** box. The matched test case appears in the test suite.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Dynamic-Test-suite.png" width="100%" alt="Results after searching query">
    
4. Hit **Run** to execute the test suite.  

  Alternatively, you can run the test suite in console mode. For detailed instructions on running a test execution in console mode, you can refer to this document: [Command Builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#command-builder).
### Test Reports

After the test suite execution, to view your test reports, go to the **Reports** folder in the **Test Explorer** panel. 

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ddt-test-case-level/KS-DDT-Reports-2.png" width="100%" alt="Reports">

Alternatively, you can also view your reports and details in `<your-project-folder>/Reports`. Katalon Studio supports exporting test reports into different formats, such as HTML, CSV, PDF, and JUnit. You can learn more about exporting reports here: [Generate reports](https://docs.katalon.com/katalon-studio/docs/test-suite-report.html#automatically-generate-reports).

> Notes:
> * For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).


