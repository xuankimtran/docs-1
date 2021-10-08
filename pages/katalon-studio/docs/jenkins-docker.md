---
title: "Jenkins on Docker hosted in Ubuntu" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/jenkins-docker-ubuntu.html 
description: This article will show you how to use Jenkins on Docker hosted in Ubuntu.
---

> Requirement:
>
> An active Katalon Runtime Engine license.
> Jenkins already installed.
> Docker already installed.

This tutorial will guide you to run your Katalon Project on Jenkins with Docker hosted in Ubuntu.

## Configure Jenkins
### Integrate with Docker on Jenkins

To integrate with Docker on Jenkins, you need to install the **Docker Plugins** and **Docker Pipeline** plugin. Do as follows:

1. Open Jenkins, then go to **Dashboard > Manage Jenkins > Manage Plugins**.
2. The Plugin Manager page appears. In the **Available** tab, search for **Docker Plugin** and **Docker Pipeline**, then select them.
3. Click **Install without restart**.

### Add environment path

After you install the plugins, you can add an environment path to Jenkins.

Go to **Dashboard > Manage Jenkins > Configure System > Global properties**. Select the **Environment variables** to add a global variable named `PATH`, which value is `$PATH:/usr/local/bin:`.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/Global-properties.png" alt="global properties" width=100%>

## Create and Build project on Jenkins

> Notes:
>
> Make sure you have opened Docker and installed Docker Plugin, Docker Pipeline plugin on Jenkins.
> You can clone or download our sample CI/CD project at our GitHub repository: [CI sample](https://github.com/katalon-studio-samples/ci-samples).

### Run your project from Git repository

1. Prepare your Katalon project repository on GitHub.
2. In Jenkins Dashboard, go to **New Item** and create a **Freestyle project**.
3. In the **Source Code Management** section, choose **Git**.
4. Enter your repository URL, select branches to build, repository browser, and additional Behaviours, if any.

### Run your Katalon Project from local workspace

1. Put your CI/CD project folder in this directory: `Users/Your_user_name/.jenkins/workspace`. Copy your project folder name.
2. In Jenkins Dashboard, go to **New Item** and create a **Freestyle project**. Name your project the same name as your project folder in your local Jenkins workspace.

## Build your project

1. In the **Build** section, click **Add build step** and choose **Execute shell**. Input your command, for example:

``` groovy
docker run -t --rm -v "$(pwd)":/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apikey=<YOUR_API_KEY>
```

2. After you are done with the configuration, click **Save** then click **Build Now**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/build.png" alt="build" width=100%>

You can view the console log in Docker, or click on your build on Jenkins and select **Console Output**.
In the console log, 
