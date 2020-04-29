---
title: "Setup and Start an Agent" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/agents.html 
description: 
---
Agent is an essential ingredient for remote execution on Katalon TestOps. This piece of software manages local servers for executing the scheduled tests. Katalon supports Agents that are compatible with different execution environments.

> Agents in TestOps CI are shared among members and projects within a team.

## Prerequisites
1. An agent executable file (e.g., **cli-macos-x64** for MacOS). 
2. A start script (`start.sh` for MacOS/Linux, `start.bat` for Windows)

> Download Agents and start scrips [here](https://github.com/katalon-studio/katalon-agent/releases).

3. An agent configuration file downloaded in TestOps.

> To start an agent, you need to put 3 files (executable, config and start script) in the same directory.

## Setup and start an Agent

1. On Katalon TestOps, go to your project and select **TestOps CI** > **Agent Setup**.
2. In **Agent Installation Package**, enter the required information:
    * **Agent Name**: It's recommended to give a meaningful name for distinguishing Agents.
    * **API Key**: Use an existing [API key](/katalon-analytics/docs/ka-api-key) or create a new one on your Profile page.
3. Click **Download Agent Configuration**.
4. Then you will see an **agentconfig** file containing Katalon TestOps integration details.
    > You may edit the agent configuration file later on your local machine.

5. Open your **Command-line Interface** and locate the agent installation package folder.
6. Start the Agent with the below command.

   * macOS or Linux: `./start.sh`
     > Please make sure you have given execute permission to both start script and executable file.
   * Windows: `start.bat`

7. It may take a while for the Agent to start.

To view Agent statuses, go to **Test Environments** in **TestOps CI**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/agents/agent-status.png)

## Authentication with Katalon TestOps

Agents will use `serverUrl` and `apikey` in **agentconfig** for:
* Activating Katalon Runtime Engine used for test execution.
* Sending test results to Katalon TestOps.

## Proxy settings for Agent

You can set up proxy for Agent in the `agentconfig` file with the `proxy` option.

For example, `proxy=http://localhost:8080`.

## Next Steps

Next, you can [upload your project code](/katalon-analytics/docs/code-repo) to Code Repo and [schedule a test](/katalon-analytics/docs/kt-scheduler).




