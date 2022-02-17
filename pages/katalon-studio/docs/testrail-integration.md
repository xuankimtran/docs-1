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
* In TestRail, you can view Test Results of Test Suites executed in Katalon Studio.
* In Katalon Studio, you can query Test Runs of TestRail in Dynamic Test Suite. See: [Dynamic Test Suite](https://docs.katalon.com/katalon-studio/docs/dynamic-test-suite-ks.html#create-a-dynamic-test-suite).

> **Notes**:
>
> The **TestRail Integration** plugin only supports integrating Katalon Studio with TestRail Cloud.

> **Requirements**:
>
> * An active Katalon Studio Enterprise license.
> * The **TestRail Integration** plugin installed. You can find the plugin here: [TestRail Integration plugin](https://store.katalon.com/product/13/TestRail-Integration).

## Configure TestRail Integration

To enable the integration of Katalon Studio with TestRail, you need to configure both your TestRail site and Katalon Studio.

### In TestRail

Enable the TestRail API. Log in to your account, go to **Administration > Site Settings > API**, and check the **Enable API** option. Then click **Save Settings**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/TR-ENABLE-API.png" width=70% alt="Test Rail Site Settings page">

### In Katalon Studio

1. Enable the **TestRail Integration** plugin. In the main menu, go to **Project > Settings > Plugins > TestRail** and check the **Using TestRail** option.

2. Enter the credentials required for **Authentication**:

* **URL**: your TestRail instance `https://<example>.testrail.io`.
* **Username**: your TestRail Username.
* **Password**: your TestRail password.
* **Project**: your TestRail project ID (an integer).

    > To get the **project ID**, open your TestRail project in the browser and view the ID at the end of the URL, e.g. `https://company.testrail.io/index.php?/projects/overview/1`.

3. To test the connection, click on the **Test Connection** button.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-TESTRAIL-Enable-testrail.png" width=70% alt="KS Project Settings dialog">

4. Click **Apply and Close**.

## Map Test Cases between Katalon Studio and TestRail

To map a Test Case between Katalon Studio and TestRail, you need to get the Test Case ID.

### In TestRail 

To view the Test Case ID, open your project in TestRail, then go to the **Test Cases** tab:

Here you can see the list of Test Cases and their IDs.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-TestRail-Test-Case-list.png" width=70% alt="TestRail List of Test Cases">

### In Katalon Studio

Open the Test Case you want to map, switch to the **Integration** tab, and specify the respective Test Case ID in TestRail (only the integer part).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-TestRail-Integration-tab.png" width=70% alt="KS Test Case Integration tab">

## Upload Test Execution Results from Katalon Studio to TestRail

When uploading the execution results of a **Test Suite** to TestRail as a Test Run, you can create a new Test Run or update an existing Test Run in TestRail.

### Create a new Test Run in TestRail

Follow these steps:

1. In Katalon Studio, create a new Test Suite or a Dynamic Test Suite.

2. Prepend the name of the Test Suite with the text `S<ID>`, where `<ID>` is the Test Suite ID of your choice.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-New-Test-Suite.png" width=70% alt="New Test Suite">

3. Add the mapped Test Cases to the Test Suite.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-Add-mapped-Test-Cases.png" width=70% alt="Test Suite add mapped Test Cases">

3. Execute the Test Suite.

    A new Test Run is created in your TestRail project.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-TestRail-Test-Run.png" width=70% alt="TestRail uploaded Test Run">

    To view the Test Run details, click on the Test Run.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-TestRail-Test-Run-details.png" width=70% alt="TestRail Test Run results">

### Update an existing Test Run in TestRail

Follow these steps:

1. In Katalon Studio, create a new Test Suite or a Dynamic Test Suite.

2. Prepend the name of the Test Suite with the text `R<ID>`, where `<ID>` is the **Test Run ID** in TestRail.

    > To view the **Test Run ID**, open your TestRail project and click on the Test Run. The ID is displayed next to the Test Run name.

    For example, `R8` is the ID of the created Test Run.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-TestRail-Test-Run-ID.png" width=70% alt="TestRail Test Run ID">

    We prepend the Test Suite with the text `R8` as follows:

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-New-Test-Suite-update.png" width=70% alt="TestRail New Test Suite">

3. Add the mapped Test Cases to the Test Suite.

3. Execute the Test Suite.

    In our example, after we execute the Test Suite, the **R8** Test Run is updated with new test results.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-TestRail-Test-Result-Updated.png" width=70% alt="TestRail updated Test Result">

## Query Test Cases linked to TestRail in Dynamic Test Suite

When the TestRail Integration plugin is enabled, the Query Provider in Dynamic Test Suite is updated with the TestRail query syntax standard. This allows you to execute a Dynamic Test Suite using the TestRail query syntax.

> To learn more about query syntax in Dynamic Test Suite, you can refer to this guide: [Dynamic Test Suite](https://docs.katalon.com/katalon-studio/docs/create-test-suite.html#dynamic-test-suite-dynamic-test-cases-list).

Follow these steps:

1. In Katalon Studio, create a new Dynamic Test Suite.

2. Prepend the name of the Dynamic Test Suite with either `S<ID>` (for generating a new test Run) or `R<ID>` (for updating an existing Test Run).

3. In the **Query** text box, enter the ID of a Test Run, then click on the **Preview** button. 

    The Test Cases associated with the Test Run are displayed.

    For example, we query the Test Cases associated with the Test Run **R8**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-Dynamic-Test-Suite.png" width=70% alt="Dynamic Test Suite query">

4. Execute the Dynamic Test Suite and verify the uploaded Test Run.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/testrail-integration/KS-Dynamic-Test-Suite-Test-Run.png" width=70% alt="TestRail uploaded Dynamic Test Suite Run">