---
title: "TestOps Integration" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/testops-integration.html
redirect_from:
    - "/katalon-studio/docs/execute_tests_periodically_on_remote_machines.html"
    - "/katalon-studio/docs/view-execution-list.html"
---

## Overview

Katalon TestOps is an enterprise-class platform for QA orchestration, test analytics, and advanced reports.

With Katalon TestOps, you can coordinate various activities, cycles, and frameworks in software testing. By doing so, you can ensure software quality at every stage without the need to sacrifice speed or require DevOps expertise.

For information on the key modules TestOps offers, see: [TestOps Overview](https://docs.katalon.com/katalon-analytics/docs/overview.html#test-planning).

## TestOps integration

You can enable TestOps integration in Katalon Studio to upload test results to Katalon TestOps for test management and reports. See: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html#upload-test-results-automatically).

## Remote execution with TestOps

You can execute tests periodically on remote machines by setting up agents in Katalon TestOps. See: [Create a Local Test Environment with an Agent](https://docs.katalon.com/katalon-analytics/docs/agents.html).

Katalon TestOps allows you to:

* Retrieve the latest version of your Katalon Studio projects stored in Katalon TestOps or Git. See: [Upload Test Scripts from a Git Repository](https://docs.katalon.com/katalon-analytics/docs/git-test-project.html).

* Install and manage multiple versions of Katalon Runtime Engine on your test machines without the need to do so manually. See: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html#schedule-test-runs).

* Execute tests and submit the test results to Katalon TestOps for review. See: [Execute Test Runs manually](https://docs.katalon.com/katalon-analytics/docs/kt-scheduler.html).

* Keep the number of concurrent executions under a configurable limit. See: [Configure an Agent's Threshold](https://docs.katalon.com/katalon-analytics/docs/load-balancing-agents.html#configure-an-agents-threshold).

    Katalon TestOps distributes jobs among active Agents to balance workload. This feature is useful especially if you only have a limited number of licenses and want to queue your executions periodically. See: [Auto-Distributed Executions](https://docs.katalon.com/katalon-analytics/docs/auto-distributed-execution.html#how-it-works).

## View execution summary in Katalon Studio

> Requirements:
>
> * Katalon Studio version 7.6.2 onwards.
> * You have enabled TestOps integration in Katalon Studio.
> * You have executed at least one test suite in Katalon Studio.

Follow these steps:

1. Open Katalon Studio.

2. On the **Tests Explorer** sidebar, go to **TestOps** > **Executions**.

    You can view a summary of your test executions here.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/view-execution-list/execution-list.png" width=100% alt="execution list">

    > Notes:
    >
    > You can click on the *Reload* icon (next to **View all executions** in the top right corner) to view the latest updates.

### View advanced reports in Katalon TestOps

For advanced reports and insights into your testing data, sign in to [Katalon TestOps](https://testops.katalon.io/login) with your Katalon account.