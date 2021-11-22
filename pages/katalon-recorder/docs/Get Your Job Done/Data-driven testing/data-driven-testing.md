---
title: "Data-driven testing"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/data-driven-testing.html
redirect_from: katalon-recorder/docs/data-driven-execution.html
description:
---

Data-driven testing (DDT) allows you to execute test cases using data from external data files in forms of table or speadsheet format. Katalon Recorder facilitates DDT by providing DDT commands and binding test cases with data files.

> **Requirements**:
>
> Katalon Recorder version 5.6.0 onwards.

This guide introduces you to DDT commands in Katalon Recorder and shows you how to implement DDT in a test case.

## Data-driven commands

Katalon Recorder provides two commands for DDT: `loadVars` and `endLoadVars`.

### loadVars

The `loadVars` command loads the values from the data file specified in the **Target** field. 

### endLoadVars

The `endLoadVars` command terminates the data-driven block. You need to add it to your test; otherwise, you will get an error message.

### Data-driven testing process

When you execute a test containing `loadVars` and `endLoadVars` commands, the following process will take place, with *i* starting with 1 and ending with the number of rows in the data file:

1. The *ith* row of the data file will be fetched.
2. The values of the row will be mapped to the variables used in the test case.
3. The steps between `loadVars` and `endLoadVars` will be executed using these mapped values.

## Implement data-driven testing

In Katalon Recorder, there are two steps to implement DDT in a test case:

1. Add data files to your workspace.
2. Configure data-driven commands and variables in the test case to use data from the data files.

### Add data files to the workspace

Katalon Recorder supports adding CSV and JSON data files to your workspace.

Follow these steps:

1. Open Katalon Recorder. In the **Workspace** sidebar, click on the *more* icon in the **Test Data** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Workspace-sidebar-Test-Data.png" width=30% alt="Click on Test Data More icon">

2. In the displayed file dialog, select the CSV or JSON file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-File-Dialog-Select-CSV.png" width=70% alt="Click on Test Data More icon">

3. The added data file is displayed under the **Test Data** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Test-Data-File-added.png" width=30% alt="Added data file">

### Configure data-driven commands and variables in the test case

In Katalon Recorder, the manual steps to configure data-driven commands and variables are as follows:

1. Add the `loadVars` command to the beginning of your test case.
2. Type in the name of the `loadVars` target file, e.g. `data.csv`.
3. In the test case, use variables with the same names as the columns in the data file.
4. Add the `endLoadVars` command to the end of your test case.

Katalon Recorder also provides a simple user interface to configure data-driven commands and variables.

Follow these steps to configure using the interface:

1. Select the data file. Click on the *more* icon next to the data file and select **Use this in a test case**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Use-Data-file-in-a-test-case.png" width=70% alt="Click on the more icon">

2. Select the test case. In the displayed menu, select the desired test case. Click **Next** to continue.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Use-Data-File-Select-Test-Case.png" width=70% alt="Select the Test Case">

3. Use the data from the data file. In the displayed test case, select the commands and specify the desired variables. Click **Add** when done.

    Katalon Recorder specifies a variable using the `${<variable_name>}` syntax as a placeholder in the **Value** field.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Select-Value-for-DDT.png" width=70% alt="Replace the value with a variable">

4. Verify that the value in the test case is replaced with the correct variable.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Test-Case-with-modified-value.png" width=70% alt="The value is replaced">

5. Play the test case and verify the results in the **Log** view. The log message should indicate that Katalon Recorder expands the specified variables into test data.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-DDT-Execution-results.png" width=70% alt="DDT execution results">

## Sample projects

Katalon Recorder comes with a set of built-in sample projects to get you started with DDT.

Follow these steps to add a sample project:

1. In the **Actions** sidebar, select **Sample Projects**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Action-sidebar-Sample-Projects.png" width=30% alt="Action sidebar">

2. In the displayed dialog, select **Fill a form with data from CSV file with Sample Test Data** sample project. Click **Add** to add the project.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Sample-Project-dialog.png" width=70% alt="Sample project dialog">
