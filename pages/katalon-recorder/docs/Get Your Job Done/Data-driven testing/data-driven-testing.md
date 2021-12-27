---
title: "Data-driven testing in Katalon Recorder"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-recorder/docs/data-driven-testing.html
redirect_from: katalon-recorder/docs/data-driven-execution.html
description:
---

Data-driven testing (DDT) allows you to execute test cases using data from external data files in table or spreadsheet format. Katalon Recorder facilitates DDT by providing DDT commands and enabling you to bind test cases with data files.

> **Requirements**:
>
> Katalon Recorder version 5.6.0 onwards.

This article introduces you to the DDT commands and data file formats supported by Katalon Recorder.

## Data-driven commands

Katalon Recorder provides two commands for DDT: `loadVars` and `endLoadVars`.

### loadVars

The `loadVars` command starts a loop to repeatedly load the values from the data file specified in the **Target** field.

### endLoadVars

The `endLoadVars` command terminates the data-driven block. You need to add it to your test; otherwise, you will get an error message.

### Data-driven testing process

When you execute a test containing `loadVars` and `endLoadVars` commands, the following process will take place, with *i* starting with 1 and ending with the number of rows in the data file:

1. The *ith* row of the data file will be fetched.
2. The values of the row will be mapped to the variables used in the test case.
3. The steps between `loadVars` and `endLoadVars` will be executed using these mapped values.

## Data file formats

Katalon Recorder supports two data file formats: CSV and JSON.

### Data files in CSV format

While performing DDT with a CSV data file, Katalon Recorder navigates the file using the column names, and extracts data from the file, row by row. Therefore, you need to create a CSV file with specific column names.

Katalon Recorder treats CSV column names as case-sensitive.

For example, a data-driven test that fills in a form with dates and comments might have a CSV data file as follows:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Sample-CSV-file.png" width=70% alt="Sample CSV file for Katalon Recorder">

### Data files in JSON format

Katalon Recorder uses JSON data files with specific syntax. Test data in a JSON file must be organized in an array. Each element (data row) in the array is represented as an object with *name/value* pairs; the name specifies the column name, and the value specifies the value in the respective row.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-DDT-Sample-JSON-syntax.png" width=70% alt="Sample JSON syntax">

For example, a JSON data file with two columns, dates and comments, might be written as follows:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Sample-JSON-file.png" width=70% alt="Sample JSON file for Katalon Recorder">

## Sample projects

Katalon Recorder comes with a set of built-in sample projects to get you started with DDT.

Follow these steps to add a sample project:

1. In the **Actions** sidebar, select **Sample Projects**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Action-sidebar-Sample-Projects.png" width=30% alt="Action sidebar">

2. In the displayed dialog, select the **Fill a form with data from CSV file with Sample Test Data** sample project. Click **Add** to add the project.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Sample-Project-dialog.png" width=70% alt="Sample project dialog">

**See also**:
* The Katalon Academy course: [Data-Driven Testing with Katalon Recorder](https://academy.katalon.com/courses/katalon-recorder-data-driven-testing/).