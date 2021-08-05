---
title: "TestOps Directory"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/testops-terminology.html
redirect_from:
---

## TestOps Terminology

**<details><summary>Agent</summary>**
Connects a local machine to the TestOps servers for test executions.
</details>

**<details><summary>API performance anomalies</summary>**
Identify web services that take more/less time to respond than usual by applying the local outlier factor (LOF) on 30 latest execution requests.
</details>

**<details><summary>Assertions</summary>**
Determine whether the automated test case succeeds or not.

Katalon TestOps provides you with a specific view of assertions in each test case to evaluate the quality of test cases and ensure your tested application/software is working correctly.

Assertions help to check whether a condition is true (e.g., whether labels, data, API responses are rendered correctly).
</details>

**<details><summary>BDD Test Result</summary>**
Represents the result of a test following the Behavior Driven Development (BDD) Framework.

In Katalon TestOps, the Features of BDD tests are displayed as Requirements, while Scenarios are displayed as Test Cases.
</details>

**<details><summary>Build</summary>**
Represents a group of features/tasks in a release, used for management or testing purposes.

In Katalon TestOps, a build can consist of one or more test cases.

When users map a test result to a build, the test result is automatically mapped to the corresponding release. However, if users map a test result to a release, the test result is not mapped to any specific build.
</details>

**<details><summary>Build Label</summary>**
Represents a piece of code committed to the source code
</details>

**<details><summary>Defect</summary>**
Identifies a failed test run to link the test result to a Jira issue (Jira bug).
</details>

**<details><summary>Interval (Trigger)</summary>**
A time period between each scheduled execution.

In Katalon TestOps, the Interval Unit values are Minute, Hour, Day, Week. For example, if you set Interval Unit as Hour, Interval as 5, it means the execution is scheduled for every 5 hours.
</details>

**<details><summary>Key (Jira)</summary>**
Represents the ID of a Jira issue you have linked a test case/test result to.

In Katalon TestOps, you link a test case to Jira Requirements and link a test result (if the test run fails) to a Jira Defect.
</details>

**<details><summary>Last Ping (Agent)</summary>**
The last time an Agent connects to a server to ask for a job to execute.
</details>

**<details><summary>Maintainer</summary>**
A role that is responsible for all test results of a test case.

In Katalon TestOps, within an organization, you can assign a person to maintain a test case and the history of its test results.
</details>

**<details><summary>Organization</summary>**
Created to brings together all users, teams, and projects of a company.

In Katalon TestOps, the organization level is the highest level of management, followed by the team level and the project level.
</details>

**<details><summary>Path</summary>**
The location of a test in Katalon Studio.

In Katalon TestOps, each test case has a path if it is uploaded from Katalon Studio.
</details>

**<details><summary>Profile</summary>**
An execution profile that is created in Katalon Studio (KS). 

In Katalon TestOps, the KS's execution profiles are displayed as Profiles. A test run can have multiple profiles. This helps cover multiple and different environments to execute automated test scripts with ease.
</details>

**<details><summary>Properties (Visual Testing)</summary>**
Represents the ID of a baseline image.
</details>

**<details><summary>Release</summary>**
Represents a version or a milestone of your tested software.

In Katalon TestOps, a release consists of one or more test cases.
</details>

**<details><summary>Request (API testing)</summary>**
Represents the action of calling a server and asking it to perform a task.
</details>

**<details><summary>Requirement (Jira)</summary>**
Represents the Jira issue that is linked to a test case.
</details>

**<details><summary>Script Repository</summary>**
Stores all the test assets for a test automation project (tests, data files, scripts files, macros, etc.)

In Katalon TestOps, you can create a script repository to manage all test scripts and decide which one to be executed along with the given test environment. You can upload files to a script repository from an external source or as a .zip file.
</details>

**<details><summary>Session</summary>**
A session that is created once a test run is executed.

In Katalon TestOps, each test run can be executed as one or many test sessions depending on whether the tests run in parallel or not.

A session can contain:
* one or more test cases
* a test environment
* test scripts (in a script repository) used for the execution of each test case.
</details>

**<details><summary>Test Case</summary>**
Consists of multiple test results once a test is executed.

In Katalon TestOps, you can see detailed information of test cases to see if your software is free of bugs and whether it is working as expected. You can link test cases to Jira Requirements to ensure good test coverage. A test case can be linked to one or more Requirements.
</details>

