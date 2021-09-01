---
title: "License Utilization Dashboard"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license-utilization-dashboard.html
description:
---

As an organization owner or administrator, the **License Utilization Dashboard** allows you to track the use of Katalon Studio Enterprise and Katalon Runtime Engine licenses to help maximize the license allocations and productivity of your team.

## License Usage Visualization

> **Requirements**:
>
> * Owner or Admin in an Organization.

In [Katalon TestOps](https://testops.katalon.io/), select an Organization. Go to **Settings > License Management > License Utilization**.

The dashboard contains a dynamic visualization with filter options.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-utilization-dashboard/license%20utilization%20page.png" alt="license utilization" width=100%>

### The Filter Bar

1. **Time range**:

    On the top right, you can see the specific date range, for example: Aug 2020 - Jul 2021.

    > **Notes**:
    >
    > The date range filter is not supported at the moment. The data you see is a fixed date range: 1 year ago from this month.

2. **User email, machine ID, and license types**:

    Use the filter to select the user email, machine ID, and license type you want to analyze. The statistics, graph, and the session table below display the session durations for each license type within the 1-year period.
    
    If you leave it blank by default, you will see the total duration used for all license types, machine IDs, and user emails, including the data of removed machine IDs and user emails.

    In each filter category, you can search and select multiple options. The removed machine IDs or user emails are excluded in the filter.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-utilization-dashboard/search-filter.png" alt="search option" width=70%>

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-utilization-dashboard/multiple.png" alt="multiple options" width=70%>

    After choosing your filter options, the dynamic graph below changes accordingly.

### License Usage

In the **License Usage** section, you can see the statistics summary and the graph.

There are two modes for view. Clicking on the button above the graph switches between the modes:

* **The linear mode** shows the stats in number and the graph in a line chart.
* **The stacked mode** shows the stats in percentage and the graph in a bar chart.

**Statistics summary**:

The statistics summary above the chart represents the total duration of testing for each license type within the time range.

**The graph**:

The graph visualizes the duration of each license type for each month. Observing this diagram helps you find out a trend in the time each user in your team use for each license.

**The linear mode**:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-utilization-dashboard/linear-example.png" alt="linear" width=100%>

**The stacked mode**:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-utilization-dashboard/stacked%20mode.png" alt="stacked" width=100%>

To see the detailed information, hover to the stats bar or the graph. The detailed box appears.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-utilization-dashboard/hover-statistic.png" alt="hover to stats" width=100%>

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-utilization-dashboard/hover-graph.png" alt="hover to graph" width=100%>

### Session Table

Below the graph section, you can view the detailed list of sessions completed by your team members.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-utilization-dashboard/detail%20session.png" alt="sessions" width=100%>

If you leave the filter blank by default, you can still find the removed user emails or machine IDs session in the session table.