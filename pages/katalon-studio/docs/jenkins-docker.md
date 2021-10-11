---
title: "Integrate Jenkins on Docker hosted in Ubuntu" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/jenkins-docker-ubuntu.html 
description: This article will show you how to use Jenkins on Docker hosted in Ubuntu.
---

> Requirement:
>
> An active Katalon Runtime Engine license.
> Docker and Jenkins are already installed and configured. You can learn how to install Docker and Jenkins at Jenkins document: [Docker](https://www.jenkins.io/doc/book/installing/docker/).

Docker is a platform for running applications in an isolated environment called a Docker container. Applications like Jenkins can be downloaded as read-only images, each of which is run in Docker as a container.

However, when your Jenkins is installed on a dynamic Docker hosted in Ubuntu without GUI, you might not be able to configure build and integration with Katalon Studio from the user interface normally.

This tutorial will guide you through configuring and building your Katalon Project with Jenkins on Docker hosted in Ubuntu.

## Integrate with Docker on Jenkins

To integrate with Docker on Jenkins, you need to install the **Docker Plugins** and **Docker Pipeline** plugin, then set an environment path to Jenkins. Do as follows:

### Install plugins

1. Open Jenkins, then go to **Dashboard > Manage Jenkins > Manage Plugins**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/new-plugin.png" alt="manage plugins" width=60%>

2. The Plugin Manager page appears. In the **Available** tab, search for **Docker Plugin** and **Docker Pipeline**, then select them.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/plugins.png" alt="plugins" width=70%>

3. Click **Install without restart**.

### Add an Environment Path

To run Docker commands from Jenkins, you need to add an environment path to Jenkins. The `PATH` specifies where to find the folder containing Docker's commands.

Go to **Dashboard > Manage Jenkins > Configure System > Global properties**. Select the **Environment variables** to add a global variable named `PATH`, which value is `$PATH:/usr/local/bin:`.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/Global-properties.png" alt="global properties" width=100%>

## Upload your Katalon project on Jenkins

> Notes:
>
> Make sure you have opened Docker and installed Docker Plugin, Docker Pipeline plugin on Jenkins.
> You can clone or download our sample CI/CD project at our GitHub repository: [CI sample](https://github.com/katalon-studio-samples/ci-samples).

You can either upload your Katalon project from a Git repository or your local workspace.

### Upload a Git repository

1. Prepare your Katalon project repository on GitHub.
2. In Jenkins Dashboard, go to **New Item** and create a **Freestyle project**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/new-item.png" alt="new item" width=85%>

3. In the **Source Code Management** section, choose **Git**.
4. Enter your repository URL, select branches to build, repository browser, and additional behaviours, if any.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/git.png" alt="add git repository" width=85%>

### Upload in the local workspace

1. Put your CI/CD project folder in this directory: `Users/Your_user_name/.jenkins/workspace`. Copy your project folder name.
2. In Jenkins Dashboard, go to **New Item** and create a **Freestyle project**. Name your project the same name as your project folder in your local Jenkins workspace.

## Build your project

1. In the **Build** section, click **Add build step** and choose **Execute shell**. Input your command, for example:

    ``` groovy
    docker run -t --rm -v "$(pwd)":/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apikey=<YOUR_API_KEY>
    ```

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/execute-shell.png" alt="command" width="100%">

    > You can find more command line options at [Command Syntax](https://docs.katalon.com/katalon-studio/docs/console-mode-execution.html#general-options).

    After you are done with the configuration, click **Save**.

4. In your project, click **Build Now**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/build-now.png" alt="build now" width=85%>

5. To view the console log, click on your current build on Jenkins and select **Console Output**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/console-output.png" alt="console output" width=100%>

    When the test is being run, you can also view this console log in Docker.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/docker-log.png" alt="docker log" width=100%>

4. To view your report files, you can go to this directory: `Users/Your_user_name/.jenkins/workspace/Your_project_name/Reports` or your third-party integration like Katalon TestOps, Azure DevOps, or qTest.

    > Notes:
    >
    > For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. See also [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-analytics/docs/integration-with-katalon-studio.html#enable-integration).