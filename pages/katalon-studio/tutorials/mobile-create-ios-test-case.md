---
title: "[Mobile] Create and Run iOS Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/mobile-create-ios-test-case.html
description: Create and Run iOS Test Case 
---

This tutorial demonstrates how to create iOS tests with Katalon Studio using **Record** and **Playback**.

To get familiar with these features, go through the "Recording a scenario of counting down the via the Coffee Timer.ipa application" scenario. The basic steps are:
1. Launch **Coffee Timer.ipa** on the device.
2. Tap on **Green Tea**.
3. Tap on **Start**.

> Coffee Timer.ipa and sample project code is available [here](https://github.com/katalon-studio-samples/ios-mobile-tests).

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

1. On the main toolbar, click on the **Record Mobile** icon and select your device type. For example, **iOS Devices**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/record-iOS.png" width=20%>

2. In the displayed **Mobile Recorder** dialog, specify the information at the **Configurations** section:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/configuration.png" width=50%>

   * **Device Name**: select one of your connected iOS  devices.
   * **Start with**: select **Application File** in the drop-down list.
   * **Application File**: Browse **Coffee Timer.ips**.

3. Click **Start** to begin recording your test case: 

   * Wait until the AUT is launched. 
   * The **Device View** and **All Objects** are ready for you to interact with the application.

4. The recorded steps and captured objects will be generated respectively in **Recorded Actions** and **Captured Objects**.

5. Stop recording and save your script.

> Click [here](https://docs.katalon.com/katalon-studio/docs/mobile-recorder-tutorials.html) for a detailed tutorial.
