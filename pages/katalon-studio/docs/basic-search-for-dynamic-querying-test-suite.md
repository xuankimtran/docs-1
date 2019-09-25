---
title: "Basic Search For Dynamic Test Suite" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/basic-search-for-dynamic-querying-test-suite.html

description: 
---

[Dynamic Test Suite](https://docs.katalon.com/katalon-studio/docs/dynamic-querying-test-suite.html) allows you to define the query search and manage query plugins from Katalon Store. [Basic Search For Dynamic Test Suite](https://store.katalon.com/product/2/Basic-Search-For-Dynamic-Test-Suite) is one of them. This plugin enables the basic search capability to look for test cases faster in Katalon Studio and help filter which test cases to be executed.

1. Create a new dynamic test suite by a right-click on **Test Suite > New > Dynamic Test Suite**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/basic-search-for-dynamic-querying-test-suite/create-ts.png" width="643" height="331">

2. Add test cases to the dynamic test suite NOT in a manual way but via [search query](https://docs.katalon.com/katalon-studio/docs/advanced-search.html). Enter the search condition, click **Preview** to query out the matching test cases and the total number of results.

    For example, to add the test cases in the “Custom-keyword samples" folder to this dynamic test suite, you can use this search query: `id=(Test Cases/Simple Examples/Katalon Shop/Custom-keyword samples)`.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/basic-search-for-dynamic-querying-test-suite/result.png" width="1029" height="376">

    Test cases that match the search conditions are chosen when the test suites are executed (unlike in built-in test suites, test cases are chosen at planning time).
