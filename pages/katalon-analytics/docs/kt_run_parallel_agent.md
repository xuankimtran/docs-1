---
title: "Run multiple Test Suites in parallel with Agents" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt_run_parallel_agent.html 
description: 
---

## Configure parallel executions

Follow these steps:

1. Create two Local Test Environments. See: [Create a Local Test Environment with an Agent](https://docs.katalon.com/katalon-analytics/docs/install_kt_agent.html).

    You then start two Agents to prepare for Test Suites execution.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_start_two_agent.png" width=100% alt="start 2 agents">

2. Update each Agent's Threshold to **2**. See [Configure an Agent's Threshold](https://docs.katalon.com/katalon-analytics/docs/load-balancing-agents.html#configure-an-agents-threshold).

    The assigned sessions for each Agent is now **2**.

3. Creat a Script Repository. See: [Upload Test Scripts from a Git Repository](https://docs.katalon.com/katalon-analytics/docs/git-test-project.html#create-git-script-repositories).

    You can now see the newly-created Script Repository appear in the **Script Repositories** page.

4. Click on the Script Repository you have created.

    The Script Repository page appears. In the **Test Suite Collection** section, you will see a **Play** button.

5. Click on the **Play** button.

    The **Schedule Test Run** dialog appears.

6. Fill in the required information. See: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html#schedule-test-runs).

    > Notes:
    >
    > * In the **Test Environments** section, select the Agents you have configured earlier.
    > * In the **Advanced settings** section, choose **Parallel** for **Execution Mode**. See: [Advanced settings](https://docs.katalon.com/katalon-analytics/docs/create-plan.html#advanced-settings).

You have created a new Test Run List for parallel executions of Test Suites.

### Update existing Test Run List

If you have previously scheduled Test Runs in sequential mode, you can also update your existing Test Run List so that it can be executed in parallel.

Follow these steps:

1. Start two Agents.
2. Update each Agent's Threshold to **2**.
3. Go to **Test Execution** > **Test Run List**.
4. Click on the Test Run List you want to update.
5. Click on the **Edit** button in the top right corner.

    The **Schedule Test Run** dialog appears.
    
    Update the schedule as follow:

    * In the **Test Environments** section, select the Agents you have started earlier.

    * In the **Advanced settings** section, choose **Parallel** for **Execution Mode**. See: [Advanced settings](https://docs.katalon.com/katalon-analytics/docs/create-plan.html#advanced-settings).

## Run Test Suites in parallel

1. Go to **Test Execution** > **Test Run List**. 
    
    You can see the new Test Run List here.

2. Click on the *Run* icon.

    The two Agents are now running at the same time.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt_run_parallel_agent/kt_two_agents_run.png" width=100% alt="2 agents run concurrently">

## View Test Suites results

Go to **Reports** > **Test Runs** to see the result of Test Suites you have run in parallel.

See also: [Auto-Distributed Executions](https://docs.katalon.com/katalon-analytics/docs/auto-distributed-execution.html).
