---
title: "Schedule a Test Plan"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-scheduler.html 
description: 
---

To schedule a test or view a list of scheduled test, log into Katalon TestOps > go to your project > select **TestOps CI** > select **Plan**.

You can plan and execute your tests using Local Agents or other test environments such as EKS or CircleCI. In this tutorial, we use CircleCI test enviroment as an example.

After you have [created a test plan](https://docs.katalon.com/katalon-analytics/docs/create-plan.html), you can schedule and execute anytime you want.

1. On the **Plan** view, select a test plan by clicking its name.
2. Select **Schedule** on the top right corner.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/schedule.png" width="" height="">

3. In the **Schedule** view, enter the required details:

   * **Name**: It's recommended to give a name that has a meaning.
   * **From-To**: The period in which the scheduled jobs start.
   * **Interval** and **Interval Unit**: Every <_Interval_> <_Interval Unit_>, a scheduled test is executed.
     For example: With Interval=3, and Interval Unit=Day, a test is executed every 3 days.
   * **Active**: You can change the status of the Schedule with this switch.
   

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/schedule-plan.png" width="" height="">

4. Click **Create** to create a schedule.


Your test plan is now ready to be executed at your preferred time. The scheduled test that is being executed will be displayed on the **Jobs** table.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/jobs.png" width="" height="">