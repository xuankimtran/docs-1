---
title: "Set up an Agent to execute tests in a Docker Environment"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-analytics/docs/docker.html
redirect_from:
---

Similar to [Create a Local Test Environment with an Agent](/katalon-analytics/docs/agents.html), you can create a Docker Test Environment with a compatible Agent in Katalon TestOps.

## Set up an Agent

1. Sign in to [Katalon TestOps](https://testops.katalon.io/login) and go to your Project.
2. Go to **Configurations** > **Agent Setup**.
3. Select the **Docker Environment** tab.

    The page appears as below.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-docker/create-agent-for-docker-environment-page.png" width=100% alt="create docker environment page">

4. Fill in the required information for the **Configure an agent** and **Select method** sections.

    > Notes:
    >
    > You then use the commands in the **Generate configuration** and **Start an agent** sections to run the Agent in your computer.

5. Leave the TestOps page open while following the instructions to start an Agent in your local machine.

## Start an Agent

1. Create a folder (e.g, **Docker** folder) in your computer.

2. Open a new Notepad file in your computer, then copy and paste the command in the **Generate configuration** section into the new file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-docker/copy-paste-notepad-docker-compose-yml-file.png" width=100% alt="docker compose yml command">

3. Save the file as .yml file in the folder you have created (as shown in the pictures below).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-docker/save-notepad-file-in-docker-folder.png" width=100% alt="docker compose yml command">

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-docker/open-cmd-windows.png" width=100% alt="cmd.exe">
    
4. Open cmd.exe on Windows.
5. Copy and paste the command in the **Start an agent** section into your cmd to start an Agent.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-docker/run-docker-compose-in-cmd.png" width=100% alt="run agent for docker">

You have started your Docker with an Agent. You can open your Docker to see the Agent running.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-docker/agent-running-in-docker.png" width=100% alt="open docker">
    
## View an Agent's status

In Katalon TestOps, go to the **Test Environments** page to see the Docker Test Environment you have created and its status.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-analytics/docs/testops-revamp-aug-docker/docker-appears-in-test-environment-page.png" width=100% alt="open docker">

Next steps:

1. [Upload Test Scripts to a Script Repository](https://docs.katalon.com/katalon-analytics/docs/code-repo.html).
2. [Schedule Test Runs](https://docs.katalon.com/katalon-analytics/docs/create-plan.html).
