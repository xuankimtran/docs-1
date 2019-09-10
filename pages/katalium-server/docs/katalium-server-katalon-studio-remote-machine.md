---
title: "Katalium Server - Execute Katalon Studio's scripts on Remote Machines" 
sidebar: katalon_studio_docs_sidebar
permalink: katalium-server/docs/katalium-server-katalon-studio-remote-machine.html 
description: Tutorials of executing Katalon Studio's scripts on remote machines using Katalium Server.
---

You can execute your scripts in Katalon Studio on remote machines by using [Katalium Server](https://docs.katalon.com/katalium-server/docs/katalium-overview.html).

1. Follow [this user guide](https://docs.katalon.com/katalium-server/docs/katalium-user-guide.html) to set up and activate Katalium Server.

2. Configure the desired capabilities for a remote machine. Open Katalon Studio. Navigate to **Project** > **Settings** > **Desired Capabilities** > **Remote** > Enter required information and then click **OK**.

* **Remote Server URL** should be in the format of `http://<hub-ip-address>:<port>/wd/hub`. E.g.: http://192.168.37.35:45339/wd/hub.
* **Remote Server type**: Selenium.
* **Add properties**. Currently, all [desired capabilities](https://github.com/SeleniumHQ/selenium/wiki/DesiredCapabilities#used-by-the-selenium-server-for-browser-selection) of the Selenium Server will be supported by Katalon Studio.
    > The value of properties is case sensitive.

3. In the drop-down list of the **Run** button, select **Remote**.
