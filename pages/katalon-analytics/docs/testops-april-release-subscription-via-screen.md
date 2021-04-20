---
title: "TestOps Subscription via Subscription Screen"
sidebar: katalon_analytics_docs_sidebar
permalink: katalon-analytics/docs/testops-subscription-via-screen.html 
description: 
---
## TestOps Subscription via Subscription Screen

Start the following steps to subscribe:
1. Log in to Katalon TestOps
2. Select an organization
3. Go to the Subscriptions view
4. Choose **Plan** and click **Check Out**

Once subscribing, continue to:
* Navigate to **Katalon TestOps Plan** screen that displays your specified orders earlier

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-april-release-subscription/subscription-1.png" width=70%>

* Click **Check Out** to review the order.
* Fill in **Billing information**. You must fill all required fields.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-april-release-subscription/subscription-2.png" width=70%>

If payment is successful, the screen displays as follow: 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-april-release-subscription/subscription-3.png" width=70%>

Continue the following steps:
* Send a request to Recurly to create a new subscription immediately
* Send a request to Stripe to create a new invoice.


If payment fails, it could be the following reasons:
* Invalid card. "Invalid card number” error displays and restricts checking out
* Other reasons. Errors from Stripe display and restrict checking out

If the card validation process has passed but the system fails in charging the card, start [dunning process](https://docs.recurly.com/docs/dunning-management).
* If successful, continue the subscription
* If failed, terminate the subscription
