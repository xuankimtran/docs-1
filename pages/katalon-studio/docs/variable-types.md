---
title: "Types of Variables"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/variable-types.html
redirect_from:
    - "/display/KD/Variable+Types/"
    - "/display/KD/Variable%20Types/"
    - "/x/RoIw/"
    - "/katalon-studio/docs/variable-types/"
description:
---
Katalon Studio supports three types of variables:

- Groovy Variable

- Test Case Variable

- Global Variable (Execution Profiles)

## Groovy Variables

> Katalon Studio supports Groovy programming language from version 2.4.x onwards.

Katalon Studio allows you to define variables in Groovy. 

For example:

```groovy
// x is defined as a variable of String type
String x = "Hello";
 
// y is defined as a variable of int type
int y = 5;

// The value of the variables are printed to the console
println(x);
println(y);
```
To learn more about Groovy programming language, you can refer to the Apache Groovy document: [Groovy documentation](http://groovy-lang.org/semantics.html). 

## Test Case Variables

Test Case Variables allow you to pass dynamic data into a test case.

You can create test case variables and call test cases with variables in the manual and script mode. 
To learn more about managing test case variables, you can refer to this document: [Test case variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html#manage-test-case-variables).

You can also use test case variables in a test suite. To learn more about binding data for test suite execution, you can refer to this document: [Manage data binding](https://docs.katalon.com/katalon-studio/docs/run-test-case-external-data.html).

## Global Variables

A global variable is a variable defined in the execution profile and can be used in a test case, test object, web service object, and email configuration in a project.
To learn more about global variables and execution profiles, you can refer to this document: [Global Variables and Execution Profile](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html#execution-profile).