---
title: "Pass Desired Capabilities at Runtime" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/desired-capabilities-at-runtime.html 
redirect_from:
description:
---

Desired capabilities configured at project settings are applied at the project level. You can also apply desired capabilities at the test case level by passing desired capabilities to the test script.
## Pass Desired Capabilities at Runtime

To apply desired capabilities at runtime, enter the following sample code before the test script. This also overrides the desired capabilities predefined in project settings.

```groovy
import com.kms.katalon.core.configuration.RunConfiguration
RunConfiguration.setWebDriverPreferencesProperty(<key>, <value>)
```

## Example

### Example 1

The following example demonstrates how to configure the desired capabilities at runtime to open a test case with window-sized 100x100 in Chrome. 

1. Open the test case in the script mode.

2. Pass the `window-size=100,100` argument to the sample code as follows. Then place the code before the test script. 

   ```groovy
   import com.kms.katalon.core.configuration.RunConfiguration
   RunConfiguration.setWebDriverPreferencesProperty("args", ["window-size=100,100"])
   ```

3. Continue writing the script or use Web Spy/Record Utility to complete your test case.
   
   <img src="url" width="70%" alt="DC at test script">

4. Run the test with Chrome.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/pass-dynamically-4.png" width="70%" alt="Run Chrome">

   > Make sure to update the browser by clicking **Tools** > **Update WebDrivers > Choose browser**. 

The test passes successfully with window-size 100x100.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/pass-dynamically-5.png" width="70%" alt="Passed test result">

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
import com.kms.katalon.core.configuration.RunConfiguration
RunConfiguration.setWebDriverPreferencesProperty('moz:firefoxOptions', '{args=[-private]}')

4.  Run the test with Chrome.

   <img src="url" width="70%" alt="DC at test script">

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/desired-capabilities-override-in-run-time/override-crop5-highlighted.png" width="70%" alt="Set DC in project settings">

The test passes successfully with Chrome window-size 100x100 (overriding Chrome window-size 1200x600).


**References:**

* [RunConfiguration](https://docs.katalon.com/javadoc/com/kms/katalon/core/configuration/RunConfiguration.html)

