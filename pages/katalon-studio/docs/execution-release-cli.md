---
title: "Link an execution with TestOps Release using CommandLine" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/execution-release-cli.html 
redirect_from:
description: 
---
## Prerequisites

You have already configured TestOps integration. [Learn more](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html)

## Create a new Release in Katalon TestOps

In Katalon TestOps, [create a new Release](https://docs.katalon.com/katalon-analytics/docs/kt-jira-release.html) or use an existing Release.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-release-cli/new-release.png)


## Select a TestOps Release to generate command

In **Katalon Studio**, open the **Command Generator** and select a Test Suite that you want to execute in CLI.

In the **Katalon TestOps** section, select a **TestOps Release** that you want to link your execution with after running the test suite.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-release-cli/generate-command.png)

> Note: If you have not created any Releases in TestOps, it will be set as **Default Release**.

After finishing the above steps, click on **Generate Command** and copy it to the command line.

## View linked execution and release in Katalon TestOps

After executing your test suite with CLI, go to [Katalon TestOps](https://analytics.katalon.com) to view your test results.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-release-cli/linked-release.png)

Your execution is now mapped with the chosen Release as below.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-release-cli/linked-execution.png)
