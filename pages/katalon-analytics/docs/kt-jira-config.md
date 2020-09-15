---
title: "Jira Settings" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-jira-config.html 
---

## Introduction

Katalon TestOps provides seamless integration with Jira that brings several benefits for team collaboration. [Learn more](https://docs.katalon.com/katalon-analytics/docs/ka-integration-jira.html)

| Item        | Description                                                                                                                                                                                                                           | Representation                           |
|--------------|--------------|--------------|
| Releases     | You can populate Jira releases or create your own releases in TestOps. This helps you better manage the progress of your projects.                                                          | Releases in Jira <br> Releases in TestOps     |
| Requirements | You can link to Jira stories to see whether the requirements are already covered or yet uncovered by related Test Cases. This helps you better keep track of all requirements that have been made. | Stories in Jira <br> Test Cases in TestOps    |
| Defects      | You can map with failed test runs in TestOps with Jira bugs to track the performance of your executions.                                                                                       | Bugs in Jira <br> Failed Test Runs in TestOps |

## Prerequisites

* The [Jira App](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira) has been installed.

## Configuration in Jira

1. Navigate to **Katalon Settings** at the bottom of Project Settings.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jira-ka-configure/1-jira-ka-config.png)

2. Enter the email registered for your Katalon account.

3. Enter an **[API Key](https://docs.katalon.com/katalon-analytics/docs/ka-api-key.html)**.

4. Enter **[Organization ID](https://docs.katalon.com/katalon-analytics/docs/getting-started.html)**.

5. Click **Save**.

## Configuration in Katalon TestOps

1. Navigate to **Jira Settings** located in the toolbar of the project page.

2. Enter Jira URL, Username, and Password.

* Jira Cloud

    a. Jira URL must be in the form of _https://<site_name>.atlassian.net_.\
    b. Enter the email registered for your Jira Cloud account in *Username*.\
    c. Enter an Atlassian Cloud's API token in *Password*. See the instructions **[here](https://confluence.atlassian.com/cloud/api-tokens-938839638.html)**.

* Jira Server

    a. Jira URL must be in the form of _http(s)://domain_ without any trailing parts e.g., _/secure_.\
    b. Use your username instead of an email in *Username*.\
    c. Enter Password.

3. Click **Test Connection** to see if the connection is successful.

4. Click **Save**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/jira-ka-configure/2-jira-ka-config.JPG)

## Next Steps

- View testing progress in [Jira Release](https://docs.katalon.com/katalon-analytics/docs/kt-jira-release.html), [Jira Requirements](https://docs.katalon.com/katalon-analytics/docs/ka-integration-jira.html), [Jira Defects](https://docs.katalon.com/katalon-analytics/docs/ka-defects.html), [Jira Dashboard](https://docs.katalon.com/katalon-analytics/docs/jira-gadgets.html).
- [Writing BDD in Jira](https://docs.katalon.com/katalon-analytics/docs/bdd-settings.html).
- [Submit Test Results from Katalon Studio to Jira](https://docs.katalon.com/katalon-studio/docs/jira-integration.html).