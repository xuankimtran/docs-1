---
title: "Load Balancing for Local Test Environments"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/load-balancing-agents.html
---

With **TestOps CI**, you can execute your test plans parallelly in load-balanced local test environments.

## Prerequisites:
- You have at least one active local test environment. Learn how to start a local test environment [here](https://docs.katalon.com/katalon-analytics/docs/agents.html).

## Configure a threshold

The threshold is the maximum number of jobs that a local test environment can execute concurrently. You need to configure the threshold value to assign one local test environment to multiple test plans.

> Note: Thresholds are set as 1 by default for all local test environments.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/load-balancing-agents/1-view-agent-threshold.png" width="" height="">


1. To configure the threshold, go to a local test environment detailed page, update the value of the threshold 
2. Click on **Update**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/load-balancing-agents/2-update-agent-threshold.png" width="" height="">


After updating the threshold value, you can assign your local test environment to execute test plans. The maximum number of parallel sessions that the local test environment can execute is equal to the threshold value you have configured.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/load-balancing-agents/3-new-agent-threshold.png" width="" height="">

## Assign local test environments to execute test runs

To assign a local test environment to a test plan, select a plan and click on **Edit**.

Go to your test plan details page. 

In the **Test Environments** section, select the local test environment you want to assign and click on **Save**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/load-balancing-agents/assign-agent.png" width="" height="">

> If you want to assign multiple test plans to the same local test environment, repeat the above steps with other test plans.
> 
> *Note: You can assign multiple local test environments to execute each test plan. If so, the most possible and active local test environment will be chosen to run the job.*


After finishing the above steps, you can [run](https://docs.katalon.com/katalon-analytics/docs/create-plan.html#run-a-test-plan) or [schedule your test plans](https://docs.katalon.com/katalon-analytics/docs/kt-scheduler.html) in the load-balanced local test environment.

Check your executing jobs in **Test Environments** page as below.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/load-balancing-agents/after-assign-agent.png" width="" height="">
