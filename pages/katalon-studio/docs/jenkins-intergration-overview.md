---
title: "Jenkins Integration Overview"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/jenkins-integration-overview.html 
description: 
redirect from: 
---

Jenkins is an open-source automation server. Jenkins provides hundreds of plugins to support building, deploying, and automating any project.

You can integrate Jenkins with Katalon Studio and execute Katalon tests with Jenkins.

## Jenkins Integration

There are two possible ways to integrate Katalon with Jenkins:

1. Use Katalon TestOps Plugin for Jenkins.
    
    Katalon TestOps Plugin for Jenkins helps execute Katalon Studio in Jenkins easily. Katalon Studio will be automatically downloaded and deployed. To integrate Jenkins with Katalon Studio via Katalon TestOps Plugin, you can refer to the following documents:

   - [On Window/MacOS](https://docs.katalon.com/katalon-studio/docs/katalon-plugin-jenkins-window-macOS.html)
   - [On Ubuntu](https://docs.katalon.com/katalon-studio/docs/jenkins-plugin-ubuntu.html)

2. Use Katalon Studio Docker Image. 
    
    This image contains up-to-date browsers, including Google Chrome, Mozilla Firefox, and Katalon Studio. Hence, when running your Katalon Project with Katalon Studio Docker Image, the pre-installed Katalon Studio and Katalon Runtime Engine in your local machine are not required. Docker Image for Katalon Studio is available here at Docker Hub: [katalonstudio/katalon](https://hub.docker.com/r/katalonstudio/katalon/).

    To integrate Jenkins with Katalon Studio via Katalon Docker Image, you can refer to the following documents:

    - [Integrate Jenkins Pipeline (Jenkinsfile) with Katalon Studio Docker Image](https://docs.katalon.com/katalon-studio/docs/jenkins-pipeline-docker.html)
    - [Integrate Jenkins on Docker hosted in Ubuntu](https://docs.katalon.com/katalon-studio/docs/jenkins-docker-ubuntu.html#integrate-with-docker-on-jenkins)
  
## Execute Katalon Studio tests in Jenkins

The following documents are tutorials and tips that can help you execute Katalon Studio tests after Jenkins integration.

- [Passing feature file and scenario tags at runtime when building with Jenkins](https://docs.katalon.com/katalon-studio/how-to-guides/jenkins-tags-runtime.html#create-global-variables)
- [Execute Katalon Studio tests with Jenkins Pipeline Script (Jenkinsfile)](https://docs.katalon.com/katalon-studio/docs/execute-katalon-tests-with-jenkins-pipeline-script.html)
