---
title: "Auto-Distributed Executions" 
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-analytics/docs/auto-distributed-execution.html
redirect from:
description:
---
 
 
## How it works

>Requirements:
>
>Katalon Studio version 8.0 onwards
>Katalon Runtime Engine
>Agent version 1.7.0 onwards
>At least 2 active Agents

In Katalon TestOps, you can execute tests in parallel. During parallel execution, test runs are automatically load-balanced. This means that each time a test run starts, the test run is distributed to an available and active local test environment, minimizing execution time.

When a test run is executed, the test sessions will be assigned to the previously configured Agents in this order of priority:

-Idle Agents
-Agents that have not exceeded their Threshold
-Agents with the least number of queued test runs

When an Agent completes a test run session, queued jobs that were first assigned to other Agents can be automatically reassigned to this Agent for immediate execution.

## Configure Auto-Distributed Executions

1. To enable Auto-Distributed Executions, make sure that you have at least 2 active Agents. You can learn how to set-up Agents here: [Create a Local Test Environment](https://docs.katalon.com/katalon-analytics/docs/Agents.html).

2. Make sure that your Test Suite Collection is configured for parallel execution. If not, you can follow these steps: [Run multiple Test Suites in Parallel](https://docs.katalon.com/katalon-analytics/docs/kt_run_parallel_Agent.html#set-up-Agents).

3. Create a Test Schedule and assign your Test Run types to those Agents. Learn more: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html#schedule-test-runs).

>Notes:
>
>When configuring multiple Test Run types, Test Run types must share a minimum of 1 mutual Agent for distributed execution. In other words, assign Test Run types to multiple, overlapping Agents.

4. Activate your Agents before the scheduled Test Run time.

5. When the Test Once the Test Run types execute, the test sessions of these Test Run types are assigned to the previously configured agents automatically.
