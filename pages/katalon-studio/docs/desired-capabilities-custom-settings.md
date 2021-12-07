---
title: "Set custom desired capabilities" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/set-custom-desired-capabilities.html 
redirect_from:
description:
---

If you want to make a list of custom desired capabilities for some environments, you can use the **Custom** settings in desired capabilities.

This article shows you how to configure custom capabilities and where they are saved.
## Custom desired capabilities

To create a custom execution with desired capabilities, follow these steps:

1. Go to **Project > Settings > Desired Capabilities > Custom**. Click **Add** on the command toolbar to add a custom profile.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/KS-DC-create-a-custom-profile.png" width="70%" alt="Create a custom profile">

2. Change the name if needed, then click on *More* (...) under the **Value** column.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/KS-DC-Edit-a-custom-profile.png" width="70%" alt="Edit the custom profile settings">

3. In the **Custom Execution Configuration Builder** dialog, click **Add**, then specify the **Driver Name** for your custom execution. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/KS-DC-Choose-environment.png" width="70%" alt="Choose the environment to set DC">

    > You can have at most one web driver and one mobile driver here since there may be a potential conflict if you use multiple web or mobile drivers in the same test execution.

4. Click on *More* (...) under the **Preferences** column.

5. The **Driver Builder** dialog opens. Set desired capabilities for the selected driver. The steps to add new desired capabilities here is similar to configuring desired capabilities in each environment. You can refer to the following documents for setting up desired capabilities in different evironment:

    - [Set up desired capabilities in WebUI testing](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-settings-webui.html)

    - [Set up desired capabilities in mobile testing](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-settings-mobile.html)

    - [Set up desired capabilities in Windows Desktop App testing](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-settings-windows.html)

    - [Set up remote server in desired capabilities](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-remote-settings.html)


    Click **OK** when you finish.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/KS-DC-Set-DC-for-the-chosen-%20environment.png" width="70%" alt="Set DC for the chosen environment">

## Location of custom desired capabilities files

You can find the settings files for custom desired capabilities in the `<your test project location>\settings\external\execution` folder. 
