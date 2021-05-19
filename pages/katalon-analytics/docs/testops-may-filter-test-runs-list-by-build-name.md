---
title: "Filter Test Runs list by Build name"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/filter-test-runs-list-by-build-name.html
description:
---

Katalon TestOps users can filter Test Runs by Build name to:
* Find and track easily the list of Test Runs linked with specific Build names.
* Monitor testing progress linked with those Builds.

## Prerequisites
* Execute tests from Katalon Runtime Engine.
* Integrate Katalon Studio with Katalon TestOps.

## Add Build name in Command Line or Console Mode
Follow these steps:
1. Open Command prompt.
2. Find this Command Line option `--info -buildLabel` and edit it with your own info.
> If you are unclear, check [here](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options) for the list of options supporting `katalonc` commands.

## View Test Runs by Build name in Katalon TestOps
Follow these steps:
1. Access to your [TestOps](https://testops.katalon.io/login) account and choose your project.
2. Navigate to **Test Runs** list in **Reports & Analytics**.
3. Find the Build filter. 

    By default, it will display _All_ which means that all of your Test Runs in all Builds are listed.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-may-filter-test-runs-list-by-build-name/v1.0-build-label-1.png" width=100%>

4. Click on the Build filter to start filtering. Manually input the `-buildLabel` value that is previously configured in Katalon Studio.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-may-filter-test-runs-list-by-build-name/v1.0-build-label-2.png" width=70%>

5. Click **Update**.

    You, then, see the list of executed Test Runs in that `-buildLabel`.
> The Build name will be displayed under **Configuration** section on each Test Run.

If you want, you can also go back to **Default** status by choosing **Clear** for the current `-buildLabel`.