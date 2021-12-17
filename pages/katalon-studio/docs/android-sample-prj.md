---
title: "Android sample project"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/android-sample-prj.html
---

This sample demonstrates Android testing fundamentals in Katalon Studio.

The Application Under Test (AUT) is the `APIDemos.apk` application. You can learn more about mobile testing in this document: [Introduction to mobile testing](https://docs.katalon.com/katalon-studio/docs/katalon_mobile_recorder_introduction.html#mobile-recorder).

> Requirements:
> * Android setup. To learn more about setting up Android devices, you can refer to this document: [[Mobile] Android Setup](https://docs.katalon.com/katalon-studio/tutorials/mobile-android-setup.html#set-up-android-tests-on-windows-linux-and-macos).
> * If you are using Android Studio, you can refer to this document for the setup: [[Mobile] Configure Android Studio](https://docs.katalon.com/katalon-studio/docs/configure-android-studio.html).

## Open the sample Android test project

To open the Android sample project, in Katalon Studio, go to **File > New Sample Project > Sample Android Mobile Tests Project**. Katalon Studio will automatically detect and ask you to install Android SDK if your current machine does not have it or your Android SDK is not located at the default folder: `~/.katalon/tools/android_sdk`.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/android-sample-prj/KS-Android-Open-sample-Android.png" width="70%" alt="Open Android sample project">

Alternatively, you can download the Android sample project from our Github repository: [Android sample](https://github.com/katalon-studio-samples/android-mobile-tests).

## Android sample project components
### Profiles

To open the execution profile, go to **Profiles > default**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/android-sample-prj/KS-Android-Execution-profile.png" width="70%" alt="Open execution profile in the sample Android project">

You can create and save all global variables in the execution profile. They can be used across test cases in your project. To learn more about execution profiles and global variables, you can refer to this document: [Execution profile and global variables](https://docs.katalon.com/katalon-studio/docs/execution-profile-v54.html).

Katalon creates four global variables in this sample project as follows:

<table>
<thead>
  <tr>
    <th>Name</th>
    <th>Value</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>G_timeout</td>
    <td>10</td>
  </tr>
  <tr>
    <td>G_NotificationMessage</td>
    <td>Your message has been sent. View message</td>
  </tr>
  <tr>
    <td>G_AndroidApp</td>
    <td>androidapp/APIDemos.apk</td>
  </tr>
  <tr>
    <td>G_ShortTimeOut</td>
    <td>5</td>
  </tr>
</tbody>
</table>

### Test cases

To access test cases in this project, go to the **Test Cases** folder in the **Test Explorer** panel. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/android-sample-prj/KS-ANDROID-Test-case.png" width="70%" alt="Sample test cases">

There are two test cases for different purposes:

1. The test case **Verify Correct Alarm Message** is to verify if we can get the correct displayed message. The flow in this test case is as follows:

    - Start the `APIDemos.apk` application. Here, the location of the AUT is under the `<sample-project-folder>/androidapp` folder. We use the following sample code to identify the absolute path to the application:

        ```groovy
        /*Get full directory's path of android application*/
        def appPath = PathUtil.relativeToAbsolutePath(GlobalVariable.G_AndroidApp, RunConfiguration.getProjectDir())

        /*Start the AUT*/
        Mobile.startApplication(appPath, false)
        ```
    - Tap **App**. We set the timeout for 10 seconds.
    - Tap **Activity**. We set the timeout for 10 seconds.
    - Tap **Custom Dialog**. We set the timeout for 10 seconds.
    - Verify if the text displaying on the **App/Activity/Custom Dialog** dialog is correct.


      <a class="pop">
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/android-sample-prj/KS-ANDROID-TC1.gif" width="70%" alt="Verify Correct Alarm Message">
      </a>
      <p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>


      <details><summary>View the test case in the script mode</summary>

      ```groovy
      import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
      import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
      import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
      import internal.GlobalVariable as GlobalVariable
      import com.kms.katalon.core.configuration.RunConfiguration as RunConfiguration
      import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
      import com.kms.katalon.core.util.internal.PathUtil as PathUtil
      import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
      import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
      import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
      import com.kms.katalon.core.model.FailureHandling as FailureHandling
      import com.kms.katalon.core.testcase.TestCase as TestCase
      import com.kms.katalon.core.testdata.TestData as TestData
      import com.kms.katalon.core.testobject.TestObject as TestObject
      import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint

      Mobile.comment('Story: Verify correct alarm message')

      Mobile.comment('Given that user has started an application')

      'Get full directory\'s path of android application'
      def appPath = PathUtil.relativeToAbsolutePath(GlobalVariable.G_AndroidApp, RunConfiguration.getProjectDir())

      Mobile.startApplication(appPath, false)

      Mobile.comment('And he navigates the application to Activity form')

      Mobile.tap(findTestObject('Alarm Message/android.widget.TextView - App'), 10)

      Mobile.tap(findTestObject('Alarm Message/android.widget.TextView - Activity'), 10)

      Mobile.comment('When he taps on the Custom Dialog button')

      Mobile.tap(findTestObject('Alarm Message/android.widget.TextView - Custom Dialog'), 10)

      'Get displayed message on the dialog'
      def message = Mobile.getText(findTestObject('Application/App/Activity/Custom Dialog/android.widget.TextViewCustomDialog'), 
          10)

      Mobile.comment('Then the correct dialog message should be displayed')

      Mobile.verifyEqual(message, 'Example of how you can use a custom Theme.Dialog theme to make an activity that looks like a customized dialog, here with an ugly frame.')

      Mobile.closeApplication()
      ```
      </details>

2. The test case **Verify Last Items In List** is to verify whether we can identify the correct last item in the list.
    
    - Start the `APIDemos.apk` application. Here, the location of the AUT is under the `<sample-project-folder>/androidapp` folder. We use the following sample code to identify the absolute path to the application:

        ```groovy
        /*Get full directory's path of android application*/
        def appPath = PathUtil.relativeToAbsolutePath(GlobalVariable.G_AndroidApp, RunConfiguration.getProjectDir())

        /*Start the AUT*/
        Mobile.startApplication(appPath, false)
        ```
    - Tap **Graphics**. We use the `G_Timeout` global variable as the timeout value.
    - Scroll to **Xfermodes** item.
    - Verify if the current screen should show Xfermodes text after scrolling

      <a class="pop">
      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/android-sample-prj/KS-ANDROID-TC2.gif" width="70%" alt="Verify Last Items In List">
      </a>
      <p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>


      <details><summary>View the test case in the script mode</summary>

      ```groovy
      import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
      import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
      import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
      import internal.GlobalVariable as GlobalVariable
      import com.kms.katalon.core.configuration.RunConfiguration as RunConfiguration
      import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
      import com.kms.katalon.core.util.internal.PathUtil as PathUtil

      Mobile.comment('Story: Verify correct alarm message')

      Mobile.comment('Given that user has started an application')

      'Get full directory\'s path of android application'
      def appPath = PathUtil.relativeToAbsolutePath(GlobalVariable.G_AndroidApp, RunConfiguration.getProjectDir())

      Mobile.startApplication(appPath, false)

      Mobile.comment('And he navigates the application to Graphics form')

      Mobile.tap(findTestObject('Last Items/android.widget.TextView - Graphics'), GlobalVariable.G_Timeout)

      Mobile.comment('When he scroll to Xfermodes text')

      Mobile.scrollToText('Xfermodes')

      Mobile.comment('Then the current screen should show Xfermodes text after scrolling')

      'Get item\'s label'
      def itemText = Mobile.getText(findTestObject('Last Items/android.widget.TextView - Xfermodes'), GlobalVariable.G_Timeout)

      Mobile.verifyEqual(itemText, 'Xfermodes')

      Mobile.closeApplication()
      ```
      </details>
### Test suite

To access the test suite in this project, in the **Test Explorer** panel, go to the **Test Suites > Regression Tests** folder. This test suite combines the two test cases shown above.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/android-sample-prj/KS-ANDROID-Test-suites.png" width=70% alt="Test Suites"> 

## Execute selected test case or test suite

To execute a test case or a test suite in the sample project:

1. Select the test case/test suite you want to execute.
2. On the main toolbar, select **Android** device in the dropdown list next to **Run**.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/android.png" width=20% alt="Execute the selected test">  

3. Select your device from the **Android Devices** list. Click **OK**. 

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/device.png" width=40% alt="Select the Android device">

4. Observe the test result in the **Log Viewer** tab. To learn more about analyzing test execution logs, you can refer to this document: [[WebUI] Analyze Test Execution Logs and Debug the Test Case](https://docs.katalon.com/katalon-studio/tutorials/webui-analyze-test-case-execution-logs-and-resolve-errors.html#analyze-test-execution-logs-in-log-viewer).

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/android-sample-prj/KS-ANDROID-Log-viewer.png" width=70% alt="View results">
    </a>
    <p style="text-align: center;"><em>Click the image to enlarge it.</em></p>

    > Notes:
    > * You can view test results in the **Result** tab at the test suite level. The test results can be Passed, Failed, Error, or Incomplete. To learn more about the test status, you can refer in this document: [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html#view-execution-log).
    > * After executing test suites, you can view your reports and details in `<your-project-folder>/Reports`. Katalon Studio also supports exporting test reports into different formats, such as HTML, CSV, PDF, and JUnit.
    > * For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).
## See also

* [[Mobile] Create and Run Android Test Case](https://docs.katalon.com/katalon-studio/tutorials/mobile-create-android-test-case.html)

