---
title: "Jenkins on Docker hosted in Ubuntu" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/jenkins-docker-ubuntu.html 
description: This article will show you how to use Jenkins on Docker hosted in Ubuntu.
---

> Requirement:
> 
> Docker and Docker Pipeline Plugins already installed. To install Docker Pipeline Plugins, go to Dashboard > Manage Jenkins > Manage Plugins > 'Available' tab > search Docker and Docker Pipeline plugins > Choose them and install

Clone or download our sample CI/CD project at our repository: [CI sample](https://github.com/katalon-studio-samples/ci-samples).

### Add environment path

Go to Dashboard > Manage jenkins > Configure System > Global properties > Tick Environment variables > Add ( Name: PATH, Value: $PATH:/usr/local/bin: )

### Create project

In Jenkins, create new project > Freestyle project > Configure > Choose 'Build' tab > Choose 'Execute shell' > write the command (Example: docker run katalonstudio/katalon katalon-notify.sh)

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/Global-properties.png" alt="global properties" width=100%>

### Build the project

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/jenkins-docker/build.png" alt="build" width=100%>