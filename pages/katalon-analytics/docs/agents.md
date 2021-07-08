---
title: "Create a Local Test Environment with an Agent" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/agents.html 
redirect_from: /katalon-analytics/docs/install_kt_agent.html
description: 
---

An Agent manages a local server for executing the scheduled Test Runs in a Local Test Environment.

Katalon TestOps supports compatible Agents for different execution environments.

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

3. Choose your Operating System (Windows, MacOS, etc.) in **Select OS**, then click **Download Agent**.

    You have downloaded the Agent file (.zip file) to your computer.

### Set up an Agent in a local machine

**For Windows**

Follow these steps:

1. Unzip the Agent file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/kt_install_agent/kt_unzip_agent_setup.png" width=100% alt="windows unzip agent file">
    
2. Open a new CMD window.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/kt_install_agent/kt_agent_cmd.png" width=100% alt="windows cmd">
    

In Agent Setup on Katalon Testops, click the button Copy at Generate configuration.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/kt_install_agent/kt_agent_copy_gen_config.png)

Paste the command, which we have just copied, in the cmd.exe. Then Enter to run.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/kt_install_agent/kt_paste_gen_config_cmd.png)

In Agent Setup on Katalon Testops, click the button Copy at Start an agent.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/kt_install_agent/kt_copy_start_agent.png)

Paste the command, which we have just copied, in the cmd.exe. Then Enter to run.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/kt_install_agent/kt_paste_start_agent.png)

After about a minute, in the Test Environments on Katalon Testops, the new Test Environment was be added.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/kt_install_agent/kt_test_environments.png)


## Start an Agent

Copy the command that was automatically generated in **Agent Setup** page and paste to your CLI.

It may take a while for the agent to start.

Start Agents step by step, see [here](https://docs.katalon.com/katalon-analytics/docs/install_kt_agent.html).

## View Agent status

You can check the Agent status by going to **Test Environments** in **Configurations**.

![](https://raw.githubusercontent.com/katalon-studio/docs-images/master/katalon-analytics/docs/agents/agent-local.png)

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

Using the `serverurl` and `apikey` was shown [here](https://docs.katalon.com/katalon-analytics/docs/install_kt_agent.html).

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
