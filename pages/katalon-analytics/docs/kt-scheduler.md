---
title: "Schedule a Test Run"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-scheduler.html 
description: 
---
## Prerequisites

- Have a Test Environment configured. [Learn more](https://docs.katalon.com/katalon-analytics/docs/agents.html)
- Have a Script Repository set up in Katalon TestOps. [Learn more](https://docs.katalon.com/katalon-analytics/docs/code-repo.html)

## Schedule a Test Run

You can schedule other Test Runs by clicking on *"Schedule Test Run"* button.

Follow the instruction in the setup wizard and click *"Create"* to finish creating a new schedule for your Test Run.

After creating schedules, scheduled Test Runs can be found in **Test Planning**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/test-run-calendar.png" width="" height="">

Click on each Test Run in the calendar to view summary.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/test-run-details.png" width="" height="">

## View a Test Run Type

After scheduling a Test Run, you can view details from *"Test Run Types"* section in **Test Planning**. Test Run Type is a collection of Test Runs having the same configurations. This sectiion allows you an ability to view the list of Test Run with similar configurations (Test Environment, Trigger, Script Repository).

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/kt-scheduler/test-run-type.png" width="" height="">

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

## Related topics

- [Set up a Local Environment](https://docs.katalon.com/katalon-analytics/docs/agents.html)
- [Set up a Script Repository](https://docs.katalon.com/katalon-analytics/docs/code-repo.html)
- [Katalon TestOps Terminology](https://docs.katalon.com/katalon-analytics/docs/testops-terminology.html#trigger)