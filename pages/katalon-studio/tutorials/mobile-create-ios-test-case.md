---
title: "[Mobile] Create iOS Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/mobile-create-ios-test-case.html
description: Create iOS Test Case 
---

From version 7.6 onwards, Katalon Studio fully supports selector strategies supported by Appium. 

This tutorial helps you get familiar with the **Record** and **Playback** features for Mobile Tests by recording a scenario of sending a message via the **APIDemos.ipa** application:

1. Launch **APIDemos.ipa** on the device.
2. Tap on **OS**.
3. Tap on **SMS Messaging**.
4. Enter a phone number and a message.
5. Tap on **Send**.

> APIDemos.ipa and sample project code is available [here](https://github.com/katalon-studio-samples/ios-mobile-tests).


## Create your first iOS test case

### Create New Project

1. In the **Test Explorer** on the sidebar > click **New Project**.

2. In the displayed **New Project** dialog:

   - Input project **Name**.
   - In project **Type** > select **Mobile**.
   - In **Project** > select **Sample iOS...**, the **Repository URL** is filled automatically.
   - Browse a **Location** to store your project > click **OK**.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/create-new-project-with-sample-project.png" width=70%>
**Record**

1. From the main toolbar, click on the **Record Mobile** icon and select your device type. For example, **iOS Devices**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/record-iOS.png" width=20%>

2. In the displayed **Mobile Recorder** dialog, specify the information at the **Configurations** section:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/configuration.png" width=50%>

   * **Device Name**: select one of your connected iOS  devices.
   * **Start with**: In the drop-down list, select **Application File**.
   * **Application File**: Browse **Coffee Timer.ips**.

3. Click **Start** to begin recording your test case: 

   * Wait until the AUT is launched. 
   * The **Device View** and **All Objects** are ready for you to interact with the application.

4. The recorded steps and captured objects will be generated respectively in **Recorded Actions** and **Captured Objects**.

5. Stop recording and save your script.

> Click [here](https://docs.katalon.com/katalon-studio/docs/mobile-recorder-tutorials.html) for a detailed tutorial.






## Create first iOS Test Case

1. Click <img alt="Native Windows Recorder without coordinates" src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-web-utility/Screen-Shot-2018-06-27-at-09.41.37.png" width=5%> icon to open Katalon Web Utility. The *Web recorder* dialog will be displayed.
2. Enter a URL of your web application (e.g., https://amazon.com/) and select a browser to start recording. The browser instance will be launched automatically.
3. Once the web page is loaded, interact with its elements. Your interaction will be generated automatically in Recorded Actions.
4. To stop recording, click *Stop* or go straight to *Save Script*. The browser will be closed automatically.
5. Choose where to store your script in the *Add element to Object Repository* dialog and click *OK*.
6. Input Name, Descripton and Tag (if any) in the *Test Case* dialog and click *OK*. Your test case is successfully created.
