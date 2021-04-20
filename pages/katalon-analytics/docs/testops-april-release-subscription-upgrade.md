---
title: "Upgrade TestOps Subscriptions"
sidebar: katalon_analytics_docs_sidebar
permalink: katalon-analytics/docs/upgrade-testops-subscription.html 
description: 
---
## Upgrade TestOps Subscriptions

If you want to increase the number of test runs or switch from monthly to yearly billing cycles, you can upgrade your subscriptions at any time. 

To upgrade your subscription, follow these steps:
1. Go to Subscriptions screen

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-april-release-upgrade/upgrade-1.png" width=70%>

* The screen displays the current subscription and TestOps plans as above
* You can only subscribe to one plan at a time 
2. Click **Upgrade** on the current plan
3. Adjust the number of test runs and review the new plan
4. Follow steps on [Create subscriptions](subscriptionlinktobeprovided)

After completing the payment process, continue the following steps:
1. Call API to update your plan in Recurly to the same OrgID
2. Send an invoice with a prorated charge for the [new plan](https://docs.recurly.com/docs/change-subscription)
3. Maintain the current billing period and current subscription term, follow the standard proration rules
4. Log subscription upgrade activities

### Upgrade to Annual billing cycle
A yearly billing cycle helps you save costs. You can only upgrade monthly subscriptions to annual ones.

Successful payment will immediately change your subscription. After upgrading, you can find new subscription information updated on the **Subscription Plan** page.
