---
title: "Schedule Test Runs"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/create-plan.html 
redirect_from: /katalon-analytics/docs/view-ci-plans.html
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

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-button.png" width=100% alt="test run page">

    > Notes:
    >
    > If you have not scheduled any Test Run yet, the calendar view on the **Test Runs** page is empty.

2. Click on the **Schedule Test Run** button.

    The **Schedule Test Run** dialog appears as below.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-page-fill-in-1.png" width=100% alt="schedule test run page new UI">

3. Fill in the required information.

    * In the **General Information** section, create a name for the schedule.
    * In the **What to run** section, fill in the following information:
        * **Script Repository**: select your repository in the drop-down list.

            > Notes:
            >
            > Katalon TestOps currently supports test scripts from Katalon Studio and Git Repositories (GitHub and Bitbucket).  

        * **Type**: select ?

    * In the **When to run** section, you can choose to either run tests automatically or manually.

        * To run tests automatically, switch the **Repeat** toggle on, then select the time and interval for your test runs. By doing so, you have created a trigger to run tests periodically and automatically.

        * To run tests manually, switch the **Repeat** toggle off, then click **Run**.

    * In the **Where to run** section, fill in the following information:
        * **Test Environment Type**: choose among **Local Test Environment**, **Kubernetes Test Environment** or **CircleCI Test Environment**.

            > Notes:
            >
            > For **Local Test Environment**, you can check the **Katalon Runtime Engine Version** box to download your test runs automatically from KRE. Or you can check the **Pre-installed Katalon Studio Location** box to retrieve Katalon Studio's tests from your local machine. 

        * **Test Environments**: select the Agents you want to use for test executions.

    * In the **Advanced Settings** section, fill in the following information:

        * **Execution Mode**: choose between **Sequential** (run one test after another) or **Parallel** (run tests at the same time).
        * **Timeout in Minutes**: enter the time after which test execution is aborted.
        * Kobiton integration: switch the **Kobiton** toggle on to enable the integration, then enter Kobiton Device ID for test runs on that devide.
        * **Release Version**: select the release version you want to link your test run to.
4. Click **Save**.
    
You have created a new schedule for your Test Runs.

After creating the schedule, Katalon TestOps automatically directs you to the **Test Run Types** page.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/test-run-type-page.png" width=100% alt="test run types page">

The **Test Run Types** page shows you a collection of Test Runs with the same configurations (Test Environment, Trigger, Script Repository).

## View Test Run Types in Katalon Studio

> Requirements:
>
> * Katalon Studio version 7.9.1 onwards.
> * [Katalon Studio Integration](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

Follow these steps:

1. Open Katalon Studio and your Project.

2. Go to **TestOps** > **Test Run Types** on the **Tests Explorer** sidebar.

    You then can view a summary of Test Run Types that have been configured in TestOps.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/navigate-to-test-run-type-in-studio.png" width=100% alt="find test run types in studio">

3. Click on one of the names to view Test Runs details in Katalon TestOps (e.g., **a Verify Match exact name(git)**).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/detail-of-test-run-type-on-testops.png" width=100% alt="test run details on testops">
    
Next step: [Execute Test Runs](https://docs.katalon.com/katalon-analytics/docs/kt-scheduler.html).
