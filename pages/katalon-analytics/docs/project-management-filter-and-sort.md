---
title: "Filter, Sort and Use Search to filter" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/project-management-filter-and-sort.html 
redirect_from:
    - "/display/KA/Filter+and+Sort/"
    - "/display/KA/Filter%20and%20Sort/"
    - "/x/ZgTR/"
    - "/katalon-analytics/docs/filter-and-sort/"
description: 
---

## Filtering

Filtering is a handy tool for users to see only their preferred data to be displayed in different types of data visualization in Katalon TestOps. By applying a filter, you can customize the demonstration of individual records in a graph or a table.

Currently, Executions, Test Cases and Test Suites come with a set of default filters you can apply.

1. On Katalon TestOps, navigate to the Execution tab.
2. Under the Executions, choose your preferred type of filter.

Default filters:

* Status: Passed/Failed.
* Started: within a month/ a month ago/ 2 months ago/ 3 months ago
* By: username

> **Notes:**
>
>* More than one filter can be applied.
>* In a graph, click on a value to directly remove it from the visual presentation. Another click is to clear the filter.
>* Licenses can be filtered only by a machine ID.

## Sorting

Filters and records in Executions, Test Cases and Test Suites tables can be sorted to provide better information.

1. On Katalon TestOps, navigate to the Executions tab or Test Design tab to access Test Cases/Test Suites.
2. In the upper-right corner, select the Sort drop-down menu.
3. Select your preferred sort among the default sorts.
4. Once a sort option is selected, the query is automatically filled in the input above. The following queries are currently supported:

**Executions**

* ID: `sort:order-asc` or `sort:order-desc`
* Started: `sort:startTime-asc` or `sort:startTime-desc`
* Duration: `sort:duration-asc` or `sort:duration-desc`

**Test Case and Test Suite**

* Name: `sort:name-asc` or `sort:name-desc`
* Flakiness: `sort:flakiness-asc` or `sort:flakiness-desc`

> Where: `asc` denotes ascending; `desc` descending.

## Using Search to filter

Every Executions, Test Cases, and Test Suites tab comes with a search bar for advanced filter management. The search bar allows you to define your custom filter and sort by some criteria.

### Advanced filters by search query for Executions

You can apply these filters with below syntax to match your expected results.

* Search by Test Suite Name
  * `TestSuite.name:|[keyword]`
  * Example: `TestSuite.name:|regression` matches executions of a Test Suite or Test Suite Collection with their names containing `regression`.

* Search by Status:
  * `status:Passed`
  * `status:Failed`

* Search by Start date:

  To match executions started before or after a day or within a period, you can construct a query as below:
  * After `startTime:>mm/dd/yyyy`
  * Before `startTime:<mm/dd/yyyy`
  * Within `startTime:<mm/dd/yyyy,>mm/dd/yyyy`

* Search by user ID:

  Test executions uploaded to TestOps by a specific person.
  * `User.id:[userID]`

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/filter-and-sort/searchbar.png"  width="1144" height="314">

### Query a Test Case or a Test Suite

`ExecutionStatistics.` should be added in front of the search queries for Executions to form search queries for a Test Case or Test Suite. Here are some examples:

* To query test cases with failed status: `ExecutionStatistics.status:FAILED`.
* To query test cases executed after August 23, 2019: `ExecutionStatistics.startTime:>08/23/2019`.
* To query test cases executed after August 23, 2019 and having failed: `ExecutionStatistics.startTime:>08/23/2019 ExecutionStatistics.status:PASSED`.
