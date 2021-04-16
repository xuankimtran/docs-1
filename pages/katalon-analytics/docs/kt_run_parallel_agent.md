---
title: "Run multiple Test Suites in parallel with Agents" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt_run_parallel_agent.html 
description: 
---

On Katalons TestOps, we can run multiple Test Suites in parallel with Agents.

## Set up Agents

At first, we have to set up some Agents. For setting up an Agent, we can read [here](https://docs.katalon.com/katalon-analytics/docs/install_kt_agent.html).

We start two agents for preparing run Test Suites.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_start_two_agent.png)

For the illustrated example, on Katalon TestOps, we set up two agents.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_set_up_multi_agents.png)

We click on an agent, the **Agent Details** displays.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_display_agent_details.png)

At the below of **Agent Details**, in the **Threshold** item, we select the number moreover than 1. For this example, we choose number 2 and click the button **Update**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_threshold_agent_update.png)

## Run multiple Test Suites

Make a Script Repository and upload it to Katalon TestOps. On Katalon TestOps, open this Script Repository, and click the run button.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_sample_script_repo.png)

The board **Test run type** displays. We choose and type the information in the cells of items.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_test_run_type.png)

At the item Test Suite Collection, we choose a Test Suite Collection which we want to run. At the item Execution Mode, we choose Parallel for running multiple Test Suite parallel. At the item Test Environment Type, we choose Local Test Environment.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_test_run_type_1.png)

At the item Test Environments, we choose agents which we have just started. We select the version of Katalon Studio at the item Katalon Studio Version or Pre-Installed Katalon Studio Location.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_test_run_type_2.png)

We click the button Creat at below for creating a new Test Run Type.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_test_run_type_3.png)

In the board Test Planning, a new Test Run Type displays with agents, which we have just started. We click the button Run for running.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_new_test_run_type.png)

Two agents run parallelly.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_two_agents_run.png)

We can see the results of Test Suites at **Report & Analysis**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_test_run.png)

## Related topics

- [Create a Local Test Environment with Agent](https://docs.katalon.com/katalon-analytics/docs/agents.html)
- [Install Katalon TestOps Agent on a test machine](https://docs.katalon.com/katalon-analytics/docs/install_kt_agent.html)

