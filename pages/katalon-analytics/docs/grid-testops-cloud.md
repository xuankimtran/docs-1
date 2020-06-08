---
title: "Execute Scheduled Tests with Katalon TestOps Cloud" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/grid-testops-cloud.html 
description: 
---

**Plan** is a great way to run your Katalon Studio tests completely on cloud and automatically feed the results into **Katalon TestOps**.
This article will show you how to execute your tests handily via Plan - TestOps CI.

> **Prerequisites**:
>
> * You have uploaded your test project onto [Test Projects](code-repo.html).

### To execute your test projects on TestOps Cloud

1. Select **Plan**
2. Select the **Create Plan** button
3. In the **Configure a Plan** screen, define your test execution plan
    * **Plan Name**: Provide a friendly plan name
    * **Test Project**: Select the test project you’ve uploaded earlier
    * **Command**: Provide command arguments to run your Katalon Studio tests. This can be retrieved from [Katalon Studio command line builder](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#katalon-command-line-options).
    * **Execution Environment**: Select TestOps Cloud
    * **Schedule**: Define a schedule for job execution
4. Select **Create** to create your plan.
5. In the **Plan** screen, go to the **Plans** list. Choose the plan you want to execute and select **Execute Plan** icon.

After that, a new job is initiated and queued on the Jobs list right on top of the screen. If it is built successfully, you will see an execution link that leads you to the execution result screen.
