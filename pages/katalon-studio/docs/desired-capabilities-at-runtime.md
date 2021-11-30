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

Desired capabilities configured at project settings are applied at the project level. You can also apply desired capabilities at the test case level by passing desired capabilities to the test script.
## Pass Desired Capabilities at Runtime

To apply desired capabilities at runtime, place the following sample code before the test script. This also overrides the desired capabilities predefined in project settings.

```groovy
import com.kms.katalon.core.configuration.RunConfiguration
RunConfiguration.setWebDriverPreferencesProperty(<key>, <value>)
```


### Example 1

The following example demonstrates how to configure the desired capabilities at runtime to open a test case with in private mode in Firefox. 

1. Open the test case in the script mode.

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

### Example 2

Suppose you want to override desired capabilities pre-configured in project settings, you can use the above sample code in the test script.

The following example demonstrates how to override Chrome window-sized 1200x600 and run the test in Chrome window-sized 100x100 instead.

1. Go to **Project > Setting > Desired Capabilities > Web UI > Chrome**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/override-crop0.png" width="70%" alt="Set DC in project settings">

2. Enter the following value, then click **Apply and Close**.

      <table>
   <thead>
   <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Value</th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td>args</td>
      <td>List</td>
      <td>window-size=1200,600</td>
   </tr>
   </tbody>
   </table>

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/override-crop2.png" width="70%" alt="Set DC in project settings">

3. To override the desired capabilities at runtime, open the test case in the script mode. Pass the `window-size=100,100` argument to the sample code as follows. Then place the code before the test script. 
   
   ```groovy
   import com.kms.katalon.core.configuration.RunConfiguration
   RunConfiguration.setWebDriverPreferencesProperty("args", ["window-size=100,100"])
   ```
4. Continue writing the script or use Web Spy/Record Utility to complete your test case.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/KS-DC-windows-100x100-chrome.png" width="70%" alt="DC at test script">

5.  Run the test with Chrome.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/override-crop5-highlighted.png" width="70%" alt="Set DC in project settings">

The test passes successfully with Chrome window-size 100x100 (overriding Chrome window-size 1200x600).


**References:**

* [RunConfiguration](https://docs.katalon.com/javadoc/com/kms/katalon/core/configuration/RunConfiguration.html)

