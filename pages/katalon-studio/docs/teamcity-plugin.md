---
title: "How to use Katalon Studio for TeamCity"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/teamcity-plugin.html 
description: To show instrcutions of how to install and setup TeamCity plugin.
---
This tutorial shows you the step by step guide on how to install and run Katalon for TeamCity for Web UI Testing.

## Installation

See how to install and configure the TeamCity server [here](https://www.jetbrains.com/help/teamcity/installing-and-configuring-the-teamcity-server.html).
Install [Katalon Studio for TeamCity](https://plugins.jetbrains.com/plugin/12653-katalon). See how to install TeamCity plugins [here](https://www.jetbrains.com/help/teamcity/installing-additional-plugins.html).

## Enable the plugin

Since TeamCity 2018.2, to enable plugin after installation, click the plugin context menu and select Load. The plugin will be enabled without server restart.

## Configuration steps

One you have installed the plugin, you will need to configure Execute Katalon Studio Test task to complete the integration.

1. Create and configure a new project in TeamCity. Read more on TeamCity’s instructions to create a new project [here](https://www.jetbrains.com/help/teamcity/configure-and-run-your-first-build.html).

2. In TeamCity, select Katalon as Build runner type.
![](../../images/katalon-studio/docs/teamcity-plugin/1-configuration.png)

3. Regarding the Command Arguments, you can enter the arguments directly in the text area or generate them from your in use Katalon Studio.

   > Please remove any irrelevant argument such as `-runmode`. See [Command Arguments in Common Configuration](https://docs.katalon.com/katalon-studio/docs/common-configuration.html#command-arguments) for more details.

![](../../images/katalon-studio/docs/teamcity-plugin/2-configuration.png)

4. X11 DISPLAY and Xvfb-run configuration: Learn more [here](http://manpages.ubuntu.com/manpages/xenial/man1/xvfb-run.1.html). If you are not sure, only change the resolution 1024x768x24 and leave other options as-is.

5. Now everything is set up and ready to be built.
