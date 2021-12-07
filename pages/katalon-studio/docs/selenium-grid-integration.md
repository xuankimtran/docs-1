---
title: "Selenium Grid - Execution on remote machines" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/selenium-grid-integration.html 
description: Tutorials of executing Katalon Studio's scripts on remote machines using Selenium Grid.
---

Katalon Studio allows you to execute your scripts on remote machines by using Selenium Grid. 

Follow these steps to set up your remote execution with Selenium Grid:

> Make sure that you are running Selenium Grid/ Appium Grid while executing the test. To set up and activate Selenium Grid, you can follow this Selenium document: [Set up Selenium Grid](https://www.selenium.dev/documentation/legacy/grid_3/setting_up_your_own_grid/#step-1-start-the-hub).

1. Open Katalon Studio and navigate to **Project > Settings > Desired Capabilities > Remote**. Enter the following information:

    * **Remote Server URL**:  the URL to the remote server, in the format of `http://<hub-ip-address>:<port>/wd/hub`. For example: `http://192.168.37.35:45339/wd/hub`.
    * **Remote Server type**: choose **Selenium**.
    
2. Click **Add** to add desired capabilities for remote execution (optional). Katalon Studio supports all Selenium Server desired capabilities. To learn more about Selenium capabilities, you can refer to the Selenium document in their Github project: [Supported capabilities](https://github.com/SeleniumHQ/selenium/wiki/DesiredCapabilities#used-by-the-selenium-server-for-browser-selection).
    
    > * Desired capabilities is a JSON object (having keys and values pair). We need to set the capability **Name** as `key` and the capability **Value** as `value`. 
    > * The capabilities keys are case-sensitive.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/remote-desired-capabilities/KS-DC-Set-remote-server-URL-types.png" width="100%" alt="Add Desired Capabilities for Remote execution">

3. Click **Apply and Close** to save your settings.
4. In the drop-down list of the **Run** button, select **Remote**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/selenium-grid-integration/KS-DC-Run-Remote-execution.png" width="30%" alt="Run remote execution">
