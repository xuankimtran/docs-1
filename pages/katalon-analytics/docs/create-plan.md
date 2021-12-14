---
title: "Schedule Test Runs"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/create-plan.html 
redirect_from: 
    - "/katalon-analytics/docs/view-ci-plans.html"
    - "/katalon-analytics/docs/grid-testops-cloud.html" 
    - "/katalon-analytics/docs/kt-remote-execution.html"
description: 
---

> Requirements:
>
> * You have created a [Local Test Environment with Agent](https://docs.katalon.com/katalon-analytics/docs/agents.html), or you have already created a different Test Environment (Docker, Kubernetes, etc.).
>
> * You have created a [Git Script Repository](https://docs.katalon.com/katalon-analytics/docs/git-test-project.html).

## Schedule Test Runs

Follow these steps:

1. Go to your Project and select the **Test Execution** tab.

    The **Test Run Calendar** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-button.png" width=100% alt="test run page">

    > Notes:
    >
    > If you have not scheduled any Test Runs yet, the calendar is empty.

2. Click on the **Schedule Test Run** button.

    The **Schedule Test Run** dialog appears as below.

     <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-new-ui-trigger-automated-test-2.png" width=100% alt="schedule test run page new UI">

3. Fill in the information.

    * In the **General Information** section, create a name for the schedule.
    * In the **What to run** section, fill in the following information:
        * **Script Repository**: select your repository in the dropdown list.

            > Notes:
            >
            > Katalon TestOps currently supports test scripts from Katalon Studio and Git Repositories (GitHub and Bitbucket). See: [Upload Test Scripts from a Git Repository](https://docs.katalon.com/katalon-analytics/docs/git-test-project.html#create-git-script-repository).

        * **Type**: choose between **Test Suite Collection**, **Katalon Command** and **Generic Command** to run your tests.

            > Notes:
            >
            > * You choose **Test Suite Collection** if you want to select the Test Suite Collections directly from Katalon Studio (KS). Katalon TestOps will automatically fetch your Test Suite Collections.
            > * You choose **Generic Command** if you want to execute tests with other frameworks outside KS (e.g., Pytest).
            > * You choose **Katalon Command** if you want to execute tests with KS. The Katalon commands can be generated from KS (in the **Command Generator** dialog). See: [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html).

    * In the **Where to run** section, fill in the following information:
        * **Test Environment Type**: choose among **Local Test Environment**, **Kubernetes Test Environment** or **CircleCI Test Environment**.

            > Notes:
            >
            > If you are using KRE, check the **Katalon Runtime Engine Version** box and select the version you are using from the dropdown list.

        * **Test Environments**: select the Agents you want to use for test executions.

    * In the **When to run** section, you have the following options:
        * If you want to run tests periodically, select **Trigger Automated Test**, turn the **Repeat** toggle on, set the time period and the interval you want to run the tests (e.g., run tests every **2 days** from **09/21/2021 10:49** to **10/20/2021 11:00**), then click **Schedule**. You have created a trigger to run tests automatically.

            <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-new-ui-trigger-automated-test-2.png" width=100% alt="schedule test run page new UI automatic run">

        * If you want to run tests immediately, select **Trigger Automated Test**, turn the **Repeat** toggle off, then click **Run**. You have run the tests manually.

            <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-new-ui-manually-2.png" width=100% alt="schedule test run page new UI manual run">
        
        * If you want to save what you have configured so far without running tests, select **Save Configurations**, then click **Save**. You then can come back another time to run tests manually. See: [Execute Test Runs manually](https://docs.katalon.com/katalon-analytics/docs/kt-scheduler.html).

            <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-new-ui-save-config-2.png" width=100% alt="schedule test run page new UI save config">
        
### Advanced settings

You can optimize your configurations in the **Advanced settings** section of the **Schedule Test Run** dialog.

Follow these steps:

1. Open the **Schedule Test Run** dialog.
2. At the bottom of the dialog, click **Advanced settings**.

    The dialog now appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/schedule-test-run-new-ui-advanced-settings-2.png" width=100% alt="schedule test run page new UI automatic run">

    * **Execution Mode**: choose between **Sequential** (run one test after another) or **Parallel** (run tests at the same time). See: [Run multiple Test Suites in parallel with Agents](https://docs.katalon.com/katalon-analytics/docs/kt_run_parallel_agent.html).
    * **Timeout in Minutes**: define the time after which test execution is cancelled.
    * Kobiton integration: switch the **Kobiton** toggle on to enable the integration, then enter your Kobiton Device ID to run tests on that device. See: [How to configure Kobiton integration with Katalon TestOps](https://docs.katalon.com/katalon-analytics/docs/kt_kobiton_integration.html).
    * **Release Version**: select the release version you want to link your test runs to. See: [Manage Test Runs by Release](https://docs.katalon.com/katalon-analytics/docs/kt-release.html#create-a-new-release).

After creating the schedule, Katalon TestOps automatically directs you to the **Test Run List** page.

The **Test Run List** page shows you a collection of Test Runs with the same configurations (Test Environment, Script Repository).

## View Test Run Types in Katalon Studio

> Notes:
>
> The **Test Run List** in TestOps is equivalent to the **Test Run Types** in Studio.

> Requirements:
>
> * Katalon Studio version 7.9.1 onwards.
> * [Katalon Studio Integration](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

Follow these steps:

1. Open Katalon Studio and your Project.

2. In the **Tests Explorer** sidebar, go to **TestOps** > **Test Run Types**.

    You then can view a summary of Test Run Types that have been configured in TestOps.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/navigate-to-test-run-type-in-studio.png" width=100% alt="find test run types in studio">

3. Click on any of the Test Run names (e.g., **a Verify Match exact name(git)**). This opens the Test Runs Summary page in Katalon TestOps.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-june-schedule-test-runs/detail-of-test-run-type-on-testops-2.png" width=100% alt="test run details on testops">

See also: [Execute Test Runs manually](https://docs.katalon.com/katalon-analytics/docs/kt-scheduler.html).