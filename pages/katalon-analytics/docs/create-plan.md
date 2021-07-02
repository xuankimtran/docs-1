---
title: "Schedule Test Runs"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/create-plan.html 
description: 
---

> Requirements:
>
> * You have created a [Local Test Environment with Agent](https://docs.katalon.com/katalon-analytics/docs/agents.html), or you have already created a different Test Environment (Docker, Kubernetes, etc.).
>
> * You have created a [Script Repository](https://docs.katalon.com/katalon-analytics/docs/code-repo.html).

## Schedule Test Runs

Follow these steps:

1. Go to your Project and select the **Test Planning** tab.

    The **Test Runs** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-button.png" width=100%>

    > Notes:
    >
    > If you have not scheduled any Test Run yet, the calendar view in the **Test Runs** page is empty.

2. Click on the **Schedule Test Run** button.

    The **Schedule Test Run** page appears as below.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-page-fill-in-1.png" width=100%>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-page-fill-in-2.png" width=100%>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-page-fill-in-3.png" width=100%>

    Fill in all the required information and click **Create**.
    
You have created a new schedule for your Test Runs.

After creating the schedule, Katalon TestOps automatically directs you to the **Test Run Types** page.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/test-run-type-page.png" width=100%>

The **Test Run Types** page shows you a collection of Test Runs with the same configurations (Test Environment, Trigger, Script Repository).

## View Test Runs

Once creating a schedule for Test Runs, the calendar in the **Test Runs** page reflects the change.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/test-runs-page-after-scheduling-test-run.png" width=100%>

Click on a Test Run in the calendar to see its summary.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/detail-of-test-run-after-clicking-it-on-calendar.png" width=100%>

If the Tests belongs to a Test Suite, you can also see a summary of the Test Suite here.

Next step: [Execute Test Runs](https://docs.katalon.com/katalon-analytics/docs/kt-scheduler.html).
