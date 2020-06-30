---
title: "Local Test Environments" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/agents.html 
description: 
---
Agents manage local servers for executing the scheduled tests in TestOps CI. Katalon supports agents that are compatible with different execution environments.

> Agents are shared among members and projects within a team.

## Set up an agent

### Step 1: Download an agent

In Katalon TestOps, go to your project and select **TestOps CI** > **Agent Setup**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/agent/agent-setup.png)


Select your compatible OS to download an agent and **unzip** the downloaded package.

### Step 2: Configure an agent

Enter the required information:

 * **Agent Name**: It's recommended to give a meaningful name for distinguishing agents.

 * **API Key**: Use an existing [API key](/katalon-analytics/docs/ka-api-key) or create a new one on your Profile page.

    > You may edit the agent configuration file later on your local machine.
    >
    > In case there is a file with different name, please make sure you have updated the file name to `agentconfig`.

### Step 3: Generate agent config

After having the agent downloaded and configured,

- navigate to the directory containing that file (E.g.: `cd Desktop`); then
- copy the command that was automatically generated in Agent Setup page and paste to your CLI.

### Step 4: Start an agent

Copy the command that was automatically generated in **Agent Setup** page and copy to your CLI.

It may take a while for the agent to start.

### Step 5: Create a new plan

After the agent starts succesfully, navigate to **Test Environments** and create a sample plan.

## View agent status

You can check the Agent status by going to **Test Environments** in **TestOps CI**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/agents/agent-status.png)

> You can delete an agent anytime by clicking on the recycle bin icon.
>
> Please note that this action cannot be undone.

## Authentication with Katalon TestOps

Agents will use `serverUrl` and `apikey` in **agentconfig** for:
* Activating Katalon Runtime Engine used for test execution.
* Sending test results to Katalon TestOps.

## Proxy settings for agent

You can set up proxy for agent in the `agentconfig` file with the `proxy` option.

For example, `proxy=http://localhost:8080`.

## Next Steps

- [Upload your project code](/katalon-analytics/docs/code-repo) to Test Projects; and 
- [Schedule a test](/katalon-analytics/docs/kt-scheduler)




