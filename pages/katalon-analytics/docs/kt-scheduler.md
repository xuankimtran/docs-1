---
title: "Schedule Remote Execution"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-scheduler.html 
description: 
---

To schedule a test or view a list of scheduled test, log into Katalon TestOps > go to your project > select **TestOps CI** > select **Plan**.

You can plan your tests and execute using Local Agents or other test environments such as EKS or CircleCI. In this tutorial, we use CircleCI test enviroment as an example.

## Plan a test

> **Prerequisites**:
>
> * Agents or Test Environments must have been configured for test execution. To start a local agent or create other test environments, please visit the below documents:
>   - [Start an Agent](https://docs.katalon.com/katalon-analytics/docs/agents.html)
>   - [Create a CircleCI test environment](https://docs.katalon.com/katalon-analytics/docs/circleci.html)
>   - [Create an EKS test environemnt](https://docs.katalon.com/katalon-analytics/docs/aws-eks.html)
> * You have created a test project in **Code Repo**.


To create a new test plan, please follow the below instruction:

1. In your project, select **Plan**.
2. Click **Create Plan** on the top right corner.
3. In **Configure a Plan**, enter required details to define your test execution plan:

  * **Plan Name**: It's recommended to give a name that has a meaning.
  * **Test Project**: Select a test project in the drop-down list.
  * **Type**:
    * **Test Suite Collection**: Select a Test Suite or a Test Suite Collection that you want to execute.
    * **Katalon Command**: Enter a command to execute Katalon Studio tests. This command can be generated from [Katalon Studio command generator](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#katalon-command-line-options).
    * **Generic Command**: Enter a command to execute this test with another tool.
  * **Cloud type**: Select the test environment which you have already configured: Local Agent or other Test Environments such as CircleCI or EKS. The following screenshots are examples of CircleCI configuration.

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/config-plan-1.png" width="" height="">

  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/config-plan-2.png" width="" height="">

  * **Katalon Studio Version** when you want the Agent to download Katalon Studio automatically.\
  Or you can use **Pre-Installed Katalon Studio Location** to browse to Katalon Studion on your machine. This option is recommended in network restricted environments.

4. Select an Agent in the drop-down list. If you have just configured an Agent, please wait for a while for it to be registered with Katalon server.
5. Click **Create**. The newly created test plan will be displayed on the **Plan** view .



## Schedule a test plan

When you have a test plan, you can schedule when to execute it.

1. On the **Plan** view, select a test plan by clicking its name.
2. Select **Schedule** on the top right corner.
3. In the **Schedule** view, enter the required details:

   * **Name**: It's recommended to give a name that has a meaning.
   * **From-To**: The period in which the scheduled jobs start.
   * **Interval** and **Interval Unit**: Every <_Interval_> <_Interval Unit_>, a scheduled test is executed.
     For example: With Interval=3, and Interval Unit=Day, a test is executed every 3 days.
   * **Active**: You can change the status of the Schedule with this switch.

4. Click **Create** to create a schedule.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/schedule-plan.png" width="" height="">

Your test plan is now ready to be executed at your preferred time. The scheduled test that is being executed will be displayed on the **Jobs** table.

