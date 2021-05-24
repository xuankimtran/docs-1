---
title: "Filter Test Runs list by Build name"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/filter-test-build-name.html

description:
---

In Katalon TestOps, you can filter Test Runs by Build name to:

* Find and track the list of Test Runs linked with specific Build names.
* Monitor testing progress linked with those Builds.

> **Prerequisites**
>
>* Execute tests from Katalon Runtime Engine.
>* Integrate Katalon Studio with Katalon TestOps.
>
>   You can learn about integration [here]( https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

## Add Build name in Command Line or Console Mode
Follow these steps:
1. Open Command prompt.
2. Find the Command Line option `--info -buildLabel` and edit it with your own info.
> You can find it in this [list of `katalonc` command options](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options).

## Filter Test Runs by Build name in Katalon TestOps
Follow these steps:
1. Go to [TestOps web page](https://testops.katalon.io/login) account and choose your project.
2. Login to your account and choose your project. 
3. Click on **Reports & Analytics**, then **Test Runs**.
4. Find the **Build Label** filter as shown below. 

    By default, it will display _All_ which means that all of your Test Runs in all Builds are listed.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-may-filter-test-runs-list-by-build-name/v1.0-build-label-1.png" width=100%>

5. Click on the Build filter to start filtering. Manually input the `-buildLabel` value that was previously configured in Katalon Studio.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-may-filter-test-runs-list-by-build-name/v1.0-build-label-2.png" width=70%>

5. Click **Update**.

    You can now see the list of Test Runs associated with that `-buildLabel`.
> The Build name will be displayed under the **Configuration** section on each Test Run.

You can also go back to the default filter by clicking **Clear**.
