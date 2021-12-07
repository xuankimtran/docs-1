---
title: "Set up desired capabilities in Windows Desktop App testing" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/desired-capabilities-settings-windows.html 
redirect_from:
    - "/katalon-studio/docs/windows-desired-capabilities.html"
description:
---

This article shows you how to configure desired capabilities for Windows Desktop Application testing.

> Notes:
>
> * From version 7.0.0 onwards, Windows Desktop Application testing is available.
> * From version 7.5.0 onwards, Native Windows Recorder is available for Katalon Studio Enterprise users.
> * From version 7.7.0 onwards, desired capabilities for Native Windows Recorder are available.
## Set desired capabilities for Windows Desktop Application testing 

To set desired capabilities for Windows Desktop Application testing, do as follows:

1. Go to **Project > Settings > Desired Capabilities > Windows**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/windows-desired-capabilities/desired-capa-win.png"  width="70%" alt="DC settings for Windows">

   Alternatively, you can also edit desired capabilities settings via a Windows execution session. Start a **Spy Windows/ Windows Recorder/ Native Windows Record** session, in the **Configuration** box, click **Edit**.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/KS-DC-alternative-way-to-dc-settings.png"  width="90%" alt="Alternative way to change DC settings">

2. Enter **WinAppDriver URL**: `http://<ip-address>:<port>` - URL to the WinAppDriver server. By default, Katalon Studio is set to `http://127.0.0.1:4723`.

3. Click **Add** on the command toolbar to add desired capabilities.
   
   Katalon Studio supports the same capabilities as WinAppDriver does. To learn more about supported capabilities for Windows Desktop App testing, you can refer to the WinAppDriver document here: [Supported capabilities](https://github.com/microsoft/WinAppDriver/blob/master/Docs/AuthoringTestScripts.md#supported-capabilities). 
   
   For Native Windows Recorder, only `appArguments` and `appWorkingDir` capabilities are supported.
   * `appArguments`: Support passing arguments to the Application Under Test. You can also use this desired capabilities to record action without opening a Windows.
   * `appWorkingDir`: Specify the Application Under Test working directory.

## Example uses
### Example 1: set delaying time for an app launch

The following example shows you how to set desired capabilities to wait for a defined amount of time before initiating an app launch.

> Requirements:
> * Download and install WinAppDriver version 1.2 onwards. You can refer to this document to install WinAppDriver: [Set up WinAppDriver](https://docs.katalon.com/katalon-studio/docs/setup-winappdriver.html).

Go to the desired capabilities settings, click **Add**, then input the following value:

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
      <td>ms:waitForAppLaunch</td>
      <td>string</td>
      <td>25(*)</td>
   </tr>
   </tbody>
   </table>
(*) <em>This means delaying the app launch for 25 seconds. You can set 50 seconds in maximum.</em>

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/KS-DC-Native-recorder-windows-final-results.png"  width="796" alt="Delay app launch">

### Example 2: set desired capabilities in Native Windows Recorder

The following example shows you how to set desired capabilities in Native Windows Recorder. 

1. Open a **Native Windows Record** session. In the **Configuration** box, click **Edit**.
2. In the pop-up dialog, click **Add**, then input the following value:

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
      <td>appWorkingDir</td>
      <td>string</td>
      <td>C:\User\thongnmtran\Desktop\workspace\katalon<td>
   </tr>
   <tr>
      <td>appArguments</td>
      <td>List</td>
      <td>--arg1,--arg2<td>
   </tr>
   </tbody>
   </table>

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/KS-DC-Native-recorder-windows-dc-settings.png" width="70%" alt="Set DC for Native Windows Recorder">

   Click **Apply and Close** when you finish. The results should be as follows:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-to-desired-capabilities/use-windows-capabilities.png" width="70%" alt="Results">
