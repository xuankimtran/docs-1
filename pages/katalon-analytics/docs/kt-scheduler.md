---
title: "Schedule Remote Execution"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-scheduler.html 
description: 
---

To schedule a test or view a list of scheduled test, log into Katalon TestOps > go to your project > select **Grid**.

To create a new test plan, please follow the below instruction:

> **Prerequisites**:
>
> * You have created a test project in Code Repo.
> * Agents must have been configured for test execution.

1. In your project, select **Grid**.
2. Click **Create Plan** on the top right corner.
3. In **Configure a Plan**, enter required details to define your test execution plan:

  * **Plan Name**: It's recommended to give a name that has a meaning.
  * **Test Project**: Select a test project in the drop-down list.
  * **Type**:
    * **Test Suite Collection**: Select a Test Suite or a Test Suite Collection that you want to execute.
    * **Katalon Command**: Enter a command to execute Katalon Studio tests. This command can be generated from [Katalon Studio command generator](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#katalon-command-line-options).
    * **Generic Command**: Enter a command to execute this test with another tool.

  * **Katalon Studio Version** when you want the Agent to download Katalon Studio automatically.\
  Or you can use **Pre-Installed Katalon Studio Location** to browse to Katalon Studion on your machine. This option is recommended in network restricted environments.

4. Select an Agent in the drop-down list.
5. Click **Create**. The newly created test plan will be displayed on the Grid view .

Your test plan is now ready to be executed at any time.
