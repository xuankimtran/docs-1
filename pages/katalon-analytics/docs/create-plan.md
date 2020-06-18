---
title: "Create and Run a Test Plan"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/create-plan.html 
description: 
---
## Create a new Test Plan

> **Prerequisites**:
>
> * Agents or Test Environments must have been configured for test execution. To start a local agent or create other test environments, please visit the below documents:
>   - [Start an Agent](https://docs.katalon.com/katalon-analytics/docs/agents.html); or
>   - [Create a CircleCI test environment](https://docs.katalon.com/katalon-analytics/docs/circleci.html); or
>   - [Create an EKS test environemnt](https://docs.katalon.com/katalon-analytics/docs/aws-eks.html).
>
> * You have created a test project in **Test Projects**.


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
5. Click **Create**. The newly created test plan will be displayed on the **Plan** view.

## Run a Test Plan

After a test plan has been created, you can run it manually or schedule your tests.

To run your test plan, in your project, go to **Plan** > click on the icon as below.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/create-plan/run-plan.png" width="" height="">

You can also run your test plan by go to the test plan details page and click on **Run** button.

After you have finished running the test plan, you can view the status in the details page. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/create-plan/run-details.png" width="" height="">

Refer to [this document](https://docs.katalon.com/katalon-analytics/docs/kt-scheduler.html) to learn how to schedule a test plan.