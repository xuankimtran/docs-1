---
title: "[Mobile] Create Android Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/mobile-create-android-test-case.html
description: Create Android Test Case 
---

This tutorial demonstrates how to create Android tests with Katalon Studio using **Record** and **Playback**.

To get familiar with these features, go through the following "Recording a scenario of sending a message via the APIDemos.apk application" example. The basic steps are:

1. Launch **APIDemos.apk** on the device.
2. Tap on **OS**.
3. Tap on **SMS Messaging**.
4. Enter a phone number and a message.
5. Tap on **Send**.

> APIDemos.apk and sample project code is available [here](https://github.com/katalon-studio-samples/android-mobile-tests).

## Create your first Android test case

### Create New Project

1. In the **Test Explorer** on the sidebar > click **New Project**.

2. In the displayed **New Project** dialog:

   - Input project **Name**.
   - In project **Type** > select **Mobile**.
   - In **Project** > select **Sample Android...**, the **Repository URL** is filled automatically.
   - Browse a **Location** to store your project > click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android/create-new-project-with-sample-project.png" width=85%>

### Record

1. On the main toolbar, click **Record Mobile** > select **Android Devices**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android-devices.png" width=30%%>

2. In the displayed **Mobile Recorder** dialog, specify the information at the **Configurations** section:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android/configure.png" width=70%>

   * **Device Name**: select one of your connected Android devices.
   * **Start with**: Select **Application File** in the drop-down list.
   * **Application File**: Browse **APIDemos.apk**.

3. Click **Start** to begin recording your test case: 

   * Wait until the AUT is launched. 
   * The **Device View** and **All Objects** are ready for you to interact with the application.

4. On the **Device View** > click **OS**, Katalon Studio selects **OS** in **All Objects** correspondingly.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android/os.png" width=85%>

5. Once **OS** is selected, **Tap** is enabled in **Available Actions** > click **Tab**, the tap action is performed as follows:

   * The **Device View** is rendered with newly displayed elements.
   * In **Recorded Actions**, **Tap** is added to the list of recorded steps.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android/tap.png" width=80%>

   * In **Captured Objects**, **OS** is captured with its properties.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android/captured.png" width=80%>

   > **Note**
   >
   > - The essential property property of an object is its locator strategy and value. The default locator is a unique value in detecting that object. Katalon Studio 7.6+ fully supports selector strategies supported by Appium except for Android Data Matcher ([Learn more](https://docs.katalon.com/katalon-studio/docs/locators_object_identification.html)).
   >
   >   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android/locator-strategy.png" width=70%>
   > - If you prefer another locator strategy, select your prefered one and generate a new locator > click **Highlight** to see if your newly updated locator can detect the target object on its screen correctly.

6. Similarly in **Device View**, click **SMS Messaging** > click **Tap** in **Available Actions**.

   You can see another tap action is added to the list of **Recorded Actions** and **Captured Objects**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android/sms-messaging.png" width=85%>

7. In **Device View**, select the text input area right next to **Recipient** > click **Set Text** in **Available Actions**.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android/text-input.png" width=85%>

   In the displayed **Text Input** dialog, enter a phone number > click **OK**. 
You can see a phone number is filled in the text field in **Device View**.

8. In **Device View**, select the text input area next to the **Message Body** > click **Set Text** in **Available Actions**.
   
   In the displayed **Text Input** dialog, enter any message > click **OK**. 
   
   You can see the message is set in the text field in **Device View** and the **Set Text** is added to the 
   **Recorded Actions**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/set-text2.png" width=85%>

9. In **Device View**, click **Send** > click **Tap** in **Available Actions**.

   > If you launch the **APIDemos.apk** application on a real device with a carrier, the message can be sent successfully.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/send.png" width=85%>

10. After finishing recording the desired interactions with the AUT, click **OK** to save the captured objects. 

      In the **Folder Browser** dialog, create a new folder or select an existing folder in **Object Repository** > click **OK**.

11. You can add the recorded test steps to a new test case, append to or overwrite an existing one.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/new-tc.png" width=85%>

### Playback

To playback the recorded scenario:

1. Select the test case where you saved the recorded actions.
2. On the main toolbar, select **Android** device on the drop-down list next to **Run**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android/android.png" width=35%>

3. In the displayed **Android Devices** dialog, select a device > click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/Android/device.png" width=85%>

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