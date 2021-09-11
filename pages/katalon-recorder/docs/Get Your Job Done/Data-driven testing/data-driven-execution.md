---
title: "Data-driven execution"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/data-driven-execution.html
description:
---

Data-driven execution allows you to execute your test with multiple data set.

## Perform data-driven testing
There are two steps to perform data-driven execution:
1. Add data files to workspace.
2. Add data-driven commands.
3. Modify your test to use the data.

### Add data files to workspace
Katalon Recorder supports CSV and JSON data files. They can be added to your workspace.
1. Click on the add icon next to **Test Data** in the **Workspace** left-side bar.
2. Select CSV or a JSON files.

You should see your data files are added to your workspace under **Test Data**.

### Add data-driven commands
Refer to [Data-driven commands](#data-driven-commands) for more information.
1. Add a `loadVars` command to the beginning of your test.
2. Type in the name of the data file in your workspace (for example, `data.csv`) to the target of the `loadVars` command.
3. Add a `endLoadVars` command to the end of your test.

### Modify your test to use the data

Modify the Value field of the test steps to use variables. 

For example, if you CSV file contains a column named `firstName` that contains a row of values, then modify a test step `type | id=first-name | Thomas` to `type | id=first-name | ${firstName}` will make it use the data from the CSV file.

## Data-driven commands
### loadVars

The `loadVars` command loads the values from the data file specified in its Target. 

When you execute a test containing `loadVars` and `endLoadVars` commands, the following process will take place, with i start with 1 and ends with the number of rows in the data file:
1. The ith row of the data file will be fetched.
2. The values of the row will be mapped to the variables used in the test case.
3. The steps between `loadVars` and `endLoadVars` will be executed using these mapped values.

### endLoadVars

The `endLoadVars` command terminates the data-driven block. You need to add it to your test, otherwise you will get an error message.

## Sample projects
Katalon Recorder comes with a set of built-in sample projects to get you started with data-driven executions.
1. Go to **Templates**.
2. Go to **Read and write value with CSV file**
3. Add **Fill a form with data from CSV file** sample project.