---
title: "Visual Testing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/ks_visual_testing.html 
redirect_from:

Description: 

Katalon TestOps Visual Testing is a feature to help us compare screenshots between executions.

---

Katalon TestOps Visual Testing is a feature to help us compare screenshots of executions.

On Katalon Studio, go to **Menu Project** > **Settings**. The board **Project Settings** displays, click **Katalon TestOps** on the left sidebar. We choose **Team** and **Project**, then click **Apply and Close**. And now, we integrate the current Katalon Studio project with Katalon TestOps.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/ks_project_setting_kt.png)

Before testing a Test Suite (or Test Suite Collection) on Katalon Studio, we need to run this Test Suite (or execute Test Suite Collection). If we do not have a Test Suite, we can download the [sample code](https://github.com/katalon-studio-samples/visual-testing-sample) to test this feature. Or we can create a Test Case and Test Suite with [this page](https://www.timeanddate.com/worldclock/), because the time usually changes, and we can compare screenshots of executions easily.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/ks_test_case_sample_time.png)

We create a Test Suite with one Test Case.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/ks_test_suite_sample_time.png)

We insert a Web UI Keyword below the row in which we want to take a screenshot.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/ks_insert_web_ui_key.png)

In the new row, and we choose the Take Screenshot As Checkpoint.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/ks_choose_take_sreenshot_checkpoint.png)

In the row Take Screenshot As Checkpoint, column Input, we double click.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/ks_double_click_new_row.png)

An Input board displays, we assign a label for the new Item (Take Screenshot As Checkpoint) and click the button OK.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/ks_input_value_checkpoint.png)

We save the project and run Test Suite.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/ks_run_test_suite.png)

After running, Katalon Studio will upload the result to the Katalon TestOps. In Katalon TestOps, a new Test Run is created in the project which we have chosen in Project Settings. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/kt_test_run_visual_testing.png)

On Katalon TestOps, run Test Suite second time. After that, in Katalon TestOps, a new Test Run is created.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/kt_new_test_run.png)

On Katalon TestOps, sidebar **Reports & Analytics** > **Visual Testing**, we click the ID of the second Test Run.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/kt_visual_testing_click_id.png)

Choose the tab Checkpoints, click on the checkpoint.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/kt_visual_testing_checkpoint.png)

The board **sample visual testing** displays a Baseline image and a Checkpoint image.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/kt_visual_testing_chekpoint_baseline.png)

In the board Visual, click the button Hide diff (Show diff) to hide (show) all the differences. 

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/kt_visual_testing_hide_diff.png)

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/kt_show_diff_visual_testing.png)

If we want to change the Baseline, choose the icon Check on the top right corner board **sample visual testing** and exit.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/kt_check_new_baseline.png)

We choose the tab **Results** and click the button **Save to baseline**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/ks_visual_testing/kt_click_new_baseline.png)

And now, Katalon TestOps will compare the new baseline with the screenshot of the new Test Run.