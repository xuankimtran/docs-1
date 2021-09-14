---
title: "View Test Usage and Balance in the Usage Dashboard" 
sidebar: katalon_studio_docs_sidebar
permalink: /katalon-analytics/docs/test-usage-balance-usage-dashboard.html
redirect from:
description:
---

Organizations in Katalon TestOps are limited in how many tests can be run monthly, defined as your monthly *quota*. This quota is defined by the license plan of your TestOps Organization. You can view the current test execution quota, usage, and remaining balance in the **Usage Dashboard**.

> Requirements:
>
> * Katalon TestOps subscription.
> * Owner, Admin, or Billing Manager role in an Organization.
> Notes:
>
> Find out more about the licensing model and test execution quota here: [TestOps Subscriptions Overview](https://docs.katalon.com/katalon-analytics/docs/testops_subscriptions_overview.html).
## Navigate to the Usage Dashboard

To navigate to the **Usage Dashboard**, follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/).

2. Click on the **Organization** scroll-down menu in the top left corner, then select your Organization.

3. Click on the *Settings* button in the top right corner. Select **License Management > Dashboard**. The **Usage Dashboard** page appears.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/test-usage-balance/dashboard.png" alt="dashboard" width=100%>

The page contains two panels: **Test Executions** and **Test Activities**.

You can export your Usage Report as a .csv file by clicking the **Export** button in the top right corner.

## Test Executions Panel

The **Test Executions** panel displays a test executions counter and your monthly quota. To view your remaining balance, hover your cursor over the panel.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/test-usage-balance/test-execution.png" alt="test execution" width=70%>

> Notes:
>
> * When you reach the monthly quota, you cannot run test on TestOps, but you can still upload the test results to TestOps.
> * For the first 3 months of any billing plan, including the free plan, you can fill 130% of your maximum quota at no extra cost.
> * Your test executions counter are reset every month, starting from the first day of your free plan or your purchased date.
> * Upgrading your subscription renews your balance and sets the new date as the first day of the first month of your new billing plan.
## Test Activities Panel

The **Test Activities** panel displays your weekly testing activity as a bar chart. Data includes tests run on Katalon TestOps as well as uploaded test results.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/test-usage-balance/test-activities.png" alt="test activates" width=70%>

Two numbers are displayed on the right side of the bar chart:

* **Test Executions** represents the total number of tests executed the preceding week.

* **Test Duration** represents the total time spent executing tests the preceding week.

Learn more about uploading test results to TestOps: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

See also:
[Upgrade TestOps Subscription](https://docs.katalon.com/katalon-analytics/docs/upgrade-subscriptions.html#add-more-test-results).