---
title: "[Mobile] Create and Run iOS Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/mobile-create-ios-test-case.html
description: Create and Run iOS Test Case 
---

This tutorial demonstrates how to create iOS tests with Katalon Studio using **Record** and **Playback**.

Go through the "Recording a scenario of counting down Green Tea making time via the Coffee Timer.ipa application" to get familiar with these features. The basic steps are:

1. Launch **Coffee Timer.ipa** on the device.
2. Tap on **Green Tea**.
3. Tap on **Start**.
4. Tap on **Stop**.

> **Coffee Timer.ipa** and sample project code is available [here](https://github.com/katalon-studio-samples/ios-mobile-tests).

## Create and Run your first iOS test case

### Create New Project

1. In the **Test Explorer** on the sidebar > click **New Project**.

2. In the displayed **New Project** dialog:

   - Input project **Name**.
   - In project **Type** > select **Mobile**.
   - In **Project** > select **Sample iOS...**, the **Repository URL** is filled automatically.
   - Browse a **Location** to store your project > click **OK**.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/create-new-project-with-sample-project.png" width=60%>

**Record**

1. On the main toolbar, click on the **Record Mobile** icon and select your device type. For example, **iOS Devices**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/record-iOS.png" width=20%>

2. In the displayed **Mobile Recorder** dialog, specify the information at the **Configurations** section:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/configuration.png" width=40%>

   * **Device Name**: select one of your connected iOS  devices.
   * **Start with**: select **Application File** in the drop-down list.
   * **Application File**: Browse **Coffee Timer.ipa**.

3. Click **Start** to begin recording your test case: 

   * Wait until the AUT is launched. 
   * The **Device View** and **All Objects** are ready for you to interact with the application.

4. On the **Device View** > click **Green Tea**, Katalon Studio selects **Green Tea** in **All Objects** correspondingly.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/Green%20Tea.png" width=55%>

5. The recorded steps and captured objects will be generated respectively in **Recorded Actions** and **Captured Objects**.

6. Once **Green Tea** is selected, **Tap** is enabled in **Available Actions** > click **Tab**, the tap action is performed as follows:

   * The **Device View** is rendered with newly displayed elements.
   * In **Recorded Actions**, **Tap** is added to the list of recorded steps.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/recorded-action.png" width=55%>


   * In **Captured Objects**, **Green Tea** is captured with its properties.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/captured-object.png" width=55%>

   > **Note**
   >
   > - The essential property of an object is its locator strategy and value. The default locator is a unique value in detecting that object. Katalon Studio 7.6+ fully supports selector strategies supported by Appium.
   >
   >   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/locator.png" width=50%>
   > - If you prefer another locator strategy, select your prefered one and generate a new locator > click **Highlight** to see if your newly updated locator can detect the target object on its screen correctly.

7. Similarly in **Device View**, click **Start** > click **Tap** in **Available Actions**.

   You can see another tap action is added to the list of **Recorded Actions** and **Captured Objects**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/start-action.png" width=60%>

8. In **Device View**, click **Stop** > click **Tap** in **Available Actions**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/stop-action.png" width=60%>

9. Click on the **Stop** button above the **CONFIGURATIONS** section to close the application and finish recording.

   After finishing recording the desired interactions with the AUT, click **Save script** to save the captured objects. 

      In the displayed **Folder Browser** dialog, create a new folder or select an existing folder in **Object Repository** > click **OK**.

10. You can add the recorded test steps to a new test case, append to or overwrite an existing one.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/save-script.png" width=55%>

### Playback

To playback the recorded scenario:

1. Select the test case where you saved the recorded actions.
2. On the main toolbar, select **iOS** device on the drop-down list next to **Run**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/select-ios.png" width=20%>

3. In the displayed **iOS Devices** dialog, select a device > click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/ios-devices-list.png" width=55%>

Katalon Studio executes the iOS test with the recorded steps accordingly.

Next: [Execute and Debug a Test Case](https://docs.katalon.com/katalon-studio/docs/execute-a-test-case-or-a-test-suite.html#execute-a-test-case).

Previous: [[Mobile] iOS Setup](https://docs.katalon.com/katalon-studio/tutorials/mobile-ios-setup.html).

   See also:
   * [Create and Run your first Android test case](http://docs.katalon.com/katalon-studio/tutorials/mobile-create-android-test-case.html).
   * [Troubleshoot automated mobile testing](https://docs.katalon.com/katalon-studio/docs/troubleshooting-automated-mobile-testing.html).