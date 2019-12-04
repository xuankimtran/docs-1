---
title: "Install and Manage Agents" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/agents.html 
description: 
---

**Agent** is an installable software that you can use to manage your own servers to run Katalon Studio tests. You can set up agents on Linux, macOS and Windows machines. After installed, Agent can be selected as the execution environment when creating an execution plan.

To create a plan to run Katalon Studio tests on your local agents, please follow this [guide](grid-local-agents.html).

### Use Cases

You have local servers available and want to utilize their capacity to execute automation tests.

### Install Agents

1. In your Team view, go to **Agents** > **Agent Installation Package**
2. Fill out the form with this configuration information:
    * **Agent Name**: Provide a friendly Agent name
    * **API Key**: Use an existing API key or create a new one from your Profile page. [More details](katalon-analytics/docs/ka-api-key.html).
    * **Katalon Studio Version**: Specify a Katalon Studio version that Agent need to download to run tests
    * **Katalon Studio Location**: Provide a pre-install Katalon Studio location (if applicable)  
    * **Agent OS**: Katalon supports these operating systems: Linux x64, Linux x86, MacOS x64, Windows x64, Windows x86
3. Select **Download Agent**
4. Unzip the downloaded package, you will see an agent config file (which has already contained TestOps integration detail) and an agent executable file (e.g. **cli-macos-x64 for MacOS**).
    > Note: You may edit the agent configuration file later on your local machine.
5. Open your **Command Line Interface** and locate the agent installation package.
6. Enter this command to start the agent: **{agent execution file} start-agent**
    > E.g. cli-macos-x64 start-agent
7. Go back and reload Agents screen. You may now see the install Agent name, its availability, and other details.