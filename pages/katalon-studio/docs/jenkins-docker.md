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

### Integrate Docker with Jenkins

To integrate Docker with Jenkins, you need to install the **Docker Plugins** and **Docker Pipeline** plugin on Jenkins. Do as follows:

1. Open Jenkins, then go to **Dashboard > Manage Jenkins > Manage Plugins**.
2. The Plugin Manager page appears. In the **Available** tab, search for **Docker Plugin** and **Docker Pipeline**, then select them.
3. Click **Install without restart**.

### Add environment path

After you install the plugins, you can add an environment path to Jenkins.

Go to **Dashboard > Manage Jenkins > Configure System > Global properties**. Select the **Environment variables** to add a global variable named `PATH`, which value is `$PATH:/usr/local/bin:`.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/Global-properties.png" alt="global properties" width=100%>

### Create and Build project on Jenkins

You can clone or download our sample CI/CD project at our GitHub repository: [CI sample](https://github.com/katalon-studio-samples/ci-samples).

In Jenkins Dashboard, go to **New Item** and create a **Freestyle project**. In the **Build** section, click **Add build step** and choose **Execute shell**.  Input your command, for example: `docker run katalonstudio/katalon katalon-notify.sh`.

After you are done with the configuration, click **Save** then click **Build Now**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/build.png" alt="build" width=100%>

