---
title: "License Utilization Dashboard"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license-utilization-dashboard.html
description:
---
> **Known Issue**:
>
> * The search bar and user filters are not available at the moment.
> * The date range provided supports 1-year range only.
> * Currently not support reports exported in CSV file.

As an organization owner or an organization administrator, you might want to keep track of your license utilization to manage the productivity usage of your team with Katalon Studio Enterprise and Katalon Runtime Engine licenses. Keeping track of the time each machine ID use helps you maximize your license subscription, enhancing the team work efficiency and even saving your company some money.

For an organization owner or an organization administrator to get the insights on the license assignments, sessions, duration in a glance, we introduce you to the **License utilization dashboard**.

## Visualized License Utilization Report

In [Katalon TestOps](link), go to the **License Utilization Dashboard**.
In the dashboard, you can see a filter and a diagram.

There are two main things this dashboard provides: the filter bar and the displayed graph.

<ADD THE SCREENSHOT>

### The Filter Bar

1. **Time range**:

On the top right, you can see the specific date range, for example: Aug 2020 - Jul 2021.

> **Notes**:
>
> The date range filter is not supported at the moment. The data you see is the Count the data of a fixed date range: 1 year ago from this month.

2. **Email and machine ID**:

Use the filter to select the email or machine ID you want to analyze. If you leave it blank, you will see the total time used for all machine IDs and emails.

You can select multiple emails or machine IDs. The removed machine IDs or emails are excluded in this filter.

3. **License types**:

To view the time used for each license, you can filter the license type of:

* KRE Node-locked
* KRE Floating
* KSE Node-locked
* KSE Floating

Once you filtered it, the total number and the diagram you want to see appear.

You can find the time used in each license type and the total amount of it.

There are two modes for view: Linear and stacked. You can switch between these two.

<LINEAR AND STACKED SCREENSHOT>

## Display Graph

The graph below shows the testing duration in hours for each month. Observing this diagram helps you find out a trend in the time each user in your team use for each license. For example, when your team reaches the peak in the graph, how many licenses are utilized during peak durations. With this information, you can decide on an upgrade in your subscription accordingly.

<ADD GRAPH SCREENSHOT>