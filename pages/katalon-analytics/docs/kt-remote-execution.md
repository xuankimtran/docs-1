---
title: "TestOps CI Overview" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/kt-remote-execution.html 
description: 
---
**TestOps CI** is an application in Katalon TestOps cloud (beta). You can maximize the capacity of local servers and speed up the testing process by executing automation tests remotely. 

## Overview

TestOps CI contains four main sections:

- **Agent Setup**: where you can create and download an agent configuration file used to start a local agent. [Learn more](https://docs.katalon.com/katalon-analytics/docs/agents.html#download-an-agent-configuration-file-in-testops)

- **Test Environments**: contains the list of current agents (Local Hosts) and other test enviroments (CircleCI and AWS EKS).

- **Code Repo**: stores test projects that need to be executed remotely.

- **Plan**: where you can [create a new plan](https://docs.katalon.com/katalon-analytics/docs/kt-scheduler.html) and [execute scheduled plan](https://docs.katalon.com/katalon-analytics/docs/grid-local-agents.html).

## Execute Tests Remotely with TestOps CI

### Step 1: Create a test environment

TestOps CI allows you to set up your test environment to schedule and execute tests remotely.

First, you need to create an agent or configure a test environment from CircleCI or EKS to get started.

- [Create and start an agent](https://docs.katalon.com/katalon-analytics/docs/agents.html)

- [Create a CircleCI test environment](https://docs.katalon.com/katalon-analytics/docs/circleci.html)

You can view agent status or a list of other test environments you have created in **Test Environments** section.

### Step 2: Upload Test Projects to Code Repo

After having the test environment, go to **Code Repo** and upload your test projects which need to be executed remotely.

- [Upload Test Projects](https://docs.katalon.com/katalon-analytics/docs/code-repo.html)

- [Create Git Test Projects](https://docs.katalon.com/katalon-analytics/docs/git-test-project.html)

### Step 3: Schedule a remote execution plan

After having an agent or test environment and a test projects created in **Code Repo**, you can schedule a test in **Plan** section.

- [Create a new test plan](https://docs.katalon.com/katalon-analytics/docs/kt-scheduler.html#plan-a-test)

- [Schedule a plan](https://docs.katalon.com/katalon-analytics/docs/kt-scheduler.html#schedule-a-test-plan)

### Step 4: Execute scheduled test

Now you can [execute your test plans](https://docs.katalon.com/katalon-analytics/docs/grid-local-agents.html) anytime you want in parallel or on schedule.



