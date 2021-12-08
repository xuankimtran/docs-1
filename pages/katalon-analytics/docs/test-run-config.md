---
title: "Configure Remote Execution"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/test-run-config.html 
description: 
---

In Katalon TestOps, you can set up a Remote Execution to run tests in console mode.

Follow these steps:
1. Create a Test Environment.
2. Create a Script Repository.
3. Schedule Test Runs.

## Create a Test Environment

A Test Environment connects your machine with Katalon TestOps to activate a Remote Execution.

You can define which machine or machines execute the remote Test Runs by configuring a Test Environment in Katalon TestOps.

Katalon TestOps offers the following options:

* [Create a Local Test Environment with an Agent](https://docs.katalon.com/katalon-analytics/docs/agents.html).
* [Set up an Agent to execute tests in a Docker Environment](https://docs.katalon.com/katalon-analytics/docs/docker.html).
* [Create a Kubernetes Test Environment](https://docs.katalon.com/katalon-analytics/docs/aws-eks.html).
* [Create a CircleCI Test Environment](https://docs.katalon.com/katalon-analytics/docs/circleci.html).

Once you have created a Test Environment, you can upload tests to a Script Repository in Katalon TestOps for test planning.

## Set up a Script Repository

A Script Repository stores test scripts for test executions. You can manage your test scripts in Katalon TestOps and decide upon the execution schedule (test planning) and execution environment (the Test Environment you have created).

Katalon TestOps offers the following options:

* Create a Script Repository. See: [Upload Test Scripts to a Script Repository](https://docs.katalon.com/katalon-analytics/docs/code-repo.html).
* Create a Git Script Repository (GitHub and Bitbucket). See: [Upload Test Scripts from a Git Repository](https://docs.katalon.com/katalon-analytics/docs/git-test-project.html).

With a set-up Test Environment and Script Repository, your tests are ready for execution in Katalon TestOps.

## Schedule Test Runs

Planning test executions allows you to keep track of testing progress and monitor test results.

You can configure a schedule for automatic Test Runs or execute tests manually in Katalon TestOps.

* For automatic test executions, see: [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).
* For manual test executions, see: [Execute Test Runs manually](https://docs.katalon.com/katalon-analytics/docs/kt-scheduler.html).
