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
>* Katalon Studio version 8.0 onwards
>* Katalon Runtime Engine
>* Agent version 1.7.0 onwards
>* At least 2 active Agents

In Katalon TestOps, you can execute tests in parallel. During parallel execution, Test Runs are automatically load-balanced. This means that each time a Test Run starts, the Test Run is distributed to an available and active local test environment, minimizing execution time.

When a Test Run is executed, the test sessions will be assigned to the previously configured Agents in this order of priority:

- Idle Agents
- Agents that have not exceeded their Threshold
- Agents with the least number of queued Test Runs

When an Agent completes a Test Run session, queued jobs that were first assigned to other Agents can be automatically reassigned to this Agent for immediate execution.

## Configure Auto-Distributed Executions

1. To enable Auto-Distributed Executions, make sure that you have at least 2 active Agents. You can learn how to set-up Agents here: [Create a Local Test Environment](https://docs.katalon.com/katalon-analytics/docs/agents.html).

2. Make sure that your Test Suite Collection is configured for parallel execution. If not, you can follow these steps: [Run multiple Test Suites in Parallel](https://docs.katalon.com/katalon-analytics/docs/kt_run_parallel_agent.html#set-up-agents).

3. Create a Test Schedule and assign your Test Run Types to those Agents. Learn more: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html#schedule-test-runs).

>Notes:
>
>When configuring multiple Test Run Types, Test Run Types must share a minimum of 1 mutual Agent for distributed execution. In other words, assign Test Run Types to multiple, overlapping Agents.

4. Activate your Agents before the scheduled Test Run time.

5. Once the Test Run Types execute, the test sessions of these Test Run Types are assigned to the previously configured agents automatically.
