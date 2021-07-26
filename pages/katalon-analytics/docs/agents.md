---
title: "Create a Local Test Environment with an Agent" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/agents.html 
redirect_from: /katalon-analytics/docs/install_kt_agent.html
description: 
---

An Agent manages a local server for executing the scheduled Test Runs in a Local Test Environment.

Katalon TestOps supports compatible Agents for different executing environments.

Once you install the Agent in your local test machine, you have created a Local Test Environment for Test Runs execution.

> Notes:
>
> You can share the Agents among Users and Projects within a Team.

## Set up an Agent

> Requirements:
>
> You have a Katalon account.

### Download an Agent from Katalon TestOps

To install an Agent, follow these steps:

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login).

2. Go to your Project > **Configurations** > **Agent Setup** > **Local Environment**.

    The **Agent Setup** page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-agent-setup/agen-setup-page-to.png" width=100% alt="testops agent setup page">

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-agent-setup/agent-setup-code-page-blurred.png" width=100% alt="testops agent setup code page">

> Notes:
>
> You use the commands in the **Generate configuration** and **Start an agent** sections when setting up an Agent in your local machine.

3. Choose your Operating System (Windows, MacOS, etc.) in **Select OS**, then click **Download Agent**.

    You have downloaded the Agent file (.zip file) to your computer.

4. Create a name for the Agent in the **Agent Name** section (e.g., **My Agent**).

5. Leave the **Agent Setup** page open while following the instructions to set up the Agent in your local machine.

### Set up an Agent in a local machine

**For Windows**

Follow these steps:

1. Unzip the Agent file you have downloaded.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/kt_install_agent/kt_unzip_agent_setup.png" width=100% alt="windows unzip agent file">
    
2. Open a new CMD window.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/kt_install_agent/kt_agent_cmd.png" width=100% alt="windows cmd">

3. Copy the command in the **Generate configuration** section on the **Agent Setup** page, and paste it into the CMD window, then click *Enter* on the keyboard to run.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/kt_install_agent/kt_paste_gen_config_cmd.png" width=100% alt="windows cmd generate config command">

4. Copy the command in the **Start an agent** section, and paste it into the CMD window, then click *Enter* to run.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/kt_install_agent/kt_paste_start_agent.png" width=100% alt="windows cmd start an agent command">

    Wait for a minute.

5. Go to the **Agent Setup** page and click on **Test Environments** (in the **Schedule a test run** section) to see the added Local Test Environment.

**For MacOS**

1. Double click on the Agent file and select **New Terminal at Folder**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-agent-setup/open-katalon-agent-for-macos.png" width=100% alt="macos setup agent">

2. Copy the command in the **Generate configuration** section on the **Agent Setup** page, and paste it into the Terminal, then click *Enter* on the keyboard to run.

> Notes:
>
> Make sure you have enabled Terminal for Developer Tools in your MacOS's **Security & Privacy** settings (as shown below).
> <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-agent-setup/enable-terminal-for-developer-tool-macos.png" width=100% alt="macos security & privacy settings">

3. Copy the command in the **Start an agent** section, and paste it into the Terminal, then click *Enter* to run. Wait for a minute.

4. Go to the **Agent Setup** page and click on **Test Environments** (in the **Schedule a test run** section).

You have created a Local Test Environment with an Agent (e.g., **My Agent**).

### Manage the Agent status

Go to **Configurations** > **Test Environments** to check the Agent status.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-agent-setup/test-environment-created-on-testops.png" width=100% alt="macos test environment added after agent setup">

You can delete an Agent by clicking on the *Trash bin* icon.

The **Delete Agent** box pops up.

Click **Delete** to confirm your action.

> Notice:
>
> You cannot undo this action.

## Agent Authentication

Agents use `serverurl` and `apikey` in *agentconfig* to:
* activate Katalon Runtime Engine.
* send test results to Katalon TestOps.

You can see the `serverurl` and `apikey` in the **Generate configuration** section on the **Agent Setup** page.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-july-agent-setup/agent-setup-code-page-blurred-red.png" width=100% alt="serveurl and apikey">

## Configure Proxy for Agents

You can set up Proxy for the Agent in the *agentconfig* file, using the `proxy` option. For example, `proxy=http://localhost:8080`.

Next steps:
* [Upload Test Scripts to a Script Repository](https://docs.katalon.com/katalon-analytics/docs/code-repo.html).
* [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).
