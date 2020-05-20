---
title: "Start an Agent" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/agents.html 
description: 
---
Agent is an essential ingredient for remote execution on Katalon TestOps. This piece of software manages local servers for executing the scheduled tests. Katalon supports Agents that are compatible with different execution environments.

> Agents in TestOps CI are shared among members and projects within a team.

## Configure an Agent

### Step 1: Download an agent configuration file in TestOps

1. In Katalon TestOps, go to your project and select **TestOps CI** > **Agent Setup**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/agents/setup-agent.png)

2. Enter the required information:

    * **Agent Name**: It's recommended to give a meaningful name for distinguishing Agents.

    * **API Key**: Use an existing [API key](/katalon-analytics/docs/ka-api-key) or create a new one on your Profile page.

3. Click **Download Agent Configuration**.

4. Then you will see an `agentconfig` file containing Katalon TestOps integration details.
    > You may edit the agent configuration file later on your local machine.
    >
    > In case there is a file with different name, please make sure you have updated the file name to `agentconfig`.

### Step 2: Download an agent executable file

Download an agent executable file [here](https://github.com/katalon-studio/katalon-agent/releases).

- For MacOS/Linux, the agent executable file should be `cli-macos-x64` or `cli-macos-x86`.

- For Windows, the agent executable file should be `cli-win-x64.exe` or `cli-win-x86.exe`.

### Step 3: Download a start script

Download a start script [here](https://github.com/katalon-studio/katalon-agent/releases).

- For MacOS/Linux, the start script should be `start.sh`.

- For Windows, the start script should be `start.bat`.

### Step 4: Put all files to the same directory

To start an agent, you need to put **an agent executable**, **configuration file** and **start script** in the same directory.


## Start an Agent

### In MacOS/Linux

1. Open your **Command-line Interface** and locate the folder where you put the 3 files as mentioned above. For example: `cd Desktop/`.

2. Please make sure you have given execute permission to both start script and executable file (for MacOs and Linux) using the following command: `chmod +x *`.

3. Start the Agent with the following command: `./start.sh`.

4. It may take a while for the Agent to start.

### In Windows

1. Open your **Command-line Interface** and locate the folder where you put the 3 files as mentioned above. For example: `cd Desktop/`.

2. Start the Agent with the following command: `start.bat`

3. It may take a while for the Agent to start.


## View Agent status

You can check the Agent status by going to **Test Environments** in **TestOps CI**.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/agents/agent-status.png)

> You can delete an agent anytime by clicking on the recycle bin icon.
>
> Please note that this action cannot be undone.

## Authentication with Katalon TestOps

Agents will use `serverUrl` and `apikey` in **agentconfig** for:
* Activating Katalon Runtime Engine used for test execution.
* Sending test results to Katalon TestOps.

## Proxy settings for Agent

You can set up proxy for Agent in the `agentconfig` file with the `proxy` option.

For example, `proxy=http://localhost:8080`.


## Next Steps

Next, you can [upload your project code](/katalon-analytics/docs/code-repo) to Code Repo and [schedule a test](/katalon-analytics/docs/kt-scheduler).




