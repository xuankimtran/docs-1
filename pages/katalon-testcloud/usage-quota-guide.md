---
title: "Usage Quota"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-testcloud/docs/usage-quota-guide.html
description: Introduces quotas in Katalon TestCloud
---

This article introduces you to the key metrics and usage quotas in Katalon TestCloud.

## Key metrics

Katalon TestCloud has three key metrics:

* **Number of sessions**: The maximum number of parallel test sessions.
* **Testing minutes**: The remaining time, calculated in minutes, to execute tests. Testing minutes are counted from the start to the end of a test session (including the delay time).
* **Expiry date**: The determined date when your TestCloud plan ends.

## Exceeding quota limits

### Session quota

If the number of parallel test requests exceeds the supported quota, TestCloud will have the following behaviors:

* If you request more parallel tests than the supported quota, the additional requests will be queued.
* The number of queued requests can not exceed three times the supported session quota. For example, if your TestCloud plan supports 5 parallel tests, the maximum number of queued requests is 15.
* A request remains in the queue for only 15 minutes; after 15 minutes, the request is dropped from the queue.

### Testing minute quota

During a test session, if the remaining testing minutes are insufficient to complete the session but are still above zero:

* The test will still be executed until the end.  

* The testing minutes exceeding the purchased quota will not be charged.

* After the number of testing minutes reaches zero, no new test execution is allowed until a new purchase is made.