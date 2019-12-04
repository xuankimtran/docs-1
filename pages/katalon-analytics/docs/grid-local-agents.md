---
title: "Execute Scheduled Tests"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/grid-local-agents.html 
description: 
---

**Grid and Local Agents** are designed to make Katalon Studio test execution simpler and schedulable on your local servers. It will also automatically feed test results into Katalon TestOps.

With this feature, you now can run your planned tests at any time with just a click. You can also speed up the test execution by distributing them across browsers and operating systems, and running them in parallel or on schedule. 

This page provides necessary information about how to execute Katalon Studio tests automatically on your Local Agents. 

> **Prerequisites**:
>
> * You have uploaded your test project to Code Repo.
> * Local Agents must have been installed and started for test execution.

To execute your test projects on Local Agents:

### Schedule a test plan with local agent
1. In your project, select **Grid**.
2. Select the **Create Plan** button.
3. In the **Configure a Plan** screen, define your test execution plan:
    * **Plan Name**: Provide a plan name which should have a meaning.
    * **Test Project**: Select the test project you’ve uploaded earlier.
    * **Command**: Provide command arguments to run your Katalon Studio tests. This command can be retrieved from [Katalon Studio command generator](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#katalon-command-line-options).
    * **Execution Environment**: Select and add **Agents**. Here is where you can choose multiple OS to run your tests later.
    * **Schedule**: Define a schedule for job execution.
4. Click **Create**.

### Execute the scheduled test plan

In the **Grid** view, **Plans** > choose the plan you want to execute > **Execute Plan**. Depending on the number of selected Agents, new jobs will be initiated and queued on the Jobs list right on top of the screen. If they are executed successfully, you will see a link that leads you to the execution result.
