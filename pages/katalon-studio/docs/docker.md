---
title: "Docker Image" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/docker.html 
redirect_from:
    - "/display/KD/Docker/"
    - "/x/swTR/"
    - "/katalon-studio/docs/docker/"
description: 
---

> Requirements:
> * Docker installed. You can refer to the instructions in the Docker document here: [Get Docker](https://docs.docker.com/get-docker/).
> * An active Katalon Runtime Engine floating license. To learn more about types of licenses, you can refer to this document: [Types of licenses](https://docs.katalon.com/katalon-studio/docs/license.html).

This tutorial shows you how to run Katalon Studio test with Katalon Docker Image (KDI). This image contains up-to-date browsers, including Google Chrome, Mozilla Firefox, and Katalon Studio. Hence when running your Katalon Project with Katalon Studio Docker Image, the pre-installed Katalon Studio and Katalon Runtime Engine in your local machine are not required. 

Docker Image for Katalon Studio is available here at Docker Hub: [katalonstudio/katalon](https://hub.docker.com/r/katalonstudio/katalon/).

> You can download our Github sample project for CI configurations using Docker Image: [Docker Images samples](https://github.com/katalon-studio/docker-images-samples).
## Pull Katalon Docker Image

To pull KDI, open **Terminal** in your local machine, copy and paste the following command line:

```
docker pull katalonstudio/katalon
```

If you want to check which version of Google Chrome and Mozilla Firefox the KDI supports, copy and paste the following command in the **Terminal**: 

```
docker run -t --rm katalonstudio/katalon cat /katalon/version
```
## Run your test with Katalon Docker Image

1. Open **Terminal**, then go to the test project directory you wish to run. For example, we want to run the **CI sample** test project.

