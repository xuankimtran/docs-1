---
title: "Create a Local Test Environment with Agent" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/agents.html 
description: 
---
Agents manage local servers for executing the scheduled Test Runs the in local Test Environment. Katalon supports Agents that are compatible with different execution environments.

> We share the Agents among members and projects within a team.

## Set up an Agent

In **Configurations**, go to **Agent setup** > Select **Local Environment** > Follow instructions in the setup wizard.

Setup Agents step by step, see [here](https://docs.katalon.com/katalon-analytics/docs/install_kt_agent.html).

## Start an Agent

Copy the command that was automatically generated in **Agent Setup** page and paste to your CLI.

It may take a while for the agent to start.

Start Agents step by step, see [here](https://docs.katalon.com/katalon-analytics/docs/install_kt_agent.html).

## View Agent status

You can check the Agent status by going to **Test Environments** in **Configurations**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-terminology/test-environment.png)

> You can delete an Agent anytime by clicking on the recycle bin icon.

> ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/agents/kt_delete_agent.png)

> The window Delete Agent displays and click the button Delete.

> ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/agents/kt_delete_agent_window.png)

> **Please note that this action cannot be undone.**

## Authentication with Katalon TestOps

Agents will use `serverurl` and `apikey` in **agentconfig** for:
* Activating Katalon Runtime Engine used for test execution.
* Sending test results to Katalon TestOps.

We can see the `serverurl` and `apikey` in Generate configuration of Agent Setup. 

 ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/agents/kt_agentconfig_server_url.png)

 ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/agents/kt_agentconfig_apikey.png)

Using the `serverurl` and `apikey` was shown [here](katalon-analytics/docs/install_kt_agent.html ).

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

