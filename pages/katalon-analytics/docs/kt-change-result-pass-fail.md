---
title: "Override Test Results status" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-change-result-pass-fail.html
description: 
---

You can edit the status of a test result in Katalon TestOps and provide a reason for such change to notify your team.
You can also see the whole history of status changes.

This feature allows you to:

* update manually the status of a test result to accomodate the actual expectations.

* keep a clear record of why a test result has been changed, who changed it, and the reason for such change.

* find out whether the status of a test result has been manually modified and what was its initial status.

## Change the status of a Test Result

> Notice:
>
> Changing the status of a Test Result affects the status of a Test Run and its Test Suite. You should override Test Results statuses with caution.
>
> See [TestOps Formulas](https://docs.katalon.com/katalon-analytics/docs/testops-terminology.html#testops-formulas) for definitions of **Status (Test Run)** and **Status (Test Suite)**.

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

2. Go to **Reports & Analytics**.

    The **Test Runs** page appears.
    
3. Click on a Test Run ID, then select the **Test Results** tab.

    You can see the list of all test results and their details (Status, ID, Name, Time, Assertions, Links) here.

4. Click on the *Extension* icon of the Test Result you want to change.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-nov-release-override-test-result/extention-icon-highlight.png" width=100% alt="test result extension icon">

5. Click **Mark as Passed** (for a **failed**/**incomplete**/**error** Test Result) or **Mark as Failed** (for a **passed** Test Result).

    > Notes:
    >
    > * See [TestOps Formulas](https://docs.katalon.com/katalon-analytics/docs/testops-terminology.html#testops-formulas) for definitions of **Status (Test Result)**.

    A box pops up asking you to choose a reason for the status change.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-nov-release-override-test-result/change-test-result-status-popup.png" width=100% alt="change status popup">
    
6. Select an option, then submit the new status for this Test Result.

## View status change details of a Test Result

You can see the detailed information and description of a status change once the status has been modified.

Select the **Test Results** tab, click on a Test Result ID, then select the **Comments** tab.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-nov-release-override-test-result/Description.png" width=100% alt="test result comments tab">

You then can check the following information:

* the member's name who changed the status of a Test Result.
* the history of a Test Result's status changes. 
* the reason for each status change.

## View the summary of a Test Result

No matter how many times a test result has been modified, you can check a full record of the modification.

Follow these steps:

1. Select the **Test Results** tab.

2. Mouse over the *Information* icon next to the Test Result status, then click **View changes log**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-nov-release-override-test-result/View%20key%20information.png"  width=100% alt="view changes log">

Now you can view the following information:

* the original status of a Test Result.
* the latest status of that Test Result.
* further detailed changes of that Test Result.
