---
title: "Set Custom Desired Capabilities" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/set-custom-desired-capabilities.html 
redirect_from:
description:
---






## Custom Desired Capabilities

* Define a custom option for execution.
* **Project > Settings > Desired Capabilities > Custom**.

> If you want to make a list of your own custom Desired Capabilities for some environments, then it's suggested to use '**Custom**' settings in this case.

Custom execution is slightly different from other execution settings. Follow these steps to create a custom execution with its desired capabilities:

1. Click **Add** on the command toolbar to add a custom execution to the custom execution list.
2. Change the name if needed, then click on the **More** icon under the **Value** column.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/image2016-11-1-143A263A29.png)
3. In the **Custom Execution Configuration Builder** dialog, specify the **Driver Name** for your custom execution.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/image2016-11-1-143A293A6.png)

    > You can have at most one web driver and one mobile driver here since there may be a potential conflict if you use multiple web or mobile drivers in the same test execution.
4. Click on the **More** icon under the **Preferences** column.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/image2016-11-1-143A303A6.png)
5. The **Driver Builder** dialog is displayed for you to set desired capabilities for the selected Driver. The steps to add new Desired Capabilities here is similar to other settings above. Click **OK** when you finish.
    ![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/execution-settings/image2016-11-1-143A353A10.png)

## Location of Desired Capabilities files

Defined configuration settings are saved in separated files under the "**<your test project location>\\settings\\internal**" location (or "**<your test project location>\\settings\\external\\execution**" in case of custom execution), as below:

| Driver | Settings' file |
| --- | --- |
| Chrome | com.kms.katalon.core.webui.chrome.properties |
| Firefox | com.kms.katalon.core.webui.firefox.properties |
| Chrome (Headless)| com.kms.katalon.core.webui.chrome (headless).properties |
| Firefox (Headless) | com.kms.katalon.core.webui.firefox (headless).properties |
| IE | com.kms.katalon.core.webui.ie.properties |
| Safari | com.kms.katalon.core.webui.safari.properties |
| Edge | com.kms.katalon.core.webui.edge.properties |
| Edge (Chromium)| com.kms.katalon.core.webui.edge chromium.properties |
| Remote Web | com.kms.katalon.core.webui.remote.properties |
| Android | com.kms.katalon.core.mobile.android.properties |
| iOS | com.kms.katalon.core.mobile.ios.properties |