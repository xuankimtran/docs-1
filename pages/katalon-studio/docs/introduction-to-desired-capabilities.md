---
title: "Introduction to Desired Capabilities" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/introduction-to-desired-capabilities.html 
redirect_from:
    - "/display/KD/Introduction+to+Desired+Capabilities/"
    - "/display/KD/Introduction%20to%20Desired%20Capabilities/"
    - "/x/ywbR/"
    - "/katalon-studio/docs/introduction-to-desired-capabilities/"
description: 
---

**Desired Capabilities** are key/value pairs that tell the browser properties such as browser name, browser version, the path of the browser driver in the system, etc. to determine the browsers' behaviors at runtime. Desired capabilities which can be used to configure such additional driver instances as FirefoxDriver, ChromeDriver, InternetExplorerDriver, Selenium WebDriver are useful in the following cases:

* Setting the browser and device properties in mobile testing
* Adding extra settings to browsers in web testing

Katalon Studio allows you to define these Desired Capabilities in Project Settings.

## Understand the Settings

You need to identify which environment you want to customize its behaviors before defining desired capabilities in a Katalon project. Below is the list of supported environments as well as their locations in project settings:

### Remote

* Define Desired Capabilities for execution on a remote web server.
* **Project > Settings > Desired Capabilities > Remote**.

### Windows

* Define Desired Capabilities for execution on WinAppDriver.
* **Project > Settings > Desired Capabilities > Windows**.

### Custom

* Define a custom option for execution.
* **Project > Settings > Desired Capabilities > Custom**.

> If you want to make a list of your own custom Desired Capabilities for some environments, then it's suggested to use '**Custom**' settings in this case.

### WebUI

* Define Desired Capabilities for local execution using Chrome, Firefox, IE, Safari, or Edge.
* **Project > Settings > Desired Capabilities > WebUI > Chrome/Firefox/IE/Safari/Edge**.

### WebUI- Headless Browsers

* Define Desired Capabilities for execution with a headless instance using Chrome or Firefox.
* **Project > Settings > Desired Capabilities > WebUI >Chrome (Headless)/Firefox (Headless)**.

### Mobile

* Define Desired Capabilities for execution with Android or iOS devices.
* **Project > Settings > Desired Capabilities > Mobile > Android/iOS**.

## Configure Desired Capabilities in Katalon Studio

After selecting the environment, you can manage its desired capabilities with:

* **Add**: to add a new row to the **Desired Capabilities** list.
  * Provide the name of the property that you'd like to configure and its type.
  * Define value for the property. Refer to [Value Types](/display/KD/Value+Types) for details regarding how to input value for different types.
* **Delete**: to delete selected records.
* **Clear**: to clear all existing records.

### Desired Capabilities for Mobile testing 

You need to select the device when configuring Desired Capabilities.

![](https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/image2016-11-1-133A593A38.png)

Where:

* **Device Name**: the device to apply Desired Capabilities settings on.

### Desired Capabilities for Custom Execution

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

> Location of Desired Capabilities files
> 
> Defined configuration settings are saved in separated files under the "**<your test project location>\\settings\\internal**" location (or "**<your test project location>\\settings\\external\\execution**" in case of custom execution), as below:
> 
> | Driver | Settings' file |
> | --- | --- |
> | Chrome | com.kms.katalon.core.webui.chrome.properties |
> | Firefox | com.kms.katalon.core.webui.firefox.properties |
> | IE | com.kms.katalon.core.webui.ie.properties |
> | Safari | com.kms.katalon.core.webui.safari.properties |
> | Edge | com.kms.katalon.core.webui.edge.properties |
> | Remote Web | com.kms.katalon.core.webui.remote.properties |
> | Android | com.kms.katalon.core.mobile.android.properties |
> | iOS | com.kms.katalon.core.mobile.ios.properties |

Please refer to the specific guide below for the your preferred environment:

* [Desired Capabilities for Windows](https://docs.katalon.com/katalon-studio/docs/windows-desired-capabilities.html)
* [Desired Capabilities for Firefox/Firefox (headless)](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-for-firefoxfirefox-headless.html)
* [Desired Capabilities for Chrome/Chrome (headless)](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-for-chromechrome-headless.html)
* [Desired Capabilities for Internet Explorer](/display/KD/Desired+Capabilities+for+Internet+Explorer)
* [Remote Desired Capabilities](/display/KD/Remote+Desired+Capabilities)