---
title: "TestRail Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/testrail-integration.html
redirect_from:
    - "/katalon-studio/docs/katalon-testrail-integration.html"
    - "/katalon-studio/tutorials/katalon-testrail-integration.html"
description:
---

**TestRail Integration** plugin establishes the connection between Katalon Studio and TestRail to deliver the following advanced capabilities:

* Map test cases between Katalon Studio and TestRail.
* In TestRail, you can send and view Test Results of both Test Suites and Test Cases executed in Katalon Studio.
* In Katalon Studio, you can query Test Runs of TestRail in [Dynamic Test Suite](https://docs.katalon.com/katalon-studio/docs/dynamic-test-suite.html).

Click [here](https://store.katalon.com/product/13/TestRail-Integration) to get the TestRail Integration plugin. After installing the plugin, open **Katalon Studio** > click **Reload Plugins**. Learn more about [how to reload plugins](https://docs.katalon.com/katalon-store/docs/user/access-store-in-KS.html#reload-plugins).

## Configurations

To enable the integration of Katalon Studio with TestRail, you need to:

### In TestRail

Log in to your account **> Administration > Site Settings > API > Enable API > Save Settings**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/TR-ENABLE-API.png" width="1035" height="397">

### In Katalon Studio

1. Enable **TestRail Integration** plugin in Project Settings:

* After installing and reloading the plugin, open **Katalon Studio** > from Katalon Studio menu bar > **Project** > **Settings**.
* In the **Project Settings** window > **Plugins** > **TestRail** >  Check **Using TestRail** to enable the integration.

2. Enter the credentials required for **Authentication**:

* **URL**: your TestRail instance `https://<example>.testrail.io`.
* **Username**: your TestRail Username.
* **Password**: your TestRail password.
* **Project**: Specify the TestRail project's ID (an integer) you'd like to integrate with Katalon Studio.

    > To view the **project ID**, open your project in TestRail > view the TestRail Project URL.

3. Click **Test Connection** and then **OK**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-CONFIG.png" width="794" height="597">

## Map test cases between Katalon Studio and TestRail

### In TestRail 

You need to enter the Test Case's ID of TestRail (only the integer) in Katalon Studio's test cases to establish a connection between them. To view the Test Case's ID, open your project in TestRail:

* For projects using one single repository for all test cases: Select **Test Case** tab > Test Case's ID.
* For projects using multiple test suites for managing test cases: Select **Test Suites and Cases** tab > click the Test Suite containing your preferred Test Case > Test Case's ID.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/TR-VIEW-TC.png" width="" height="">

### In Katalon Studio

Double-click a Test Case to open the test case view > **Integrations** tab > specify the Test Case's ID of TestRail (only an integer) > **Save**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-LINK.png" width="" height="">

## Add test results to TestRail

Before executing a **Test Suite** containing the Katalon Studio test cases mapped with TestRail ones, you can prepend the test suite's name to newly create a new Test Run or update an existing Test Run in TestRail.

### Create new test runs in TestRail

#### In TestRail

To generate a new Test Run of a Test Suite in TestRail, you need the test suite's ID. For example, Test Suite no.4 of Project no.4 we have specified in the configuration.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/TR-VIEW-TC.png" width="" height="">

#### In Katalon Studio

1. Create a new Test Suite or a [Dynamic Test Suite](https://docs.katalon.com/katalon-studio/docs/testrail-integration.html#query-test-cases-linked-to-testrail-in-dynamic-test-suite).

2. Prepend the Test Suite's name with `S<ID>` where `<ID>` is the ID of that test suite in TestRail.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-S4.png" width="498" height="256">

3. Execute the Test Suite. A new Test Run (e.g. **R2**) will be created in the respective Test Suite.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/TR-SEND-RESULTS.png" width="" height="">

    Click the test run to view its details:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/TR-NEW.png" width="" height="">

### Overwrite test runs in TestRail

#### In Katalon Studio

1. Create a new Test Suite or a [Dynamic Test Suite](https://docs.katalon.com/katalon-studio/docs/testrail-integration.html#query-test-cases-linked-to-testrail-in-dynamic-test-suite).

2. Prepend its name with `R<ID>` where `<ID>` is the ID of that test run in TestRail. (e.g., **R2** was newly created after execution in Katalon Studio)

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-R2.png" width="498" height="255">

    > To view the Test Run's ID, open **Dashboard** in TestRail > Select **Test Runs** under your preferred project > select a test suite > you can view the test run's ID on the top left corner.

3. Execute the test suite. In the example, the **R2** Test Run is updated with new test results.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/TR-OVERWRITE.png" width="" height="">

## Query Test Cases linked to TestRail in Dynamic Test Suite

> Learn more about [Dynamic Test Suite](https://docs.katalon.com/katalon-studio/docs/dynamic-test-suite.html).

When TestRail Integration plugin is enabled, Query Provider in Dynamic Test Suite is also enabled with TestRail syntax standard, which means you can re-execute those test cases that have already mapped with TestRail before.

### In Katalon Studio

1. Create a new dynamic test suite: Right-click on Test Suite in Test Explorer > New > Dynamic Test Suite.

2. Prepend the dynamic test suite's name with either `R<ID>` (for overwriting an existing test run) or `S<ID>` (for generating a new test run in this suite).

3. Enter the TestRail Test Run's ID in the Query box > Click **Preview** > Display all Katalon Studio test cases that have been mapped with the TestRail test cases of that test run.

    For example, to query the test cases that have been executed in Test Run R2.
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/QUERY-R2.png" width="" height="">

4. Execute the dynamic test suite.

    Prepend **S4** to the test suite's name, then execute the dynamic test suite, a new test run named **S4 DYNAMIC TS** is sent to TestRail, click it to view details.
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/NEW-S4.png" width="" height="">

    A new test run **R3** is created in TestRail.
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/NEW-R3.png" width="" height="">

    You can also overwrite the above test run by creating a new dynamic test suite > changing its name to **R3 DYNAMIC TS** > querying **R3** > executing the suite. 
    
    In TestRail, when the execution is done, new results replace the previous ones. Click **Activity** of that test run in TestRail to see its history:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/VIEW-ACTIVITY.png" width="" height="">
