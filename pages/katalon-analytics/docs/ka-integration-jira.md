---
title: "Integration with Jira" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/ka-integration-jira.html 
description: 
---
## Overview

Katalon TestOps provides seamless integration with Jira that brings several benefits for team collaboration, including:
- Quickly map Test Cases to Jira Requirements or Test Runs to Jira Defects.
- Easily view details of Jira issues on one click from Katalon TestOps.
- Map executions to Releases for better management.
- Easily see the Test Results for each release in Jira.

## Configure in Jira and TestOps

Please refer to [this document](https://docs.katalon.com/katalon-analytics/docs/kt-jira-config.html) for more details.

## Key features


| Item        | Description                                                                                                                                                                                                                           | Representation                           |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Releases     | You can populate Jira releases or create your own releases in TestOps. This helps you better manage the progress of your projects.                                                          | Releases in Jira <br> Releases in TestOps     |
| Requirements | You can link to Jira stories to see whether the requirements are already covered or yet uncovered by related Test Cases. This helps you better keep track of all requirements that have been made. | Stories in Jira <br> Test Cases in TestOps    |
| Defects      | You can map with failed test runs in TestOps with Jira bugs to track the performance of your executions.                                                                                       | Bugs in Jira <br> Failed Test Runs in TestOps |

### Working with Releases

You can [populate Jira issues](https://docs.katalon.com/katalon-analytics/docs/kt-jira-release.html) or [create a new release](https://docs.katalon.com/katalon-analytics/docs/release.html) and map executions to the release.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/release/release-list.png" width="" height="">

### Mapping Test Cases to Jira Requirements

In the **Test Cases** section, select a test case and enter the Jira issue you need to map with a Jira requirement.


<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ka-integration-jira/requirements-testops.png" width="" height="">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ka-integration-jira/linked-test-case.png" width="" height="">


### Mapping Test Runs to Jira Defects

To  map a test run to a Jira defect, go to **Executions** > Select a test run by clicking on its ID.

Enter the Jira issue you need to map with a test run in TestOps. The defect has been created after completing these steps.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ka-integration-jira/test-run-testops.png" width="" height="">

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ka-integration-jira/linked-test-run.png" width="" height="">

> **Quick tips**: You can Jira add-on to quickly map Test Runs to Jira Defects directly in Jira. [Learn more](https://docs.katalon.com/katalon-analytics/docs/kt-jira-issue.html)

You can view defects you have added to the execution in the **Defects** tab.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ka-integration-jira/defect-tab.png" width="" height="">

To view all defects, go to the **Defects** section in the navigation bar.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/ka-integration-jira/defect-menu.png" width="" height="">

