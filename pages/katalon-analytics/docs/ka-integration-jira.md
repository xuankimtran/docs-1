---
title: "Integration with Jira" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/ka-integration-jira.html 
description: 
---
## Overview

Katalon TestOps provides seamless integration with Jira that brings several benefits for team collaboration, including:
- Quickly attach Jira requirements to Test Cases or defects to Test Runs.
- Easily view details of Jira issues on one click from Katalon TestOps.
- Map executions to Releases for better management.
- Easily see the Test Results for each release in Jira.

## Configure in Jira and TestOps

Please refer to [this document](https://docs.katalon.com/katalon-analytics/docs/kt-jira-config.html) for more details.

## Key features

With the seamless integration between Jira and TestOps, you can 


| Item         | Description                                                                                                                                                                                                                           | Representation                           |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Releases     | A set of executions in your release plan. You can populate Jira releases or create your own releases in TestOps. This helps you better manage the progress of your projects.                                                          | Releases in Jira Releases in TestOps     |
| Requirements | A Test Case before being executed. You can link to Jira stories to see whether the requirements are already covered or yet uncovered by related Test Cases. This helps you better keep track of all requirements that have been made. | Stories in Jira Test Cases in TestOps    |
| Defects      | A failure after executing a Test Case. You can map with failed test runs in TestOps with Jira bugs to track the performance of your executions.                                                                                       | Bugs in Jira Failed Test Runs in TestOps |

### Releases

You can [populate Jira issues](https://docs.katalon.com/katalon-analytics/docs/kt-jira-release.html) or [create a new release](https://docs.katalon.com/katalon-analytics/docs/release.html) and map executions to the release.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/release-list.png" width="" height="">

### Requirements

In the **Test Cases** section, select a test case and enter the Jira issue you need to map with a Jira requirement.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ka-integration-jira/requirements-jira.png" width="" height="">


<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ka-integration-jira/requirements-testops.png" width="" height="">


### Defects

To map defects with test runs, go to **Executions** > Select a test run by clicking on its ID.

Enter the Jira issue you need to map with a test run in TestOps. The defect has been created after completing these steps.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ka-integration-jira/defects-jira.png" width="" height="">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ka-integration-jira/defects-testops.png" width="" height="">

> **Quick tips**: You can Jira add-on to quickly map Jira issues to Defects directly in Jira. [Learn more](https://docs.katalon.com/katalon-analytics/docs/kt-jira-issue.html)

Now you can view all defects you have added to TestOps in the **Defects** section.


<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ka-integration-jira/defect-tab.png" width="" height="">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ka-integration-jira/defect-menu.png" width="" height="">

