---
title: "Execute Test Runs by a Trigger"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-scheduler.html 
description: 
---

In Katalon TestOps, you can execute Test Runs manually or automatically.

> Requirements:
>
> You have already created a Test Runs schedule. See: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).
>
> You have set up an Agent and let it run while executing Test Runs. See: [Agent Setup](https://docs.katalon.com/katalon-analytics/docs/install_kt_agent.html).

## Execute Test Runs by a Trigger

Using a Trigger allows you to execute a Test Run automatically. By doing so, you can leverage Remote Execution to take a full control of your testing plan.

### Create a Trigger

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project. 

  The Project's **Dashboard** page appears.

2. Go to **Reports & Analytics** > **Test Runs**.

3. Click on the ID number of a Test Run you want to create a Trigger for.

  The **Test Run: #** page appears and **#** represents the ID number.

  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_report_analytic_test_run.png)

4. Click on the *Configuration* icon at the top right corner of the page.

  The **Configuration** page appears as below.  

  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_test_run_summary.png)

> Notes:
  >
  > Make sure the Agent of that Test Run appears on the page (e.g., **My Agent**).

5. Click on the **Create Trigger** button.

  The **Create Trigger** page appears as below.
   
  ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_test_plan_create_trigger.png)

6. Fill in the required information.

   * In the **Name** section, create a name for the Trigger.
   * In the **From** and **To** sections, set the time and date during which a Test is executed.
   * In the **Interval** and **Interval Unit** sections, create the frequency for that Test Run.

     For example: If the **Interval Unit** is **Day** and the **Interval** is **3**, a Test is executed every three days.
   * The **Active** switch allows you to change the status of the Trigger.

7. Click **Create**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_create_trigger.png)
 
You have created a Trigger to execute a Test Run. The execution starts automatically at the time you have configured.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_trigger_run.png)

You can see all Triggers you have created in the **Test Run Types** page.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_config_test_run_type.png)

> Notes:
>
> The Agent must always be running for Test Runs execution.

## Execute Test Runs manually

You can also execute Test Runs manually by following these steps:

1. Go to your Project > **Test Planning** >  **Test Run Types**. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/execute-test-runs/kt2_test_run_type_run.png)

2. Click on the *Run* icon for manual execution.

## View the status of Test Runs

With a Trigger, your Test Runs are executed automatically based on your configurations when creating a Trigger.

With a manual click, you have executed Test Runs manually at the time you click on the *Run* icon.

After executing Test Runs, go to **Test Planning** to check their status in a calendar view. See: [View Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html#view-test-runs).

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/kt_trigger_test_plan.png)

![](https://github.com/katalon-studio/docs-images/raw/9f5d0c65c5fbca35fb4237a7ccfc7d282fab1038/katalon-analytics/docs/execute-test-runs/kt2_test_planning.png)

See also:
* [Set up Configurations for Remote Execution](https://docs.katalon.com/katalon-analytics/docs/test-run-config.html).

* [Katalon TestOps Terminology](https://docs.katalon.com/katalon-analytics/docs/testops-terminology.html#release).