**<details><summary>Test Environment</summary>**
A place where a test run could be executed with the command line interface.

In Katalon TestOps, you can use your local machine as a test environment. This test environment must be controlled by an agent.
</details>

**<details><summary>Test Execution</summary>**
The results of test cases executed by TestOps scheduler.

> Notes:
>
> Not including reports uploaded from Katalon Studio or other tools.
</details>

**<details><summary>Test Run</summary>**
Consists of one or more test cases to be executed (execution of more test cases depends on whether a test run is conducted in parallel).

In Katalon TestOps, a test run keeps track of all test results, status, duration, assignee, etc.
</details>

**<details><summary>Test Run Type</summary>**
A collection of all test runs that have the same configurations.
</details>

**<details><summary>Test Suite</summary>**
A collection of test cases.
</details>

**<details><summary>Test Suite Collection</summary>**
A list of test suites that allows users to manage and plan test executions better.
</details>

**<details><summary>Threshold (Agent)</summary>**
The maximum number of sessions that an agent can execute at the same time.
</details>

**<details><summary>Total Assigned Sessions (Agent)</summary>**
The total number of sessions assigned to an agent to execute tests.

In Katalon TestOps, the maximum number of assigned sessions is also called Threshold.
</details>

**<details><summary>Total Executing Sessions (Agent)</summary>**
The number of sessions an agent executes in real time.
</details>

**<details><summary>Traceability Matrix</summary>**
Manages the relationships across requirements, test cases and defects.
</details>

**<details><summary>Trigger</summary>**
Determines when a test run is executed.

In Katalon TestOps, this function helps leverage remote execution for complete control of the testing plan.
</details>

**<details><summary>User Management</summary>**
An administration tool to manage users.

In Katalon TestOps, this feature allows you to:
* invite users to your organization (you can also set up permission access for other Katalon products).
* delete pending invitations.
* set and edit a user's role.
* remove users from your organization.
</details>

**<details><summary>UUID (Agent)</summary>**
An identifier that is generated when an agent is set up successfully.
</details>

**<details><summary>Visual Baseline (Visual Testing)</summary>**
A standard reference image used to compare with the Checkpoint screenshot(s) during a test execution.
</details>

## TestOps Calculations

**<details><summary>% change of Test Case (Dashboard)</summary>**
$$
\frac{Total-test-cases-this-week}{Total-test-cases-last-week} * 100
$$
</details>

**<details><summary>% change of Test Result (Dashboard)</summary>**
$$
\frac{Total-test-results-this-week}{Total-test-results-last-week} * 100
$$
</details>

**<details><summary>% fail (Build)</summary>**
$$
\frac{Total-failed-test-cases}{Total-test-cases} * 100
$$
</details>

**<details><summary>% flakiness</summary>**
$$
\frac{Number-of-times-the-status-of-test-results-changes}{Total-number-of-test-results} * 100
$$

> Notes:
>
> Total number of test results =  30 latest test results (ordered by the start time of execution).
</details>

**<details><summary>% pass (Build)</summary>**
$$
\frac{Total-passed-test-cases}{Total-test-cases} * 100
$$
</details>

**<details><summary>Active/Archived Release</summary>**
A new release is active by default. You can track it when it's active.

In Katalon TestOps, you can also archive a release to stop tracking it.
</details>

**<details><summary>Active Test Case</summary>**
A test case that has been run last 2 months (based on the start time of execution).
</details>

**<details><summary>Average Duration (Test Case)</summary>**
$$
\frac{Total-duration-of-all-test-results}{Total-number-of-test-results} * 100
$$

> Notes:
>
> The calculation is based on the last 100 test results.
</details>

**<details><summary>Average Duration (Web Services)</summary>**
The average amount based on the last 30 execution requests (ordered by the start time of execution).
</details>

**<details><summary>Development Progress (Dashboard)</summary>**
$$
\frac{Resolved-Jira-issues}{Total-Jira-issues} * 100
$$
</details>

**<details><summary>Duration (Session)</summary>**
= (End time - Start time)

> Notes:
>
> Start time is when an agent starts receiving a job.
>
> End time is when uploading reports to TestOps is done.
</details>

**<details><summary>Duration (Test Result)</summary>**
= (End time - Start time)
</details>

**<details><summary>Duration (Test Run)</summary>**
= (End time - Start time)

> Notes:
>
> This shows the actual time of running tests, including test runs via Scheduler and Upload Reports.
</details>

