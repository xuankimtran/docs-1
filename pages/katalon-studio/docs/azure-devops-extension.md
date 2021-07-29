---
title: "How to use Katalon for Azure DevOps"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/azure-devops-extension.html 
description: To show instructions of how to install and setup Azure DevOps extension.
---
> Katalon TestOps CI is an easier way to execute Katalon Studio tests remotely or schedule remote Katalon Studio execution. See [Test Planning Overview](https://docs.katalon.com/katalon-analytics/docs/kt-remote-execution.html) for detailed information.

This tutorial shows you the step-by-step guide on installing and running Katalon with Azure DevOps for Web UI testing. Refer to this [Sample pipeline](https://github.com/katalon-studio-samples/azure-devops-extension-samples) on Github for your reference.

## Azure DevOps Extension for Linux

The Azure DevOps extension is available on Linux. This extension was tested on Ubuntu 16.0.4 and Ubuntu 18.04. For continuous integration using this version, we recommend our sample scripts on Github: [Azure DevOps sample script](https://github.com/katalon-studio-samples/azure-devops-extension-samples/blob/master/azure-pipelines.yml).

## Katalon for Azure DevOps Installation

* Go to the Visual Studio Market Place, download and install the free extension of [Katalon for Azure DevOps](https://marketplace.visualstudio.com/items?itemName=katalon-llc.katalon&ssr=false#overview).
* To run UI tests on Azure Pipelines, you might need to adjust the screen resolution (See Microsoft documentation on [Setting screen resolution](https://docs.microsoft.com/en-us/azure/devops/pipelines/test/ui-testing-considerations?view=azure-devops&tabs=mstest#setting-screen-resolution)). You can also install the [Screen Resolution Utility](https://marketplace.visualstudio.com/items?itemName=ms-autotest.screen-resolution-utility-task#overview) extension from the Visual Studio Marketplace. See our Github example on how to run a Katalon Studio test: [Azure DevOps Usage example](https://github.com/duyluonganh/kat-download-file/blob/master/azure-pipelines.yml).

## Configuration steps

Once you have installed the extension, you need to configure **Execute Katalon Studio Tests** task to complete the integration.

1. In **Azure DevOps**, to find and add task **Execute Katalon Studio Tests** to your list, go to the **Search** box or the **Task** category.

   > We support VM Image in Windows, MacOS, and Linux.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-extension/1-search.png" alt="add task Execute Katalon Studio Tests" width=100%>

2. Enter the **Command Arguments** directly in the text area or generate the arguments from Katalon Studio.

   > Please leave out any irrelevant argument such as `-runmode`. See [Command Arguments in Common Configuration](https://docs.katalon.com/katalon-studio/docs/common-configuration.html#command-arguments) for more details.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-extension/2-command.png" alt="enter the arguments" width=100%>

3. Leave the **X11 DISPLAY** field blank.

4. Configure **Xvfb-run** following Ubuntu Manuals on [Xenial xvfb-run](http://manpages.ubuntu.com/manpages/xenial/man1/xvfb-run.1.html). The function still works if you only change the resolution to 1024x768x24 and leave other options as-is.

5. After everything is set up, click the **Queue** button to build.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-extension/3-result.png" alt="Azure DevOps extension result 1" width=100%>

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/azure-devops-extension/4-result.png" alt="Azure DevOps extension result 2" width=100%>