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

* find out whether the status of a test result has been manually modified, knowing who modified it and what was its initial status.

## Change the status of a Test Result

> Notice:
>
> Changing the status of a Test Result affects the status of a Test Run and its Test Suite. You should override Test Results status with caution.

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.

2. Go to **Reports & Analytics**.

    The **Test Runs** page appears.
    
3. Click on a Test Run ID, then select the **Test Results** tab.

    You can see all test results and their details (Status, ID, Name, Time, Assertions, Links) here.

4. Click on the *Extension* icon of the Test Result you want to change its status.

5. Click **Mark as Passed** (for a **failed**/**incomplete**/**error** Test Result) or **Mark as Failed** (for a **passed** Test Result).

    > Notes:
    >
    > * See [TestOps Formulas](https://docs.katalon.com/katalon-analytics/docs/testops-terminology.html#testops-formulas) for definitions of **Status (Test Result)**.

    A box pops up asking you to choose a reason for the status change.

6. Select an option, then submit the new status for this Test Result.

## View change details of a Test Result

You can see the detailed information and description of a status change once the status has been modified. 

Select the **Test Results** tab, then click on the **Comments** tab. 
You can check the following information:

* the member's name who changed the status of a Test Result.
* the history of a Test Result's status changes. 
* the reason for each status change.

## View the summary of a Test Result

No matter how many times a test result has been modified, you can check a full record of the modification.

Follow these steps:

1. Select the **Test Results** tab, then click on the **Summary** tab. 

2. Mouse over the *Information* icon, then click **View changes log**.

    You can view the following information:

    * the original status of a Test Result.
    * the latest status of that Test Result.
    * further detailed changes of that Test Result.
    
On Katalon TestOps, if we are team owners or admins, we can change a failed Test Result of a Test Run to a passed Test Result. 

We choose **Reports & Analytics** > **Test Runs**. Then we click to select an ID of the Test Run that we want to execute.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-change-result-pass-fail/kt_choose_test_run.png)

The Summary of Test Run displays, click and choose **Mark as Passed** at the Test Result, which we want to change from failed status to passed status.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-change-result-pass-fail/kt_id_mark_pass.png)

On the board **Change status** display, click **Yes** to accept.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-change-result-pass-fail/kt_change_status.png)

The board **Test Results** displays, and we can see the test result with passed status.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-change-result-pass-fail/kt_test_results_change.png)

We click test result, which we have changed from failed status to passed status, and the board **Test Result:** displays. We click on the **Comments** tab.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-change-result-pass-fail/kt_test_result_should_failed.png)

And now, we can see the comments about changing the status.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-change-result-pass-fail/kt_comment_result_pass_fail.png)

We can change a passed Test Results to failed Test Results with similar steps.
