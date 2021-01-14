---
title: "Execute Test Runs by a Trigger"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-scheduler.html 
description: 
---
## Prerequisites

- You have scheduled your Test Runs. [Learn more](katalon-analytics/docs/create-plan.html)

## Create a Trigger

Trigger is used to determine when a Test Run is executed. This helps you leverage remote execute to take fully control of your testing plan.

To create a Trigger, select a Test Run Type to access its details page > Click on *"Create Trigger"*.


<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/create-trigger-details.png" width="" height="">

In the *"Create Trigger"* view, enter the required details:

   * *Name*: It's recommended to give a name that has a meaning.
   * *From-To*: The period in which the scheduled jobs start.
   * *Interval* and *Interval Unit*: Every <_Interval_> <_Interval Unit_>, a scheduled test is executed.
     For example: With Interval=3, and Interval Unit=Day, a test is executed every 3 days.
   * *Active*: You can change the status of the Trigger with this switch.


<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/create-trigger.png" width="" height="">


Your Test Run is now ready to be executed at your preferred time. You can view a list of your Triggers in *"Configuration"* tab in *"Test Run Types"* section.


<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/view-triggers.png" width="" height="">

## View Test Run status

Your Test Runs will be automatically executed based on your configurations. 

Test Run status can be found in the calendar view in **Test Planning**. [Learn more](katalon-analytics/docs/create-plan.html#view-test-runs)

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/execute-test-runs/view-test-runs.png" width="" height="">

## Related topics

- [Set up Configurations for Remote Execution](/katalon-analytics/docs/test-run-config.html)
- [Execute a Test Run manually](/katalon-analytics/docs/execute-test-run.html)
- [Katalon TestOps Terminology](/https://docs.katalon.com/katalon-analytics/docs/testops-terminology.html#trigger)