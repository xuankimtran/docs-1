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

### Integrate Docker with Jenkins

To integrate Docker with Jenkins, you need to install the **Docker Pipeline** and **Docker Plugins**.

In Jenkins, go to **Dashboard > Manage Jenkins > Manage Plugins**. The Plugin Manager page appears. Select the **Available** tab and search for **Docker Plugin** and **Docker Pipeline**. Select these plugins and click **Install without restart**.

You can clone or download our sample CI/CD project at our GitHub repository: [CI sample](https://github.com/katalon-studio-samples/ci-samples).

### Add environment path

After you install the plugins, you can add an environment path to Jenkins.

Go to **Dashboard > Manage Jenkins > Configure System > Global properties**. Select the **Environment variables** to add a global variable named `PATH`, which value is `$PATH:/usr/local/bin:`.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/Global-properties.png" alt="global properties" width=100%>

### Create project

In Jenkins Dashboard, go to **New Item** and create a **Freestyle project**. In the **Build** section, click **Add build step** and choose **Execute shell**.  Input your command, for example: `docker run katalonstudio/katalon katalon-notify.sh`.

After you are done with the configuration, click **Save**.

### Build the project

 then click **Build Now**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/build.png" alt="build" width=100%>