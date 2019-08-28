---
title: "Windows Record Tutorials"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/windows-recorder-tutorials.html
---
> Starting with **Katalon Studio version 7.0**, you can record a test on a Windows desktop application.

1. To start recording a Windows action, Click the **Record Windows Action** icon on the main toolbar of Katalon Studio.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/introduction-desktop-app-testing/Windows_Record_Action.png" width="600.5" height="65">

2. The Windows Recorder dialog box is displayed. Specify the information at the **CONFIGURATIONS** section.

* **Configuration**: where you can view and edit the `WinAppDriver URL` and `Desired Capabilities`.

* **Application File**: the absolute path to the `Windows Executable File (*.exe)` of the testing machine. For Windows users, click **Browse...** button to locate the application file.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/Record-step2.png" width="402" height="144">

The **Start** button is enabled after the Application File text box is filled.

Click **Start** when you're done with the settings.

3. The specified Windows application is deployed and opened on a testing machine.

4. The **Screen View** dialog box is displayed to show the current screenshot of your application on the testing machine.

All the Windows objects in that screenshot are analyzed and organized in a tree at the **Screen Objects** section.

Click on any object in that tree and it's highlighted in the Screen View accordingly.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/highlighted.png">

5. Select an element, then specify an action to perform at the **Possible Actions** section.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/step6.png" width="291" height="165">

6. All of the specified actions above are recorded at the **Recorded Actions** section.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/recorded-action.png" width="390" height="192">

7. You can stop the application or start another application if needed. To reload the **Screen View** as well as **Screen Objects**, simply click on the **Refresh Screen** button.\
When you’re done with recording, click **OK** to save the recorded actions in Katalon Studio.

8. You will be prompted to save the captured objects in the Object Repository of Katalon Studio. Choose an existing folder or create a new one, then click **OK** to continue.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/Step9.png" width="267" height="258">

9. When you finish your recording session, export the  recorded steps to a new test case.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/Export-new-TC.png" width="494" height="197">

10. Recorded objects and actions are saved in the test case.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/test-case.png" width="609" height="191">

11. Select the **Windows** icon in the **Run** button on the main Toolbar to execute the script.  

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/record-windows-actions/step13.png" width="228" height="330">

12. The Windows test is executed with those recorded steps accordingly.

>**Notes**:
>
> 1. While any action is being performed on a test object, there should be no other actions taken on the application. One action at a time.
> 2. Remember not to lock your screen while spying, recording or executing a test on a desktop application.
> 3. You're recommended not to run multiple applications simultaneously.
