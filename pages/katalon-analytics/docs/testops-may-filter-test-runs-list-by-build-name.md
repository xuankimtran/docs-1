---
title: "Filter Test Runs list by Build name"
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-analytics/docs/filter-test-build-name.html
description:
---

In Katalon TestOps, you can filter Test Runs by Build name to:

* Find and track the list of Test Runs linked with specific Build names.
* Monitor testing progress linked with those Builds.

> Requirements:
>
>* You must execute tests from Katalon Runtime Engine.
>* You have integrated Katalon Studio with Katalon TestOps. See: [Katalon Studio Integration](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

## Add Build name in Command Line or Console Mode

Follow these steps:
1. Open Command prompt.
2. Find the Command Line option `--info -buildLabel` and edit it with your own info.

> Notes:
>
> You can find it in [this list of `katalonc` command options](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options).

## Filter Test Runs by Build name in Katalon TestOps

Follow these steps:
1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

2. Go to **Reports** > **Test Runs**.
4. Find the **Build Label** filter as shown below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-may-filter-test-runs-list-by-build-name/build-label-button-2.png"  width=100% alt="build name new UI">

    By default, it will display _All_ which means that all of your Test Runs in all Builds are listed.

5. Click **Build Label**, then manually input the `-buildLabel` value that was previously configured in Katalon Studio.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-may-filter-test-runs-list-by-build-name/build-label-box.png" width=70% alt="build name box">

5. Click **Update**.

    You can now see the list of Test Runs associated with that `-buildLabel`.

> Notes:
>
> * The Build name will be displayed under the **Configuration** section on each Test Run.
> * You can also go back to the default filter by clicking **Clear**.
