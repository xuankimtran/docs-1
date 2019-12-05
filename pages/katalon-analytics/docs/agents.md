---
title: "Install and Manage Agents" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/agents.html 
description: 
---

**Agent** a required ingredient for remote execution on Katalon TestOps. This piece of software manages local servers for executing the scheduled tests. Katalon supports Agents that are compatible with different Execution Environments.

To download and install an Agent, please follow this guide:

1. In Katalon TestOps, go to your project and select **Agents**.
2. In **Agent Installation Package**, enter the required information:
    * **Agent Name**: Provide a friendly Agent name
    * **API Key**: Use an existing [API key](/katalon-analytics/docs/ka-api-key.html) or create a new one in your Profile page.
    * **Agent OS**: Katalon supports the following operating systems: Linux x64, MacOS x64, and Windows x64.
3. Click **Download Agent**
4. Unzip the downloaded package, you will see an **agentconfig** file containing Katalon TestOps integration details and an agent executable file (e.g. **cli-macos-x64** for MacOS).
    > Note: You may edit the agent configuration file later on your local machine.
5. Open your **Command-line Interface** and locate the agent installation package folder.
6. Start the Agent with the below command:

    * macOS: `./start.sh`

  > It may take a while for the Agent to start. Be patient!

7. When the starting Agent process finishes, reload the **Agent** View in your Project on Katalon TestOps. Here you can see the installed Agent, and its details.

Next, you can upload your project code to Code Repo and schedule a test.
