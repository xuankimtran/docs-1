---
title: "Testing Mobile Apps Using Custom Cloud Devices"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-testing-apps-cloud-devices.html
description: "Support spying, recording and running Mobile script on custom Cloud devices"
---

## Execution

Starting with **Katalon Studio version 6.3.0**, you can test your mobile applications on such custom cloud devices as Sauce Labs, BrowserStack,..

Katalon Studio supports running a Mobile script on both remote and custom cloud devices.

> Notes: Generate Command dialog doesn't require the **Remote Server URL** and **Remote Server Type**, Katalon Studio uses the current settings of Remote execution.

## Mobile Object Spy and  Mobile Recorder

Starting with **Katalon Studio version 6.3.0**, *Mobile Object Spy* and *Mobile Recorder* are available on remote devices (not custom devices).

### Remote Devices

In addition to Android, iOS and Kobiton devices, a new tool item **Remote Devices** is added to the UI of Mobile Object Spy and  Mobile Recorder.

### Configure a remote device

You can configure a remote device in 2 ways:

* **Project** -> **Settings** -> **Desired Capabilities** -> **Remote** -> Enter the server URL, server type and desired capabilities.

* Select **Mobile Object Spy**/**Mobile Recorder** -> **Remote Devices**. In the configurations field, click **Edit**. In the pop-up, users can enter the server URL, server type and desired capabilities.

### Enter a Cloud Application ID

**Cloud Application ID** is the ID of the application file (.apk; .ipa) after being uploaded  to the cloud. The Kobiton’s application ID, for instance, is **kobiton-store:23616**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-testing-cloud-devices/2-AppID.png" width="393" height="210">

After you enter the application ID, the **Start** button is enabled.
