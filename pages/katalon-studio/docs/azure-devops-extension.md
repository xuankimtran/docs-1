---
title: "How to use Katalon for Azure DevOps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/azure-devops-extension.html 
description: To show instrcutions of how to install and setup Azure DevOps extension.
---
This tutorial shows you the step by step guide on how to install and run Katalon for Azure DevOps for Web UI testing.

> You need to have **Katalon Studio version 7.0.0** or later to use Azure DevOps extension.

> This extension is NOT available for Linux.

Refer to this [sample pipeline](https://github.com/katalon-studio-samples/azure-devops-extension-samples) for your reference.

## Installation

Go to [this link](https://marketplace.visualstudio.com/items?itemName=katalon-llc.katalon&ssr=false#overview) to install the extension.

## Configuration steps

Once you have installed the extension, you will need to configure Execute Katalon Studio Tests task to complete the integration.

1. In Azure DevOps, add task **Execute Katalon Studio Tests** to your list. You can quickly lookup Execute Katalon Studio Tests from the search box or find it under the Task category.

> We only support VM Image in Windows and MacOS.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-extension/1-search.png)

2. Regarding the **Command Arguments**, you can enter the arguments directly in the text area or generate them from Katalon Studio. 

   > Please leave out any irrelevant argument such as `-runmode`. See [Command Arguments in Common Configuration](https://docs.katalon.com/katalon-studio/docs/common-configuration.html#command-arguments) for more details.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-extension/2-command.png)

3. **X11 DISPLAY**: Leave this field blank. 

4. **Xvfb-run** configuration: Learn more [here](http://manpages.ubuntu.com/manpages/xenial/man1/xvfb-run.1.html). If you are not sure, only change the resolution 1024x768x24 and leave other options as-is.

5. After everything is set up, click **Queue** button to build.

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-extension/3-result.png)

   ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-extension/4-result.png)

