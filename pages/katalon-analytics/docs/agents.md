---
title: "Create a Local Test Environment with Agent" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/agents.html 
description: 
---
Agents manage local servers for executing the scheduled Test Runs in local Test Environment. Katalon supports Agents that are compatible with different execution environments.

> Agents are shared among members and projects within a team.

## Set up an Agent

1. Under **Configurations**, go to *"Agent setup"*. 
2. Select *"Local Environment"*. 
3. Follow 5-step instructions in the setup wizard.

## Start an Agent

* Copy the command that was automatically generated in *Agent Setup* page and paste to your CLI.
* It may take a while for the agent to start.

## View Agent status

You can check the Agent status by going to *"Test Environments"* in **Configurations**.

![](https://github.com/katalon-studio/docs-images/blob/master/katalon-analytics/docs/agents/agent-local.png)

> You can delete an Agent anytime by clicking on the recycle bin icon.

> You can delete an Agent anytime by clicking on the recycle bin icon. **Please note that this action cannot be undone.**

## Authentication with Katalon TestOps

Agents will use `serverUrl` and `apikey` in **agentconfig** for:
* Activating Katalon Runtime Engine used for test execution.
* Sending test results to Katalon TestOps.

## Configure Proxy for Agent

You can set up proxy for Agent in the `agentconfig` file with the `proxy` option.

For example, `proxy=http://localhost:8080`.

## Next Steps

- [Set up a Script Repository](/katalon-analytics/docs/code-repo)
- [Schedule Test Runs](/katalon-analytics/docs/kt-scheduler)

## Related topics

- [Create a Docker environment](https://docs.katalon.com/katalon-analytics/docs/docker.html)
- [Create a CircleCI Environment](https://docs.katalon.com/katalon-analytics/docs/circleci.html)
- [Create a Kubernetes Environment](https://docs.katalon.com/katalon-analytics/docs/aws-eks.html)
- [Load balancing for Local Test Environment](https://docs.katalon.com/katalon-analytics/docs/load-balancing-agents.html)
- [Katalon TestOps Terminology](/katalon-analytics/docs/testops-terminology.html)

