---
title: "Spy and Record Utilities for testing an existing application"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/mobile-spy-record-existing-apps.html
description: "Support spying and recording an existing app"
---
> Starting with **Katalon Studio version 6.3.0**, you can spy and record testing an installed application on Android and iOS devices, NOT on Kobiton and remote ones.

1. Open **Mobile Object Spy**/**Mobile Recorder** with Android or iOS devices.

2. In configurations, you can start spying or recording on an existing application with an application ID. Select **Application ID**, enter the application ID in the corresponding text field, the **Start** button will be enabled.

    **Application ID** is the ID of the application file (.apk; .ipa) after being uploaded  to the cloud. The Kobiton’s application ID, for instance, is **kobiton-store:23616**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-testing-cloud-devices/2-AppID.png" width="393" height="210">

In **Mobile Recorder**

* In **Recorded Actions**, the first action is **Start Existing Application**.

* After you press **OK** button to finish its recording session, Katalon Studio will generate script with `Mobile.startExistingApplication(appId)`.
