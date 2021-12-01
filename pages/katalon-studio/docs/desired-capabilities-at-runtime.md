---
title: "Pass Desired Capabilities at Runtime" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/desired-capabilities-at-runtime.html 
redirect_from:
    - "/display/KD/Override+desired+capabilities+at+runtime/"
    - "/display/KD/Override%20desired%20capabilities%20at%20runtime/"
    - "/x/dwXR/"
    - "/katalon-studio/docs/override-desired-capabilities-at-runtime/"
    - "/katalon-studio/docs/override-desired-capabilities-at-runtime.html"
description:
---

Desired capabilities configured at project settings are applied at the project level. You can also use desired capabilities at the test case level by passing desired capabilities to the test script.
## Pass Desired Capabilities at Runtime for WebUI Testing

To apply desired capabilities at runtime, place the following sample code before the test script. This also overrides the desired capabilities predefined in project settings.

```groovy
import com.kms.katalon.core.configuration.RunConfiguration
RunConfiguration.setWebDriverPreferencesProperty(<key>, <value>)
```
### Open Firefox browser in private mode

The following example demonstrates how to configure the desired capabilities at runtime to open a test case in private mode in Firefox. 

1. Open the test case in script mode.

2. Pass the `-private` argument to the sample code as follows. Then place the code before the test script. 

   ```groovy
   import com.kms.katalon.core.configuration.RunConfiguration
   Map firefoxOptions =[args:"-private"]
   RunConfiguration.setWebDriverPreferencesProperty('moz:firefoxOptions', firefoxOptions)
   ```

3. Continue writing the script or use Web Spy/Record Utility to complete your test case.
   
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/KS-DC-firefox-private-mode-runtime.png" width="70%" alt="DC at test script">

4. Run the test with Firefox.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/KS-DC-run-with-firefox.png" width="70%" alt="Run Firefox">

   > Make sure to update the browser by clicking **Tools** > **Update WebDrivers > Choose browser**. 

   The test successfully opens a Firefox browser in private mode.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/KS-DC-Open-firefox-private.png" width="70%" alt="Open Firefox in private mode">

### Override desired capabilities in project settings 

Suppose you want to override desired capabilities pre-configured in project settings; you can use the above sample code in the test script.

The following example demonstrates how to override Chrome window-sized 1200x600 and run the test with Chrome window-sized 100x100 in private mode instead.

1. After defining the desired capabilities for Chrome window-sized 1200x600 in **Project > Setting > Desired Capabilities > Web UI > Chrome**, click **Apply and Close**.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/override-crop0.png" width="70%" alt="Set DC in project settings">

      <img src="https://github.com/Yen8298/docs-images/raw/da382cef70da7f464af14a6d7e8765c7cca37562/katalon-studio/docs/desired-capabilities-override-in-run-time/KS-DC-window-size-1200x600-settings.png" width="70%" alt="Set DC in project settings">

2. To override the desired capabilities at runtime, open the test case in script mode. Pass the desired capabilities to the same key with the capabilities defined in project settings. Then place the code before the test script. 

      Here, we want to override the `--window-size=1200,600` capabilities. We pass the `--window-size=100,100` and `--incognito` capabilities to the `args` key in the sample code as follows. Then place the code before the test script. 
      
      ```groovy
      import com.kms.katalon.core.configuration.RunConfiguration
      RunConfiguration.setWebDriverPreferencesProperty("args", ["--window-size=100,100","--incognito"])
      ```
3. Continue writing the script or use Web Spy/Record Utility to complete your test case.
   
      <img src="https://github.com/Yen8298/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/KS-DC-window-sized-100x100-incognito-runtime.png" width="70%" alt="DC at test script">

4.  Run the test with Chrome.

      <img src="https://github.com/Yen8298/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/KS-DC-Chrome-windows-100x100-incognito-run.png" width="70%" alt="Set DC in project settings">

      The test successfully opens a Chrome window-size 100x100 in private mode (overriding Chrome window-size 1200x600).
## Pass Desired Capabilities at Runtime for Remote execution

To apply desired capabilities at runtime, place the following sample code before the test script. This also overrides the desired capabilities predefined in project settings.

```groovy
import com.kms.katalon.core.configuration.RunConfiguration
RunConfiguration.setDriverPreferencesProperty('Remote',  capsName , capsValue)  

```

For example, we want to set remote execution environment as Windows 10, enter the following sample code before the test script:

```groovy
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.configuration.RunConfiguration

RunConfiguration.setDriverPreferencesProperty('Remote', 'os', 'Windows')  
RunConfiguration.setDriverPreferencesProperty('Remote', 'os_version', '10')  

WebUI.openBrowser('google.com')
```


**References:**

* [RunConfiguration](https://docs.katalon.com/javadoc/com/kms/katalon/core/configuration/RunConfiguration.html)

