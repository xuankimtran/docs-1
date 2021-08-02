---
title: "TestOps Directory"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/testops-terminology.html
redirect_from:
---

## TestOps Terminology

**<details><summary>Agent</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>API performance anomalies</summary>**
Identify web services that take more/less time to respond than usual by applying the local outlier factor (LOF) on 30 latest execution requests.
</details>

**<details><summary>Assertions</summary>**
Determine whether the automated test case succeeds or not.

Katalon TestOps provides users a specific view of assertions in each test case to evaluate the quality of test cases and ensure your tested application/software is working correctly.

Assertions help checking whether a condition is true (e.g., whether labels, data, API responses are rendered correctly).
</details>

**<details><summary>BDD Test Result</summary>**
Represents the result of a test following the Behavior Driven Development (BDD) Framework.

In Katalon TestOps, the Features of BDD tests are displayed as Requirements, while Scenarios are displayed as Test Cases.
</details>

**<details><summary>Build</summary>**
Represents a group of features/tasks in a release for management or testing purposes.

In Katalon TestOps, a build can consist of one or more test cases.
When users map a test result to a build, it’s automatically mapped to the corresponding release. However, if users map a test result to a release, it’s not mapped to any specific build.
</details>

**<details><summary>Build Label</summary>**
Represents a piece of code committed to the source code
</details>

**<details><summary>Defect</summary>**
Identifies a failed test run on TestOps to link the test result to a Jira issue (Jira bug).
</details>

**<details><summary>Interval (Trigger)</summary>**
A time period between each scheduled execution.

In Katalon TestOps, the Interval Unit values are Minute, Hour, Day, Week. For example, if you set Interval Unit as Hour, Interval as 5, it means the execution is scheduled for every 5 hours.
</details>

**<details><summary>Key (Jira)</summary>**
Represents an ID of the Jira issue you have linked a test case/test result to.

In Katalon TestOps, you link a test case to Jira Requirements and link a test result to a Jira Defect.
</details>

**<details><summary>Last Ping (Agent)</summary>**
The last time an Agent connects to a server to ask for a job to execute.
</details>

**<details><summary>Maintainer</summary>**
A role responsible for all test results of a test case.

In Katalon TestOps, within an organization, you can assign a person to maintain a test case. The maintainer is then in charge of all history results of a test case.
</details>

**<details><summary>Organization</summary>**
Brings together users, teams and projects in your company.

In Katalon TestOps, the organization level is the highest level of management, followed by the team level and then project level.
</details>

**<details><summary>Path</summary>**
Location of a test in Katalon Studio.

In Katalon TestOps, each test has a path if it is uploaded from Katalon Studio to Katalon TestOps.
</details>

**<details><summary>Profile</summary>**
A profile is set for each test suite in Katalon Studio. Hence, a test run can have multiple profiles in Katalon TestOps. This helps cover multiple and different environments to execute automated test scripts with ease.
</details>

**<details><summary>Properties (Visual Testing)</summary>**
Represents an ID of the baseline image.
</details>

**<details><summary>Release</summary>**
Represents a version or a milestone of a software product.

In Katalon TestOps, a release consists of one or more test cases.
</details>

**<details><summary>Request (API testing)</summary>**
Represents the action of calling a server and asking it to perform a task.
</details>

**<details><summary>Requirement (Jira)</summary>**
Represents a Jira issue linked to a test case
</details>

**<details><summary>Script Repository</summary>**
Stores all the test assets for a test automation project (tests, data files, scripts files, macros, etc.)

In Katalon TestOps, you can create a script repository to manage all test scripts and decide which one to be executed along with the given test environment. You can upload files to a script repository from an external source or as a .zip file.
</details>

**<details><summary>Session</summary>**
A session is created once a test run is executed.

In Katalon TestOps, each test run can be executed as one or many test sessions depending on whether the test runs in parallel or not.

A session can contain:
* one or more test cases
* a test environment
* test scripts (in a script repository) used for the execution of each test case.
</details>

**<details><summary>Test Case</summary>**
Consists of multiple test results once being executed. 

In Katalon TestOps, you can see detailed information of test cases to see if your software is free of bugs and whether it is working as expected. You can link test cases to Jira Requirements to ensure a good test coverage. A test case can be linked to one or more Requirements.  
</details>

**<details><summary>Test Environment</summary>**
Represents a place where a test run could be executed in command line interface.

In Katalon TestOps, you can use your local machine as a test environment. This test environment must be controlled by an agent.
</details>

**<details><summary>Test Execution</summary>**
The results of test cases executed with TestOps scheduler.

> Notes:
>
> Not including reports uploaded from Katalon Studio or other tools.
</details>

**<details><summary>Test Run</summary>**
Consists of one or more test cases to be executed (execution of more test cases depends on whether a test run is conducted in parallel).

In Katalon TestOps, a test run keeps track of all test results, status, duration, asignee, etc.
</details>

**<details><summary>Test Run Type</summary>**
A collection of all test runs that have same configurations.
</details>

**<details><summary>Test Suite</summary>**
A collection of test cases.
</details>

**<details><summary>Test Suite Collection</summary>**
A list of test suites that allows users to manage and plan tes executions better.
</details>

**<details><summary>Threshold (Agent)</summary>**
The maximum number of sessions that an agent can execute at the same time.
</details>

**<details><summary>Total Assigned Sessions (Agent)</summary>**
Number of sessions assigned to an agent to execute tests.

In Katalon TestOps, the maximum number of assigned sessions is called Threshold.
</details>

**<details><summary>Total Executing Sessions (Agent)</summary>**
Number of sessions an agent executes in real time.
</details>

**<details><summary>Traceability Matrix</summary>**
Manages the relationships across requirements, test cases and defects.
</details>

**<details><summary>Trigger</summary>**
Determines when a test run is executed.

In Katalon TestOps, this function helps leverage remote execution for a complete control of testing plan.
</details>

**<details><summary>User Management</summary>**
An administration tool to manage users.

In Katalon TestOps, this feature allows you to:
* invite users to your organization (you can also set up access permission to other Katalon products).
* delete pending invitations.
* set and edit a user's role.
* remove users from your organization.
</details>

**<details><summary>UUID (Agent)</summary>**
A identifier generated when an agent is set up successfully..
</details>

**<details><summary>Visual Baseline (Visual Testing)</summary>**
A standard reference image used to compare with the Checkpoint screenshot(s) during a test execution.
</details>

## TestOps Calculations

**<details><summary>% change (Test Case in Dashboard)</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>% change (Test Result in Dashboard)</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>% pass/fail (Build)</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>Active/Archived Release</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>Active Test Case</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>Average Duration (Test Case)</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>Average Duration (Web Services)</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>Development Progress (Dashboard)</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>Duration (Session)</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>Duration (Test Result)</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>Duration (Test Run)</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>Execution Time (Dashboard)</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>Flakiness (%)</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>Flaky Test Case</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

**<details><summary>Max/Min Duration (Web Services)</summary>**
Connects a local machine to the TestOps servers for test runs execution.
</details>

