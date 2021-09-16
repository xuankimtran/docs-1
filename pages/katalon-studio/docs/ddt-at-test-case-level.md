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

In this article, we demonstrate how to manage data binding at test case level and execute them in a test suite.

## Data-driven testing at test case level

Do as follows:
### Create Test Case 

  1. Create a new test case. Go to **File > New > Test Case**. A new test case opens.
  2. Switch to the the **Variables & Data** tab. There are two sections in this tab:

  - **Variables** section: Support defining variables populated in the **Variables Binding** table.
  - **Data Binding** section: Support adding predefined test data files and manage variable binding for your test case execution.
### Manage Test case variables 

### Manage data binding



  - **Test Data** table: Support specifying data files for your test execution.
  - **Variable Binding** table: Display all variables from the **Variables** section in the test case. See also [Test case Variables](https://docs.katalon.com/katalon-studio/docs/test-case-variables.html#view-and-declare-variables-in-script-mode).
<img src="url" width="70%" alt="Data binding section">


## Execute Test Suite with Associated Test Case

### Dynamic Test Suite


### Data-binding Test Suite

> **What is a Suite Test Case?**
>
> A Suite Test Case is a test case added to a test suite.


Katalon allows you to select Data Binding options between Test Case level and Suite Test Case level.
