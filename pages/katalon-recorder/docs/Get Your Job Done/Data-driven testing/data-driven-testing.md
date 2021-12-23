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

This article introduces you to DDT commands in Katalon Recorder and shows you how to implement DDT in a test case.

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

## Data file formats

Katalon Recorder supports two data file formats: CSV and JSON.

### Data files in CSV format

Katalon Recorder navigates using column names in a CSV file, so you need to create a CSV file with specific column names.

For example, a data-driven test that fills in a form with dates and comments might be written as follows:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Sample-CSV-file.png" width=70% alt="Sample CSV file for Katalon Recorder">

### Data files in JSON format

Katalon Recorder uses JSON data files with specific syntax.

For example, a JSON data file with two data types, dates and comments, might be written as follows:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Sample-JSON-file.png" width=70% alt="Sample JSON file for Katalon Recorder">

Test data in a JSON file must be organized in an array and enclosed in square brackets. Each row is represented as an object with *name/value* pairs; the name specifies the column name, and the value specifies the value in the respective row.

## Sample projects

Katalon Recorder comes with a set of built-in sample projects to get you started with DDT.

Follow these steps to add a sample project:

1. In the **Actions** sidebar, select **Sample Projects**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Action-sidebar-Sample-Projects.png" width=30% alt="Action sidebar">

2. In the displayed dialog, select the **Fill a form with data from CSV file with Sample Test Data** sample project. Click **Add** to add the project.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-recorder/docs/ddt-guide/KR-Sample-Project-dialog.png" width=70% alt="Sample project dialog">
