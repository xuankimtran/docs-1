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
* **Testing minutes**: The available time, calculated in minutes, to execute tests. Spent testing minutes are counted from the start to the end of a test session (including the delays set after each test execution, if any).
* **Expiry date**: The determined date when your TestCloud plan ends.

## Usage quota

Katalon TestCloud (trial period) offers the **free trial** package, with the following quota:

<table>
    <thead>
        <tr>
            <th><b>Category</b></th>
            <th><b>Limit</b></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Expiry date</td>
            <td>23∶59 PM April 5, 2022 EST.</td>
        </tr>
        <tr>
            <td>Number of parallel tests</td>
            <td>5.</td>
        </tr>
        <tr>
            <td>Number of testing minutes</td>
            <td>500 minutes.</td>
        </tr>
        <tr>
            <td>Supported OS</td>
            <td>Windows and Linux.</td>
        </tr>
        <tr>
            <td>Supported browsers</td>
            <td>Chrome, Firefox, and Edge.</td>
        </tr>
    </tbody>
</table>

If you exceed the supported quota, the following behaviors apply:
### Session quota

If the number of parallel test requests exceeds the supported quota, the additional requests will be queued.

The number of queued requests cannot exceed the session quota by more than 3 times. For example, if the quota is 5 parallel tests, the maximum number of queued requests is 15.

A request remains in the queue for only 15 minutes; after 15 minutes, the request is dropped from the queue.

### Testing minute quota

During a test session, if the remaining testing minutes are insufficient to complete the session but are still above zero, the test will still be executed until the end.

Once the number of testing minutes has reached zero, no new test execution is allowed.

> **Notes**:
>
> If you want to renew your quota, contact us at success@katalon.com for quota options.

## Track TestCloud quota

You can track your TestCloud quota on the TestOps **License Management** page.

Follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your project.

2. Go to **Settings** > **License Management**.

    The **License Management** page appears.

3. Click on the **Katalon TestCloud** tab.

<a class="pop">
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-testcloud/usage-quota/TC-Track-quota.png" width=100% alt="License Management Katalon TestCloud tab">
</a>

<p style="text-align: center;"><em>Click the image to enlarge</em></p>

You can then check the following information:

* the number of parallel tests.
* the testing time.