**<details><summary>Execution Time (Dashboard)</summary>**
The total duration of test results.
</details>

**<details><summary>Flaky Test Case</summary>**
Represents test cases that fail to produce the same results each time the same analytics is run.
</details>

**<details><summary>Max/Min Duration (Web Services)</summary>**
The max/min duration that is based on the last 30 execution requests.
</details>

**<details><summary>Offline Agent</summary>**
An agent is offline when the time of last Ping is longer than the active time

> Notes:
>
> By default, the active time is 5 minutes.
</details>

**<details><summary>Platform Coverage (Test Case)</summary>**
Shows the quality of test cases by operating system (OS) and browser-basis.

The color of the dot indicates that the test has passed or failed.
* Red dot = failed test
* Green dot = passed test

The size of the dot represents the number of tests (e.g., the bigger the dot is, the more tests are).
</details>

**<details><summary>Run Frequency (Test Run)</summary>**
A statistic of the scheduled test runs in a day.

The color of the dot indicates that the test has passed or failed.

The size of the dot represents the number of test results.
</details>

**<details><summary>Similar Failures</summary>**
The test runs that have at least 70% of error similarities.
</details>

**<details><summary>Slowest Test Case</summary>**
A test case that has the longest average duration.

Katalon TestOps ranks active test cases by their average duration. The shorter an average duration is, the more active/faster a test execution is.
</details>

**<details><summary>Stale Test Case</summary>**
A test case whose last test run is already 2 months ago.

Katalon TestOps calculates the 2-month period based on the time you first click to view a test report in real time.
</details>

**<details><summary>Status (Release)</summary>**
The status of a release, including:
* *Ready*: all test cases have passed.
* *Not Ready*: at least one test case has failed.
* *Empty*: there's no test case linked to the release.
</details>

**<details><summary>Status (Session)</summary>**
The status of a session, including:
* *Queued*: session has been created, waiting to be executed. 
* *Running*: session is in progress.
* *Failed*: session has failed (the exit code is different from 0).
* *Success*: session has succeeded (the exit code is 0).
* *Canceled*: session is canceled manually or session timeout.
</details>

**<details><summary>Status (Test Case)</summary>**
The status of a test case, including:
* *Passed*: all test results have passed.
* *Failed*: one of the test results has not passed.

> Notes:
>
> The status of a test case is defined by its latest execution.
</details>

**<details><summary>Status (Test Result)</summary>**
The status of a test result, including:
* *Passed*: test case runs successfully.
* *Failed*: test case runs unsuccessfully.
* *Error*: an error occurs during the execution.
* *Incomplete*: (defined by KS).
</details>

**<details><summary>Status (Test Run)</summary>**
The status of a test run, including:
* *Passed*: all test results have passed.
* *Failed*: one of the test results has failed.
</details>

**<details><summary>Status (Test Suite)</summary>**
The status of a test suite, including:
* *Passed*: all test cases have passed.
* *Failed*: one of the test cases has failed.
</details>

**<details><summary>Status (Visual Checkpoint)</summary>**
The status of a visual checkpoint, including:
* *Pass*: checkpoint image has matched the baseline, or it's manually marked as *Pass*.
* *Fail*: checkpoint image is marked manually as *Fail*.
* *Unresolved*: checkpoint image has mismatched the baseline. You can compare with the baseline image, then mark it as *Pass* or *Fail*.
</details>

**<details><summary>Status (Visual Test Run)</summary>**
The status of a visual test run, including:
* *Pass*: all new checkpoint images match the baseline image.
* *Fail*: one or more checkpoints has failed but no unresolved checkpoints.
* *Unresolved*: one or more checkpoints is unresolved.
</details>

**<details><summary>Test Progress (Dashboard)</summary>**
$$
\frac{Total-passed-test-results-in-release}{Total-test-results-in-release} * 100
$$
</details>

**<details><summary>Test Run Coverage</summary>**
The quality of each requirement based on the status of the corresponding test result.
</details>

**<details><summary>Time (Test Suite)</summary>**
The duration of the last run of a test suite. Also, the start time of the last run of a test suite.
</details>

**<details><summary>Time (Visual Test Run)</summary>**
= (End time - Start time of a visual test run)
</details>

**<details><summary>Total Duration in Summary (Test Results)</summary>**
A sum of all test result durations in a day.
</details>

**<details><summary>Total Duration (Release)</summary>**
The total duration of all test runs in a release.
</details>
