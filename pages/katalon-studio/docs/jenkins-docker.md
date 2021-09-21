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

To integrate Docker with Jenkins, you need to install the Docker Pipeline Plugins. In Jenkins, go to **Dashboard > Manage Jenkins > Manage Plugins** > 'Available' tab > search Docker and Docker Pipeline plugins > Choose them and install

You can clone or download our sample CI/CD project at our repository: [CI sample](https://github.com/katalon-studio-samples/ci-samples).

### Add environment path

Go to Dashboard > Manage jenkins > Configure System > Global properties > Tick Environment variables > Add ( Name: PATH, Value: $PATH:/usr/local/bin: )

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/Global-properties.png" alt="global properties" width=100%>

### Create project

In Jenkins, create new project > Freestyle project > Configure > Choose 'Build' tab > Choose 'Execute shell' > write the command (Example: docker run katalonstudio/katalon katalon-notify.sh)

### Build the project

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/build.png" alt="build" width=100%>