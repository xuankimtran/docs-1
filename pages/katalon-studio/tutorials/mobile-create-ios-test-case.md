---
title: "[Mobile] Create and Run iOS Test Case"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/tutorials/mobile-create-ios-test-case.html
description: Create and Run iOS Test Case 
---

This tutorial demonstrates how to create iOS tests with Katalon Studio using Mobile Record Utility, then run the recorded test case.

> Requirements:
> * iOS setup. To set up Xcode simulators/ real iOS devices, you can refer to this document: [[Mobile] iOS Setup](https://docs.katalon.com/katalon-studio/tutorials/mobile-ios-setup.html).

In this example, we record the following actions to test the **Coffee Timer** application:

1. Launch the **Coffee Timer** application on the device.
2. Tap on **Green Tea**.
3. Tap on **Start**.
4. Tap on **Stop**.

> You can download the sample project as a .zip file here: [iOS Mobile Tests](https://github.com/katalon-studio-samples/ios-mobile-tests).
### Create a new project

1. To create a new project, go to **File > New > New Project**.

2. Fill in the displayed **New Project** dialog as shown below:

   <table>
   <tbody>
   <tr>
   <td><strong>Name</strong></td>
   <td>The project name</td>
   </tr>
   <tr>
   <td><strong>Type</strong></td>
   <td>The project type. In this example, we choose the&nbsp;<strong>Mobile&nbsp;</strong>project type.</td>
   </tr>
   <tr>
   <td>
   <div>
   <div><strong>Project</strong></div>
   </div>
   </td>
   <td>This section allows you to choose a sample project. If you don't want to open a sample project, select the&nbsp;<strong>Blank</strong> option. In this example, we choose the <strong>Sample iOS Mobile Tests Project </strong>project<strong>.</strong></td>
   </tr>
   <tr>
   <td>
   <div>
   <div>
   <div>
   <div><strong>Repository URL</strong></div>
   </div>
   </div>
   </div>
   </td>
   <td>The Github repository URL. After choosing the sample project, Katalon automatically fills in the URL</td>
   </tr>
   <tr>
   <td>
   <div>
   <div>
   <div>
   <div>
   <div>
   <div><strong>Location</strong></div>
   </div>
   </div>
   </div>
   </div>
   </div>
   </td>
   <td>&nbsp;The save location of your project.&nbsp;</td>
   </tr>
   </tbody>
   </table>

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/create-new-project-with-sample-project.png" width=70%>

3. After filling in the project details, click **OK**. A new mobile project opens.

### Record a new Test Case

1. On the main toolbar, click **Record Mobile** <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/KS-iOS-record-mobile-icon.png" width=4% alt="Record Mobile icon"> and select your device type. For our example, we choose the **iOS Devices** option.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/record-iOS.png" width=30%>

2. In the displayed **Mobile Recorder** dialog, specify the information in the **Configurations** section:

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/configuration.png" width=65%>

   <table width="927">
   <tbody>
   <tr>
   <td>
   <div>
   <div><strong>Device Name</strong></div>
   </div>
   </td>
   <td>
   <div>
   <div>To select one of your connected iOS devices or Xcode simulators</div>
   </div>
   </td>
   </tr>
   <tr>
   <td>
   <div>
   <div>
   <div>
   <div><strong>Start with</strong></div>
   </div>
   </div>
   </div>
   </td>
   <td>
   <div>
   <div>To select <strong>Application File</strong> in the drop-down list.</div>
   </div>
   </td>
   </tr>
   <tr>
   <td>
   <div>
   <div>
   <div>
   <div>
   <div>
   <div><strong>Application File</strong></div>
   </div>
   </div>
   </div>
   </div>
   </div>
   </td>
   <td>
   <p>For Xcode simulators: browse <code>Coffee Timer.app</code></p>
   <p>For real iOS devices: browse <code>Coffee Timer.ipa</code></p>
   </td>
   </tr>
   </tbody>
   </table>

3. Click **Start** to begin recording your test case. After the application under test (AUT) is launched, you can now see:

   -  **Device View**: this section displays the start page of your AUT. You can interact with the **Device View** section the same way as in a real iOS device.
   -  **All Objects**: this section displays all objects of the current view in the **Device View** section.

4. In the **Device View** section, click **Green Tea**. Katalon Studio correspondingly selects the **Green Tea** object in the **All Objects** section.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/Green%20Tea.png" width=65%>

5. Once **Green Tea** is selected, click the **Tab** action in the **Available Action** section, you will see:

   * The **Device View** section displays the countdown for **Green Tea**.
   * Katalon automatically adds the **Tap** action to the list of recorded steps in the **Recorded Actions** tab.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/recorded-action.png" width=65%>

   * Katalon also captures the **Green Tea** object properties including in the **Captured Objects** tab. To learn more about mobile object properties, you can refer to this document: [Manage Mobile Test Objects](https://docs.katalon.com/katalon-studio/docs/manage-mobile-test-object.html#validate-test-object-on-aut).

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/captured-object.png" width=65%>

   > Notes:
   > * Select your preferred one if you prefer another locator strategy, then click **Generate** to generate a new locator. You can also check if your newly updated locator can detect the target object correctly by clicking **Highlight**.
   >  <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/locator.png" width=70%>

6. Similarly, click **Start** in the **Device View** section, then click **Tap** in the **Available Actions** section. 
   
    Katalon automatically adds another **Tap** action to the list of **Recorded Actions** and the **Start** object properties in the **Captured Objects** tab.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/start-action.png" width=70%>

7. Next, click **Stop** in the **Device View** section, then click **Tap** in the **Available Actions** section. 

   Katalon automatically adds another **Tap** action to the list of **Recorded Actions** and the **Stop** object properties in the **Captured Objects** tab.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/stop-action.png" width=70%>

8.  Click **Save script**. An open dialog asks you to save captured objects into the Object Repository of Katalon Studio. You can create a new folder or select an existing folder in **Object Repository**, then click **OK**.

9.  A dialog opens, providing you three options to save your recorded test:

   <table>
   <tbody>
   <tr>
   <td><strong>Export to new test case</strong></td>
   <td>To export the recorded test steps to a new test case.</td>
   </tr>
   <tr>
   <td><strong>Append to test case</strong></td>
   <td>To add the recorded test steps to an existing test case.</td>
   </tr>
   <tr>
   <td>
   <div>
   <div><strong>Overwrite test case</strong></div>
   </div>
   </td>
   <td>To replace an existing test case with the recorded test case</td>
   </tr>
   </tbody>
   </table>

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/save-script.png" width=65%>

### Run the recorded test case

To playback the recorded scenario:

1. Select the test case where you saved the recorded actions.
2. On the main toolbar, select **iOS** device on the drop-down list next to **Run**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/select-ios.png" width=30%>

3. In the displayed **iOS Devices** dialog, select a device, then click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/ios-devices-list.png" width=70%>

   Katalon Studio executes the iOS test with the recorded steps accordingly.

   **<details><summary>View the test case in Script mode.</summary>**

   ```groovy
   import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
   import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
   import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
   import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
   import static com.kms.katalon.core.testobject.ObjectRepository.findWindowsObject
   import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
   import com.kms.katalon.core.cucumber.keyword.CucumberBuiltinKeywords as CucumberKW
   import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
   import com.kms.katalon.core.model.FailureHandling as FailureHandling
   import com.kms.katalon.core.testcase.TestCase as TestCase
   import com.kms.katalon.core.testdata.TestData as TestData
   import com.kms.katalon.core.testobject.TestObject as TestObject
   import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
   import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
   import com.kms.katalon.core.windows.keyword.WindowsBuiltinKeywords as Windows
   import internal.GlobalVariable as GlobalVariable
   import org.openqa.selenium.Keys as Keys

   Mobile.startApplication('/Users/thuyngo/Desktop/Project/iOS/App/Coffee Timer 2021-01-27 16-49-52/Apps/Coffee Timer.ipa', true)

   Mobile.tap(findTestObject('Object Repository/XCUIElementTypeStaticText - Green Tea (1)'), 0)

   Mobile.tap(findTestObject('Object Repository/XCUIElementTypeButton - Start (2)'), 0)

   Mobile.tap(findTestObject('Object Repository/XCUIElementTypeButton - Stop (1)'), 0)

   Mobile.closeApplication()
   ```
   </details>
### See also:

   * [Execute and Debug a Test Case](https://docs.katalon.com/katalon-studio/docs/execute-a-test-case-or-a-test-suite.html#debug-a-test-case)
   * [Troubleshoot automated mobile testing](https://docs.katalon.com/katalon-studio/docs/troubleshooting-automated-mobile-testing.html).