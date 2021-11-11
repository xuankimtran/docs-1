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

## Pull Katalon Docker Image

1. Go to [katalonstudio/katalon](https://hub.docker.com/r/katalonstudio/katalon/) for Katalon Docker Image. 
2. Open terminal in your local machine, copy and paste the following command line:

```
docker pull katalonstudio/katalon
```

* Learn more about its usage in our Github project: [Docker Images](https://github.com/katalon-studio/docker-images).
* You can also download our sample project for CI configurations using Docker Image: [Docker Images samples](https://github.com/katalon-studio/docker-images-samples).
