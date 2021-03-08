---
title: "Execute Test Runs by a Trigger"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-scheduler.html 
description: 
---

Trigger is used to determine when a Test Run is executed. This helps you leverage remote execute to take fully control of your testing plan.

## Prerequisites

- You have scheduled your Test Runs. [Learn more](https://docs.katalon.com/katalon-analytics/docs/create-plan.html)

On Katalon TestOps, choose **Reports & Analytics** > **Test Run**. Then we choose an ID of a Test Run which you want to create a Trigger.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_report_analytic_test_run.png)

Click the Configuration button on the top right corner.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_test_run_summary.png)

## Create a Trigger

For creating a Trigger of Test Run, click Create Trigger button on the top right corner. And note that the Agent of Test Run displays below.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_test_plan_create_trigger.png)

Type information of a Trigger which we want to create. In the **Create Trigger** view, enter the required details:
   * **Name**: give a name that has a meaning.
   * **From-To**: the period in which the scheduled jobs start.
   * **Interval** and **Interval Unit**: a schedule of executing test.
     For example: With Interval=3, and Interval Unit=Day, we execute the test every three days.
   * **Active**: You can change the status of the Trigger with this switch.

Before creating a Trigger, we have to run the Agent of Test Run. For running the Agent, we can [see here](https://docs.katalon.com/katalon-analytics/docs/install_kt_agent.html). Then click Create button.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_create_trigger.png)

We created a Trigger successfully, and Test Run will start executing at our preferred time.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_trigger_run.png)

After we finish executing Test Run, the diagram of Test Run is displayed.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_trigger_end.png)

You can view a list of your Triggers in the **Configuration** tab in the **Test Run Types** section.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_config_test_run_type.png)

## View Test Run status

Your Test Runs will execute automatically based on your configurations. 

Test Run status can be found in the calendar view in **Test Planning**. [Learn more](katalon-analytics/docs/create-plan.html#view-test-runs)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_trigger_test_plan.png)

## Related topics

- [Set up Configurations for Remote Execution](/katalon-analytics/docs/test-run-config.html)
- [Execute a Test Run manually](/katalon-analytics/docs/execute-test-run.html)
- [Katalon TestOps Terminology](/https://docs.katalon.com/katalon-analytics/docs/testops-terminology.html#trigger)