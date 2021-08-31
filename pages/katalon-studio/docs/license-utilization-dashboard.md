---
title: "License Utilization Dashboard"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/license-utilization-dashboard.html
description:
---
> **Known Issue**:
>
> * The search bar and user filters are not available at the moment.
> * The date range provided supports the 1-year range only.
> * Currently cannot export reports as **.csv** files.

As an organization owner or administrator, the **License Utilization Dashboard** allows you to track the use of Katalon Studio Enterprise and Katalon Runtime Engine licenses to help maximize the license allocations and productivity of your team.

## License Usage Visualization

> **Requirements**:
>
> * Owner or Admin in an Organization.

In [Katalon TestOps](https://testops.katalon.io/), select an Organization. Go to **Settings > Subscription Management > License Utilization**.

The dashboard contains a dynamic visualization with filter options.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-utilization-dashboard/license%20utilization.png" alt="license utilization" wwidth=100%>

### The Filter Bar

1. **Time range**:

    On the top right, you can see the specific date range, for example: Aug 2020 - Jul 2021.

    > **Notes**:
    >
    > The date range filter is not supported at the moment. The data you see is a fixed date range: 1 year ago from this month.

2. **User email and machine ID**:

    Use the filter to select the user email and machine ID you want to analyze. If you leave it blank, you will see the total time used for all machine IDs and user emails.

    You can select multiple user emails or machine IDs. The removed machine IDs or user emails are excluded in this filter.

3. **License types**:

    To view the time used for each license, you can filter the license type of:

    * KRE Node-locked
    * KRE Floating
    * KSE Node-locked
    * KSE Floating

### The Displayed Graph

The graph shows the testing duration in hours for each month. Observing this diagram helps you find out a trend in the time each user in your team use for each license. For example, when your team reaches the peak in the graph, how many licenses are utilized during peak durations. With this information, you can decide on an upgrade in your subscription accordingly.

There are two modes for view: linear and stacked. Clicking on the button above the graph switches between the modes.

After choosing your filter options, the graph appears. You can find the time used in each license type and the total amount of it.

**The linear mode**:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-utilization-dashboard/linear-mode.png" alt="linear" width=100%>

**The stacked mode**:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-utilization-dashboard/stacked%20mode.png" alt="stacked" width=100%>

You can also view the detailed session list right below the graph section.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/license-utilization-dashboard/detail%20session.png" alt="sessions" width=100%>