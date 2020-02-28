---
title: "Install and Manage Agents" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/agents.html 
description: 
---
Agent is an essential ingredient for remote execution on Katalon TestOps. This piece of software manages local servers for executing the scheduled tests. Katalon supports Agents that are compatible with different execution environments.

To download and install an Agent, please follow this guide:

1. On Katalon TestOps, select your Project > **Agents**.
2. In **Agent Installation Package**, enter the required information:
    * **Agent Name**: It's recommended to give a meaningful name for distinguishing Agents.
    * **API Key**: Use an existing [API key](/katalon-analytics/docs/ka-api-key) or create a new one on your Profile page.
    * **Agent OS**: Katalon supports the following operating systems: Windows x64, Linux x64, and MacOS x64.
3. Click **Download Agent**.
4. Unzip the downloaded package. You will see an **agentconfig** file containing Katalon TestOps integration details and an agent executable file (e.g., **cli-macos-x64** for MacOS).
    > You may edit the agent configuration file later on your local machine.
5. Open your **Command-line Interface** and locate the agent installation package folder.
6. Start the Agent with the below command.

   * macOS or Linux: `./start.sh`
     > Please make sure you have given execute permission to both start script and executable file.
   * Windows: `start.bat`

7. It may take a while for the Agent to start. When the starting Agent process finishes, reload the **Agents** view in your Project on Katalon TestOps. Here you can see the installed Agent and its details.

### Authentication in Katalon TestOps

Based on `serverUrl` in **agentconfig**, the Agent will identify if users are using the cloud or on-premise Katalon TestOps version.

#### Cloud Katalon TestOps

For cloud version, Katalon TestOps will use `serverUrl` and `apikey` in **agentconfig** for sending test results to Katalon TestOps and checking online activation.

#### Katalon TestOps OnPremise

Katalon TestOps will use `serverUrl` and `apikey` in **agentconfig** for sending test results to Katalon TestOps.

While `serverURL` and `apiKey` in **.katalon/licenseServer.properties** will be used for activation.

  > **Notes**:
  >
  > You have to create a **{user.home}/.katalon/licenseServer.properties** (.katalon is a hidden folder). The **licenseServer.properties** must contain the following properties for Katalon Studio to authenticate:
  >
  > * `serverURL=https://analytics.katalon.com`
  > * `apiKey=xxxxxxxx`.
  >
  > Go to your profile page > Select **API Key** > Copy an existing API Key for this purpose or create a new one.

Next, you can [upload your project code](/katalon-analytics/docs/code-repo) to Code Repo and [schedule a test](/katalon-analytics/docs/kt-scheduler).

### Proxy settings for Agent

You can setup proxy for Agent by one of the following options:

1. Update Proxy field in Katalon TestOps.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/agent/proxy-agent.png)

2. Configure proxy settings in `agentconfig` file with the `proxy` option.

For example, `proxy=http://localhost:8080`.





