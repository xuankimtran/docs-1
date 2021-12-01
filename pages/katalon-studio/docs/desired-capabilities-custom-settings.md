---
title: "Set Custom Desired Capabilities" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/set-custom-desired-capabilities.html 
redirect_from:
description:
---

If you want to make a list of custom desired capabilities for some environments, you can use the **Custom** settings in desired capabilities.

This article shows you how to configure custom capabilities and the location of custom desired capabilities files.
## Custom Desired Capabilities

To create a custom execution with desired capabilities. Follow these steps:

1. Go to **Project > Settings > Desired Capabilities > Custom**. Click **Add** on the command toolbar to add a custom profile.

    <img src="url" width="70%" alt="Create a custom profile">

2. Change the name if needed, then click on the *More* (...) under the **Value** column.

    <img src="url" width="70%" alt="Edit the custom profile settings">

3. In the **Custom Execution Configuration Builder** dialog, click **Add**, then specify the **Driver Name** for your custom execution. Here, 

    <img src="url" width="70%" alt="Click More">

    > You can have at most one web driver and one mobile driver here since there may be a potential conflict if you use multiple web or mobile drivers in the same test execution.

4. Click on the *More* (...) under the **Preferences** column.

    <img src="url" width="70%" alt="Click More">

5. The **Driver Builder** dialog opens. Set desired capabilities for the selected Driver. The steps to add new Desired Capabilities here is similar to configuring desired capabilities in each environment. You can refer to the following documents for setting up desired capabilities in different evironment:

    - [Set up Desired Capabilities in WebUI Testing](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-settings-webui.html)

    - [Set up Desired Capabilities in Mobile Testing](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-settings-mobile.html)

    - [Set up Desired Capabilities in Windows Desktop App Testing](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-settings-windows.html)

    - [Set up Remote Server in Desired Capabilities](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-remote-settings.html)


    Click **OK** when you finish.

    <img src="url" width="70%" alt="Set DC for each environment">

## Location of Custom Desired Capabilities files

You can find the settings files for custom desired capabilities in the `<your test project location>\settings\external\execution` folder. 
