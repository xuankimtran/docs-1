---
title: "[Mobile] Create Android Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/mobile-create-android-test-case.html
description: Create Android Test Case 
---

From version 7.6 onwards, Katalon Studio fully supports selector strategies supported by Appium except for [Android Data Matcher](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html). This tutorial helps you get familiar with the **Record** and **Playback** features for Mobile Tests by recording a scenario of sending a message via the **APIDemos.apk** application:

1. Launch **APIDemos.apk** on the device
2. Tap on **OS**
3. Tap on **SMS Messaging**
4. Enter a phone number and a message
5. Tap on **Send**

> APIDemos.apk and sample project code is available [here](https://github.com/katalon-studio-samples/sample-Android-demo-project).

### Create your first Android test case

**Record**

1. From the main Toolbar, click on the **Record Mobile** icon and select your device type, for instance, **Android Devices**

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android-devices.png" width=180>

2. In the displayed **Mobile Recorder** dialog, specify the information at the **Configurations** section:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/configurations.png" width=369>
   
   Where:

   * **Device Name**: select one of your connected Android devices.
   * **Start with**: In the drop-down list, select **Application File**
   * **Application File**: Browse **APIDemos.apk**

3. Click **Start** to begin recording your test case. Wait until the AUT is launched, and the **Device View** and **All Objects** are ready for you to interact with the application.
4. On **Device View**, click on **OS**; Katalon Studio selects **OS** in **All Objects** correspondingly.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/OS.png" width=727>

5. Once **OS** is selected, **Tap** is enabled in **Available Actions**, click **Tab**.

   Once **Tap** action is performed:

* The **Device View** is rendered with newly displayed elements.
* In **Recorded Actions**, **Tap** is added to the list of recorded test steps.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/tap1.png" width=361>
* In  **Captured Objects**, **OS** is captured with its properties.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/selector.png" width=362>

   > Important
   >
   > The most important property of an object is its locator strategy and value. The default locator is a unique value in detecting that object. Katalon Studio 7.6+ fully supports selector strategies supported by Appium except for Android Data Matcher ([Learn more](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html)). If you prefer another locator strategy among the provided options, you can choose it and generate a new locator. Then click **Highlight** to see if your newly updated locator can detect the target object on its screen correctly.

7. Similarly, in **Device View**, select **SMS Messaging**; in **Available Actions**, select **Tap**. Observe the **Recorded Actions** table; you can see another Tap item is added to the list.
8. To continue, in **Device View**, select the text input area right next to the **Recipient** object; in **Available Actions**, click on the **Set Text** action. In the displayed **Text Input** dialog, enter a phone number and click **OK**. Observe **Device View**; you can see a phone number is filled in the text field.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/set-text1.png" width=1097>

9. In **Device View**, select the text input area right next to the **Message Body** object; in **Available Actions**, click on the **Set Text** action. In the displayed **Text Input** dialog, enter any message, for instance, "Hello world! This is Katalon Mobile Recorder", and click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/set-text2.png" width=1100>

* In **Device View**, you can see the message is set in the text field.
* In **Recorded Actions**, **Set Text** is added to the table.

10. In **Device View**, select **Send**; in **Available Actions**, select **Tap**.

   > If you launch **APIDemos.apk** application on a real device with a carrier, the message can be sent successfully.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/send.png" width=1097>

11. After finishing recording the desired interactions with the AUT, click **OK** to save the captured objects. In the **Folder Browser** dialog, create a new folder or select an existing folder in **Object Repository**, then click **OK**.

12. You can add the recorded test steps to a new test case or append to/overwrite an existing one.
   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/new-tc.png" width=500>

**Playback**

To playback the recorded scenario:

1. Select the test case where you have saved the recorded actions
2. From the main Toolbar, open the drop-down list next to the **Run** button and to select a mobile device type

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/run.png" width=703>

3. In the displayed dialog, select a device and click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-mobile-utility/device.png" width=452>

   Katalon Studio executes the mobile test with the recorded steps accordingly.

You can also view the test case in Script mode:

```groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject

import com.kms.katalon.core.configuration.RunConfiguration
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.model.FailureHandling as FailureHandling

'Start the Application'
Mobile.startApplication(RunConfiguration.getProjectDir() + '/APIDemos.apk', true)

'Tap on OK if this is the first time this application is launched on an Android 9+ device'
Mobile.tap(findTestObject('Object Repository/APIDemo/android.widget.Button - OK'), 0, FailureHandling.OPTIONAL)

'Tap on text "OS"'
Mobile.tap(findTestObject('Object Repository/APIDemo/android.widget.TextView - OS'), 0)

'Tap on text "SMS Messaging"'
Mobile.tap(findTestObject('Object Repository/APIDemo/android.widget.TextView - SMS Messaging'), 0)

'Enter a phone number in Recipient text box'
Mobile.setText(findTestObject('Object Repository/APIDemo/android.widget.EditText'), '+84345678910', 0)

'Enter a message in Body Message text box'
Mobile.setText(findTestObject('Object Repository/APIDemo/android.widget.EditText (1)'), 'Hello world! This is Katalon Mobile Recorder', 0)

'Send the message'
Mobile.tap(findTestObject('Object Repository/APIDemo/android.widget.Button - Send'), 0)

'Close the Application'
Mobile.closeApplication()

```