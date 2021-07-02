---
title: "Execute Test Runs"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-scheduler.html 
redirect_from: /katalon-analytics/docs/execute-test-run.html 
description: 
---

In Katalon TestOps, you can manually execute Test Runs, or schedule them automatically.

> Requirements:
>
> You have already created a Test Runs schedule. See: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).

## Execute Test Runs with a Trigger

Using a Trigger allows you to execute a Test Run automatically. By doing so, you can leverage Remote Execution to take complete control of your testing plan.

### Create a Trigger

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

2. Go to **Test Planning** > **Test Run Types**.

3. Click on the Test Run you want to create a Trigger for.

    The Test Run page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-execute-test-runs-by-trigger/config-of-test-trigger.png" width=100%>

    > Notes:
    >
    > If you have already set up an Agent, the Agent of Test Runs displays on the page (e.g., **My Agent**).

5. Click on the **Create Trigger** button.

    The **Create Trigger** page appears as below.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-execute-test-runs-by-trigger/create-trigger-page.png" width=100%> 
 
6. Fill in the required information.

   * In the **Name** section, create a name for the Trigger.
   * In the **From** and **To** sections, set the time and date during which a Test Run is executed.
   * In the **Interval** and **Interval Unit** sections, create the frequency for that Test Run.

     For example: If the **Interval Unit** is **Day** and the **Interval** is **3**, a Test Run is executed every three days.

   * The **Active** switch allows you to turn the Trigger on or off.

7. Click **Create**.

You have created a Trigger to execute a Test Run. The execution starts automatically at the time you have configured.

You can see all Triggers you have created on the **Test Run Types** page.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-execute-test-runs-by-trigger/list-of-triggers-for-test-run-in-test-run-types-page.png" width=100%> 

By creating Triggers, **Next Run** is scheduled for automatic execution.

> Notes:
>
> The Agent must always be running for Test Runs execution.

## Execute Test Runs manually

You can also execute Test Runs manually by following these steps:

1. Go to your Project > **Test Planning** > **Test Run Types**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-execute-test-runs-by-trigger/test-run-manual-mode-button.png" width=100%> 

2. Click on the *Run* icon for manual execution.

## View the status of Test Runs

After executing Test Runs, go to **Test Planning** to check their status in a calendar view.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/test-runs-page-after-scheduling-test-run.png" width=100%>

Click on a Test Run in the calendar to see its summary.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/detail-of-test-run-after-clicking-it-on-calendar.png" width=100%>

If the Tests belongs to a Test Suite, you can also see a summary of the Test Suite here.

Next step: [Manage Test Runs by Release](https://docs.katalon.com/katalon-analytics/docs/kt-release.html).
