---
title: "Selenium Grid - Execution on Remote Machines" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/selenium-grid-integration.html 
description: Tutorials of executing Katalon Studio's scripts on remote machines using Selenium Grid.
---

You can execute your scripts on remote machines by using [Selenium Grid](https://www.seleniumhq.org/docs/07_selenium_grid.jsp).

1. Follow [this user guide](https://www.seleniumhq.org/docs/07_selenium_grid.jsp#installation) to set up and activate Selenium Grid.

2. Configure the desired capabilities for a remote machine. Open Katalon Studio and navigate to **Project** > **Settings** > **Desired Capabilities** > **Remote** > Enter required information and then click **OK**.

* **Remote Server URL** should be in the format of `http://<hub-ip-address>:<port>/wd/hub`. E.g.: http://192.168.37.35:45339/wd/hub.
* **Remote Server type**: Selenium.
* **Add properties**. Currently, all [desired capabilities](https://github.com/SeleniumHQ/selenium/wiki/DesiredCapabilities#used-by-the-selenium-server-for-browser-selection) of the Selenium Server will be supported by Katalon Studio.
    > The value of properties is case sensitive.

3. In the drop-down list of the **Run** button, select **Remote**.
