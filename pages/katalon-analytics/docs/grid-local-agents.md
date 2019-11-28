---
title: "Execute Scheduled Tests with Local Agents" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/grid-local-agents.html 
description: 
---

**Grid - Local Agents** is designed to make Katalon Studio test execution simpler and schedulable on your local servers. It will also automatically feeds the results into Katalon Analytics.

With this feature, you may now run your planned tests any time with just a button click. You can also speed up the test execution by distributing them across browsers and operating systems, running them in parallel or on schedule. 

This page provides basic information about how to execute Katalon Studio tests automatically on your Local Agents. 

> **Prerequisites**:
>
> * You have uploaded your test project onto Code Repo.
> * Local Agents must have been installed and available for test execution. If not, please follow this guide.

To execute your test projects on Local Agents:

1. Select **Grid**
2. Select the **Create Plan** button
3. In the **Configure a Plan** screen, define your test execution plan
    * **Plan Name**: Provide a friendly plan name
    * **Test Project**: Select the test project you’ve uploaded earlier
    * **Command**: Provide command arguments to run your Katalon Studio tests. This can be retrieved from [Katalon Studio command line builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#katalon-command-line-options).
    * **Execution Environment**: Select and add **Agents**. Here is where you can choose multiple OS to run your tests later
    * **Schedule**: Define a schedule for job execution
4. Select **Create** to create your plan.
5. In the **Grid** screen, go to the **Plans** list. Choose the plan you want to execute and select **Execute Plan** icon.
After that, depending on the number of selected Agents, new jobs will be initiated and queued on the Jobs list right on top of the screen. If they are built successfully, you will see an execution link that leads you to the execution result screen.