---
title: "Create a Local Test Environment" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/agents.html 
description: 
---
To create a Local Test Environment to execute or schedule Test Runs, you need to have an agent that manages local servers. **Katalon TestOps** supports agents that are compatible with different execution environments.

> Agents are shared among members and projects within a team.

## Set up and start an agent

In your project, go to *Configurations* and select *Agent Setup*.

Follow the steps in the setup wizard.

## Create a Local Test Environment

After finishing the setup and having the agent started, you now have a Local Test Environment ready to schedule a Test Run.

> View a list of Test Environment that you have created in *Test Environments* page.
>
> ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/agents/test-environment.png)
>
> You can delete an agent anytime by clicking on the recycle bin icon. **Please note that this action cannot be undone.**

## Authentication with Katalon TestOps

Agents will use `serverUrl` and `apikey` in **agentconfig** for:
* Activating Katalon Runtime Engine used for test execution.
* Sending test results to Katalon TestOps.

## Configure Proxy Settings for agent

You can set up proxy for agent in the `agentconfig` file with the `proxy` option.

For example, `proxy=http://localhost:8080`.

## Next steps

- [Create a Script Repository](/katalon-analytics/docs/code-repo)
- [Schedule a Test Run](/katalon-analytics/docs/kt-scheduler)


## Related topics

- Create a Docker environment
- [Create a Kubernetes Environment](https://docs.katalon.com/katalon-analytics/docs/aws-eks.html)
- [Create a CircleCI Environment](https://docs.katalon.com/katalon-analytics/docs/circleci.html)
