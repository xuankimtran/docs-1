---
title: "Sample iOS mobile tests project"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/iOS-sample-prj.html
---

This sample demonstrates iOS testing fundamentals in Katalon Studio.

The Application Under Test (AUT) is the `Coffee Timer` application. You can learn more about mobile testing in this document: [Introduction to mobile testing](https://docs.katalon.com/katalon-studio/docs/katalon_mobile_recorder_introduction.html#mobile-recorder).

> Requirements:
> * iOS setup. To set up Xcode simulators/ real iOS devices, you can refer to this document: [[Mobile] iOS Setup](https://docs.katalon.com/katalon-studio/tutorials/mobile-ios-setup.html#part-1-setting-up-the-environment-for-ios-testing).

## Open the sample iOS test project

To open the iOS sample project, in Katalon Studio, go to **File > New Sample Project > Sample iOS Mobile Tests Project**. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/iOS-sample-projects/KS-iOS-Open-the-iOS-sample.png" width="70%" alt="Open iOS sample project">

Alternatively, you can download the iOS sample project from our Github repository: [iOS sample](https://github.com/katalon-studio-samples/ios-mobile-tests).

## Prepare the iOS application file

The `Coffee Timer` application located in the `App` folder of this sample project is pre-built and signed by the Katalon team to only run on Katalon devices.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/iOS-sample-projects/KS-iOS-Coffee-timer-app.png" width="50%" alt="The sample coffee timer application">

As part of the iOS development procedure, to execute the sample test cases with your iOS devices, you need to build and sign the `Coffee Timer` application for your iOS devices. Follow these steps:

**<details><summary>For Xcode simulators</summary>**

To execute the sample test cases with Xcode simulators, you need to prepare an `.app` file.

1. Open the `Coffee Timer.xcodeproj` project file with Xcode. To find the project save location, go to **&lt;your-project-folder&gt; > App > Your-First-iOS-App > Coffee Timer**. Double-click the `Coffee Timer.xcodeproj` file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/open-xcode-file.png" width=70% alt="Open Coffee Timer Xcode project">

2. After opening the project in Xcode, choose one of the iOS simulators to launch the apps.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/iOS-sample-projects/KS-iOS-Choose-simulator-1.png" width=50% alt="Choose the iOS simulators">

3. To build the `.app` file, click **Product > Build**. 
    
    Wait for the build to finish, to find the `app` file, go to `~/Library/Developer/Xcode/DerivedData/Coffee Timer/Build/Products/Debug-iphonesimulator/Coffee Timer.app`.

    > Notes:
    > 
    > To quickly search for the `DerivedData` folder, copy and paste the following path `~/Library/Developer/Xcode/DerivedData` into the **Spotlight**. 

4. Copy and paste the `Coffee Time.app` file into the `App` folder of the sample project. Katalon will use this file to start the `Coffee Time` application.

</details>

**<details><summary>For real iOS devices</summary>**

To execute mobile testing with real iOS devices, you need to prepare an `.ipa` file. 

1. Open the `Coffee Timer.xcodeproj` project file with Xcode. To find the project save location, go to **&lt;your-project-folder&gt; > App > Your-First-iOS-App > Coffee Timer**. Double-click the `Coffee Timer.xcodeproj` file.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/open-xcode-file.png" width=70% alt="Open Coffee Timer Xcode project">

2. After opening the project in Xcode, select an iOS device to launch the apps.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/select-device.png" width=35% alt="Choose the iOS device">

3. In the **General** tab, set the deployment iOS version and select the device type in the **Deployment Info** section.

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/deployment.png" width=45% alt="Choose the iOS system">

4. Switch to the **Signing & Capabilities** tab, check the **Automatically manage signing** box, then choose the team that has your device registered in the Apple Developer Portal.

5. To build the `.ipa` file, click **Product > Build**. 

6. To export the `.ipa` file, click **Product > Archive**. Follow the instructions to get the `Coffee Timer.ipa` file.

    <a class="pop">
    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/export.gif" width=70% alt="Build the Coffee Timer.ipa">
    </a>
    <p style="text-align: center;"><em>Click the gif to enlarge it.</em></p>

7. Verify the `.ipa` file, do as follows:

   - Navigate to **Window > Devices** in Xcode.
   - Choose your device from the **Devices** list.
   - Click *Add* (+) to browse the `.ipa` file.

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A5.png" width=60% alt="Add the .ipa file to Xcode devices">
      
   - Once installed successfully, the application appears in the **Installed Apps** section.  

      <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-on-macos/image2016-8-8-143A313A14.png" width=60% alt="Add the .ipa file to Xcode devices">

8. Put the `Coffee Time.ipa` file into the `App` folder of the sample project. Katalon will use this file to start the `Coffee Time` application.

</details>

## iOS sample project components

### Custom keywords

You can use custom keywords in the test case. To learn more about custom keywords, you can refer to this document: [Introduction to custom keywords](https://docs.katalon.com/katalon-studio/docs/introduction-to-custom-keywords.html).

Katalon creates the `sample.Common.startApplication` custom keyword to define the absolute path for starting the iOS application. To see the custom keyword, in the **Test Explorer** panel, go to **Keywords > sample > Common.groovy**.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/iOS-sample-projects/KS-iOS-sample-custom-keywords.png" width="50%" alt="Custom keywords in the iOS project">

<table>
<thead>
  <tr>
    <th>Parameter</th>
    <th>Type</th>
    <th>Mandatory</th>
    <th>Description</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>appPath</td>
    <td>String</td>
    <td>Yes</td>
    <td>The absolute path of the application installation file.</td>
  </tr>
  <tr>
    <td>uninstallAfterCloseApp</td>
    <td>boolean</td>
    <td>Yes</td>
    <td>true if uninstalling the application automatically after run.</td>
  </tr>
  <tr>
    <td>flowControl</td>
    <td>FailureHandling</td>
    <td>Optional</td>
    <td>Specify failure handling schema to determine whether the execution should be allowed to continue or stop. To learn more about failure handling settings, you can refer to this document: <a href="https://docs.katalon.com/katalon-studio/docs/failure-handling.html#default-failure-handlingbehavior" target="_blank" rel="noopener noreferrer">Failure handling</a>.</td>
  </tr>
</tbody>
</table>

```groovy
public class Common {
	@Keyword
	def startAppliucation() {
		String appPath = RunConfiguration.getProjectDir() + '/App/Coffee Timer.ipa'
		Mobile.startApplication(appPath, false)
	}
}
```

> Notes:
> * If you change the name of the `Coffee Timer` application while building it, make sure to change the absolute path to the new file accordingly. For example, if the application name is `Coffee Timer2.ipa`, the absolute path should be `/App/Coffee Timer2.ipa`.
> * If you are running test cases with Xcode simulators, the path should lead to the `Coffee Timer.app` file instead.

### Test cases

To access test cases in this project, go to the **Test Cases** folder in the **Test Explorer** panel. 

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/iOS-sample-projects/KS-iOS-Test-cases.png" width="70%" alt="Sample test cases">

There are two test cases for different purposes:

1. The test case **Mexican Coffee Timer** starts and stops the timer for making a Mexican coffee. In this example, we run the test case with a real iOS device.

    - Start the `Coffee Timer.ipa` application. Here, we use the `sample.Common.startApplication` custom keyword to run the application.
    - Tap **Mexican**. We set the timeout for 0 seconds.
    - Tap **Start**. We set the timeout for 0 seconds.
    - Tap **3:19**. We set the timeout for 0 seconds.
    - Tap **Stop**. We set the timeout for 0 seconds.
    - Tap **Back**. We set the timeout for 0 seconds.
    - Close the application.

    **<details><summary>View the test case in the script mode</summary>**

    ```groovy
    import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
    import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
    import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
    import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
    import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
    import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
    import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
    import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
    import com.kms.katalon.core.model.FailureHandling as FailureHandling
    import com.kms.katalon.core.testcase.TestCase as TestCase
    import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
    import com.kms.katalon.core.testdata.TestData as TestData
    import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
    import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
    import com.kms.katalon.core.testobject.TestObject as TestObject
    import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
    import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
    import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
    import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
    import internal.GlobalVariable as GlobalVariable

    CustomKeywords.'sample.Common.startAppliucation'()

    Mobile.verifyElementText(findTestObject('Spy/XCUIElementTypeStaticText - Mexican'), 'Mexican')

    Mobile.tap(findTestObject('XCUIElementTypeStaticText - Mexican'), 0)

    Mobile.tap(findTestObject('XCUIElementTypeButton - Start'), 0)

    Mobile.tap(findTestObject('XCUIElementTypeStaticText - 319'), 0)

    Mobile.tap(findTestObject('XCUIElementTypeButton - Stop'), 0)

    Mobile.tap(findTestObject('XCUIElementTypeButton - Back'), 0)

    Mobile.closeApplication()
    ```
    </details>

2. The test case **Verify the main list** verifies the list of the coffee name in the application. In this example, we run the test case with a real iOS device.

    - Start the `Coffee Timer.ipa` application. Here, we use the `sample.Common.startApplication` custom keyword to run the application.
    - Verify if the application is showing the **Mexican** item.
    - Verify if the application is showing the **Colombian** item.
    - Verify if the application is showing the **Coffees** item.
    - Close the application.

    **<details><summary>View the test case in the script mode</summary>**

    ```groovy
    import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
    import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
    import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
    import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
    import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
    import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
    import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
    import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
    import com.kms.katalon.core.model.FailureHandling as FailureHandling
    import com.kms.katalon.core.testcase.TestCase as TestCase
    import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
    import com.kms.katalon.core.testdata.TestData as TestData
    import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
    import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
    import com.kms.katalon.core.testobject.TestObject as TestObject
    import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
    import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
    import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
    import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
    import internal.GlobalVariable as GlobalVariable

    CustomKeywords.'sample.Common.startAppliucation'()

    Mobile.verifyElementText(findTestObject('Spy/XCUIElementTypeStaticText - Mexican'), 'Mexican')

    MobileBuiltInKeywords.verifyElementText(findTestObject('Spy/XCUIElementTypeStaticText - Colombian'), 'Colombian')

    MobileBuiltInKeywords.verifyElementText(findTestObject('Spy/XCUIElementTypeStaticText - Coffees'), 'Coffees')

    Mobile.closeApplication()
    ```
    </details>

### Test suites

To access the test suite in this project, in the **Test Explorer** panel, go to the **Test Suites > Smoke Tests** folder. This test suite combines the two test cases shown above.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/iOS-sample-projects/KS-iOS-Test-suite.png" width=70% alt="Test Suites"> 

## Execute selected test case or test suite

To execute a test case or a test suite in the sample project:

1. Select the test case/test suite you want to execute.
2. On the main toolbar, select **iOS** as the device type in the dropdown list next to **Run**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/select-ios.png" width=30%>

3. In the displayed **iOS Devices** dialog, select an iOS device or Xcode simulator, then click **OK**.

   <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/mobile-recorder-76/iOS/ios-devices-list.png" width=50%>

   Katalon Studio executes the iOS test with the recorded steps accordingly.

4. Observe the test result in the **Log Viewer** tab. To learn more about analyzing test execution logs, you can refer to this document: [[WebUI] Analyze Test Execution Logs and Debug the Test Case](https://docs.katalon.com/katalon-studio/tutorials/webui-analyze-test-case-execution-logs-and-resolve-errors.html#analyze-test-execution-logs-in-log-viewer).

    <img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/android-sample-prj/KS-ANDROID-Log-viewer.png" width=70% alt="View results">
    </a>

    > Notes:
    > * You can view test results in the **Result** tab at the test suite level. The test results can be Passed, Failed, Error, or Incomplete. To learn more about the test status, you can refer in this document: [View and Customize Execution Log](https://docs.katalon.com/katalon-studio/docs/working-with-execution-log.html#view-execution-log).
    > * After executing test suites, you can view your reports and details in `<your-project-folder>/Reports`. Katalon Studio also supports exporting test reports into different formats, such as HTML, CSV, PDF, and JUnit.
    > * For real-time monitoring and better reporting capabilities, consider integrating your project with Katalon TestOps. Learn more about test result reports here: [Upload Test Results to Katalon TestOps from Katalon Studio](https://docs.katalon.com/katalon-studio/docs/katalon-analytics-beta-integration.html).

## See also

* [[Mobile] Create and Run iOS Test Case](https://docs.katalon.com/katalon-studio/tutorials/mobile-create-ios-test-case.html)
