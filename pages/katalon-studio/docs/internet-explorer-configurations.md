---
title: "Internet Explorer Configurations" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/internet-explorer-configurations.html 
redirect_from:
    - "/display/KD/Internet+Explorer+Configurations/"
    - "/display/KD/Internet%20Explorer%20Configurations/"
    - "/x/iwEo/"
    - "/katalon-studio/docs/internet-explorer-configurations/"
    - "/katalon-studio/tutorials/configure_katalon_studio_web_automation_test_project.html"
description: 
---

> Notes:
> 
> * Katalon Studio only supports Internet Explorer 9,10,11 in Windows. 
> * You can configure Internet Explorer at the project level with desired capabilities here: [Desired capabilities for IE](https://docs.katalon.com/katalon-studio/docs/desired-capabilities-settings-webui.html/#internet-explorer)

To run tests on Internet Explorer (IE), you need the following setups:

1.  **Enable Protected Mode** must be disabled for all available zones. 
    
    To do so, choose **Internet Options** from **Control Panel**, then switch to the **Security** tab. Uncheck the **Enable Protected Mode** box.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/internet-explorer-configurations/cypgm2bz42y8.png" width="60%" alt="Uncheck the enable protecte mode box">

2.  Zoom the IE browser to 100% so that native mouse events can be set to correct coordinates.  

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/internet-explorer-configurations/image2017-2-20-153A123A18.png" width="70%" alt="Zoom browser to 100%">

3.  For IE 11, you also need to set a registry entry on the target computer so that the driver can maintain a connection to the Internet Explorer instances. To do so, follow these steps:

    - To open the **Registry Editor**, type `regedit` into **Command Prompt**.
            
    - Locate the **FEATURE_BFCACHE** subkey. If you cannot find the **FEATURE_BFCACHE** subkey, create one.

      - For 32-bit Windows, the key is at _`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Internet Explorer\Main\FeatureControl\FEATURE_BFCACHE`_. 
      - For 64-bit Windows, the key is at _`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Internet Explorer\Main\FeatureControl\FEATURE_BFCACHE`_. 

    - Inside this subkey, create a **DWORD** value called **`iexplore.exe`** with the value of **0**.  

        <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/internet-explorer-configurations/image2016-10-24-163A143A28.png" width="70%" alt="Create DWORD value">

**Next step:**

After setting up Internet Explorer, you can begin creating your first WebUI tests. You can refer to the following document for further details: 
* [Create test cases using Record Web Utility](https://docs.katalon.com/katalon-studio/docs/record-web-utility.html#record-a-new-test-case)
* [Create test cases using Spy Web Utility](https://docs.katalon.com/katalon-studio/docs/spy-web-utility.html)